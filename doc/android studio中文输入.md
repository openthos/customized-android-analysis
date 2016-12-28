# ���
ͨ����װfcitx���뷨ƽ̨��ʹ��Archlinux�µ��������뷨���Ӷ�ʵ���������롣

# ��������
Ŀǰ�޷�ͨ����ݼ�```Ctrl + Space```�������뷨���л�����˽���ʹ��fcitx�Դ���ƴ�����뷨��ͨ��```shift```��ʵ����Ӣ���л�
����ʹ�õ��������뷨����Ҫ��ǰͨ��```fcitx-configtool```���߽���Ӧ�ĵ��������뷨����ΪĬ�����뷨���������ݼ������޷�������������

# ��������
���²������趼��ִ��
```
prearch
arch
```
����Archlinux������ִ��

## һ����װfcitx����Ӧ���뷨ģ���Լ����ù���
ͨ�����·�ʽ��װfcitx���뷨ƽ̨����Ӧ�����뷨ģ���fcitx���ù��ߣ�����fcitx-im��Ҫ���� fcitx-gtk2, fcitx-gtk3, fcitx-qt4 �� fcitx-qt5��ģ��
```
sudo pacman -S fcitx fcitx-im fcitx-configtool
```
�����fcitx�и����˽⣬��鿴[Arch wiki Fcitx (��������)](https://wiki.archlinux.org/index.php/Fcitx_(%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87)#.E7.AC.AC.E4.B8.89.E6.96.B9.E6.8B.BC.E9.9F.B3.E8.BE.93.E5.85.A5.E6.B3.95)

## ������װ����
ʹ�����·�ʽ���а�װ������ѡ����ʵ������滻wqy-microhei��
```
sudo pacman -S wqy-microhei
```


����ͨ�����·�ʽ�鿴pacman���������壬��Ѱ���ʵĽ����滻
```
pacman -Ss font
```
>���������������
+ adobe-source-han-sans-cn-fonts
˼Դ����������Ĳ���
+ adobe-source-han-sans-tw-fonts
˼Դ���己�����Ĳ���
+ wqy-microhei
��Ȫ��΢�׺ڣ��޳�����ʽ�ĸ��������պ�Խ (CJKV) �������塣
+ wqy-zenhei
��Ȫ�����ڣ����� (�޳���) �������������壬������Ȫ��������� (Ҳ֧�ֲ����պ��ַ�)��
+ ttf-arphic-ukai
���� (���бʴ�) Unicode ���� (�Ƽ����÷����)
+ ttf-arphic-uming
���� (ӡˢ) Unicode ����
+ opendesktop-fonts
�������壬֮ǰΪ ttf-fireflysung
+ wqy-bitmapfont
��Ȫ��������� (����) ��������
+ ttf-hannom
���ġ�Խ���� TrueType ����
+ ttf-twAUR
�����壩̨����������еı�׼���顢��������

����������и����˽⣬��鿴[Arch wiki Fonts (��������)](https://wiki.archlinux.org/index.php/Fonts_(%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87)#.E4.B8.AD.E6.96.87.E5.AD.97)

## ����ִ�нű�
ͨ�����·�ʽִ��env.sh�ű��ļ�������dbus������fcitx��Ӧ��������
```
source env.sh
```

ִ�к��ͨ��ִ����������
```
export
```
�۲������Ƿ����```DBUS_SESSION_BUS_ADDRESS```��```XMODIFIERS```��```GTK_IM_MODULE```�Լ�```QT_IM_MODULE```���ĸ��������������Ӷ�ȷ���Ƿ�ִ�гɹ�
�粻�ɹ�����ȷ������������ȷ�����ٽ�����һ��������fcitx�޷�����

## �ġ�����fcitx
�˲�����ִ�й�```./linuxgui.sh```��ִ�У�����fcitx�޷���������

ͨ�����·�ʽ����fcitx
```
fcitx &
```
ִ�н�����ܳ���```(ERROR-4488 /build/fcitx/src/fcitx-4.2.9.1/src/lib/fcitx/ime.c:432) fcitx-keyboard-cm-mmuock already exists```�Ĵ��󣬿��Ժ��Բ���Ӱ��

ִ����ɺ����ͨ�����·�ʽ�鿴�Ƿ�ִ�гɹ�
```
ps aux | grep fcitx
```
�鿴������Ƿ������Ϊfcitx�Ľ��̣��������ִ�гɹ�

## �塢����fcitx���뷨
ͨ�����·�ʽ����fcitx���뷨
```
fcitx-configtool
```
ִ�к�������´��ڣ������+������ѡ�����뷨���м���
![image](https://github.com/openthos/linux-android-analysis/tree/master/doc/.pic/1.jpg)

��"Only Show Current Language"��ȡ��
![image](https://github.com/openthos/linux-android-analysis/tree/master/doc/.pic/2.jpg)


�ҵ���Ϊ��pinyin����ѡ�fcitx�Դ�������ƴ�����뷨����ѡ�в�������½ǡ�OK���������뷨����
![image](https://github.com/openthos/linux-android-analysis/tree/master/doc/.pic/3.jpg)
������Ҫʹ�õ��������뷨����Ҫ�ڴ˲����ҵ���Ӧ��ѡ����м��������ͼ�е�Google Pinyin��


ѡ�С�pinyin������·���^��ͼ�꣬���Ѽ����"pinyin" ����ΪĬ�����뷨
![image](https://github.com/openthos/linux-android-analysis/tree/master/doc/.pic/4.jpg)

��ͼΪ������ɵĽ��
![image](https://github.com/openthos/linux-android-analysis/tree/master/doc/.pic/5.jpg)

## ��������Android studio
���뷨������ɺ�ִ��һ�´����Android studio������������
```
./opt/android-studio/bin/studio.sh
```