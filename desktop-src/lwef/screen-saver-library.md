---
title: Lidando com proteções de tela
description: A API do Microsoft Win32 dá suporte a aplicativos especiais chamados de proteções de tela.
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- proteções de tela
- Painel de controle, proteções de tela
- ScreenSaverConfigureDialog
- arquivos de definição de módulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61343cd586ed022c334b797a77320ee25eccdf48653b4732adc597f4aedde26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975716"
---
# <a name="handling-screen-savers"></a>Lidando com proteções de tela

A API do Microsoft Win32 dá suporte a aplicativos especiais chamados de *proteções de tela*. As proteções de tela iniciam quando o mouse e o teclado ficam ociosos por um período de tempo especificado. Eles são usados por esses dois motivos:

-   Para proteger uma tela da gravação Phosphor causada por imagens estáticas.
-   Ocultar informações confidenciais deixadas em uma tela.

Este tópico é dividido nas seções a seguir.

-   [Sobre as proteções de tela](#about-screen-savers)
-   [Usando as funções de proteção de tela](#using-the-screen-saver-functions)
    -   [Criando uma proteção de tela](#creating-a-screen-saver)
    -   [Instalando novas proteções de tela](#installing-new-screen-savers)
    -   [Adicionando ajuda à caixa de diálogo configuração de proteção de tela](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a>Sobre as proteções de tela

o aplicativo de área de trabalho no painel de controle de Windows permite que os usuários selecionem em uma lista de proteções de tela, especifiquem quanto tempo deve decorrer antes que a proteção de tela seja iniciada, configure as proteções de tela e visualize os protedores de tela. as proteções de tela são carregadas automaticamente quando Windows é iniciada ou quando um usuário ativa a proteção de tela por meio do painel de controle.

quando uma proteção de tela é escolhida, o Windows monitora os pressionamentos de tecla e os movimentos do mouse e, em seguida, inicia a proteção de tela após um período de inatividade. no entanto, Windows não iniciará a proteção de tela se qualquer uma das seguintes condições existir:

-   o aplicativo ativo não é um aplicativo baseado em Windows.
-   Uma janela de treinamento baseado em computador (CBT) está presente.
-   O aplicativo ativo recebe a [mensagem \_ SYSCOMMAND do WM](../menurc/wm-syscommand.md) com o parâmetro *wParam* definido como o \_ valor SC SCREENSAVE, mas não passa a mensagem para a função [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .

**Contexto de segurança da proteção de tela**

O contexto de segurança da proteção de tela depende de se um usuário está conectado interativamente. Se um usuário estiver conectado interativamente quando a proteção de tela for chamada, a proteção de tela será executada no contexto de segurança do usuário interativo. se nenhum usuário estiver conectado, o contexto de segurança da proteção de tela dependerá da versão do Windows que está sendo usado.

-   Windows XP e Windows 2000-a proteção de tela é executada no contexto de LocalSystem com contas restritas.
-   Windows 2003-a proteção de tela é executada no contexto de LocalService com todos os privilégios removidos e grupo de administradores desabilitado.
-   não se aplica a Windows o NT4.

O contexto de segurança determina o nível de operações privilegiadas que podem ser feitas em uma proteção de tela.

**Windows Vista e posterior:** Se a proteção por senha estiver habilitada pela política, a proteção de tela será iniciada, independentemente do que um aplicativo faz com a \_ notificação SC SCREENSAVE.

As proteções de tela contêm funções exportadas específicas, definições de recursos e declarações de variáveis. A biblioteca de proteção de tela contém a função **principal** e outro código de inicialização necessário para uma proteção de tela. Quando uma proteção de tela é iniciada, o código de inicialização na biblioteca de proteção de tela cria uma janela de tela inteira. A classe de janela dessa janela é declarada da seguinte maneira:


```
WNDCLASS cls; 
cls.hCursor        = NULL; 
cls.hIcon          = LoadIcon(hInst, MAKEINTATOM(ID_APP)); 
cls.lpszMenuName   = NULL; 
cls.lpszClassName  = "WindowsScreenSaverClass"; 
cls.hbrBackground  = GetStockObject(BLACK_BRUSH); 
cls.hInstance      = hInst; 
cls.style          = CS_VREDRAW  | CS_HREDRAW | CS_SAVEBITS | CS_DBLCLKS; 
cls.lpfnWndProc    = (WNDPROC) ScreenSaverProc; 
cls.cbWndExtra     = 0; 
cls.cbClsExtra     = 0;
```



Para criar uma proteção de tela, a maioria dos desenvolvedores cria um módulo de código-fonte que contém três funções necessárias e as vincula à biblioteca de proteção de tela. Um módulo de proteção de tela é responsável apenas pela configuração e pelo fornecimento de efeitos visuais.

Uma das três funções necessárias em um módulo de proteção de tela é [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc). Essa função processa mensagens específicas e passa todas as mensagens não processadas de volta para a biblioteca de proteção de tela. A seguir estão algumas das mensagens típicas processadas pelo **ScreenSaverProc**.



| Mensagem        | Significado                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| criação do WM \_     | Recupere todos os dados de inicialização do arquivo de Regedit.ini. Defina um timer de janela para a janela de proteção de tela. Execute qualquer outra inicialização necessária.                                     |
| ERASEBKGND do WM \_ | Apague a janela proteção de tela e prepare-se para operações de desenho subsequentes.                                                                                                               |
| \_temporizador do WM      | Executar operações de desenho.                                                                                                                                                                |
| destruição do WM \_    | Destrua os temporizadores criados quando o aplicativo processou a mensagem de [ \_ criação do WM](../winmsg/wm-create.md) . Execute qualquer limpeza adicional necessária. |



 

O [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) passa mensagens não processadas para a biblioteca de proteção de tela chamando a função [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) . A tabela a seguir descreve como essa função processa várias mensagens.



| Mensagem         | Ação                                                                    |
|-----------------|---------------------------------------------------------------------------|
| WM \_ SETcursor   | Defina o cursor para o cursor NULL, removendo-o da tela.           |
| pintura do WM \_       | Paint o plano de fundo da tela.                                              |
| LBUTTONDOWN do WM \_ | Encerre a proteção de tela.                                               |
| MBUTTONDOWN do WM \_ | Encerre a proteção de tela.                                               |
| RBUTTONDOWN do WM \_ | Encerre a proteção de tela.                                               |
| o WM \_ KEYDOWN     | Encerre a proteção de tela.                                               |
| admousemove do WM \_   | Encerre a proteção de tela.                                               |
| ativar o WM \_    | Encerre a proteção de tela se o parâmetro *wParam* estiver definido como **false**. |



 

A segunda função necessária em um módulo de proteção de tela é [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog). Essa função exibe uma caixa de diálogo que permite ao usuário configurar a proteção de tela (um aplicativo deve fornecer um modelo de caixa de diálogo correspondente). Windows exibe a caixa de diálogo configuração quando o usuário seleciona o botão **instalação** na caixa de diálogo proteção de tela do painel de controle.

A terceira função necessária em um módulo de proteção de tela é [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses). Essa função deve ser chamada por todos os aplicativos de proteção de tela. No entanto, os aplicativos que não exigem janelas especiais ou controles personalizados na caixa de diálogo de configuração podem simplesmente retornar **true**. Aplicativos que exigem controles especiais do Windows ou personalizados devem usar essa função para registrar as classes de janela correspondentes.

Além de criar um módulo que dê suporte às três funções que acabamos de descrever, uma proteção de tela deve fornecer um ícone. Esse ícone só é visível quando a proteção de tela é executada como um aplicativo autônomo. (Para ser executado pelo painel de controle, uma proteção de tela deve ter a extensão de nome de arquivo. SCR; para ser executada como um aplicativo autônomo, ela deve ter a extensão de nome de arquivo .exe.) O ícone deve ser identificado no arquivo de recurso da proteção de tela pelo aplicativo de ID de constante \_ , que é definido no arquivo de cabeçalho SCRNSAVE. h.

Um requisito final é uma cadeia de caracteres de descrição de proteção de tela. O arquivo de recurso para uma proteção de tela deve conter uma cadeia de caracteres que o painel de controle exibe como o nome da proteção de tela. A cadeia de caracteres de descrição deve ser a primeira cadeia de caracteres na tabela de cadeias de caracteres do arquivo de recurso (identificada com o valor ordinal 1). No entanto, a cadeia de caracteres de descrição será ignorada pelo painel de controle se a proteção de tela tiver um nome de arquivo longo. Nesse caso, o nome do arquivo será usado como a cadeia de caracteres de descrição.

## <a name="using-the-screen-saver-functions"></a>Usando as funções de proteção de tela

Esta seção usa o código de exemplo obtido de um aplicativo de proteção de tela para ilustrar as seguintes tarefas:

-   [Criando uma proteção de tela](#creating-a-screen-saver)
-   [Instalando novas proteções de tela](#installing-new-screen-savers)
-   [Adicionando ajuda à caixa de diálogo configuração de proteção de tela](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a>Criando uma proteção de tela

Em intervalos variando de 1 a 10 segundos, o aplicativo neste exemplo redesenha a tela com uma das quatro cores: branco, cinza claro, cinza escuro e preto. O aplicativo pinta a tela toda vez que recebe uma mensagem de [ \_ temporizador do WM](../winmsg/wm-timer.md) . O usuário pode ajustar o intervalo no qual essa mensagem é enviada, selecionando a caixa de diálogo configuração do aplicativo e ajustando uma barra de rolagem horizontal única.

### <a name="screen-saver-library"></a>Biblioteca de proteção de tela

As funções de proteção de tela estática estão contidas na biblioteca de proteção de tela. Há duas versões da biblioteca disponíveis, SCRNSAVE. lib e Scrnsavw. lib. Você deve vincular seu projeto com um deles. SCRNSAVE. lib é usado para proteções de tela que usam caracteres ANSI e Scrnsavw. lib é usado para proteções de tela que usam caracteres Unicode. uma proteção de tela vinculada a Scrnsavw. lib só será executada em plataformas Windows que dão suporte a Unicode, enquanto uma proteção de tela vinculada a Scrnsave. lib será executada em qualquer plataforma de Windows.

### <a name="supporting-the-configuration-dialog-box"></a>Suporte à caixa de diálogo de configuração

A maioria das proteções de tela fornece uma caixa de diálogo de configuração para permitir que o usuário especifique dados de personalização, como cores exclusivas, velocidades de desenho, espessura de linha, fontes e assim por diante. Para dar suporte à caixa de diálogo configuração, o aplicativo deve fornecer um modelo de caixa de diálogo e também deve dar suporte à função [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) . A seguir está o modelo de caixa de diálogo para o aplicativo de exemplo.


```
DLG_SCRNSAVECONFIGURE DIALOG 6, 18, 160, 63
LANGUAGE LANG_NEUTRAL, SUBLANG_NEUTRAL
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
CAPTION "Sample Screen-Saver Setup"
FONT 8, "MS Shell Dlg"
BEGIN
    GROUPBOX      "Redraw Speed", 101, 0, 6, 98, 40
    SCROLLBAR     ID_SPEED, 5, 31, 89, 10
    LTEXT         "Fast", 103, 6, 21, 20, 8
    LTEXT         "Slow", 104, 75, 21, 20, 8
    PUSHBUTTON    "OK", ID_OK, 117, 10, 40, 14
    PUSHBUTTON    "Cancel", ID_CANCEL, 117, 32, 40, 14
END
```



Você deve definir a constante usada para identificar o modelo da caixa de diálogo usando o valor decimal 2003, como no exemplo a seguir:


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



O exemplo a seguir mostra a função [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) encontrada no aplicativo de exemplo.


```
#define MINVEL  1                 // minimum redraw speed value     
#define MAXVEL  10                // maximum redraw speed value    
#define DEFVEL  5                 // default redraw speed value    
 
LONG    lSpeed = DEFVEL;          // redraw speed variable         
  
extern HINSTANCE hMainInstance;   // screen saver instance handle  
 
CHAR   szAppName[80];             // .ini section name             
CHAR   szTemp[20];                // temporary array of characters  
CHAR   szRedrawSpeed[ ] = "Redraw Speed";   // .ini speed entry 
CHAR   szIniFile[MAXFILELEN];     // .ini or registry file name  
 
BOOL WINAPI ScreenSaverConfigureDialog(hDlg, message, wParam, lParam) 
HWND     hDlg; 
UINT     message; 
DWORD    wParam; 
LONG     lParam; 
HRESULT  hr;
{ 
    static HWND hSpeed;   // handle to speed scroll bar 
    static HWND hOK;      // handle to OK push button  
 
    switch(message) 
    { 
        case WM_INITDIALOG: 
 
            // Retrieve the application name from the .rc file.  
            LoadString(hMainInstance, idsAppName, szAppName, 
                       80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, 
                       MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry. 
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // If the initialization file does not contain an entry 
            // for this screen saver, use the default value. 
            if(lSpeed > MAXVEL || lSpeed < MINVEL) 
                lSpeed = DEFVEL; 
 
            // Initialize the redraw speed scroll bar control.
            hSpeed = GetDlgItem(hDlg, ID_SPEED); 
            SetScrollRange(hSpeed, SB_CTL, MINVEL, MAXVEL, FALSE); 
            SetScrollPos(hSpeed, SB_CTL, lSpeed, TRUE); 
 
            // Retrieve a handle to the OK push button control.  
            hOK = GetDlgItem(hDlg, ID_OK); 
 
            return TRUE; 
 
        case WM_HSCROLL: 

            // Process scroll bar input, adjusting the lSpeed 
            // value as appropriate. 
            switch (LOWORD(wParam)) 
                { 
                    case SB_PAGEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_LINEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_PAGEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_LINEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_THUMBPOSITION: 
                        lSpeed = HIWORD(wParam); 
                    break; 
 
                    case SB_BOTTOM: 
                        lSpeed = MINVEL; 
                    break; 
 
                    case SB_TOP: 
                        lSpeed = MAXVEL; 
                    break; 
 
                    case SB_THUMBTRACK: 
                    case SB_ENDSCROLL: 
                        return TRUE; 
                    break; 
                } 

                if ((int) lSpeed <= MINVEL) 
                    lSpeed = MINVEL; 
                if ((int) lSpeed >= MAXVEL) 
                    lSpeed = MAXVEL; 
 
                SetScrollPos((HWND) lParam, SB_CTL, lSpeed, TRUE); 
            break; 
 
        case WM_COMMAND: 
            switch(LOWORD(wParam)) 
            { 
                case ID_OK: 
 
                    // Write the current redraw speed variable to
                    // the .ini file. 
                    hr = StringCchPrintf(szTemp, 20, "%ld", lSpeed);
                    if (SUCCEEDED(hr))
                        WritePrivateProfileString(szAppName, szRedrawSpeed, 
                                                  szTemp, szIniFile); 
 
                case ID_CANCEL: 
                    EndDialog(hDlg, LOWORD(wParam) == ID_OK); 

                return TRUE; 
            } 
    } 
    return FALSE; 
}
```



Além de fornecer o modelo de caixa de diálogo e dar suporte à função [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) , um aplicativo também deve oferecer suporte à função [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) . Essa função registra qualquer classe de janela não padrão exigida pela proteção de tela. Como o aplicativo de exemplo usou apenas as classes de janela padrão em seu procedimento de caixa de diálogo, essa função simplesmente retorna **true**, como no exemplo a seguir:


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a>Procedimento de suporte à janela de proteção de tela

Cada proteção de tela deve dar suporte a um procedimento de janela chamado [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc). Assim como a maioria dos procedimentos de janela, o **ScreenSaverProc** processa um conjunto de mensagens específicas e passa todas as mensagens não processadas para um procedimento padrão. No entanto, em vez de passá-los para a função [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) , o **ScreenSaverProc** passa mensagens não processadas para a função [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) . Outra diferença entre **ScreenSaverProc** e um procedimento de janela normal é que o identificador passado para **ScreenSaverProc** identifica toda a área de trabalho em vez de uma janela do cliente. O exemplo a seguir mostra o procedimento de janela **ScreenSaverProc** para a proteção de tela de exemplo.


```
LONG WINAPI ScreenSaverProc(hwnd, message, wParam, lParam) 
HWND  hwnd; 
UINT  message; 
DWORD wParam; 
LONG  lParam; 
{ 
    static HDC          hdc;      // device-context handle  
    static RECT         rc;       // RECT structure  
    static UINT         uTimer;   // timer identifier  
 
    switch(message) 
    { 
        case WM_CREATE: 
 
            // Retrieve the application name from the .rc file. 
            LoadString(hMainInstance, idsAppName, szAppName, 80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry.  
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // Set a timer for the screen saver window using the 
            // redraw rate stored in Regedit.ini. 
            uTimer = SetTimer(hwnd, 1, lSpeed * 1000, NULL); 
            break; 
 
        case WM_ERASEBKGND: 
 
            // The WM_ERASEBKGND message is issued before the 
            // WM_TIMER message, allowing the screen saver to 
            // paint the background as appropriate. 

            hdc = GetDC(hwnd); 
            GetClientRect (hwnd, &rc); 
            FillRect (hdc, &rc, GetStockObject(BLACK_BRUSH)); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_TIMER: 
 
            // The WM_TIMER message is issued at (lSpeed * 1000) 
            // intervals, where lSpeed == .001 seconds. This 
            // code repaints the entire desktop with a white, 
            // light gray, dark gray, or black brush each 
            // time a WM_TIMER message is issued. 

            hdc = GetDC(hwnd); 
            GetClientRect(hwnd, &rc); 
            if (i++ <= 4) 
                FillRect(hdc, &rc, GetStockObject(i)); 
            else 
                (i = 0); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_DESTROY: 
 
            // When the WM_DESTROY message is issued, the screen saver 
            // must destroy any of the timers that were set at WM_CREATE 
            // time. 

            if (uTimer) 
                KillTimer(hwnd, uTimer); 
            break; 
    } 
 
    // DefScreenSaverProc processes any messages ignored by ScreenSaverProc. 
    return DefScreenSaverProc(hwnd, message, wParam, lParam); 
}
```



### <a name="creating-a-module-definition-file"></a>Criando um arquivo de definição de módulo

As funções [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) e [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) devem ser exportadas no arquivo de definição de módulo do aplicativo; No entanto, o [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) não deve ser exportado. O exemplo a seguir mostra o arquivo de definição de módulo para o aplicativo de exemplo.


```
NAME    SSTEST.SCR 

DESCRIPTION 'SCRNSAVE : Test' 
 
STUB    'WINSTUB.EXE' 
EXETYPE WINDOWS 
 
CODE    MOVEABLE 
DATA    MOVEABLE MULTIPLE 
 
HEAPSIZE  1024 
STACKSIZE 4096 
 
EXPORTS 
        ScreenSaverProc 
        ScreenSaverConfigureDialog
```



### <a name="installing-new-screen-savers"></a>Instalando novas proteções de tela

ao compilar a lista de proteções de tela disponíveis, o painel de controle pesquisa o Windows diretório de inicialização para arquivos com a extensão. scr. como os salvadores de tela são arquivos executáveis Windows padrão com extensões de .exe, você deve renomeá-los para que tenham extensões. scr e copiá-los para o diretório correto.

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a>Adicionando ajuda à caixa de diálogo configuração de proteção de tela

A caixa de diálogo configuração de uma proteção de tela normalmente inclui um botão de **ajuda** . os aplicativos de proteção de tela podem verificar o identificador do botão de ajuda e chamar a função [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) da mesma forma que a ajuda é fornecida em outros aplicativos baseados em Windows.

 

 