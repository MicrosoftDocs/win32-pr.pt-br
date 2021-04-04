---
title: Como preparar itens e imagens do ComboBoxEx
description: Este tópico demonstra como adicionar itens a um controle ComboBoxEx.
ms.assetid: 2603DFBE-9E7A-4B2F-BE33-418997D323B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7474b46e5227d91b1cc2b51462a43a0fb75d8b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824000"
---
# <a name="how-to-prepare-comboboxex-items-and-images"></a><span data-ttu-id="9cf09-103">Como preparar itens e imagens do ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="9cf09-103">How to Prepare ComboBoxEx Items and Images</span></span>

<span data-ttu-id="9cf09-104">Este tópico demonstra como adicionar itens a um controle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="9cf09-104">This topic demonstrates how to add items to a ComboBoxEx control.</span></span>

<span data-ttu-id="9cf09-105">Para adicionar um item a um controle ComboBoxEx, primeiro defina uma estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) .</span><span class="sxs-lookup"><span data-stu-id="9cf09-105">To add an item to a ComboBoxEx control, first define a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span> <span data-ttu-id="9cf09-106">Em seguida, defina o membro **Mask** da estrutura para indicar quais membros você deseja que o controle use.</span><span class="sxs-lookup"><span data-stu-id="9cf09-106">Then, set the **mask** member of the structure to indicate which members you want the control to use.</span></span> <span data-ttu-id="9cf09-107">Por fim, defina os membros especificados da estrutura para os valores desejados e envie a mensagem [**CBEM \_ INSERTITEM**](cbem-insertitem.md) para adicionar o item ao controle.</span><span class="sxs-lookup"><span data-stu-id="9cf09-107">Finally, set the specified members of the structure to the desired values and send the [**CBEM\_INSERTITEM**](cbem-insertitem.md) message to add the item to the control.</span></span>

<span data-ttu-id="9cf09-108">A função definida pelo aplicativo a seguir adiciona 15 itens a um controle ComboBoxEx existente.</span><span class="sxs-lookup"><span data-stu-id="9cf09-108">The following application-defined function adds 15 items to an existing ComboBoxEx control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9cf09-109">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="9cf09-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9cf09-110">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="9cf09-110">Technologies</span></span>

-   [<span data-ttu-id="9cf09-111">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="9cf09-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9cf09-112">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9cf09-112">Prerequisites</span></span>

-   <span data-ttu-id="9cf09-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="9cf09-113">C/C++</span></span>
-   <span data-ttu-id="9cf09-114">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="9cf09-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9cf09-115">Instruções</span><span class="sxs-lookup"><span data-stu-id="9cf09-115">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="9cf09-116">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="9cf09-116">Step 1:</span></span>

<span data-ttu-id="9cf09-117">Para adicionar um item a um controle ComboBoxEx, primeiro defina uma estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) .</span><span class="sxs-lookup"><span data-stu-id="9cf09-117">To add an item to a ComboBoxEx control, first define a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span>


```C++
COMBOBOXEXITEM cbei;
int iCnt;


typedef struct {
    int iImage;
    int iSelectedImage;
    int iIndent;
    LPTSTR pszText;
} ITEMINFO, *PITEMINFO;

ITEMINFO IInf[ ] = {
    { 0, 3,  0, L"first"}, 
    { 1, 4,  1, L"second"},
    { 2, 5,  2, L"third"},
    { 0, 3,  0, L"fourth"},
    { 1, 4,  1, L"fifth"},
    { 2, 5,  2, L"sixth"},
    { 0, 3,  0, L"seventh"},
    { 1, 4,  1, L"eighth"},
    { 2, 5,  2, L"ninth"},
    { 0, 3,  0, L"tenth"},
    { 1, 4,  1, L"eleventh"},
    { 2, 5,  2, L"twelfth"},
    { 0, 3,  0, L"thirteenth"},
    { 1, 4,  1, L"fourteenth"},
    { 2, 5,  2, L"fifteenth"}
};
```



### <a name="step-2"></a><span data-ttu-id="9cf09-118">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="9cf09-118">Step 2:</span></span>

<span data-ttu-id="9cf09-119">Defina o membro **Mask** da estrutura para indicar quais membros você deseja que o controle use.</span><span class="sxs-lookup"><span data-stu-id="9cf09-119">Set the **mask** member of the structure to indicate which members you want the control to use.</span></span> <span data-ttu-id="9cf09-120">Observe que o membro **Mask** da estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) inclui valores de sinalizador que dizem ao controle para exibir imagens para cada item.</span><span class="sxs-lookup"><span data-stu-id="9cf09-120">Note that the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure includes flag values that tell the control to display images for each item.</span></span>


```C++
// Set the mask common to all items.
cbei.mask = CBEIF_TEXT | CBEIF_INDENT |
            CBEIF_IMAGE| CBEIF_SELECTEDIMAGE;
```



### <a name="step-3"></a><span data-ttu-id="9cf09-121">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="9cf09-121">Step 3:</span></span>

<span data-ttu-id="9cf09-122">Defina os membros especificados da estrutura com os valores desejados e, em seguida, envie a mensagem [**CBEM \_ INSERTITEM**](cbem-insertitem.md) para adicionar o item ao controle.</span><span class="sxs-lookup"><span data-stu-id="9cf09-122">Set the specified members of the structure to the values you want, and then send the [**CBEM\_INSERTITEM**](cbem-insertitem.md) message to add the item to the control.</span></span>


```C++
for(iCnt=0;iCnt<MAX_ITEMS;iCnt++){
    // Initialize the COMBOBOXEXITEM struct.
    cbei.iItem          = iCnt;
    cbei.pszText        = IInf[iCnt].pszText;
    cbei.cchTextMax     = sizeof(IInf[iCnt].pszText);
    cbei.iImage         = IInf[iCnt].iImage;
    cbei.iSelectedImage = IInf[iCnt].iSelectedImage;
    cbei.iIndent        = IInf[iCnt].iIndent;

    
    // Tell the ComboBoxEx to add the item. Return FALSE if 
    // this fails.
    if(SendMessage(hwndCB,CBEM_INSERTITEM,0,(LPARAM)&cbei) == -1)
        return FALSE;
```



### <a name="step-4"></a><span data-ttu-id="9cf09-123">Etapa 4:</span><span class="sxs-lookup"><span data-stu-id="9cf09-123">Step 4:</span></span>

<span data-ttu-id="9cf09-124">Atribua a lista de imagens existente ao controle ComboBoxEx e defina o tamanho do controle.</span><span class="sxs-lookup"><span data-stu-id="9cf09-124">Assign the existing image list to the ComboBoxEx control and set the size of control.</span></span>


```C++
// Assign the existing image list to the ComboBoxEx control 
// and return TRUE. 
// g_himl is the handle to the existing image list
SendMessage(hwndCB,CBEM_SETIMAGELIST,0,(LPARAM)g_himl);

// Set size of control to make sure it's displayed correctly now
// that the image list is set.
SetWindowPos(hwndCB,NULL,20,20,250,120,SWP_NOACTIVATE);

return TRUE; 
```



## <a name="complete-example"></a><span data-ttu-id="9cf09-125">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="9cf09-125">Complete example</span></span>


```C++
// AddItems - Uses the CBEM_INSERTITEM message to add items to an
// existing ComboBoxEx control.

BOOL WINAPI AddItems(HWND hwndCB)
{
    
    //  Declare and init locals.
    COMBOBOXEXITEM cbei;
    int iCnt;
    

    typedef struct {
        int iImage;
        int iSelectedImage;
        int iIndent;
        LPTSTR pszText;
    } ITEMINFO, *PITEMINFO;

    ITEMINFO IInf[ ] = {
        { 0, 3,  0, L"first"}, 
        { 1, 4,  1, L"second"},
        { 2, 5,  2, L"third"},
        { 0, 3,  0, L"fourth"},
        { 1, 4,  1, L"fifth"},
        { 2, 5,  2, L"sixth"},
        { 0, 3,  0, L"seventh"},
        { 1, 4,  1, L"eighth"},
        { 2, 5,  2, L"ninth"},
        { 0, 3,  0, L"tenth"},
        { 1, 4,  1, L"eleventh"},
        { 2, 5,  2, L"twelfth"},
        { 0, 3,  0, L"thirteenth"},
        { 1, 4,  1, L"fourteenth"},
        { 2, 5,  2, L"fifteenth"}
    };

    // Set the mask common to all items.
    cbei.mask = CBEIF_TEXT | CBEIF_INDENT |
                CBEIF_IMAGE| CBEIF_SELECTEDIMAGE;

    for(iCnt=0;iCnt<MAX_ITEMS;iCnt++){
        // Initialize the COMBOBOXEXITEM struct.
        cbei.iItem          = iCnt;
        cbei.pszText        = IInf[iCnt].pszText;
        cbei.cchTextMax     = sizeof(IInf[iCnt].pszText);
        cbei.iImage         = IInf[iCnt].iImage;
        cbei.iSelectedImage = IInf[iCnt].iSelectedImage;
        cbei.iIndent        = IInf[iCnt].iIndent;
    
        
        // Tell the ComboBoxEx to add the item. Return FALSE if 
        // this fails.
        if(SendMessage(hwndCB,CBEM_INSERTITEM,0,(LPARAM)&cbei) == -1)
            return FALSE;
    }
    // Assign the existing image list to the ComboBoxEx control 
    // and return TRUE. 
    // g_himl is the handle to the existing image list
    SendMessage(hwndCB,CBEM_SETIMAGELIST,0,(LPARAM)g_himl);

    // Set size of control to make sure it's displayed correctly now
    // that the image list is set.
    SetWindowPos(hwndCB,NULL,20,20,250,120,SWP_NOACTIVATE);

    return TRUE; 
}
```



## <a name="related-topics"></a><span data-ttu-id="9cf09-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9cf09-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cf09-127">Sobre controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="9cf09-127">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="9cf09-128">Referência de controle ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="9cf09-128">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="9cf09-129">Usando controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="9cf09-129">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="9cf09-130">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="9cf09-130">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 