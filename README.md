"�ҵ�firefox���vimperator�����ļ�
"�����ķ���������
"��һ�������� :set ����Ը������ý����趨
"Ȼ������ :mkv �������Զ����������ļ�
"�ڶ������Լ�����
"Ubuntu����~/.vimperatorrc
"Windows����C:\Users\name\_vimperatorrc

":colorscheme vimium
":colorscheme desert 
" ����Hints��UI��ʾ��Ҳ��ָ��colors�ڵ����⣬������д������
highlight -link=FontFixed CmdLine font-family: "Lucida Grande", "Fixedsys", "Sans"; font-size: 13px;
highlight CompDesc padding-left: 6px;
highlight CompIcon display: none;
highlight CompItem[selected] background: #FFC542 !important;
highlight CompTitle text-transform: uppercase; background: -moz-linear-gradient(top, #FFF785, #FFC542); font-size: 11px; padding: 1px 3px 0px 3px; font-family : "Helvetica Neue", "Helvetica", "Arial", "Sans"; font-weight: bold; color: #302505;
highlight CompTitleSep height: 1px; background: #C38A22;
highlight ErrorMsg background: #a00 !important; color: #fff !important; font: 11px "Menlo" !important; padding: 2px 4px !important;
highlight Hint text-transform: uppercase; font-family : "Helvetica Neue", "Helvetica", "Arial", "Sans"; font-weight: bold; font-size: 12px; text-shadow: 0 1px 0 rgba(255, 255, 255, 0.6); color: #302505; padding: 1px 3px 0px 3px; background: -moz-linear-gradient(top, #FFF785, #FFC542); border: 1px #C38A22 solid; -moz-border-radius: 3px; -moz-box-shadow: 0 3px 7px 0px rgba(0,0,0,0.3);
highlight HintActive background-color: inherit !important
highlight HintElem background-color: inherit !important
highlight HintImage opacity: .5 !important;
highlight Normal background-color: #FFF; color: black; font-family: "Lucida Grande", "Arial", "Sans"; font-size: 12px;
highlight WarningMsg background: #a00 !important; color: #fff !important; font: 11px "Menlo" !important; padding: 2px 4px !important;
 
" �޸�UI�������˱�ǩͼ���ϱ���ţ�����Pentadactyl״̬����������Ϣ����������ʾ
set guioptions=brNsC
"brTNs
"set showstatuslinks=command
set complete=location,file

" ���Ҹ�������
set hlfind
 
" ��ǿ���õ� ]] �� [[ �ķ�ҳ
set nextpattern^=\s*(��һҳ|��һ��|��һ��|��һƪ|��ҳ|��ҳ)\s*
set previouspattern^=\s*(��һҳ|��һ��|��һ��|��һƪ|��ҳ|ǰҳ)\s* 

"map -modes=n j -builtin 10j
"map -modes=n k -builtin 10k
map -modes=n j -builtin 10<down>
map -modes=n k -builtin 10<up>

map -modes=n,v ; -builtin F

map -modes=n,v = -builtin <c-=>

"��ĳЩ��ݼ�ʧЧ����Щ����ϰ�߶����õ���
map A <Nop>
map a <Nop>
map <C-o> <Nop>
map <C-i> <Nop>

" ����������
map x :set go!=TB<CR>

" ֹͣˢ��
map -modes=n s -builtin <count>:stop<Return>

"����ǰ��
"map -modes=n H -builtin <C-o>
"map -modes=n L -builtin <C-i>
map -modes=n w -builtin <count>H
map -modes=n e -builtin <count>L

"ǰ���ǩ
"map J gT
"map K gt
map -modes=n l -builtin <count><C-n>
map -modes=n h -builtin <count><C-p>

"���´��ڴ���ҳ(��ǰ���ڴ���ҳ��gh)
map gy gH
map -modes=n t -builtin gH<Return>


"����ģʽ�°� jj ���˳� Esc
imap jj <Esc>
imap kk <Esc>

"��ĳЩ���ü���firefox�ӹ�
map -m n,v,i,c,t <C-a> <Pass>
map -m n,v,i,c,t <C-c> <Pass>
map -m i,c,t <C-v> <Pass>
map -m i,c,t <C-x> <Pass>
map -m i,c,t <C-z> <Pass>
map -m n,v,i,c,t <C-d> <Pass>
map -m n,v,i,c,t <C-f> <Pass>
map -m n,v,i,c,t <C-t> <Pass>
map -m n,v,i,c,t <C-w> <Pass>

"�����ӻ����ֱ�ѡ��ʱ���� t �� o ����ֱ������
map t -js str=util.domToString(buffer.focusedFrame.getSelection()); str!=""?dactyl.open(str, {where: dactyl.NEW_TAB}):CommandExMode().open("tabopen ")
map o -js str=util.domToString(buffer.focusedFrame.getSelection()); str!=""?dactyl.open(str, {where: dactyl.CURRENT_TAB}):CommandExMode().open("open ") 

"�Զ��� hint keys
:set hintkeys=asdfjklgheruio
:set hinttimeout=800
":hi Hint font:bold 15px "Droid Sans Mono", monospace !important; margin:-.2ex; padding: 0 0 0 1px; outline:1px solid rgba(0, 0, 0, .5); background:rgba(255,248,231,.8); color:black; text-transform:uppercase;

" ��֤����������ʱ���뷨��disable�ģ�����������������
style chrome://* #dactyl-commandline-command input {ime-mode: inactive;}
style chrome://* #dactyl-statusline-field-commandline-command input {ime-mode: inactive;}

" ��IE��
map ie :js io.run("c:\\Program Files (x86)\\internet explorer\\iexplore.exe", [buffer.URL])<CR>

" �г�ҳ����ת��ʷ�б�
map Z :jump<CR>

" �±�ǩ�鿴Դ����
map gf :tab viewsource<CR>
 
" ���õ���չ����
map a :addons<CR>

" ��Firefoxѡ��
map -modes=n,v,i <C-F12> :prefs<CR>

" ���ñ��룬���硸:! ping �� ��������
set fileencoding=gbk

