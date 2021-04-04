---
title: Como criar um Owner-Drawn caixa de combinação
description: Este tópico demonstra como usar uma caixa de combinação de desenho proprietário.
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5355dd33fe0067165308e9e6e5885b76edbe7ceb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008399"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a><span data-ttu-id="e14a7-103">Como criar um Owner-Drawn caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="e14a7-103">How to Create an Owner-Drawn Combo Box</span></span>

<span data-ttu-id="e14a7-104">Este tópico demonstra como usar uma caixa de combinação de desenho proprietário.</span><span class="sxs-lookup"><span data-stu-id="e14a7-104">This topic demonstrates how to use an owner-drawn combo box.</span></span> <span data-ttu-id="e14a7-105">O exemplo de código C++ usa uma caixa de listagem suspensa desenhada pelo proprietário para exibir os quatro grupos de alimentos, cada um representado por um bitmap e um nome.</span><span class="sxs-lookup"><span data-stu-id="e14a7-105">The C++ code example uses an owner-drawn drop-down list box to display the four food groups, each represented by a bitmap and a name.</span></span> <span data-ttu-id="e14a7-106">Selecionar um grupo de alimentos faz com que o pratos nesse grupo apareça em uma lista.</span><span class="sxs-lookup"><span data-stu-id="e14a7-106">Selecting a food group causes the foods in that group to appear in a list.</span></span>

![captura de tela mostrando uma caixa de diálogo com uma caixa de listagem e uma caixa de listagem suspensa expandida mostrando um ícone e um rótulo para cada item](images/cscbx-01.png)

<span data-ttu-id="e14a7-108">A caixa de diálogo também contém uma caixa de listagem (IDLIST) e dois botões: **OK** (IDOK) e **Cancel** (IDCANCEL).</span><span class="sxs-lookup"><span data-stu-id="e14a7-108">The dialog box also contains a list box (IDLIST) and two buttons: **OK** (IDOK) and **Cancel** (IDCANCEL).</span></span> <span data-ttu-id="e14a7-109">As constantes IDOK e IDCANCEL são definidas pelos arquivos de cabeçalho do SDK.</span><span class="sxs-lookup"><span data-stu-id="e14a7-109">The IDOK and IDCANCEL constants are defined by the SDK header files.</span></span> <span data-ttu-id="e14a7-110">A constante IDLIST é definida no arquivo de cabeçalho do aplicativo, assim como o identificador de controle, IDCOMBO.</span><span class="sxs-lookup"><span data-stu-id="e14a7-110">The constant IDLIST is defined in the application's header file, as is the control identifier, IDCOMBO.</span></span> <span data-ttu-id="e14a7-111">Para obter mais informações sobre caixas de diálogo, consulte [caixas de diálogo](/windows/desktop/dlgbox/dialog-boxes).</span><span class="sxs-lookup"><span data-stu-id="e14a7-111">For more information about dialog boxes, see [Dialog Boxes](/windows/desktop/dlgbox/dialog-boxes).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e14a7-112">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="e14a7-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e14a7-113">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="e14a7-113">Technologies</span></span>

-   [<span data-ttu-id="e14a7-114">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="e14a7-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e14a7-115">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e14a7-115">Prerequisites</span></span>

-   <span data-ttu-id="e14a7-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="e14a7-116">C/C++</span></span>
-   <span data-ttu-id="e14a7-117">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="e14a7-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e14a7-118">Instruções</span><span class="sxs-lookup"><span data-stu-id="e14a7-118">Instructions</span></span>

### <a name="step-1-create-the-owner-drawn-dialog-box"></a><span data-ttu-id="e14a7-119">Etapa 1: criar a caixa de diálogo Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="e14a7-119">Step 1: Create the Owner-Drawn Dialog Box</span></span>

<span data-ttu-id="e14a7-120">O exemplo de código usa a função [**caixa**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) para criar uma caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="e14a7-120">The code example uses the [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) function to create a modal dialog box.</span></span> <span data-ttu-id="e14a7-121">O modelo de caixa de diálogo, IDD \_ SQMEAL, define os estilos de janela, os botões e os identificadores de controle da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="e14a7-121">The dialog box template, IDD\_SQMEAL, defines the window styles, buttons, and control identifiers for the combo box.</span></span> <span data-ttu-id="e14a7-122">A caixa de combinação neste exemplo usa os estilos de [**CBS \_ DROPDOWNLIST**](combo-box-styles.md), [**CBS \_ OwnerDrawFixed**](combo-box-styles.md), CBS [**\_ Sort**](combo-box-styles.md), [**CBS \_ HASSTRINGS**](combo-box-styles.md), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)e [**WS \_ TabStop**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="e14a7-122">The combo box in this example uses the [**CBS\_DROPDOWNLIST**](combo-box-styles.md), [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md), [**CBS\_SORT**](combo-box-styles.md), [**CBS\_HASSTRINGS**](combo-box-styles.md), [**WS\_VSCROLL**](/windows/desktop/winmsg/window-styles), and [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) styles.</span></span>


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a><span data-ttu-id="e14a7-123">Etapa 2: processar as mensagens do WM \_ INITDIALOG e do WM \_ Destroy em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e14a7-123">Step 2: Process the WM\_INITDIALOG and WM\_DESTROY messages in a dialog box.</span></span>

<span data-ttu-id="e14a7-124">Quando você usa uma caixa de combinação em uma caixa de diálogo, geralmente responde a uma mensagem do [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) inicializando a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="e14a7-124">When you use a combo box in a dialog box, you usually respond to a [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message by initializing the combo box.</span></span> <span data-ttu-id="e14a7-125">O aplicativo carrega os bitmaps usados para a caixa de combinação desenhada pelo proprietário e, em seguida, chama a função definida pelo aplicativo `InitGroupList` para inicializar a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="e14a7-125">The application loads the bitmaps used for the owner-drawn combo box and then calls the application-defined `InitGroupList` function to initialize the combo box.</span></span> <span data-ttu-id="e14a7-126">Ele também seleciona o primeiro item de lista na caixa de combinação e, em seguida, chama a função definida pelo aplicativo `InitFoodList` para inicializar a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="e14a7-126">It also selects the first list item in the combo box and then calls the application-defined `InitFoodList` function to initialize the list box.</span></span>

<span data-ttu-id="e14a7-127">No exemplo, a caixa de combinação desenhada pelo proprietário é uma caixa de listagem suspensa que contém os nomes de cada um dos quatro grupos de alimentos.</span><span class="sxs-lookup"><span data-stu-id="e14a7-127">In the example, the owner-drawn combo box is a drop-down list box that contains the names of each of the four food groups.</span></span> <span data-ttu-id="e14a7-128">`InitGroupList` Adiciona o nome de cada grupo de alimentos e usa a mensagem [**CB \_ SETITEMDATA**](cb-setitemdata.md) para associar um identificador de bitmap a cada item de lista que identifica um grupo de alimentos.</span><span class="sxs-lookup"><span data-stu-id="e14a7-128">`InitGroupList` adds the name of each food group , and uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item that identifies a food group.</span></span>

<span data-ttu-id="e14a7-129">A caixa de listagem no exemplo contém os nomes de pratos no grupo de alimentos selecionado.</span><span class="sxs-lookup"><span data-stu-id="e14a7-129">The list box in the example contains the names of foods in the selected food group.</span></span> <span data-ttu-id="e14a7-130">**InitFoodList** redefine o conteúdo da caixa de listagem e, em seguida, adiciona os nomes da seleção de alimentos atual na caixa de listagem suspensa grupo de alimentos atual.</span><span class="sxs-lookup"><span data-stu-id="e14a7-130">**InitFoodList** resets the contents of the list box, then adds the names of the current food selection in the current food group drop-down list box.</span></span>


```C++
case WM_INITDIALOG:

    // Call an application-defined function to load bitmap resources.
    if (!LoadIconBitmaps())
    {
        EndDialog(hDlg, -1);
        break;
    }

    // Initialize the food groups combo box and select the first item.
    InitGroupList(hDlg);
    SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

    // Initialize the food list box and select the first item.
    InitFoodList(hDlg);
    SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

     return (INT_PTR)TRUE;
```



<span data-ttu-id="e14a7-131">Quando recebe a mensagem do [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , o aplicativo exclui os bitmaps na caixa de combinação do desenho proprietário.</span><span class="sxs-lookup"><span data-stu-id="e14a7-131">When it receives the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the application deletes the bitmaps in the owner-drawn combo box.</span></span>


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a><span data-ttu-id="e14a7-132">Etapa 3: processar a mensagem do WM \_ MEASUREITEM.</span><span class="sxs-lookup"><span data-stu-id="e14a7-132">Step 3: Process the WM\_MEASUREITEM message.</span></span>

<span data-ttu-id="e14a7-133">Uma caixa de combinação desenhada pelo proprietário envia a mensagem do [**WM \_ MEASUREITEM**](wm-measureitem.md) para sua janela pai ou procedimento de caixa de diálogo para que o aplicativo possa definir as dimensões de cada item de lista.</span><span class="sxs-lookup"><span data-stu-id="e14a7-133">An owner-drawn combo box sends the [**WM\_MEASUREITEM**](wm-measureitem.md) message to its parent window or dialog box procedure so that the application can set the dimensions of each list item.</span></span> <span data-ttu-id="e14a7-134">Como a caixa de combinação de exemplo tem o estilo [**\_ OwnerDrawFixed do CBS**](combo-box-styles.md) , o sistema envia a mensagem do **WM \_ MEASUREITEM** apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="e14a7-134">Because the example combo box has the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) style, the system sends the **WM\_MEASUREITEM** message only once.</span></span> <span data-ttu-id="e14a7-135">As caixas de combinação com o estilo [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) enviam uma mensagem do **WM \_ MEASUREITEM** para cada item de lista.</span><span class="sxs-lookup"><span data-stu-id="e14a7-135">Combo boxes with the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style send a **WM\_MEASUREITEM** message for each list item.</span></span>

<span data-ttu-id="e14a7-136">O parâmetro *lParam* é um ponteiro para uma estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que identifica o controle e o item de lista.</span><span class="sxs-lookup"><span data-stu-id="e14a7-136">The *lParam* parameter is a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="e14a7-137">Ele também contém as dimensões padrão do item de lista.</span><span class="sxs-lookup"><span data-stu-id="e14a7-137">It also contains the default dimensions of the list item.</span></span> <span data-ttu-id="e14a7-138">O exemplo modifica o membro da estrutura **ItemHeight** para garantir que os itens da lista sejam altos o suficiente para acomodar os bitmaps do grupo de alimentos.</span><span class="sxs-lookup"><span data-stu-id="e14a7-138">The example modifies the **itemHeight** structure member to ensure that the list items are high enough to accommodate the food-group bitmaps.</span></span>


```C++
case WM_MEASUREITEM:
    {
    // Set the height of the items in the food groups combo box.
    LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

    if (lpmis->itemHeight < CY_BITMAP + 2)
        lpmis->itemHeight = CY_BITMAP + 2;

    break;
    }
```



### <a name="step-4-process-the-wm_drawitem-message"></a><span data-ttu-id="e14a7-139">Etapa 4: processar a mensagem do WM \_ DRAWITEM.</span><span class="sxs-lookup"><span data-stu-id="e14a7-139">Step 4: Process the WM\_DRAWITEM message.</span></span>

<span data-ttu-id="e14a7-140">Uma caixa de combinação desenhada pelo proprietário envia a mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) para sua janela pai ou procedimento de caixa de diálogo cada vez que o aplicativo deve redesenhar um item de lista.</span><span class="sxs-lookup"><span data-stu-id="e14a7-140">An owner-drawn combo box sends the [**WM\_DRAWITEM**](wm-drawitem.md) message to its parent window or dialog box procedure each time the application must repaint a list item.</span></span> <span data-ttu-id="e14a7-141">O parâmetro *lParam* é um ponteiro para uma estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que identifica o controle e o item de lista.</span><span class="sxs-lookup"><span data-stu-id="e14a7-141">The *lParam* parameter is a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="e14a7-142">Ele também contém as informações necessárias para pintar o item.</span><span class="sxs-lookup"><span data-stu-id="e14a7-142">It also contains information needed to paint the item.</span></span>

<span data-ttu-id="e14a7-143">O aplicativo de exemplo exibe o texto do item de lista e o bitmap associado ao grupo de alimentos.</span><span class="sxs-lookup"><span data-stu-id="e14a7-143">The example application displays the list-item text and the bitmap associated with the food group.</span></span> <span data-ttu-id="e14a7-144">Se o item tiver o foco, ele também desenha um retângulo de foco.</span><span class="sxs-lookup"><span data-stu-id="e14a7-144">If the item has the focus, it also draws a focus rectangle.</span></span> <span data-ttu-id="e14a7-145">Antes de exibir o texto, o exemplo define as cores de primeiro e segundo plano, com base no item selecionado.</span><span class="sxs-lookup"><span data-stu-id="e14a7-145">Before displaying the text, the example sets the foreground and background colors, based on the item selected.</span></span> <span data-ttu-id="e14a7-146">Como a caixa de combinação tem o estilo [**\_ HASSTRINGS do CBS**](combo-box-styles.md) , a caixa de combinação mantém o texto para cada item de lista que pode ser recuperado usando a mensagem [**CB \_ GETLBTEXT**](cb-getlbtext.md) .</span><span class="sxs-lookup"><span data-stu-id="e14a7-146">Because the combo box has the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the combo box maintains the text for each list item that can be retrieved using the [**CB\_GETLBTEXT**](cb-getlbtext.md) message.</span></span>

<span data-ttu-id="e14a7-147">Os bitmaps usados para o item de lista dependem do grupo de alimentos.</span><span class="sxs-lookup"><span data-stu-id="e14a7-147">The bitmaps used for the list item depend on the food group.</span></span> <span data-ttu-id="e14a7-148">`InitGroupList` usa a [**mensagem \_ SETITEMDATA CB**](cb-setitemdata.md) para associar um identificador de bitmap a cada item de lista.</span><span class="sxs-lookup"><span data-stu-id="e14a7-148">`InitGroupList` uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item.</span></span> <span data-ttu-id="e14a7-149">O procedimento de janela recupera o identificador de bitmap do membro de **dados** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="e14a7-149">The window procedure retrieves the bitmap handle from the **itemData** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="e14a7-150">O sistema usa dois bitmaps para cada símbolo de grupo de alimentos: um bitmap monocromático com a operação de varredura SRCAND para apagar a região irregular por trás da imagem e um bitmap de cor com a operação de varredura SRCPAINT para pintar a imagem.</span><span class="sxs-lookup"><span data-stu-id="e14a7-150">The system uses two bitmaps for each food group symbol: a monochrome bitmap with the SRCAND raster operation to erase the irregular region behind the image, and a color bitmap with the SRCPAINT raster operation to paint the image.</span></span>


```C++
case WM_DRAWITEM:
    {
    COLORREF clrBackground;
    COLORREF clrForeground;
    TEXTMETRIC tm;
    int x;
    int y;
    HRESULT hr;
    size_t cch;

    LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
       
    if (lpdis->itemID == -1) // Empty item)
        break;

    // Get the food icon from the item data.
    hbmIcon = (HBITMAP) lpdis->itemData;

    // The colors depend on whether the item is selected.
    clrForeground = SetTextColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

    clrBackground = SetBkColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHT : COLOR_WINDOW));

    // Calculate the vertical and horizontal position.
    GetTextMetrics(lpdis->hDC, &tm);
    y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
    x = LOWORD(GetDialogBaseUnits()) / 4;

    // Get and display the text for the list item.
    SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
        lpdis->itemID, (LPARAM) achTemp);

    hr = StringCchLength(achTemp, 256, &cch);
    if (FAILED(hr))
    {
        // TODO: Write error handler.
    }

    ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
        ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
        achTemp, (UINT)cch, NULL);

    // Restore the previous colors.
    SetTextColor(lpdis->hDC, clrForeground);
    SetBkColor(lpdis->hDC, clrBackground);
    
    //  Draw the food icon for the item. 
    HDC hdc = CreateCompatibleDC(lpdis->hDC); 
    if (hdc == NULL) 
        break; 
 
    SelectObject(hdc, hbmMask); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
    SelectObject(hdc, hbmIcon); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
    DeleteDC(hdc); 
  
    // If the item has the focus, draw the focus rectangle.
    if (lpdis->itemState & ODS_FOCUS)
        DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

    break;
    }
```



### <a name="step-5-process-the-wm_command-message"></a><span data-ttu-id="e14a7-151">Etapa 5: processar a mensagem de comando do WM \_ .</span><span class="sxs-lookup"><span data-stu-id="e14a7-151">Step 5: Process the WM\_COMMAND message.</span></span>

<span data-ttu-id="e14a7-152">Quando um evento ocorre em um controle de caixa de diálogo, o controle notifica o procedimento da caixa de diálogo por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e14a7-152">When an event occurs in a dialog box control, the control notifies the dialog box procedure by means of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="e14a7-153">O exemplo processa mensagens de notificação da caixa de combinação, da caixa de listagem e do botão **OK** .</span><span class="sxs-lookup"><span data-stu-id="e14a7-153">The example processes notification messages from the combo box, the list box, and the **OK** button.</span></span> <span data-ttu-id="e14a7-154">O identificador de controle está na palavra de ordem inferior de *wParam* e o código de notificação está na palavra de ordem superior de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="e14a7-154">The control identifier is in the low-order word of *wParam*, and the notification code is in the high-order word of *wParam*.</span></span>

<span data-ttu-id="e14a7-155">Se o identificador de controle for IDCOMBO, ocorrerá um evento na caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="e14a7-155">If the control identifier is IDCOMBO, an event has occurred in the combo box.</span></span> <span data-ttu-id="e14a7-156">Em resposta, o procedimento da caixa de diálogo ignora todos os outros eventos da caixa de combinação, exceto [**CBN \_ SELENDOK**](cbn-selendok.md), que indica que uma seleção foi feita, a caixa de listagem suspensa foi fechada e as alterações feitas devem ser aceitas.</span><span class="sxs-lookup"><span data-stu-id="e14a7-156">In response, the dialog box procedure ignores all other combo box events except [**CBN\_SELENDOK**](cbn-selendok.md), which indicates that a selection was made, the drop down list box was closed, and the changes made should be accepted.</span></span> <span data-ttu-id="e14a7-157">O procedimento da caixa de diálogo chama `InitFoodList` para redefinir o conteúdo da caixa de listagem e adicionar os nomes das seleções atuais na caixa de listagem suspensa.</span><span class="sxs-lookup"><span data-stu-id="e14a7-157">The dialog box procedure calls `InitFoodList` to reset the contents of the list box and to add the names of the current selections in the drop-down list box.</span></span>

<span data-ttu-id="e14a7-158">Se o identificador de controle for IDLIST, ocorrerá um evento na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="e14a7-158">If the control identifier is IDLIST, an event has occurred in the list box.</span></span> <span data-ttu-id="e14a7-159">Isso faz com que o procedimento da caixa de diálogo ignore todos os eventos da caixa de listagem, exceto [**lbn \_ DBLCLK**](lbn-dblclk.md), que indica que o usuário clicou duas vezes em um item de lista.</span><span class="sxs-lookup"><span data-stu-id="e14a7-159">This causes the dialog box procedure to ignore all list box events except [**LBN\_DBLCLK**](lbn-dblclk.md), which indicates that the user has double-clicked a list item.</span></span> <span data-ttu-id="e14a7-160">Esse evento é processado da mesma maneira como se um botão **OK** tivesse sido escolhido.</span><span class="sxs-lookup"><span data-stu-id="e14a7-160">This event is processed in the same way as if an **OK** button had been chosen.</span></span>

<span data-ttu-id="e14a7-161">Se o identificador de controle for IDOK, o usuário escolheu o botão **OK** .</span><span class="sxs-lookup"><span data-stu-id="e14a7-161">If the control identifier is IDOK, the user has chosen the **OK** button.</span></span> <span data-ttu-id="e14a7-162">Em resposta, o procedimento da caixa de diálogo insere o nome da comida selecionada no controle de edição de várias linhas do aplicativo e, em seguida, chama a função [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) para fechar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e14a7-162">In response, the dialog box procedure inserts the name of the selected food into the application's multi-line edit control, then calls the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function to close the dialog box.</span></span>

<span data-ttu-id="e14a7-163">Se o identificador de controle for IDCANCEL, o usuário clicou no botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="e14a7-163">If the control identifier is IDCANCEL, the user has clicked the **Cancel** button.</span></span> <span data-ttu-id="e14a7-164">Em resposta, o procedimento da caixa de diálogo chama [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) para fechar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e14a7-164">In response, the dialog box procedure calls [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) to close the dialog box.</span></span>


```C++
case WM_COMMAND:
        switch (LOWORD(wParam)) 
        { 
            case IDCOMBO: 
                if (HIWORD(wParam) == CBN_SELENDOK) 
                { 
                    InitFoodList(hDlg); 
                    SendDlgItemMessage(hDlg, IDLIST, 
                        LB_SETCURSEL, 0, 0); 
                } 
                break; 
 
            case IDLIST: 
                if (HIWORD(wParam) != LBN_DBLCLK) 
                    break; 
 
            // For a double-click, process the OK case. 
            case IDOK: 
 
                // Get the text for the selected list item. 
                hwnd = GetDlgItem(hDlg, IDLIST); 

                // Here it is assumed the text can fit into achTemp.
                // If there is doubt, call LB_GETTEXTLENGTH first.
                SendMessage(hwnd, LB_GETTEXT, 
                    SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                    (LPARAM) achTemp); 
 
                // TODO: Do something with the selected text.
 
                EndDialog(hDlg, 0); 
                break; 
 
            case IDCANCEL: 
                hwnd = GetDlgItem(hDlg, IDCOMBO); 
                if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                    SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                else EndDialog(hDlg, 0); 
        } 
        break; 
```



## <a name="complete-example"></a><span data-ttu-id="e14a7-165">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="e14a7-165">Complete example</span></span>

<span data-ttu-id="e14a7-166">A seguir está o procedimento da caixa de diálogo e as funções de suporte para a caixa de diálogo **refeição quadrada** .</span><span class="sxs-lookup"><span data-stu-id="e14a7-166">Following is the dialog box procedure and the supporting functions for the **Square Meal** dialog box.</span></span>


```C++
#define ID_BREAD 0
#define ID_DAIRY 1
#define ID_FRUIT 2
#define ID_MEAT  3

#define CX_BITMAP 24
#define CY_BITMAP 24

HBITMAP hbmBread;
HBITMAP hbmDairy;
HBITMAP hbmMeat;
HBITMAP hbmFruit;
HBITMAP hbmMask;

HBITMAP hbmIcon;
```

```C++
// Message handler for Square Meal dialog box.
INT_PTR CALLBACK FoodDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam)
{
    UNREFERENCED_PARAMETER(lParam);
    TCHAR achTemp[256];
    HWND hwnd;

    switch (message)
    {
    case WM_INITDIALOG:

        // Call an application-defined function to load bitmap resources.
        if (!LoadIconBitmaps())
        {
            EndDialog(hDlg, -1);
            break;
        }

        // Initialize the food groups combo box and select the first item.
        InitGroupList(hDlg);
        SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

        // Initialize the food list box and select the first item.
        InitFoodList(hDlg);
        SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

         return (INT_PTR)TRUE;
   
    case WM_MEASUREITEM:
        {
        // Set the height of the items in the food groups combo box.
        LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

        if (lpmis->itemHeight < CY_BITMAP + 2)
            lpmis->itemHeight = CY_BITMAP + 2;

        break;
        }

    case WM_DRAWITEM:
        {
        COLORREF clrBackground;
        COLORREF clrForeground;
        TEXTMETRIC tm;
        int x;
        int y;
        HRESULT hr;
        size_t cch;

        LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
           
        if (lpdis->itemID == -1) // Empty item)
            break;

        // Get the food icon from the item data.
        hbmIcon = (HBITMAP) lpdis->itemData;

        // The colors depend on whether the item is selected.
        clrForeground = SetTextColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

        clrBackground = SetBkColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHT : COLOR_WINDOW));

        // Calculate the vertical and horizontal position.
        GetTextMetrics(lpdis->hDC, &tm);
        y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
        x = LOWORD(GetDialogBaseUnits()) / 4;

        // Get and display the text for the list item.
        SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
            lpdis->itemID, (LPARAM) achTemp);

        hr = StringCchLength(achTemp, 256, &cch);
        if (FAILED(hr))
        {
            // TODO: Write error handler.
        }

        ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
            ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
            achTemp, (UINT)cch, NULL);

        // Restore the previous colors.
        SetTextColor(lpdis->hDC, clrForeground);
        SetBkColor(lpdis->hDC, clrBackground);
        
        //  Draw the food icon for the item. 
        HDC hdc = CreateCompatibleDC(lpdis->hDC); 
        if (hdc == NULL) 
            break; 
 
        SelectObject(hdc, hbmMask); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
        SelectObject(hdc, hbmIcon); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
        DeleteDC(hdc); 
      
        // If the item has the focus, draw the focus rectangle.
        if (lpdis->itemState & ODS_FOCUS)
            DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

        break;
        }

    case WM_COMMAND:
            switch (LOWORD(wParam)) 
            { 
                case IDCOMBO: 
                    if (HIWORD(wParam) == CBN_SELENDOK) 
                    { 
                        InitFoodList(hDlg); 
                        SendDlgItemMessage(hDlg, IDLIST, 
                            LB_SETCURSEL, 0, 0); 
                    } 
                    break; 
 
                case IDLIST: 
                    if (HIWORD(wParam) != LBN_DBLCLK) 
                        break; 
 
                // For a double-click, process the OK case. 
                case IDOK: 
 
                    // Get the text for the selected list item. 
                    hwnd = GetDlgItem(hDlg, IDLIST); 

                    // Here it is assumed the text can fit into achTemp.
                    // If there is doubt, call LB_GETTEXTLENGTH first.
                    SendMessage(hwnd, LB_GETTEXT, 
                        SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                        (LPARAM) achTemp); 
 
                    // TODO: Do something with the selected text.
 
                    EndDialog(hDlg, 0); 
                    break; 
 
                case IDCANCEL: 
                    hwnd = GetDlgItem(hDlg, IDCOMBO); 
                    if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                        SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                    else EndDialog(hDlg, 0); 
            } 
            break; 

    case WM_DESTROY:

        // Call the application-defined function to free the bitmap resources.
        DeleteIconBitmaps();
        break;
    }
    return (INT_PTR)FALSE;
}

// Loads string resources and adds them as items to the drop-down list of
//   the food groups combo box. The bitmap handle of each item&#39;s icon is
//   stored as item data for easy access when the item needs to be drawn.
// 
void InitGroupList(HWND hDlg)
{
    TCHAR achTemp[256];
    DWORD dwIndex;

    // Get the handle of the food groups combo box.
    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);

    LoadString(hInst, IDS_BREAD, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmBread);
    
    LoadString(hInst, IDS_DAIRY, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmDairy);

    LoadString(hInst, IDS_FRUIT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmFruit); 

    LoadString(hInst, IDS_MEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmMeat);

    return;
}

// Fills the food list based on the selected item in the food groups
//   combo box.
void InitFoodList(HWND hDlg)
{
    TCHAR achTemp[256];

    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);
    HWND hwndFoodList = GetDlgItem(hDlg, IDLIST);

    // Clear the list contents.
    SendMessage(hwndFoodList, LB_RESETCONTENT, 0, 0);

    // Find out which food group is selected.
    int idFoodGroup = SendMessage(hwndGroupsBox, CB_GETCURSEL, 0, 0);

    switch (idFoodGroup)
    {
    case ID_BREAD:
        LoadString(hInst, IDS_OAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_WHEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_RYE, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        break;

    case ID_DAIRY:
        LoadString(hInst, IDS_CHEDDAR, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_MILK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PROCESSED, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_SWISS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        
        break;

    case ID_FRUIT:
        LoadString(hInst, IDS_APPLES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_BANANAS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_ORANGES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    case ID_MEAT:
        LoadString(hInst, IDS_BEEF, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_CHICKEN, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PORK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    default:
        break;
    }

    return;
}

// Loads the food icon bitmaps from the application resources.
//
BOOL LoadIconBitmaps(void)
{
    hbmBread = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_BREAD));

    if (hbmBread != NULL)
         hbmDairy = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_DAIRY));

    if (hbmDairy != NULL)
         hbmMeat = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MEAT));

    if (hbmMeat != NULL)
        hbmFruit = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_FRUIT));
    
    if (hbmFruit != NULL)
        hbmMask = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MASK));

    if (hbmMask != NULL)
        return TRUE;
        
    return FALSE;
}

// Frees the icon bitmps.
//
void DeleteIconBitmaps(void)
{
    FreeResource(reinterpret_cast<HGLOBAL>(hbmBread));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmDairy));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMeat));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmFruit));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMask));
}
```


## <a name="related-topics"></a><span data-ttu-id="e14a7-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e14a7-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e14a7-168">Usando caixas de combinação</span><span class="sxs-lookup"><span data-stu-id="e14a7-168">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> </dl>

 

 