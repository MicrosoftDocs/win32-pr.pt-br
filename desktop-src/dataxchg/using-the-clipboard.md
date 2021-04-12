---
title: Usando a área de transferência
description: Esta seção tem exemplos de código para as seguintes tarefas
ms.assetid: 377fb2cc-5b46-481a-8222-9291e504ae2c
keywords:
- área de transferência, recortando dados
- área de transferência, copiando dados
- área de transferência, colando dados
- área de transferência, selecionando dados
- área de transferência, comandos de menu Editar
- área de transferência, visualizadores
- área de transferência, janelas de visualizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c7e7d6db6f25bc1016eefbcc5afc9f5e0db44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294168"
---
# <a name="using-the-clipboard"></a>Usando a área de transferência

Esta seção tem exemplos de código para as seguintes tarefas:

-   [Implementando os comandos Recortar, copiar e colar](#implementing-the-cut-copy-and-paste-commands)
    -   [Selecionando dados](#selecting-data)
    -   [Criando um menu Editar](#creating-an-edit-menu)
    -   [Processando a \_ mensagem INITMENUPOPUP do WM](#processing-the-wm_initmenupopup-message)
    -   [Processando a \_ mensagem de comando do WM](#processing-the-wm_command-message)
    -   [Copiando informações para a área de transferência](#copying-information-to-the-clipboard)
    -   [Colando informações da área de transferência](#pasting-information-from-the-clipboard)
    -   [Registrando um formato de área de transferência](#registering-a-clipboard-format)
    -   [Processando as \_ mensagens do WM RENDERFORMAT e do WM \_ RENDERALLFORMATS](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [Processando a \_ mensagem DESTROYCLIPBOARD do WM](#processing-the-wm_destroyclipboard-message)
    -   [Usando o formato de área de transferência Owner-Display](#using-the-owner-display-clipboard-format)
-   [Conteúdo da área de transferência de monitoramento](#monitoring-clipboard-contents)
-   [Consultando o número de sequência da área de transferência](#querying-the-clipboard-sequence-number)
-   [Criando um ouvinte de formato de área de transferência](#creating-a-clipboard-format-listener)
-   [Criando uma janela do Visualizador da área de transferência](#creating-a-clipboard-viewer-window)
-   [Adicionando uma janela à cadeia do Visualizador da área de transferência](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [Processando a \_ mensagem CHANGECBCHAIN do WM](#processing-the-wm_changecbchain-message)
    -   [Removendo uma janela da cadeia do Visualizador da área de transferência](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [Processando a \_ mensagem DRAWCLIPBOARD do WM](#processing-the-wm_drawclipboard-message)
    -   [Exemplo de um visualizador de área de transferência](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a>Implementando os comandos Recortar, copiar e colar

Esta seção descreve como os comandos **recortar**, **copiar** e **colar** padrão são implementados em um aplicativo. O exemplo nesta seção usa esses métodos para inserir dados na área de transferência usando um formato de área de transferência registrado, o formato de **\_ OWNERDISPLAY do CF** e o formato de **\_ texto do CF** . O formato registrado é usado para representar janelas de texto retangulares ou elípticos, chamadas rótulos.

### <a name="selecting-data"></a>Selecionando dados

Antes que as informações possam ser copiadas para a área de transferência, o usuário deve selecionar informações específicas a serem copiadas ou recortadas. Um aplicativo deve fornecer um meio para que o usuário selecione informações dentro de um documento e algum tipo de comentário visual para indicar os dados selecionados.

### <a name="creating-an-edit-menu"></a>Criando um menu Editar

Um aplicativo deve carregar uma tabela de acelerador que contém os aceleradores de teclado padrão para os comandos do menu **Editar** . A função [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) deve ser adicionada ao loop de mensagem do aplicativo para que os aceleradores entrem em vigor. Para obter mais informações sobre aceleradores de teclado, consulte [aceleradores de teclado](/windows/desktop/menurc/keyboard-accelerators).

### <a name="processing-the-wm_initmenupopup-message"></a>Processando a \_ mensagem INITMENUPOPUP do WM

Nem todos os comandos da área de transferência estão disponíveis para o usuário em um determinado momento. Um aplicativo deve processar a mensagem do [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) para habilitar os itens de menu para os comandos disponíveis e desabilitar os comandos não disponíveis.

Veja a seguir o caso do [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) para um aplicativo chamado Label.


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



A função InitMenu é definida da seguinte maneira.


```
void WINAPI InitMenu(HMENU hmenu) 
{ 
    int  cMenuItems = GetMenuItemCount(hmenu); 
    int  nPos; 
    UINT id; 
    UINT fuFlags; 
    PLABELBOX pbox = (hwndSelected == NULL) ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    for (nPos = 0; nPos < cMenuItems; nPos++) 
    { 
        id = GetMenuItemID(hmenu, nPos); 
 
        switch (id) 
        { 
            case IDM_CUT: 
            case IDM_COPY: 
            case IDM_DELETE: 
                if (pbox == NULL || !pbox->fSelected) 
                    fuFlags = MF_BYCOMMAND | MF_GRAYED; 
                else if (pbox->fEdit) 
                    fuFlags = (id != IDM_DELETE && pbox->ichSel 
                            == pbox->ichCaret) ? 
                        MF_BYCOMMAND | MF_GRAYED : 
                        MF_BYCOMMAND | MF_ENABLED; 
                else 
                    fuFlags = MF_BYCOMMAND | MF_ENABLED; 
 
                EnableMenuItem(hmenu, id, fuFlags); 
                break; 
 
            case IDM_PASTE: 
                if (pbox != NULL && pbox->fEdit) 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable(CF_TEXT) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
                else 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable( 
                                uLabelFormat) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
 
        } 
    } 
}
```



### <a name="processing-the-wm_command-message"></a>Processando a \_ mensagem de comando do WM

Para processar comandos de menu, adicione o caso de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) ao procedimento de janela principal do seu aplicativo. Veja a seguir o caso de **\_ comando do WM** para o procedimento de janela do aplicativo de rótulo.


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_CUT: 
            if (EditCopy()) 
                EditDelete(); 
            break; 
 
        case IDM_COPY: 
            EditCopy(); 
            break; 
 
        case IDM_PASTE: 
            EditPaste(); 
            break; 
 
        case IDM_DELETE: 
            EditDelete(); 
            break; 
 
        case IDM_EXIT: 
            DestroyWindow(hwnd); 
    } 
    break; 
```



Para executar os comandos **Copy** e **Cut** , o procedimento window chama a função EditCopy definida pelo aplicativo. Para obter mais informações, consulte [copiando informações para a área de transferência](#copying-information-to-the-clipboard). Para executar o comando **Paste** , o procedimento window chama a função EditPaste definida pelo aplicativo. Para obter mais informações sobre a função EditPaste, consulte [colando informações da área de transferência](#pasting-information-from-the-clipboard).

### <a name="copying-information-to-the-clipboard"></a>Copiando informações para a área de transferência

No aplicativo Label, a função EditCopy definida pelo aplicativo copia a seleção atual para a área de transferência. Essa função faz o seguinte:

1.  Abre a área de transferência chamando a função [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .
2.  Esvazia a área de transferência chamando a função [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) .
3.  Chama a função [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) uma vez para cada formato de área de transferência que o aplicativo fornece.
4.  Fecha a área de transferência chamando a função [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

Dependendo da seleção atual, a função EditCopy copia um intervalo de texto ou copia uma estrutura definida pelo aplicativo que representa um rótulo inteiro. A estrutura, chamada LABELBOX, é definida da seguinte maneira.


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



A seguir está a função EditCopy.


```
BOOL WINAPI EditCopy(VOID) 
{ 
    PLABELBOX pbox; 
    LPTSTR  lptstrCopy; 
    HGLOBAL hglbCopy; 
    int ich1, ich2, cch; 
 
    if (hwndSelected == NULL) 
        return FALSE; 
 
    // Open the clipboard, and empty it. 
 
    if (!OpenClipboard(hwndMain)) 
        return FALSE; 
    EmptyClipboard(); 
 
    // Get a pointer to the structure for the selected label. 
 
    pbox = (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If text is selected, copy it using the CF_TEXT format. 
 
    if (pbox->fEdit) 
    { 
        if (pbox->ichSel == pbox->ichCaret)     // zero length
        {   
            CloseClipboard();                   // selection 
            return FALSE; 
        } 
 
        if (pbox->ichSel < pbox->ichCaret) 
        { 
            ich1 = pbox->ichSel; 
            ich2 = pbox->ichCaret; 
        } 
        else 
        { 
            ich1 = pbox->ichCaret; 
            ich2 = pbox->ichSel; 
        } 
        cch = ich2 - ich1; 
 
        // Allocate a global memory object for the text. 
 
        hglbCopy = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglbCopy == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
 
        // Lock the handle and copy the text to the buffer. 
 
        lptstrCopy = GlobalLock(hglbCopy); 
        memcpy(lptstrCopy, &pbox->atchLabel[ich1], 
            cch * sizeof(TCHAR)); 
        lptstrCopy[cch] = (TCHAR) 0;    // null character 
        GlobalUnlock(hglbCopy); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglbCopy); 
    } 
 
    // If no text is selected, the label as a whole is copied. 
 
    else 
    { 
        // Save a copy of the selected label as a local memory 
        // object. This copy is used to render data on request. 
        // It is freed in response to the WM_DESTROYCLIPBOARD 
        // message. 
 
        pboxLocalClip = (PLABELBOX) LocalAlloc( 
            LMEM_FIXED, 
            sizeof(LABELBOX) 
        ); 
        if (pboxLocalClip == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
        memcpy(pboxLocalClip, pbox, sizeof(LABELBOX)); 
        pboxLocalClip->fSelected = FALSE; 
        pboxLocalClip->fEdit = FALSE; 
 
        // Place a registered clipboard format, the owner-display 
        // format, and the CF_TEXT format on the clipboard using 
        // delayed rendering. 
 
        SetClipboardData(uLabelFormat, NULL); 
        SetClipboardData(CF_OWNERDISPLAY, NULL); 
        SetClipboardData(CF_TEXT, NULL); 
    } 
 
    // Close the clipboard. 
 
    CloseClipboard(); 
 
    return TRUE; 
}
```



### <a name="pasting-information-from-the-clipboard"></a>Colando informações da área de transferência

No aplicativo Label, a função EditPaste definida pelo aplicativo cola o conteúdo da área de transferência. Essa função faz o seguinte:

1.  Abre a área de transferência chamando a função [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .
2.  Determina qual dos formatos de área de transferência disponíveis recuperar.
3.  Recupera o identificador para os dados no formato selecionado chamando a função [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) .
4.  Insere uma cópia dos dados no documento.

    O identificador retornado por [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) ainda pertence à área de transferência, portanto um aplicativo não deve liberá-lo ou deixá-lo bloqueado.

5.  Fecha a área de transferência chamando a função [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

Se um rótulo for selecionado e contiver um ponto de inserção, a função EditPaste inserirá o texto da área de transferência no ponto de inserção. Se não houver nenhuma seleção ou se um rótulo for selecionado, a função criará um novo rótulo usando a estrutura LABELBOX definida pelo aplicativo na área de transferência. A estrutura LABELBOX é colocada na área de transferência usando um formato de área de transferência registrado.

A estrutura, chamada LABELBOX, é definida da seguinte maneira.


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



A seguir está a função EditPaste.


```
VOID WINAPI EditPaste(VOID) 
{ 
    PLABELBOX pbox; 
    HGLOBAL   hglb; 
    LPTSTR    lptstr; 
    PLABELBOX pboxCopy; 
    int cx, cy; 
    HWND hwnd; 
 
    pbox = hwndSelected == NULL ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If the application is in edit mode, 
    // get the clipboard text. 
 
    if (pbox != NULL && pbox->fEdit) 
    { 
        if (!IsClipboardFormatAvailable(CF_TEXT)) 
            return; 
        if (!OpenClipboard(hwndMain)) 
            return; 
 
        hglb = GetClipboardData(CF_TEXT); 
        if (hglb != NULL) 
        { 
            lptstr = GlobalLock(hglb); 
            if (lptstr != NULL) 
            { 
                // Call the application-defined ReplaceSelection 
                // function to insert the text and repaint the 
                // window. 
 
                ReplaceSelection(hwndSelected, pbox, lptstr); 
                GlobalUnlock(hglb); 
            } 
        } 
        CloseClipboard(); 
 
        return; 
    } 
 
    // If the application is not in edit mode, 
    // create a label window. 
 
    if (!IsClipboardFormatAvailable(uLabelFormat)) 
        return; 
    if (!OpenClipboard(hwndMain)) 
        return; 
 
    hglb = GetClipboardData(uLabelFormat); 
    if (hglb != NULL) 
    { 
        pboxCopy = GlobalLock(hglb); 
        if (pboxCopy != NULL) 
        { 
            cx = pboxCopy->rcText.right + CX_MARGIN; 
            cy = pboxCopy->rcText.top * 2 + cyText; 
 
            hwnd = CreateWindowEx( 
                WS_EX_NOPARENTNOTIFY | WS_EX_TRANSPARENT, 
                atchClassChild, NULL, WS_CHILD, 0, 0, cx, cy, 
                hwndMain, NULL, hinst, NULL 
            ); 
            if (hwnd != NULL) 
            { 
                pbox = (PLABELBOX) GetWindowLong(hwnd, 0); 
                memcpy(pbox, pboxCopy, sizeof(LABELBOX)); 
                ShowWindow(hwnd, SW_SHOWNORMAL); 
                SetFocus(hwnd); 
            } 
            GlobalUnlock(hglb); 
        } 
    } 
    CloseClipboard(); 
}
```



### <a name="registering-a-clipboard-format"></a>Registrando um formato de área de transferência

Para registrar um formato de área de transferência, adicione uma chamada à função [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) à função de inicialização de instância do aplicativo, da seguinte maneira.


```
// Register a clipboard format. 
 
// We assume that atchTemp can contain the format name and
// a null-terminator, otherwise it is truncated.
//
LoadString(hinstCurrent, IDS_FORMATNAME, atchTemp, 
    sizeof(atchTemp)/sizeof(TCHAR)); 
uLabelFormat = RegisterClipboardFormat(atchTemp); 
if (uLabelFormat == 0) 
    return FALSE;
```



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a>Processando as \_ mensagens do WM RENDERFORMAT e do WM \_ RENDERALLFORMATS

Se uma janela passar um identificador **nulo** para a função [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) , ela deverá processar as mensagens do [**WM \_ RENDERFORMAT**](wm-renderformat.md) e do [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) para renderizar dados na solicitação.

Se uma janela atrasar o processamento de um formato específico e outro aplicativo solicitar dados nesse formato, uma mensagem do [**WM \_ RENDERFORMAT**](wm-renderformat.md) será enviada para a janela. Além disso, se uma janela atrasar o processamento de um ou mais formatos, e se alguns desses formatos permanecerem sem renderização quando a janela estiver prestes a ser destruída, uma mensagem do [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) será enviada para a janela antes da sua destruição.

Para renderizar um formato de área de transferência, o procedimento de janela deve colocar um identificador de dados não **nulo** na área de transferência usando a função [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) . Se o procedimento de janela estiver renderizando um formato em resposta à mensagem do [**WM \_ RENDERFORMAT**](wm-renderformat.md) , ele não deverá abrir a área de transferência antes de chamar **SetClipboardData**. Mas se estiver renderizando um ou mais formatos em resposta à mensagem do [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) , ele deverá abrir a área de transferência e verificar se a janela ainda é proprietária da área de transferência antes de chamar **SetClipboardData** e deve fechar a área de transferência antes de retornar.

O aplicativo de rótulo processa as mensagens do [**WM \_ RENDERFORMAT**](wm-renderformat.md) e do [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) da seguinte maneira.


```
case WM_RENDERFORMAT: 
    RenderFormat((UINT) wParam); 
    break; 
 
case WM_RENDERALLFORMATS:
    if (OpenClipboard(hwnd))
    {
        if (GetClipboardOwner() == hwnd)
        {
            RenderFormat(uLabelFormat);
            RenderFormat(CF_TEXT);
        }
        CloseClipboard();
    }
    break;
```



Em ambos os casos, o procedimento de janela chama a função RenderFormat definida pelo aplicativo, definida da seguinte maneira.

A estrutura, chamada LABELBOX, é definida da seguinte maneira.


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```




```
void WINAPI RenderFormat(UINT uFormat) 
{ 
    HGLOBAL hglb; 
    PLABELBOX pbox; 
    LPTSTR  lptstr; 
    int cch; 
 
    if (pboxLocalClip == NULL) 
        return; 
 
    if (uFormat == CF_TEXT) 
    { 
        // Allocate a buffer for the text. 
 
        cch = pboxLocalClip->cchLabel; 
        hglb = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglb == NULL) 
            return; 
 
        // Copy the text from pboxLocalClip. 
 
        lptstr = GlobalLock(hglb); 
        memcpy(lptstr, pboxLocalClip->atchLabel, 
            cch * sizeof(TCHAR)); 
        lptstr[cch] = (TCHAR) 0; 
        GlobalUnlock(hglb); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglb); 
    } 
    else if (uFormat == uLabelFormat) 
    { 
        hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(LABELBOX)); 
        if (hglb == NULL) 
            return; 
        pbox = GlobalLock(hglb); 
        memcpy(pbox, pboxLocalClip, sizeof(LABELBOX)); 
        GlobalUnlock(hglb); 
 
        SetClipboardData(uLabelFormat, hglb); 
    } 
}
```



### <a name="processing-the-wm_destroyclipboard-message"></a>Processando a \_ mensagem DESTROYCLIPBOARD do WM

Uma janela pode processar a mensagem do [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) para liberar todos os recursos que ele Reserve para dar suporte à renderização atrasada. Por exemplo, o aplicativo Label, ao copiar um rótulo para a área de transferência, aloca um objeto de memória local. Em seguida, ele libera esse objeto em resposta à mensagem do **WM \_ DESTROYCLIPBOARD** , da seguinte maneira.


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a>Usando o formato de área de transferência Owner-Display

Se uma janela colocar informações na área de transferência usando o formato de área de transferência do **CF \_ OWNERDISPLAY** , ela deverá fazer o seguinte:

-   Processar a mensagem do [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) . Essa mensagem é enviada para o proprietário da área de transferência quando uma parte da janela do Visualizador da área de transferência deve ser redesenhada.

-   Processar a mensagem do [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) . Esta mensagem é enviada para o proprietário da área de transferência quando a janela do Visualizador da área de transferência foi redimensionada ou seu conteúdo foi alterado.

    Normalmente, uma janela responde a essa mensagem definindo as posições e os intervalos de rolagem para a janela do Visualizador da área de transferência. Em resposta a essa mensagem, o aplicativo de rótulo também atualiza uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) para a janela do Visualizador da área de transferência.

-   Processe as mensagens do [**WM \_ HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) e do [**WM \_ VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) . Essas mensagens são enviadas para o proprietário da área de transferência quando ocorre um evento de barra de rolagem na janela do Visualizador da área de transferência.

-   Processar a mensagem do [**WM \_ ASKCBFORMATNAME**](wm-askcbformatname.md) . A janela Visualizador da área de transferência envia essa mensagem a um aplicativo para recuperar o nome do formato de exibição do proprietário.

O procedimento de janela para o aplicativo Label processa essas mensagens, da seguinte maneira.


```
LRESULT CALLBACK MainWindowProc(hwnd, msg, wParam, lParam) 
HWND hwnd; 
UINT msg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static RECT rcViewer; 
 
    RECT rc; 
    LPRECT lprc; 
    LPPAINTSTRUCT lpps; 
 
    switch (msg) 
    { 
        //
        // Handle other messages.
        //
        case WM_PAINTCLIPBOARD: 
            // Determine the dimensions of the label. 
 
            SetRect(&rc, 0, 0, 
                pboxLocalClip->rcText.right + CX_MARGIN, 
                pboxLocalClip->rcText.top * 2 + cyText 
            ); 
 
            // Center the image in the clipboard viewer window. 
 
            if (rc.right < rcViewer.right) 
            { 
                rc.left = (rcViewer.right - rc.right) / 2; 
                rc.right += rc.left; 
            } 
            if (rc.bottom < rcViewer.bottom) 
            { 
                rc.top = (rcViewer.bottom - rc.bottom) / 2; 
                rc.bottom += rc.top; 
            } 
 
            // Paint the image, using the specified PAINTSTRUCT 
            // structure, by calling the application-defined 
            // PaintLabel function. 
 
            lpps = (LPPAINTSTRUCT) GlobalLock((HGLOBAL) lParam); 
            PaintLabel(lpps, pboxLocalClip, &rc); 
            GlobalUnlock((HGLOBAL) lParam); 
            break; 
 
        case WM_SIZECLIPBOARD: 
            // Save the dimensions of the window in a static 
            // RECT structure. 
 
            lprc = (LPRECT) GlobalLock((HGLOBAL) lParam); 
            memcpy(&rcViewer, lprc, sizeof(RECT)); 
            GlobalUnlock((HGLOBAL) lParam); 
 
            // Set the scroll ranges to zero (thus eliminating 
            // the need to process the WM_HSCROLLCLIPBOARD and 
            // WM_VSCROLLCLIPBOARD messages). 
 
            SetScrollRange((HWND) wParam, SB_HORZ, 0, 0, TRUE); 
            SetScrollRange((HWND) wParam, SB_VERT, 0, 0, TRUE); 
 
            break; 
 
        case WM_ASKCBFORMATNAME: 
            LoadString(hinst, IDS_OWNERDISPLAY, 
                (LPSTR) lParam, wParam); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
}
```



## <a name="monitoring-clipboard-contents"></a>Conteúdo da área de transferência de monitoramento

Há três maneiras de monitorar alterações na área de transferência. O método mais antigo é criar uma janela do Visualizador da área de transferência. O Windows 2000 adicionou a capacidade de consultar o número de sequência da área de transferência e o Windows Vista adicionou suporte para ouvintes de formato da área de transferência. As janelas do Visualizador da área de transferência têm suporte para compatibilidade com versões anteriores do Windows. Novos programas devem usar ouvintes de formato de área de transferência ou o número de sequência da área de transferência.

## <a name="querying-the-clipboard-sequence-number"></a>Consultando o número de sequência da área de transferência

Cada vez que o conteúdo da área de transferência é alterado, um valor de 32 bits conhecido como o número de sequência da área de transferência é incrementado. Um programa pode recuperar o número de sequência da área de transferência atual chamando a função [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) . Comparando o valor retornado em relação a um valor retornado por uma chamada anterior para **GetClipboardSequenceNumber**, um programa pode determinar se o conteúdo da área de transferência foi alterado. Esse método é mais adequado para programas que armazenam os resultados em cache com base no conteúdo da área de transferência atual e precisam saber se os cálculos ainda são válidos antes de usar os resultados desse cache. Observe que esse não é um método de notificação e não deve ser usado em um loop de sondagem. Para ser notificado quando o conteúdo da área de transferência for alterado, use um ouvinte de formato da área de transferência ou um visualizador de

## <a name="creating-a-clipboard-format-listener"></a>Criando um ouvinte de formato de área de transferência

Um ouvinte de formato de área de transferência é uma janela que foi registrada para ser notificada quando o conteúdo da área de transferência é alterado. Esse método é recomendado para a criação de uma janela do Visualizador da área de transferência porque é mais simples implementar e evitar problemas se os programas não mantiverem a cadeia do Visualizador da área de transferência corretamente ou se uma janela na cadeia do Visualizador da área de transferência parar de responder às mensagens.

Uma janela é registrada como um ouvinte de formato da área de transferência chamando a função [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) . Quando o conteúdo da área de transferência for alterado, a janela será postada uma mensagem do [**WM \_ CLIPBOARDUPDATE**](wm-clipboardupdate.md) . O registro permanece válido até que a janela Cancele seu registro chamando a função [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) .

## <a name="creating-a-clipboard-viewer-window"></a>Criando uma janela do Visualizador da área de transferência

Uma janela do Visualizador da área de transferência exibe o conteúdo atual da área de transferência e recebe mensagens quando o conteúdo da área de transferência é alterado. Para criar uma janela do Visualizador da área de transferência, o aplicativo deve fazer o seguinte:

-   Adicione a janela à cadeia do Visualizador da área de transferência.
-   Processar a mensagem do [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .
-   Processar a mensagem do [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) .
-   Remova a janela da cadeia do Visualizador da área de transferência antes de ela ser destruída.

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a>Adicionando uma janela à cadeia do Visualizador da área de transferência

Uma janela adiciona-se à cadeia do Visualizador da área de transferência chamando a função [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) . O valor de retorno é o identificador para a próxima janela na cadeia. Uma janela deve manter o controle desse valor, por exemplo, salvando-o em uma variável estática chamada *hwndNextViewer*.

O exemplo a seguir adiciona uma janela à cadeia do Visualizador da área de transferência em resposta à mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) .


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



Os trechos de código são mostrados para as seguintes tarefas:

-   [Processando a \_ mensagem CHANGECBCHAIN do WM](/windows)
-   [Removendo uma janela da cadeia do Visualizador da área de transferência](#removing-a-window-from-the-clipboard-viewer-chain)
-   [Processando a \_ mensagem DRAWCLIPBOARD do WM](/windows)
-   [Exemplo de um visualizador de área de transferência](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a>Processando a \_ mensagem CHANGECBCHAIN do WM

Uma janela do Visualizador da área de transferência recebe a mensagem [**\_ CHANGECBCHAIN do WM**](wm-changecbchain.md) quando outra janela está se removendo da cadeia do Visualizador da área de transferência. Se a janela que está sendo removida for a próxima janela na cadeia, a janela que receberá a mensagem deverá desvincular a próxima janela da cadeia. Caso contrário, essa mensagem deve ser passada para a próxima janela na cadeia.

O exemplo a seguir mostra o processamento da mensagem do [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .


```
case WM_CHANGECBCHAIN: 
 
    // If the next window is closing, repair the chain. 
 
    if ((HWND) wParam == hwndNextViewer) 
        hwndNextViewer = (HWND) lParam; 
 
    // Otherwise, pass the message to the next link. 
 
    else if (hwndNextViewer != NULL) 
        SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
    break;
```



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a>Removendo uma janela da cadeia do Visualizador da área de transferência

Para se remover da cadeia do Visualizador da área de transferência, uma janela chama a função [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) . O exemplo a seguir remove uma janela da cadeia do Visualizador da área de transferência em resposta à mensagem de [**\_ destruição do WM**](/windows/desktop/winmsg/wm-destroy) .


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a>Processando a \_ mensagem DRAWCLIPBOARD do WM

A mensagem do [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) notifica uma janela do Visualizador da área de transferência de que o conteúdo da área de transferência foi alterado. Uma janela deve fazer o seguinte ao processar a **mensagem \_ DRAWCLIPBOARD do WM** :

1.  Determine qual dos formatos de área de transferência disponíveis exibir.
2.  Recupere os dados da área de transferência e exiba-os na janela. Ou se o formato da área de transferência for **CF \_ OWNERDISPLAY**, envie uma mensagem do [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) para o proprietário da área de transferência.
3.  Envie a mensagem para a próxima janela na cadeia do Visualizador da área de transferência.

Para obter um exemplo de processamento da mensagem do [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) , consulte a listagem de exemplo em [exemplo de um visualizador da área de transferência](#example-of-a-clipboard-viewer).

### <a name="example-of-a-clipboard-viewer"></a>Exemplo de um visualizador de área de transferência

O exemplo a seguir mostra um aplicativo de visualizador de área de transferência simples.


```
HINSTANCE hinst; 
UINT uFormat = (UINT)(-1); 
BOOL fAuto = TRUE; 
 
LRESULT APIENTRY MainWndProc(hwnd, uMsg, wParam, lParam) 
HWND hwnd; 
UINT uMsg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static HWND hwndNextViewer; 
 
    HDC hdc; 
    HDC hdcMem; 
    PAINTSTRUCT ps; 
    LPPAINTSTRUCT lpps; 
    RECT rc; 
    LPRECT lprc; 
    HGLOBAL hglb; 
    LPSTR lpstr; 
    HBITMAP hbm; 
    HENHMETAFILE hemf; 
    HWND hwndOwner; 
 
    switch (uMsg) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
 
            // Branch depending on the clipboard format. 
 
            switch (uFormat) 
            { 
                case CF_OWNERDISPLAY: 
                    hwndOwner = GetClipboardOwner(); 
                    hglb = GlobalAlloc(GMEM_MOVEABLE, 
                        sizeof(PAINTSTRUCT)); 
                    lpps = GlobalLock(hglb);
                    memcpy(lpps, &ps, sizeof(PAINTSTRUCT)); 
                    GlobalUnlock(hglb); 
 
                    SendMessage(hwndOwner, WM_PAINTCLIPBOARD, 
                        (WPARAM) hwnd, (LPARAM) hglb); 
 
                    GlobalFree(hglb); 
                    break; 
 
                case CF_BITMAP: 
                    hdcMem = CreateCompatibleDC(hdc); 
                    if (hdcMem != NULL) 
                    { 
                        if (OpenClipboard(hwnd)) 
                        { 
                            hbm = (HBITMAP) 
                                GetClipboardData(uFormat); 
                            SelectObject(hdcMem, hbm); 
                            GetClientRect(hwnd, &rc); 
 
                            BitBlt(hdc, 0, 0, rc.right, rc.bottom, 
                                hdcMem, 0, 0, SRCCOPY); 
                            CloseClipboard(); 
                        } 
                        DeleteDC(hdcMem); 
                    } 
                    break; 
 
                case CF_TEXT: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hglb = GetClipboardData(uFormat); 
                        lpstr = GlobalLock(hglb); 
 
                        GetClientRect(hwnd, &rc); 
                        DrawText(hdc, lpstr, -1, &rc, DT_LEFT); 
 
                        GlobalUnlock(hglb); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case CF_ENHMETAFILE: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hemf = GetClipboardData(uFormat); 
                        GetClientRect(hwnd, &rc); 
                        PlayEnhMetaFile(hdc, hemf, &rc); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case 0: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "The clipboard is empty.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
                    break; 
 
                default: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "Unable to display format.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
            } 
            EndPaint(hwnd, &ps); 
            break; 
 
        case WM_SIZE: 
            if (uFormat == CF_OWNERDISPLAY) 
            { 
                hwndOwner = GetClipboardOwner(); 
                hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(RECT)); 
                lprc = GlobalLock(hglb); 
                GetClientRect(hwnd, lprc); 
                GlobalUnlock(hglb); 
 
                SendMessage(hwndOwner, WM_SIZECLIPBOARD, 
                    (WPARAM) hwnd, (LPARAM) hglb); 
 
                GlobalFree(hglb); 
            } 
            break; 
 
        case WM_CREATE: 
 
            // Add the window to the clipboard viewer chain. 
 
            hwndNextViewer = SetClipboardViewer(hwnd); 
            break; 
 
        case WM_CHANGECBCHAIN: 
 
            // If the next window is closing, repair the chain. 
 
            if ((HWND) wParam == hwndNextViewer) 
                hwndNextViewer = (HWND) lParam; 
 
            // Otherwise, pass the message to the next link. 
 
            else if (hwndNextViewer != NULL) 
                SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
            break; 
 
        case WM_DESTROY: 
            ChangeClipboardChain(hwnd, hwndNextViewer); 
            PostQuitMessage(0); 
            break; 
 
        case WM_DRAWCLIPBOARD:  // clipboard contents changed. 
 
            // Update the window by using Auto clipboard format. 
 
            SetAutoView(hwnd); 
 
            // Pass the message to the next window in clipboard 
            // viewer chain. 
 
            SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
            break; 
 
        case WM_INITMENUPOPUP: 
            if (!HIWORD(lParam)) 
                InitMenu(hwnd, (HMENU) wParam); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_EXIT: 
                    DestroyWindow(hwnd); 
                    break; 
 
                case IDM_AUTO: 
                    SetAutoView(hwnd); 
                    break; 
 
                default: 
                    fAuto = FALSE; 
                    uFormat = LOWORD(wParam); 
                    InvalidateRect(hwnd, NULL, TRUE); 
            } 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return (LRESULT) NULL; 
} 
 
void WINAPI SetAutoView(HWND hwnd) 
{ 
    static UINT auPriorityList[] = { 
        CF_OWNERDISPLAY, 
        CF_TEXT, 
        CF_ENHMETAFILE, 
        CF_BITMAP 
    }; 
 
    uFormat = GetPriorityClipboardFormat(auPriorityList, 4); 
    fAuto = TRUE; 
 
    InvalidateRect(hwnd, NULL, TRUE); 
    UpdateWindow(hwnd); 
} 
 
void WINAPI InitMenu(HWND hwnd, HMENU hmenu) 
{ 
    UINT uFormat; 
    char szFormatName[80]; 
    LPCSTR lpFormatName; 
    UINT fuFlags; 
    UINT idMenuItem; 
 
    // If a menu is not the display menu, no initialization is necessary. 
 
    if (GetMenuItemID(hmenu, 0) != IDM_AUTO) 
        return; 
 
    // Delete all menu items except the first. 
 
    while (GetMenuItemCount(hmenu) > 1) 
        DeleteMenu(hmenu, 1, MF_BYPOSITION); 
 
    // Check or uncheck the Auto menu item. 
 
    fuFlags = fAuto ? MF_BYCOMMAND | MF_CHECKED : 
        MF_BYCOMMAND | MF_UNCHECKED; 
    CheckMenuItem(hmenu, IDM_AUTO, fuFlags); 
 
    // If there are no clipboard formats, return. 
 
    if (CountClipboardFormats() == 0) 
        return; 
 
    // Open the clipboard. 
 
    if (!OpenClipboard(hwnd)) 
        return; 
 
    // Add a separator and then a menu item for each format. 
 
    AppendMenu(hmenu, MF_SEPARATOR, 0, NULL); 
    uFormat = EnumClipboardFormats(0); 
 
    while (uFormat) 
    { 
        // Call an application-defined function to get the name 
        // of the clipboard format. 
 
        lpFormatName = GetPredefinedClipboardFormatName(uFormat); 
 
        // For registered formats, get the registered name. 
 
        if (lpFormatName == NULL) 
        {

        // Note that, if the format name is larger than the
        // buffer, it is truncated. 
            if (GetClipboardFormatName(uFormat, szFormatName, 
                    sizeof(szFormatName))) 
                lpFormatName = szFormatName; 
            else 
                lpFormatName = "(unknown)"; 
        } 
 
        // Add a menu item for the format. For displayable 
        // formats, use the format ID for the menu ID. 
 
        if (IsDisplayableFormat(uFormat)) 
        { 
            fuFlags = MF_STRING; 
            idMenuItem = uFormat; 
        } 
        else 
        { 
            fuFlags = MF_STRING | MF_GRAYED; 
            idMenuItem = 0; 
        } 
        AppendMenu(hmenu, fuFlags, idMenuItem, lpFormatName); 
 
        uFormat = EnumClipboardFormats(uFormat); 
    } 
    CloseClipboard(); 
 
} 
 
BOOL WINAPI IsDisplayableFormat(UINT uFormat) 
{ 
    switch (uFormat) 
    { 
        case CF_OWNERDISPLAY: 
        case CF_TEXT: 
        case CF_ENHMETAFILE: 
        case CF_BITMAP: 
            return TRUE; 
    } 
    return FALSE; 
} 
```



 

 