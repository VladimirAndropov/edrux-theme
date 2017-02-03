# edruX-themes

# ��������� ���� edruX: #

## ��� 1 - ������������� memcached: ##
>     telnet localhost 11211
>     flush_all
>     quit

## ��� 2 - ��������� ���� � /edx/app/edxapp/themes  ##

>     cd /edx/app/edxapp/themes
> 
>     clone https://github.com/VladimirAndropov/edrux-theme

��� 3 - ����������� � *lms.env.json* 

 >     "COMPREHENSIVE_THEME_DIRS": [
>         "/edx/app/edxapp/themes"
> 
>     "USE_CUSTOM_THEME":  true
>  
>     "THEME_NAME": "edrux", 
>  
>     "DEFAULT_SITE_THEME": "edrux", 

��� 3 - ��������� ������ ���� �������


> ������� �� �� ����� */tmp/mako_lms/*
> 
>  ������� ��� �� *staticfiles* �� ���� */edx/var/edxapp*
>  
>  ������ ����� ��� edxapp:edxapp �� /edx/app/edxapp/themes/edrux
 

��� 4 - �������� ����

>     sudo -H -u edxapp bash
>     source /edx/app/edxapp/edxapp_env
>     cd /edx/app/edxapp/edx-platform
>     paver update_assets lms --settings=aws --themes=edrux

������ ���������� ��� ����� [http://edrux.ru](http://edrux.ru "EdruX")
