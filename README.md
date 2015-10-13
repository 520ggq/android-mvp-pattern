##Android MVP Pattern

### What is this?
This Project offers a `simple but clear` Android Sample project designed with `MVP Pattern`, which comes to become a more and more important `design pattern` in android application project.

**Activity and Fragment** take most parts of Android Developing jobs. With MVP pattern, the Acitivity will be just activity, which only does the job of "Find View", "Set Listener" and "React to the LifeCycle". The jobs of  UI Logic will be moved to IView, while the jobs of Business Logic will be moved to IPresenter. In this case, the Activity remains very simple and clear, so that it is read-friendly. And since the business logic is written in Presenter, it can be reused in other Activity easily.

This Project is a sample project used in the following post in my Blog.

## ����
�����Ŀ��һ���򵥵�Android MVP��Ŀ������չʾMVP�ṹ�Ļ���д����

### ������Ϣ

- ���ߣ�[Kaede Akatsuki](http://kaedea.com)
- ��Ŀ��[Android-MVP-Pattern](https://github.com/kaedea/Android-MVP-Pattern)
- ��־��[Android MVPģʽ ���׶��Ľ��ܷ�ʽ](http://kaedea.com/2015/10/11/android-mvp-pattern)


## �ص�Ҫ˵��MVPģʽ
��Android��Ŀ�У�Activity��Fragmentռ���˴󲿷ֵĿ��������������һ�����ģʽ������˵����ṹ��ר����Ϊ�Ż�Activity��Fragment�Ĵ���������ģ���˵����ģʽ��Ҫ���������MVP���ģʽ��

����MVC�ķֲ㣬Activity��Fragment������ֻ˵Activity��Ӧ������View�㣬����չʾUI���棬�Լ������û������룬���⻹Ҫ�е�һЩ�������ڵĹ�����Activity����Android�����г䵱�ǳ���Ҫ�Ľ�ɫ���ر���TA���������ڵĹ��ܣ����Կ�����ʱ�����Ǿ�����һЩҵ���߼�ֱ��д��Activity���棬��ǳ�ֱ�۷��㣬���۾���Activity��Խ��Խӷ�ף�����1000�д����ǳ��е��£����������һЩ����ͨ�õ�ҵ���߼��������û���¼����д�ھ����Activity�����ζ������߼����ܸ����ˡ�����н��д����ع�������ˣ�����1000+�е���϶����������ǡ���ˣ�Activity�����е���View�Ľ�ɫ�����е���һ���ֵ�Controller��ɫ������һ��V��C�������һ���ˣ���Ȼ����д���㣬�������ҵ������Ļ���Ҫά�����������ˣ�������һ��ӷ�׵�Activity�����ҵ���߼��Ĵ���Ҳ��ǳ����ۣ����Կ������б�Ҫ��Activity�У���View��Controller���뿪�����������MVPģʽ�Ĺ����ˡ�

![MVP�ṹ](http://7xih5c.com1.z0.glb.clouddn.com/15-10-11/2114527.jpg "MVP�ṹ")

MVPģʽ�ĺ���˼��
>**MVP��Activity�е�UI�߼������View�ӿڣ���ҵ���߼������Presenter�ӿڣ�Model�໹��ԭ����Model**��

�����MVPģʽ�����������Ļ���Activity�Ĺ����ļ��ˣ�ֻ������Ӧ�������ڣ���������������Presenter��ȥ��ɡ�����ͼ���Կ�����Presenter��Model��View֮���������Ϊ���ýṹ��ø��Ӽ򵥣�View������ֱ�Ӷ�Model���в�������Ҳ��MVP��MVC���Ĳ�֮ͬ����

## MVPģʽ������
MVP�ĺô�����ɶ��˭˵���˾͸�����

- ��������ͼ�߼���ҵ���߼������������
- Activityֻ�����������ڵ����񣬴����ø��Ӽ��
- ��ͼ�߼���ҵ���߼��ֱ������View��Presenter�Ľӿ���ȥ����ߴ���Ŀ��Ķ���
- ��ҵ���߼��鵽Presenter��ȥ�������̨�߳�������Activity����Activity����Դ�޷���ϵͳ���մӶ������ڴ�й¶��OOM
- Presenter������ɽӿڣ������ж��־����ʵ�֣����Է�����е�Ԫ����

˵����ô�࣬û�������ðɣ����Լ���û�����Լ�д�ģ����ǻ���ֱ�ӿ�����ɡ�

## MVPģʽ��ʹ��
![��MVP��UML](http://7xih5c.com1.z0.glb.clouddn.com/15-10-12/94032090.jpg "��MVP��UML")

����һ�ż򵥵�MVPģʽ��UMLͼ����ͼ�п��Կ�����ʹ��MVP��������Ҫ�������²��裺

 1. ����IPresenter�ӿڣ�������ҵ���߼��Ľӿڶ������������������ʵ��PresenterCompl����������Է���ز鿴ҵ���ܣ����ڽӿڿ����ж���ʵ������Ҳ����д��Ԫ���ԣ�
 2. ����IView�ӿڣ���������ͼ�߼��Ľӿڶ����������ʵ�����ǵ�ǰ��Activity/Fragment
 3. ��UMLͼ���Կ�����Activity�������һ��IPresenter����PresenterCompl���ְ�����һ��IView����������Model��Activity��ֻ������IPresenter�ĵ��ã���������ȫ������PresenterCompl��ʵ��
 4. Model�����Ǳ����еģ�����һ������View��Presenter

ͨ������Ľ��ܣ�MVP����Ҫ�ص���ǰ�Activity�������߼������뵽View��Presenter�ӿ���ȥ�����ɾ����ʵ��������ɡ�����д���������IView��IPresenter�Ľӿڣ���ĳ�̶ֳ��ϼӴ��˿����Ĺ��������տ�ʼʹ��MVP��С�����ܻ��������д���Ƚϱ�Ť���������Լ�ס����ʵһ��ʼ��̫��Ҳû��ʲô���ã�ֻҪ�ھ�����Ŀ�ж�д���Σ�������ϤMVPģʽ��д�������TA����ͼ���Լ������������ĺô���

������ô�࣬���Ǻ���û��ʲô���ã��Ͼ�
>Talk is cheap, let me show you the code!

����ϸ����Ϣ�뵽[Android MVPģʽ ���׶��Ľ��ܷ�ʽ](http://kaedea.com/2015/10/11/android-mvp-pattern)Χ�ۡ�

