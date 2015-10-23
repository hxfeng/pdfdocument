(set-language-environment "Chinese-GB")
;;自定义快捷键
;;(global-set-key (kbd "C->") 'other-window) 
(add-to-list 'load-path "~/.emacs.d/extra/")
(require 'sr-speedbar)
(add-to-list 'load-path "~/.emacs.d/emacs-nav/")
(require 'nav)
(nav-disable-overeager-window-splitting)
(global-set-key [f8] 'nav-toggle)
(global-set-key [f5] 'compile)
    (setq-default compile-command "make")

(global-set-key [f6] 'speedbar)
;;自定义一个现实当前目录的函数
(defun myls ()
  (interactive);;这句需要有否则参数错误
 ;;   "excute shell command"
    (shell-command "ls -l");;交互执行shell命令

 )

;(global-set-key [f3] 'myls);;绑定到f3上
    ;;(setq-default shell-command "ls")

(put 'upcase-region 'disabled nil)


;;关闭欢迎界面
(setq inhibit-startup-message t)
;;(setq gnus-inhibit-startup-message nil)

;;最大化窗口的函数
(defun my-maximized ()  
  (interactive)  
  (x-send-client-message   nil 0 nil "_NET_WM_STATE" 32    '(2 "_NET_WM_STATE_MAXIMIZED_HORZ" 0)  
  )  
  (x-send-client-message   nil 0 nil "_NET_WM_STATE" 32    '(2 "_NET_WM_STATE_MAXIMIZED_VERT" 0)  
  )  
)  
;;启动时最大化  
;;(my-maximized)  
(global-set-key [f11] 'my-maximized)  

;;全屏设置
(global-set-key [f12] 'my-fullscreen)
(defun my-fullscreen ()
(interactive)
(x-send-client-message nil 0 nil "_NET_WM_STATE" 32 '(2 "_NET_WM_STATE_FULLSCREEN" 0))
) 








;;设置透明效果
(global-set-key [(f9)] 'loop-alpha)  ;;注意这行中的F9 , 可以改成你想要的按键    
    
(setq alpha-list '((75 55) (100 100)))    
    
(defun loop-alpha ()    
  (interactive)    
  (let ((h (car alpha-list)))                    
    ((lambda (a ab)    
       (set-frame-parameter (selected-frame) 'alpha (list a ab))    
       (add-to-list 'default-frame-alist (cons 'alpha (list a ab)))    
       ) (car h) (car (cdr h)))    
    (setq alpha-list (cdr (append alpha-list (list h))))    
    )    
)    
  
;; 显示时间，格式如下
(display-time-mode 1)
(setq display-time-24hr-format t)
(setq display-time-day-and-date t)

(transient-mark-mode t)

;; 支持emacs和外部程序的粘贴
(setq x-select-enable-clipboard t) 
;; 去掉工具栏
(tool-bar-mode nil)

;;去掉菜单栏
(menu-bar-mode nil)

;; 去掉滚动栏
(scroll-bar-mode nil)



;;颜色设置，其实有个color-theme.el可以将Emacs设置丰富多彩，非常漂亮，不过启动有些慢，我只是选择了一些颜色设置。  
;;;;;去掉工具栏  
(tool-bar-mode nil)  
;; 去掉菜单栏 (C-Mouse2：显示菜单项) ,以右键形式显示   
(menu-bar-mode nil)   
  
;;;;;不要滚动栏，现在都用滚轴鼠标了，可以不用滚动栏了  
(scroll-bar-mode nil)  
;;;;;改变emacs标题栏的标题  
(setq frame-title-format "%b@Alex-GDLC")  
;;;;;允许emacs和外部其他程序的粘贴  
(setq x-select-enable-clipboard t)  
;; 显示列号  
(setq column-number-mode t)  
;;开启语法高亮。  
(global-font-lock-mode 1)  
;;设置tab为4个空格的宽度  
(setq default-tab-width 4)  
(setq c-basic-offset 4)  


;;;;;;;;;  设置界面 start  这个会改变颜色方案
(set-cursor-color "Wheat")  
(set-mouse-color "Wheat")  
(set-foreground-color "Wheat")  
(set-background-color "DarkSlateGray")  
;(if window-system 
;(setq default-frame-alist            
;(append  
;'(
; (top . 80)    (left   . 100)  
; (width . 110) (height . 35 )
; ) 
; default-frame-alist)
;)  
;)  
;;;启动最大化  
;;;(setq initial-frame-alist '((top . 0) (left . 0) (width . 97) (height . 49)))  
;;高亮当前行
(global-hl-line-mode t)  
(global-linum-mode t)

(add-to-list 'load-path "~/.emacs.d")
(require 'rect-mark)
(global-set-key (kbd "C-x r C-w") 'rm-kill-region)
(global-set-key (kbd "C-x r M-w") 'rm-kill-ring-save)
(global-set-key (kbd "C-x r C-y") 'yank-rectangle)
(global-set-key (kbd "C-x r C-M-d") 'delete-rectangle)
(global-set-key (kbd "C-x r C-i") 'string-insert-rectangle)
(global-set-key (kbd "C-x r C-M-i") 'string-rectangle)
(global-set-key (kbd "C-x C-g") 'rm-set-mark) 

(require 'window-numbering)
(window-numbering-mode 1)
