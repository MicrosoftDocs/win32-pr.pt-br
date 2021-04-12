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
# <a name="using-the-clipboard"></a><span data-ttu-id="ae4d8-110">Usando a área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-110">Using the Clipboard</span></span>

<span data-ttu-id="ae4d8-111">Esta seção tem exemplos de código para as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="ae4d8-111">This section has code samples for the following tasks:</span></span>

-   [<span data-ttu-id="ae4d8-112">Implementando os comandos Recortar, copiar e colar</span><span class="sxs-lookup"><span data-stu-id="ae4d8-112">Implementing the Cut, Copy, and Paste Commands</span></span>](#implementing-the-cut-copy-and-paste-commands)
    -   [<span data-ttu-id="ae4d8-113">Selecionando dados</span><span class="sxs-lookup"><span data-stu-id="ae4d8-113">Selecting Data</span></span>](#selecting-data)
    -   [<span data-ttu-id="ae4d8-114">Criando um menu Editar</span><span class="sxs-lookup"><span data-stu-id="ae4d8-114">Creating an Edit Menu</span></span>](#creating-an-edit-menu)
    -   [<span data-ttu-id="ae4d8-115">Processando a \_ mensagem INITMENUPOPUP do WM</span><span class="sxs-lookup"><span data-stu-id="ae4d8-115">Processing the WM\_INITMENUPOPUP Message</span></span>](#processing-the-wm_initmenupopup-message)
    -   [<span data-ttu-id="ae4d8-116">Processando a \_ mensagem de comando do WM</span><span class="sxs-lookup"><span data-stu-id="ae4d8-116">Processing the WM\_COMMAND Message</span></span>](#processing-the-wm_command-message)
    -   [<span data-ttu-id="ae4d8-117">Copiando informações para a área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-117">Copying Information to the Clipboard</span></span>](#copying-information-to-the-clipboard)
    -   [<span data-ttu-id="ae4d8-118">Colando informações da área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-118">Pasting Information from the Clipboard</span></span>](#pasting-information-from-the-clipboard)
    -   [<span data-ttu-id="ae4d8-119">Registrando um formato de área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-119">Registering a Clipboard Format</span></span>](#registering-a-clipboard-format)
    -   [<span data-ttu-id="ae4d8-120">Processando as \_ mensagens do WM RENDERFORMAT e do WM \_ RENDERALLFORMATS</span><span class="sxs-lookup"><span data-stu-id="ae4d8-120">Processing the WM\_RENDERFORMAT and WM\_RENDERALLFORMATS Messages</span></span>](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [<span data-ttu-id="ae4d8-121">Processando a \_ mensagem DESTROYCLIPBOARD do WM</span><span class="sxs-lookup"><span data-stu-id="ae4d8-121">Processing the WM\_DESTROYCLIPBOARD Message</span></span>](#processing-the-wm_destroyclipboard-message)
    -   [<span data-ttu-id="ae4d8-122">Usando o formato de área de transferência Owner-Display</span><span class="sxs-lookup"><span data-stu-id="ae4d8-122">Using the Owner-Display Clipboard Format</span></span>](#using-the-owner-display-clipboard-format)
-   [<span data-ttu-id="ae4d8-123">Conteúdo da área de transferência de monitoramento</span><span class="sxs-lookup"><span data-stu-id="ae4d8-123">Monitoring Clipboard Contents</span></span>](#monitoring-clipboard-contents)
-   [<span data-ttu-id="ae4d8-124">Consultando o número de sequência da área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-124">Querying the Clipboard Sequence Number</span></span>](#querying-the-clipboard-sequence-number)
-   [<span data-ttu-id="ae4d8-125">Criando um ouvinte de formato de área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-125">Creating a Clipboard Format Listener</span></span>](#creating-a-clipboard-format-listener)
-   [<span data-ttu-id="ae4d8-126">Criando uma janela do Visualizador da área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-126">Creating a Clipboard Viewer Window</span></span>](#creating-a-clipboard-viewer-window)
-   [<span data-ttu-id="ae4d8-127">Adicionando uma janela à cadeia do Visualizador da área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-127">Adding a Window to the Clipboard Viewer Chain</span></span>](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [<span data-ttu-id="ae4d8-128">Processando a \_ mensagem CHANGECBCHAIN do WM</span><span class="sxs-lookup"><span data-stu-id="ae4d8-128">Processing the WM\_CHANGECBCHAIN Message</span></span>](#processing-the-wm_changecbchain-message)
    -   [<span data-ttu-id="ae4d8-129">Removendo uma janela da cadeia do Visualizador da área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-129">Removing a Window from the Clipboard Viewer Chain</span></span>](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [<span data-ttu-id="ae4d8-130">Processando a \_ mensagem DRAWCLIPBOARD do WM</span><span class="sxs-lookup"><span data-stu-id="ae4d8-130">Processing the WM\_DRAWCLIPBOARD Message</span></span>](#processing-the-wm_drawclipboard-message)
    -   [<span data-ttu-id="ae4d8-131">Exemplo de um visualizador de área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-131">Example of a Clipboard Viewer</span></span>](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a><span data-ttu-id="ae4d8-132">Implementando os comandos Recortar, copiar e colar</span><span class="sxs-lookup"><span data-stu-id="ae4d8-132">Implementing the Cut, Copy, and Paste Commands</span></span>

<span data-ttu-id="ae4d8-133">Esta seção descreve como os comandos **recortar**, **copiar** e **colar** padrão são implementados em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-133">This section describes how standard **Cut**, **Copy**, and **Paste** commands are implemented in an application.</span></span> <span data-ttu-id="ae4d8-134">O exemplo nesta seção usa esses métodos para inserir dados na área de transferência usando um formato de área de transferência registrado, o formato de **\_ OWNERDISPLAY do CF** e o formato de **\_ texto do CF** .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-134">The example in this section uses these methods to place data on the clipboard using a registered clipboard format, the **CF\_OWNERDISPLAY** format, and the **CF\_TEXT** format.</span></span> <span data-ttu-id="ae4d8-135">O formato registrado é usado para representar janelas de texto retangulares ou elípticos, chamadas rótulos.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-135">The registered format is used to represent rectangular or elliptical text windows, called labels.</span></span>

### <a name="selecting-data"></a><span data-ttu-id="ae4d8-136">Selecionando dados</span><span class="sxs-lookup"><span data-stu-id="ae4d8-136">Selecting Data</span></span>

<span data-ttu-id="ae4d8-137">Antes que as informações possam ser copiadas para a área de transferência, o usuário deve selecionar informações específicas a serem copiadas ou recortadas.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-137">Before information can be copied to the clipboard, the user must select specific information to be copied or cut.</span></span> <span data-ttu-id="ae4d8-138">Um aplicativo deve fornecer um meio para que o usuário selecione informações dentro de um documento e algum tipo de comentário visual para indicar os dados selecionados.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-138">An application should provide a means for the user to select information within a document and some kind of visual feedback to indicate selected data.</span></span>

### <a name="creating-an-edit-menu"></a><span data-ttu-id="ae4d8-139">Criando um menu Editar</span><span class="sxs-lookup"><span data-stu-id="ae4d8-139">Creating an Edit Menu</span></span>

<span data-ttu-id="ae4d8-140">Um aplicativo deve carregar uma tabela de acelerador que contém os aceleradores de teclado padrão para os comandos do menu **Editar** .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-140">An application should load an accelerator table containing the standard keyboard accelerators for the **Edit** menu commands.</span></span> <span data-ttu-id="ae4d8-141">A função [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) deve ser adicionada ao loop de mensagem do aplicativo para que os aceleradores entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-141">The [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function must be added to the application's message loop for the accelerators to take effect.</span></span> <span data-ttu-id="ae4d8-142">Para obter mais informações sobre aceleradores de teclado, consulte [aceleradores de teclado](/windows/desktop/menurc/keyboard-accelerators).</span><span class="sxs-lookup"><span data-stu-id="ae4d8-142">For more information about keyboard accelerators, see [Keyboard Accelerators](/windows/desktop/menurc/keyboard-accelerators).</span></span>

### <a name="processing-the-wm_initmenupopup-message"></a><span data-ttu-id="ae4d8-143">Processando a \_ mensagem INITMENUPOPUP do WM</span><span class="sxs-lookup"><span data-stu-id="ae4d8-143">Processing the WM\_INITMENUPOPUP Message</span></span>

<span data-ttu-id="ae4d8-144">Nem todos os comandos da área de transferência estão disponíveis para o usuário em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-144">Not all clipboard commands are available to the user at any given time.</span></span> <span data-ttu-id="ae4d8-145">Um aplicativo deve processar a mensagem do [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) para habilitar os itens de menu para os comandos disponíveis e desabilitar os comandos não disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-145">An application should process the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message to enable the menu items for available commands and disable unavailable commands.</span></span>

<span data-ttu-id="ae4d8-146">Veja a seguir o caso do [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) para um aplicativo chamado Label.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-146">Following is the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) case for an application named Label.</span></span>


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



<span data-ttu-id="ae4d8-147">A função InitMenu é definida da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-147">The InitMenu function is defined as follows.</span></span>


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



### <a name="processing-the-wm_command-message"></a><span data-ttu-id="ae4d8-148">Processando a \_ mensagem de comando do WM</span><span class="sxs-lookup"><span data-stu-id="ae4d8-148">Processing the WM\_COMMAND Message</span></span>

<span data-ttu-id="ae4d8-149">Para processar comandos de menu, adicione o caso de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) ao procedimento de janela principal do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-149">To process menu commands, add the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) case to your application's main window procedure.</span></span> <span data-ttu-id="ae4d8-150">Veja a seguir o caso de **\_ comando do WM** para o procedimento de janela do aplicativo de rótulo.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-150">Following is the **WM\_COMMAND** case for the Label application's window procedure.</span></span>


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



<span data-ttu-id="ae4d8-151">Para executar os comandos **Copy** e **Cut** , o procedimento window chama a função EditCopy definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-151">To carry out the **Copy** and **Cut** commands, the window procedure calls the application-defined EditCopy function.</span></span> <span data-ttu-id="ae4d8-152">Para obter mais informações, consulte [copiando informações para a área de transferência](#copying-information-to-the-clipboard).</span><span class="sxs-lookup"><span data-stu-id="ae4d8-152">For more information, see [Copying Information to the Clipboard](#copying-information-to-the-clipboard).</span></span> <span data-ttu-id="ae4d8-153">Para executar o comando **Paste** , o procedimento window chama a função EditPaste definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-153">To carry out the **Paste** command, the window procedure calls the application-defined EditPaste function.</span></span> <span data-ttu-id="ae4d8-154">Para obter mais informações sobre a função EditPaste, consulte [colando informações da área de transferência](#pasting-information-from-the-clipboard).</span><span class="sxs-lookup"><span data-stu-id="ae4d8-154">For more information about the EditPaste function, see [Pasting Information from the Clipboard](#pasting-information-from-the-clipboard).</span></span>

### <a name="copying-information-to-the-clipboard"></a><span data-ttu-id="ae4d8-155">Copiando informações para a área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-155">Copying Information to the Clipboard</span></span>

<span data-ttu-id="ae4d8-156">No aplicativo Label, a função EditCopy definida pelo aplicativo copia a seleção atual para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-156">In the Label application, the application-defined EditCopy function copies the current selection to the clipboard.</span></span> <span data-ttu-id="ae4d8-157">Essa função faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ae4d8-157">This function does the following:</span></span>

1.  <span data-ttu-id="ae4d8-158">Abre a área de transferência chamando a função [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-158">Opens the clipboard by calling the [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) function.</span></span>
2.  <span data-ttu-id="ae4d8-159">Esvazia a área de transferência chamando a função [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-159">Empties the clipboard by calling the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function.</span></span>
3.  <span data-ttu-id="ae4d8-160">Chama a função [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) uma vez para cada formato de área de transferência que o aplicativo fornece.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-160">Calls the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function once for each clipboard format the application provides.</span></span>
4.  <span data-ttu-id="ae4d8-161">Fecha a área de transferência chamando a função [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-161">Closes the clipboard by calling the [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) function.</span></span>

<span data-ttu-id="ae4d8-162">Dependendo da seleção atual, a função EditCopy copia um intervalo de texto ou copia uma estrutura definida pelo aplicativo que representa um rótulo inteiro.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-162">Depending on the current selection, the EditCopy function either copies a range of text or copies an application-defined structure representing an entire label.</span></span> <span data-ttu-id="ae4d8-163">A estrutura, chamada LABELBOX, é definida da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-163">The structure, called LABELBOX, is defined as follows.</span></span>


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



<span data-ttu-id="ae4d8-164">A seguir está a função EditCopy.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-164">Following is the EditCopy function.</span></span>


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



### <a name="pasting-information-from-the-clipboard"></a><span data-ttu-id="ae4d8-165">Colando informações da área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-165">Pasting Information from the Clipboard</span></span>

<span data-ttu-id="ae4d8-166">No aplicativo Label, a função EditPaste definida pelo aplicativo cola o conteúdo da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-166">In the Label application, the application-defined EditPaste function pastes the content of the clipboard.</span></span> <span data-ttu-id="ae4d8-167">Essa função faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ae4d8-167">This function does the following:</span></span>

1.  <span data-ttu-id="ae4d8-168">Abre a área de transferência chamando a função [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-168">Opens the clipboard by calling the [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) function.</span></span>
2.  <span data-ttu-id="ae4d8-169">Determina qual dos formatos de área de transferência disponíveis recuperar.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-169">Determines which of the available clipboard formats to retrieve.</span></span>
3.  <span data-ttu-id="ae4d8-170">Recupera o identificador para os dados no formato selecionado chamando a função [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-170">Retrieves the handle to the data in the selected format by calling the [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) function.</span></span>
4.  <span data-ttu-id="ae4d8-171">Insere uma cópia dos dados no documento.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-171">Inserts a copy of the data into the document.</span></span>

    <span data-ttu-id="ae4d8-172">O identificador retornado por [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) ainda pertence à área de transferência, portanto um aplicativo não deve liberá-lo ou deixá-lo bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-172">The handle returned by [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) is still owned by the clipboard, so an application must not free it or leave it locked.</span></span>

5.  <span data-ttu-id="ae4d8-173">Fecha a área de transferência chamando a função [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-173">Closes the clipboard by calling the [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) function.</span></span>

<span data-ttu-id="ae4d8-174">Se um rótulo for selecionado e contiver um ponto de inserção, a função EditPaste inserirá o texto da área de transferência no ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-174">If a label is selected and contains an insertion point, the EditPaste function inserts the text from the clipboard at the insertion point.</span></span> <span data-ttu-id="ae4d8-175">Se não houver nenhuma seleção ou se um rótulo for selecionado, a função criará um novo rótulo usando a estrutura LABELBOX definida pelo aplicativo na área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-175">If there is no selection or if a label is selected, the function creates a new label, using the application-defined LABELBOX structure on the clipboard.</span></span> <span data-ttu-id="ae4d8-176">A estrutura LABELBOX é colocada na área de transferência usando um formato de área de transferência registrado.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-176">The LABELBOX structure is placed on the clipboard by using a registered clipboard format.</span></span>

<span data-ttu-id="ae4d8-177">A estrutura, chamada LABELBOX, é definida da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-177">The structure, called LABELBOX, is defined as follows.</span></span>


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



<span data-ttu-id="ae4d8-178">A seguir está a função EditPaste.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-178">Following is the EditPaste function.</span></span>


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



### <a name="registering-a-clipboard-format"></a><span data-ttu-id="ae4d8-179">Registrando um formato de área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-179">Registering a Clipboard Format</span></span>

<span data-ttu-id="ae4d8-180">Para registrar um formato de área de transferência, adicione uma chamada à função [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) à função de inicialização de instância do aplicativo, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-180">To register a clipboard format, add a call to the [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) function to your application's instance initialization function, as follows.</span></span>


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



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a><span data-ttu-id="ae4d8-181">Processando as \_ mensagens do WM RENDERFORMAT e do WM \_ RENDERALLFORMATS</span><span class="sxs-lookup"><span data-stu-id="ae4d8-181">Processing the WM\_RENDERFORMAT and WM\_RENDERALLFORMATS Messages</span></span>

<span data-ttu-id="ae4d8-182">Se uma janela passar um identificador **nulo** para a função [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) , ela deverá processar as mensagens do [**WM \_ RENDERFORMAT**](wm-renderformat.md) e do [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) para renderizar dados na solicitação.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-182">If a window passes a **NULL** handle to the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function, it must process the [**WM\_RENDERFORMAT**](wm-renderformat.md) and [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) messages to render data upon request.</span></span>

<span data-ttu-id="ae4d8-183">Se uma janela atrasar o processamento de um formato específico e outro aplicativo solicitar dados nesse formato, uma mensagem do [**WM \_ RENDERFORMAT**](wm-renderformat.md) será enviada para a janela.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-183">If a window delays rendering a specific format and then another application requests data in that format, then a [**WM\_RENDERFORMAT**](wm-renderformat.md) message is sent to the window.</span></span> <span data-ttu-id="ae4d8-184">Além disso, se uma janela atrasar o processamento de um ou mais formatos, e se alguns desses formatos permanecerem sem renderização quando a janela estiver prestes a ser destruída, uma mensagem do [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) será enviada para a janela antes da sua destruição.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-184">In addition, if a window delays rendering one or more formats, and if some of those formats remain unrendered when the window is about to be destroyed, then a [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) message is sent to the window before its destruction.</span></span>

<span data-ttu-id="ae4d8-185">Para renderizar um formato de área de transferência, o procedimento de janela deve colocar um identificador de dados não **nulo** na área de transferência usando a função [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-185">To render a clipboard format, the window procedure should place a non-**NULL** data handle on the clipboard using the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function.</span></span> <span data-ttu-id="ae4d8-186">Se o procedimento de janela estiver renderizando um formato em resposta à mensagem do [**WM \_ RENDERFORMAT**](wm-renderformat.md) , ele não deverá abrir a área de transferência antes de chamar **SetClipboardData**.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-186">If the window procedure is rendering a format in response to the [**WM\_RENDERFORMAT**](wm-renderformat.md) message, it must not open the clipboard before calling **SetClipboardData**.</span></span> <span data-ttu-id="ae4d8-187">Mas se estiver renderizando um ou mais formatos em resposta à mensagem do [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) , ele deverá abrir a área de transferência e verificar se a janela ainda é proprietária da área de transferência antes de chamar **SetClipboardData** e deve fechar a área de transferência antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-187">But if it is rendering one or more formats in response to the [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) message, it must open the clipboard and check that the window still owns the clipboard before calling **SetClipboardData**, and it must close the clipboard before returning.</span></span>

<span data-ttu-id="ae4d8-188">O aplicativo de rótulo processa as mensagens do [**WM \_ RENDERFORMAT**](wm-renderformat.md) e do [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-188">The Label application processes the [**WM\_RENDERFORMAT**](wm-renderformat.md) and [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) messages as follows.</span></span>


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



<span data-ttu-id="ae4d8-189">Em ambos os casos, o procedimento de janela chama a função RenderFormat definida pelo aplicativo, definida da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-189">In both cases, the window procedure calls the application-defined RenderFormat function, defined as follows.</span></span>

<span data-ttu-id="ae4d8-190">A estrutura, chamada LABELBOX, é definida da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-190">The structure, called LABELBOX, is defined as follows.</span></span>


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



### <a name="processing-the-wm_destroyclipboard-message"></a><span data-ttu-id="ae4d8-191">Processando a \_ mensagem DESTROYCLIPBOARD do WM</span><span class="sxs-lookup"><span data-stu-id="ae4d8-191">Processing the WM\_DESTROYCLIPBOARD Message</span></span>

<span data-ttu-id="ae4d8-192">Uma janela pode processar a mensagem do [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) para liberar todos os recursos que ele Reserve para dar suporte à renderização atrasada.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-192">A window can process the [**WM\_DESTROYCLIPBOARD**](wm-destroyclipboard.md) message in order to free any resources that it set aside to support delayed rendering.</span></span> <span data-ttu-id="ae4d8-193">Por exemplo, o aplicativo Label, ao copiar um rótulo para a área de transferência, aloca um objeto de memória local.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-193">For example the Label application, when copying a label to the clipboard, allocates a local memory object.</span></span> <span data-ttu-id="ae4d8-194">Em seguida, ele libera esse objeto em resposta à mensagem do **WM \_ DESTROYCLIPBOARD** , da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-194">It then frees this object in response to the **WM\_DESTROYCLIPBOARD** message, as follows.</span></span>


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a><span data-ttu-id="ae4d8-195">Usando o formato de área de transferência Owner-Display</span><span class="sxs-lookup"><span data-stu-id="ae4d8-195">Using the Owner-Display Clipboard Format</span></span>

<span data-ttu-id="ae4d8-196">Se uma janela colocar informações na área de transferência usando o formato de área de transferência do **CF \_ OWNERDISPLAY** , ela deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ae4d8-196">If a window places information on the clipboard by using the **CF\_OWNERDISPLAY** clipboard format, it must do the following:</span></span>

-   <span data-ttu-id="ae4d8-197">Processar a mensagem do [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-197">Process the [**WM\_PAINTCLIPBOARD**](wm-paintclipboard.md) message.</span></span> <span data-ttu-id="ae4d8-198">Essa mensagem é enviada para o proprietário da área de transferência quando uma parte da janela do Visualizador da área de transferência deve ser redesenhada.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-198">This message is sent to the clipboard owner when a portion of the clipboard viewer window must be repainted.</span></span>

-   <span data-ttu-id="ae4d8-199">Processar a mensagem do [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-199">Process the [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span> <span data-ttu-id="ae4d8-200">Esta mensagem é enviada para o proprietário da área de transferência quando a janela do Visualizador da área de transferência foi redimensionada ou seu conteúdo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-200">This message is sent to the clipboard owner when the clipboard viewer window has been resized or its content has changed.</span></span>

    <span data-ttu-id="ae4d8-201">Normalmente, uma janela responde a essa mensagem definindo as posições e os intervalos de rolagem para a janela do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-201">Typically, a window responds to this message by setting the scroll positions and ranges for the clipboard viewer window.</span></span> <span data-ttu-id="ae4d8-202">Em resposta a essa mensagem, o aplicativo de rótulo também atualiza uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) para a janela do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-202">In response to this message, the Label application also updates a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure for the clipboard viewer window.</span></span>

-   <span data-ttu-id="ae4d8-203">Processe as mensagens do [**WM \_ HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) e do [**WM \_ VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-203">Process the [**WM\_HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) and [**WM\_VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) messages.</span></span> <span data-ttu-id="ae4d8-204">Essas mensagens são enviadas para o proprietário da área de transferência quando ocorre um evento de barra de rolagem na janela do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-204">These messages are sent to the clipboard owner when a scroll bar event occurs in the clipboard viewer window.</span></span>

-   <span data-ttu-id="ae4d8-205">Processar a mensagem do [**WM \_ ASKCBFORMATNAME**](wm-askcbformatname.md) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-205">Process the [**WM\_ASKCBFORMATNAME**](wm-askcbformatname.md) message.</span></span> <span data-ttu-id="ae4d8-206">A janela Visualizador da área de transferência envia essa mensagem a um aplicativo para recuperar o nome do formato de exibição do proprietário.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-206">The clipboard viewer window sends this message to an application to retrieve the name of the owner-display format.</span></span>

<span data-ttu-id="ae4d8-207">O procedimento de janela para o aplicativo Label processa essas mensagens, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-207">The window procedure for the Label application processes these messages, as follows.</span></span>


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



## <a name="monitoring-clipboard-contents"></a><span data-ttu-id="ae4d8-208">Conteúdo da área de transferência de monitoramento</span><span class="sxs-lookup"><span data-stu-id="ae4d8-208">Monitoring Clipboard Contents</span></span>

<span data-ttu-id="ae4d8-209">Há três maneiras de monitorar alterações na área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-209">There are three ways of monitoring changes to the clipboard.</span></span> <span data-ttu-id="ae4d8-210">O método mais antigo é criar uma janela do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-210">The oldest method is to create a clipboard viewer window.</span></span> <span data-ttu-id="ae4d8-211">O Windows 2000 adicionou a capacidade de consultar o número de sequência da área de transferência e o Windows Vista adicionou suporte para ouvintes de formato da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-211">Windows 2000 added the ability to query the clipboard sequence number, and Windows Vista added support for clipboard format listeners.</span></span> <span data-ttu-id="ae4d8-212">As janelas do Visualizador da área de transferência têm suporte para compatibilidade com versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-212">Clipboard viewer windows are supported for backward compatibility with earlier versions of Windows.</span></span> <span data-ttu-id="ae4d8-213">Novos programas devem usar ouvintes de formato de área de transferência ou o número de sequência da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-213">New programs should use clipboard format listeners or the clipboard sequence number.</span></span>

## <a name="querying-the-clipboard-sequence-number"></a><span data-ttu-id="ae4d8-214">Consultando o número de sequência da área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-214">Querying the Clipboard Sequence Number</span></span>

<span data-ttu-id="ae4d8-215">Cada vez que o conteúdo da área de transferência é alterado, um valor de 32 bits conhecido como o número de sequência da área de transferência é incrementado.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-215">Each time the contents of the clipboard change, a 32-bit value known as the clipboard sequence number is incremented.</span></span> <span data-ttu-id="ae4d8-216">Um programa pode recuperar o número de sequência da área de transferência atual chamando a função [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-216">A program can retrieve the current clipboard sequence number by calling the [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) function.</span></span> <span data-ttu-id="ae4d8-217">Comparando o valor retornado em relação a um valor retornado por uma chamada anterior para **GetClipboardSequenceNumber**, um programa pode determinar se o conteúdo da área de transferência foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-217">By comparing the value returned against a value returned by a previous call to **GetClipboardSequenceNumber**, a program can determine whether the clipboard contents have changed.</span></span> <span data-ttu-id="ae4d8-218">Esse método é mais adequado para programas que armazenam os resultados em cache com base no conteúdo da área de transferência atual e precisam saber se os cálculos ainda são válidos antes de usar os resultados desse cache.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-218">This method is more suitable to programs which cache results based on the current clipboard contents and need to know whether the calculations are still valid before using the results from that cache.</span></span> <span data-ttu-id="ae4d8-219">Observe que esse não é um método de notificação e não deve ser usado em um loop de sondagem.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-219">Note that this is a not a notification method and should not be used in a polling loop.</span></span> <span data-ttu-id="ae4d8-220">Para ser notificado quando o conteúdo da área de transferência for alterado, use um ouvinte de formato da área de transferência ou um visualizador de</span><span class="sxs-lookup"><span data-stu-id="ae4d8-220">To be notified when clipboard contents change, use a clipboard format listener or a clipboard viewer.</span></span>

## <a name="creating-a-clipboard-format-listener"></a><span data-ttu-id="ae4d8-221">Criando um ouvinte de formato de área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-221">Creating a Clipboard Format Listener</span></span>

<span data-ttu-id="ae4d8-222">Um ouvinte de formato de área de transferência é uma janela que foi registrada para ser notificada quando o conteúdo da área de transferência é alterado.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-222">A clipboard format listener is a window which has registered to be notified when the contents of the clipboard has changed.</span></span> <span data-ttu-id="ae4d8-223">Esse método é recomendado para a criação de uma janela do Visualizador da área de transferência porque é mais simples implementar e evitar problemas se os programas não mantiverem a cadeia do Visualizador da área de transferência corretamente ou se uma janela na cadeia do Visualizador da área de transferência parar de responder às mensagens.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-223">This method is recommended over creating a clipboard viewer window because it is simpler to implement and avoids problems if programs fail to maintain the clipboard viewer chain properly or if a window in the clipboard viewer chain stops responding to messages.</span></span>

<span data-ttu-id="ae4d8-224">Uma janela é registrada como um ouvinte de formato da área de transferência chamando a função [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-224">A window registers as a clipboard format listener by calling the [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) function.</span></span> <span data-ttu-id="ae4d8-225">Quando o conteúdo da área de transferência for alterado, a janela será postada uma mensagem do [**WM \_ CLIPBOARDUPDATE**](wm-clipboardupdate.md) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-225">When the contents of the clipboard change, the window is posted a [**WM\_CLIPBOARDUPDATE**](wm-clipboardupdate.md) message.</span></span> <span data-ttu-id="ae4d8-226">O registro permanece válido até que a janela Cancele seu registro chamando a função [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-226">The registration remains valid until the window unregister itself by calling the [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) function.</span></span>

## <a name="creating-a-clipboard-viewer-window"></a><span data-ttu-id="ae4d8-227">Criando uma janela do Visualizador da área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-227">Creating a Clipboard Viewer Window</span></span>

<span data-ttu-id="ae4d8-228">Uma janela do Visualizador da área de transferência exibe o conteúdo atual da área de transferência e recebe mensagens quando o conteúdo da área de transferência é alterado.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-228">A clipboard viewer window displays the current content of the clipboard, and receives messages when the clipboard content changes.</span></span> <span data-ttu-id="ae4d8-229">Para criar uma janela do Visualizador da área de transferência, o aplicativo deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ae4d8-229">To create a clipboard viewer window, your application must do the following:</span></span>

-   <span data-ttu-id="ae4d8-230">Adicione a janela à cadeia do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-230">Add the window to the clipboard viewer chain.</span></span>
-   <span data-ttu-id="ae4d8-231">Processar a mensagem do [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-231">Process the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>
-   <span data-ttu-id="ae4d8-232">Processar a mensagem do [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-232">Process the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message.</span></span>
-   <span data-ttu-id="ae4d8-233">Remova a janela da cadeia do Visualizador da área de transferência antes de ela ser destruída.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-233">Remove the window from the clipboard viewer chain before it is destroyed.</span></span>

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a><span data-ttu-id="ae4d8-234">Adicionando uma janela à cadeia do Visualizador da área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-234">Adding a Window to the Clipboard Viewer Chain</span></span>

<span data-ttu-id="ae4d8-235">Uma janela adiciona-se à cadeia do Visualizador da área de transferência chamando a função [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-235">A window adds itself to the clipboard viewer chain by calling the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span> <span data-ttu-id="ae4d8-236">O valor de retorno é o identificador para a próxima janela na cadeia.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-236">The return value is the handle to the next window in the chain.</span></span> <span data-ttu-id="ae4d8-237">Uma janela deve manter o controle desse valor, por exemplo, salvando-o em uma variável estática chamada *hwndNextViewer*.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-237">A window must keep track of this value — for example, by saving it in a static variable named *hwndNextViewer*.</span></span>

<span data-ttu-id="ae4d8-238">O exemplo a seguir adiciona uma janela à cadeia do Visualizador da área de transferência em resposta à mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-238">The following example adds a window to the clipboard viewer chain in response to the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span>


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



<span data-ttu-id="ae4d8-239">Os trechos de código são mostrados para as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="ae4d8-239">Code snippets are shown for the following tasks:</span></span>

-   [<span data-ttu-id="ae4d8-240">Processando a \_ mensagem CHANGECBCHAIN do WM</span><span class="sxs-lookup"><span data-stu-id="ae4d8-240">Processing the WM\_CHANGECBCHAIN Message</span></span>](/windows)
-   [<span data-ttu-id="ae4d8-241">Removendo uma janela da cadeia do Visualizador da área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-241">Removing a Window from the Clipboard Viewer Chain</span></span>](#removing-a-window-from-the-clipboard-viewer-chain)
-   [<span data-ttu-id="ae4d8-242">Processando a \_ mensagem DRAWCLIPBOARD do WM</span><span class="sxs-lookup"><span data-stu-id="ae4d8-242">Processing the WM\_DRAWCLIPBOARD Message</span></span>](/windows)
-   [<span data-ttu-id="ae4d8-243">Exemplo de um visualizador de área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-243">Example of a Clipboard Viewer</span></span>](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a><span data-ttu-id="ae4d8-244">Processando a \_ mensagem CHANGECBCHAIN do WM</span><span class="sxs-lookup"><span data-stu-id="ae4d8-244">Processing the WM\_CHANGECBCHAIN Message</span></span>

<span data-ttu-id="ae4d8-245">Uma janela do Visualizador da área de transferência recebe a mensagem [**\_ CHANGECBCHAIN do WM**](wm-changecbchain.md) quando outra janela está se removendo da cadeia do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-245">A clipboard viewer window receives the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message when another window is removing itself from the clipboard viewer chain.</span></span> <span data-ttu-id="ae4d8-246">Se a janela que está sendo removida for a próxima janela na cadeia, a janela que receberá a mensagem deverá desvincular a próxima janela da cadeia.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-246">If the window being removed is the next window in the chain, the window receiving the message must unlink the next window from the chain.</span></span> <span data-ttu-id="ae4d8-247">Caso contrário, essa mensagem deve ser passada para a próxima janela na cadeia.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-247">Otherwise, this message should be passed to the next window in the chain.</span></span>

<span data-ttu-id="ae4d8-248">O exemplo a seguir mostra o processamento da mensagem do [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-248">The following example shows the processing of the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>


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



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a><span data-ttu-id="ae4d8-249">Removendo uma janela da cadeia do Visualizador da área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-249">Removing a Window from the Clipboard Viewer Chain</span></span>

<span data-ttu-id="ae4d8-250">Para se remover da cadeia do Visualizador da área de transferência, uma janela chama a função [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-250">To remove itself from the clipboard viewer chain, a window calls the [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) function.</span></span> <span data-ttu-id="ae4d8-251">O exemplo a seguir remove uma janela da cadeia do Visualizador da área de transferência em resposta à mensagem de [**\_ destruição do WM**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="ae4d8-251">The following example removes a window from the clipboard viewer chain in response to the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a><span data-ttu-id="ae4d8-252">Processando a \_ mensagem DRAWCLIPBOARD do WM</span><span class="sxs-lookup"><span data-stu-id="ae4d8-252">Processing the WM\_DRAWCLIPBOARD Message</span></span>

<span data-ttu-id="ae4d8-253">A mensagem do [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) notifica uma janela do Visualizador da área de transferência de que o conteúdo da área de transferência foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-253">The [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message notifies a clipboard viewer window that the content of the clipboard has changed.</span></span> <span data-ttu-id="ae4d8-254">Uma janela deve fazer o seguinte ao processar a **mensagem \_ DRAWCLIPBOARD do WM** :</span><span class="sxs-lookup"><span data-stu-id="ae4d8-254">A window should do the following when processing the **WM\_DRAWCLIPBOARD** message:</span></span>

1.  <span data-ttu-id="ae4d8-255">Determine qual dos formatos de área de transferência disponíveis exibir.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-255">Determine which of the available clipboard formats to display.</span></span>
2.  <span data-ttu-id="ae4d8-256">Recupere os dados da área de transferência e exiba-os na janela.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-256">Retrieve the clipboard data and display it in the window.</span></span> <span data-ttu-id="ae4d8-257">Ou se o formato da área de transferência for **CF \_ OWNERDISPLAY**, envie uma mensagem do [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) para o proprietário da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-257">Or if the clipboard format is **CF\_OWNERDISPLAY**, send a [**WM\_PAINTCLIPBOARD**](wm-paintclipboard.md) message to the clipboard owner.</span></span>
3.  <span data-ttu-id="ae4d8-258">Envie a mensagem para a próxima janela na cadeia do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-258">Send the message to the next window in the clipboard viewer chain.</span></span>

<span data-ttu-id="ae4d8-259">Para obter um exemplo de processamento da mensagem do [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) , consulte a listagem de exemplo em [exemplo de um visualizador da área de transferência](#example-of-a-clipboard-viewer).</span><span class="sxs-lookup"><span data-stu-id="ae4d8-259">For an example of processing the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message, see the example listing in [Example of a Clipboard Viewer](#example-of-a-clipboard-viewer).</span></span>

### <a name="example-of-a-clipboard-viewer"></a><span data-ttu-id="ae4d8-260">Exemplo de um visualizador de área de transferência</span><span class="sxs-lookup"><span data-stu-id="ae4d8-260">Example of a Clipboard Viewer</span></span>

<span data-ttu-id="ae4d8-261">O exemplo a seguir mostra um aplicativo de visualizador de área de transferência simples.</span><span class="sxs-lookup"><span data-stu-id="ae4d8-261">The following example shows a simple clipboard viewer application.</span></span>


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



 

 