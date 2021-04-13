---
title: Mensagem de TB_SETPRESSEDIMAGELIST (commctrl. h)
description: Define a lista de imagens que a barra de ferramentas usa para exibir botões que estão em um estado pressionado.
ms.assetid: d0e061ec-3a89-4c2d-b7f7-5f2061098428
keywords:
- Controles de TB_SETPRESSEDIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a3c6dafed6dbfdf2a654f4f95f1cef636ba762
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499862"
---
# <a name="tb_setpressedimagelist-message"></a><span data-ttu-id="1cdb2-104">TB de \_ mensagem SETPRESSEDIMAGELIST</span><span class="sxs-lookup"><span data-stu-id="1cdb2-104">TB\_SETPRESSEDIMAGELIST message</span></span>

<span data-ttu-id="1cdb2-105">Define a lista de imagens que a barra de ferramentas usa para exibir botões que estão em um estado pressionado.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-105">Sets the image list that the toolbar uses to display buttons that are in a pressed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="1cdb2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cdb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cdb2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1cdb2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cdb2-108">O índice da lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-108">The index of the image list.</span></span> <span data-ttu-id="1cdb2-109">Se você usar apenas uma lista de imagens, defina esse parâmetro como zero.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-109">If you use only one image list, set this parameter to zero.</span></span> <span data-ttu-id="1cdb2-110">Consulte comentários para obter detalhes sobre como usar várias listas de imagens.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-110">See Remarks for details on using multiple image lists.</span></span>

</dd> <dt>

<span data-ttu-id="1cdb2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1cdb2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cdb2-112">Identificador para a lista de imagens a ser definida.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-112">Handle to the image list to set.</span></span> <span data-ttu-id="1cdb2-113">Se esse parâmetro for **nulo**, nenhuma imagem será exibida nos botões.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-113">If this parameter is **NULL**, no images are displayed in the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cdb2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1cdb2-114">Return value</span></span>

<span data-ttu-id="1cdb2-115">Retorna o identificador para a lista de imagens usada anteriormente para exibir botões no estado pressionado, ou **NULL** se nenhuma lista de imagens desse tipo foi definida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-115">Returns the handle to the image list previously used to display buttons in their pressed state, or **NULL** if no such image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cdb2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cdb2-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1cdb2-117">Seu aplicativo é responsável por liberar a lista de imagens depois que a barra de ferramentas é destruída.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-117">Your application is responsible for freeing the image list after the toolbar is destroyed.</span></span>

 

<span data-ttu-id="1cdb2-118">Não é possível combinar a mensagem **TB \_ SETPRESSEDIMAGELIST** com [**TB \_ AddBitmap**](tb-addbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="1cdb2-118">The **TB\_SETPRESSEDIMAGELIST** message cannot be combined with [**TB\_ADDBITMAP**](tb-addbitmap.md).</span></span> <span data-ttu-id="1cdb2-119">Ele também não pode ser usado com barras de ferramentas criadas com [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), que chama **TB \_ AddBitmap** internamente.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-119">It also cannot be used with toolbars created with [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), which calls **TB\_ADDBITMAP** internally.</span></span> <span data-ttu-id="1cdb2-120">Quando você cria uma barra de ferramentas com **CreateToolbarEx** ou usa **TB \_ AddBitmap** para adicionar imagens, a barra de ferramentas gerencia a lista de imagens internamente.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-120">When you create a toolbar with **CreateToolbarEx** or use **TB\_ADDBITMAP** to add images, the toolbar manages the image list internally.</span></span> <span data-ttu-id="1cdb2-121">Tentar modificá-lo com **TB \_ SETPRESSEDIMAGELIST** tem consequências imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-121">Attempting to modify it with **TB\_SETPRESSEDIMAGELIST** has unpredictable consequences.</span></span>

<span data-ttu-id="1cdb2-122">As imagens de botão não precisam vir da mesma lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-122">Button images need not come from the same image list.</span></span> <span data-ttu-id="1cdb2-123">Para usar várias listas de imagens para suas imagens de botão da barra de ferramentas:</span><span class="sxs-lookup"><span data-stu-id="1cdb2-123">To use multiple image lists for your toolbar button images:</span></span>

1.  <span data-ttu-id="1cdb2-124">Habilite várias listas de imagens enviando a barra de ferramentas controle uma mensagem [**CCM \_ SetVersion**](ccm-setversion.md) com *wParam* (o número de versão) definido como 5.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-124">Enable multiple image lists by sending the toolbar control a [**CCM\_SETVERSION**](ccm-setversion.md) message with *wParam* (the version number) set to 5.</span></span>
2.  <span data-ttu-id="1cdb2-125">Para cada lista de imagens que você deseja usar, envie a barra de ferramentas para o controle de uma mensagem **\_ SETPRESSEDIMAGELIST TB** .</span><span class="sxs-lookup"><span data-stu-id="1cdb2-125">For each image list you want to use, send the toolbar control a **TB\_SETPRESSEDIMAGELIST** message.</span></span> <span data-ttu-id="1cdb2-126">Defina *wParam* como um valor *wParam* definido pelo aplicativo que será usado para identificar a lista.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-126">Set *wParam* to an application-defined *wParam* value that will be used to identify the list.</span></span> <span data-ttu-id="1cdb2-127">Defina *lParam* como o identificador HIMAGELIST da lista.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-127">Set *lParam* to the list's HIMAGELIST handle.</span></span>
3.  <span data-ttu-id="1cdb2-128">Para cada botão, defina o membro **iBitmap** da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) do botão como MAKELONG (*iIndex*, *iImageID*).</span><span class="sxs-lookup"><span data-stu-id="1cdb2-128">For each button, set the **iBitmap** member of the button's [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure to MAKELONG(*iIndex*, *iImageID*).</span></span> <span data-ttu-id="1cdb2-129">O valor de *iImageID* é a ID da lista de imagens apropriada que foi definida na etapa dois.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-129">The *iImageID* value is the ID of the appropriate image list that was defined in step two.</span></span> <span data-ttu-id="1cdb2-130">O valor de *iIndex* é o índice da imagem específica dentro dessa lista.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-130">The *iIndex* value is the index of the particular image within that list.</span></span>
4.  <span data-ttu-id="1cdb2-131">Adicione os botões enviando a barra de ferramentas o controle uma mensagem de [**\_ rebotão de TB**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="1cdb2-131">Add the buttons by sending the toolbar control a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>

<span data-ttu-id="1cdb2-132">O fragmento de código a seguir ilustra como adicionar cinco botões a uma barra de ferramentas, com imagens de três listas de imagens diferentes.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-132">The following code fragment illustrates how to add five buttons to a toolbar, with images from three different image lists.</span></span> <span data-ttu-id="1cdb2-133">O suporte para várias listas de imagens é habilitado com uma mensagem [**CCM \_ SetVersion**](ccm-setversion.md) .</span><span class="sxs-lookup"><span data-stu-id="1cdb2-133">Support for multiple image lists is enabled with a [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="1cdb2-134">As listas de imagens são, então, definidas e atribuídas IDs de 0-2.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-134">The image lists are then set and assigned IDs of 0-2.</span></span> <span data-ttu-id="1cdb2-135">Os botões recebem imagens das listas de imagens da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1cdb2-135">The buttons are assigned images from the image lists as follows:</span></span>

-   <span data-ttu-id="1cdb2-136">O botão 0 é da lista de imagens zero (ahim \[ 0 \] ) com o índice de 1.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-136">Button 0 is from image list zero (ahim\[0\]) with index of 1.</span></span>
-   <span data-ttu-id="1cdb2-137">O botão 1 é da lista de imagens um (ahim \[ 1 \] ) com um índice de 1.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-137">Button 1 is from image list one (ahim\[1\]) with an index of 1.</span></span>
-   <span data-ttu-id="1cdb2-138">O botão 2 é da lista de imagens dois (ahim \[ 2 \] ) com um índice de 1.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-138">Button 2 is from image list two (ahim\[2\]) with an index of 1.</span></span>
-   <span data-ttu-id="1cdb2-139">O botão 3 é da lista de imagens zero (ahim \[ 0 \] ) com um índice de 2.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-139">Button 3 is from image list zero (ahim\[0\]) with an index of 2.</span></span>
-   <span data-ttu-id="1cdb2-140">O botão 4 é da lista de imagens um (ahim \[ 1 \] ) com um índice de 3.</span><span class="sxs-lookup"><span data-stu-id="1cdb2-140">Button 4 is from image list one (ahim\[1\]) with an index of 3.</span></span>

<span data-ttu-id="1cdb2-141">Por fim, os botões são adicionados ao controle barra de ferramentas com uma mensagem de [**\_ hiperbotãos de TB**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="1cdb2-141">Finally, the buttons are added to the toolbar control with a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>


```
// Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a><span data-ttu-id="1cdb2-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cdb2-142">Requirements</span></span>



| <span data-ttu-id="1cdb2-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cdb2-143">Requirement</span></span> | <span data-ttu-id="1cdb2-144">Valor</span><span class="sxs-lookup"><span data-stu-id="1cdb2-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cdb2-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cdb2-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1cdb2-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1cdb2-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1cdb2-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cdb2-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1cdb2-148">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1cdb2-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1cdb2-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1cdb2-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cdb2-150"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cdb2-150"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cdb2-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cdb2-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="1cdb2-152">**Referência**</span><span class="sxs-lookup"><span data-stu-id="1cdb2-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1cdb2-153">**TB de \_ GETPRESSEDIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="1cdb2-153">**TB\_GETPRESSEDIMAGELIST**</span></span>](tb-getpressedimagelist.md)
</dt> <dt>

<span data-ttu-id="1cdb2-154">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="1cdb2-154">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="1cdb2-155">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1cdb2-155">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span></span>
</dt> </dl>

 

