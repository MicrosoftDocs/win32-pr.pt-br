---
title: Mensagem de TB_SETIMAGELIST (commctrl. h)
description: Define a lista de imagens que a barra de ferramentas usa para exibir botões que estão em seu estado padrão.
ms.assetid: 432ffdfc-bb63-4405-90da-9392910fdbb6
keywords:
- Controles de TB_SETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0b7ad631e8b56824ae65a2b262c5478611e75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769028"
---
# <a name="tb_setimagelist-message"></a><span data-ttu-id="5684a-104">Mensagem de TB \_ SETimagelist</span><span class="sxs-lookup"><span data-stu-id="5684a-104">TB\_SETIMAGELIST message</span></span>

<span data-ttu-id="5684a-105">Define a lista de imagens que a barra de ferramentas usa para exibir botões que estão em seu estado padrão.</span><span class="sxs-lookup"><span data-stu-id="5684a-105">Sets the image list that the toolbar uses to display buttons that are in their default state.</span></span>

## <a name="parameters"></a><span data-ttu-id="5684a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5684a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5684a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5684a-107">*wParam*</span></span> 
</dt> <dd>

[<span data-ttu-id="5684a-108">Versão 5,80.</span><span class="sxs-lookup"><span data-stu-id="5684a-108">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="5684a-109">O índice da lista.</span><span class="sxs-lookup"><span data-stu-id="5684a-109">The index of the list.</span></span> <span data-ttu-id="5684a-110">Se você usar apenas uma lista de imagens ou uma versão anterior dos controles comuns, defina *wParam* como zero.</span><span class="sxs-lookup"><span data-stu-id="5684a-110">If you use only one image list, or an earlier version of the common controls, set *wParam* to zero.</span></span> <span data-ttu-id="5684a-111">Consulte comentários para obter detalhes sobre como usar várias listas de imagens.</span><span class="sxs-lookup"><span data-stu-id="5684a-111">See Remarks for details on using multiple image lists.</span></span>

</dd> <dt>

<span data-ttu-id="5684a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5684a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5684a-113">Identificador para a lista de imagens a ser definida.</span><span class="sxs-lookup"><span data-stu-id="5684a-113">Handle to the image list to set.</span></span> <span data-ttu-id="5684a-114">Se esse parâmetro for **nulo**, nenhuma imagem será exibida nos botões.</span><span class="sxs-lookup"><span data-stu-id="5684a-114">If this parameter is **NULL**, no images are displayed in the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5684a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5684a-115">Return value</span></span>

<span data-ttu-id="5684a-116">Retorna o identificador para a lista de imagens usada anteriormente para exibir botões em seu estado padrão, ou **NULL** se nenhuma lista de imagens tiver sido definida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5684a-116">Returns the handle to the image list previously used to display buttons in their default state, or **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="5684a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5684a-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5684a-118">Seu aplicativo é responsável por liberar a lista de imagens depois que a barra de ferramentas é destruída.</span><span class="sxs-lookup"><span data-stu-id="5684a-118">Your application is responsible for freeing the image list after the toolbar is destroyed.</span></span>

 

<span data-ttu-id="5684a-119">A mensagem de **TB \_ SetImageList** não pode ser combinada com [**TB \_ AddBitmap**](tb-addbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="5684a-119">The **TB\_SETIMAGELIST** message cannot be combined with [**TB\_ADDBITMAP**](tb-addbitmap.md).</span></span> <span data-ttu-id="5684a-120">Ele também não pode ser usado com barras de ferramentas criadas com [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), que chama **TB \_ AddBitmap** internamente.</span><span class="sxs-lookup"><span data-stu-id="5684a-120">It also cannot be used with toolbars created with [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), which calls **TB\_ADDBITMAP** internally.</span></span> <span data-ttu-id="5684a-121">Quando você cria uma barra de ferramentas com **CreateToolbarEx** ou usa **TB \_ AddBitmap** para adicionar imagens, a barra de ferramentas gerencia a lista de imagens internamente.</span><span class="sxs-lookup"><span data-stu-id="5684a-121">When you create a toolbar with **CreateToolbarEx** or use **TB\_ADDBITMAP** to add images, the toolbar manages the image list internally.</span></span> <span data-ttu-id="5684a-122">A tentativa de modificá-lo com **TB \_ SetImageList** tem consequências imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="5684a-122">Attempting to modify it with **TB\_SETIMAGELIST** has unpredictable consequences.</span></span>

<span data-ttu-id="5684a-123">Com a [versão 5,80](common-control-versions.md) ou posterior dos controles comuns, as imagens de botão não precisam vir da mesma lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="5684a-123">With [version 5.80](common-control-versions.md) or later of the common controls, button images need not come from the same image list.</span></span> <span data-ttu-id="5684a-124">Para usar várias listas de imagens para suas imagens de botão da barra de ferramentas:</span><span class="sxs-lookup"><span data-stu-id="5684a-124">To use multiple image lists for your toolbar button images:</span></span>

1.  <span data-ttu-id="5684a-125">Habilite várias listas de imagens enviando a barra de ferramentas controle uma mensagem [**CCM \_ SetVersion**](ccm-setversion.md) com *wParam* (o número de versão) definido como 5.</span><span class="sxs-lookup"><span data-stu-id="5684a-125">Enable multiple image lists by sending the toolbar control a [**CCM\_SETVERSION**](ccm-setversion.md) message with *wParam* (the version number) set to 5.</span></span>
2.  <span data-ttu-id="5684a-126">Para cada lista de imagens que você deseja usar, envie a barra de ferramentas para o controle de uma mensagem de **TB \_ SetImageList** .</span><span class="sxs-lookup"><span data-stu-id="5684a-126">For each image list you want to use, send the toolbar control a **TB\_SETIMAGELIST** message.</span></span> <span data-ttu-id="5684a-127">Defina *wParam* como um valor *wParam* definido pelo aplicativo que será usado para identificar a lista.</span><span class="sxs-lookup"><span data-stu-id="5684a-127">Set *wParam* to an application-defined *wParam* value that will be used to identify the list.</span></span> <span data-ttu-id="5684a-128">Defina *lParam* como o identificador HIMAGELIST da lista.</span><span class="sxs-lookup"><span data-stu-id="5684a-128">Set *lParam* to the list's HIMAGELIST handle.</span></span>
3.  <span data-ttu-id="5684a-129">Para cada botão, defina o membro **iBitmap** da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) do botão como MAKELONG (*iIndex*, *iImageID*).</span><span class="sxs-lookup"><span data-stu-id="5684a-129">For each button, set the **iBitmap** member of the button's [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure to MAKELONG(*iIndex*, *iImageID*).</span></span> <span data-ttu-id="5684a-130">O valor de *iImageID* é a ID da lista de imagens apropriada que foi definida na etapa dois.</span><span class="sxs-lookup"><span data-stu-id="5684a-130">The *iImageID* value is the ID of the appropriate image list that was defined in step two.</span></span> <span data-ttu-id="5684a-131">O valor de *iIndex* é o índice da imagem específica dentro dessa lista.</span><span class="sxs-lookup"><span data-stu-id="5684a-131">The *iIndex* value is the index of the particular image within that list.</span></span>
4.  <span data-ttu-id="5684a-132">Adicione os botões enviando a barra de ferramentas o controle uma mensagem de [**\_ rebotão de TB**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="5684a-132">Add the buttons by sending the toolbar control a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>

<span data-ttu-id="5684a-133">O fragmento de código a seguir ilustra como adicionar cinco botões a uma barra de ferramentas, com imagens de três listas de imagens diferentes.</span><span class="sxs-lookup"><span data-stu-id="5684a-133">The following code fragment illustrates how to add five buttons to a toolbar, with images from three different image lists.</span></span> <span data-ttu-id="5684a-134">O suporte para várias listas de imagens é habilitado com uma mensagem [**CCM \_ SetVersion**](ccm-setversion.md) .</span><span class="sxs-lookup"><span data-stu-id="5684a-134">Support for multiple image lists is enabled with a [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="5684a-135">As listas de imagens são, então, definidas e atribuídas IDs de 0-2.</span><span class="sxs-lookup"><span data-stu-id="5684a-135">The image lists are then set and assigned IDs of 0-2.</span></span> <span data-ttu-id="5684a-136">Os botões recebem imagens das listas de imagens da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5684a-136">The buttons are assigned images from the image lists as follows:</span></span>

-   <span data-ttu-id="5684a-137">O botão 0 é da lista de imagens zero (ahim \[ 0 \] ) com o índice de 1.</span><span class="sxs-lookup"><span data-stu-id="5684a-137">Button 0 is from image list zero (ahim\[0\]) with index of 1.</span></span>
-   <span data-ttu-id="5684a-138">O botão 1 é da lista de imagens um (ahim \[ 1 \] ) com um índice de 1.</span><span class="sxs-lookup"><span data-stu-id="5684a-138">Button 1 is from image list one (ahim\[1\]) with an index of 1.</span></span>
-   <span data-ttu-id="5684a-139">O botão 2 é da lista de imagens dois (ahim \[ 2 \] ) com um índice de 1.</span><span class="sxs-lookup"><span data-stu-id="5684a-139">Button 2 is from image list two (ahim\[2\]) with an index of 1.</span></span>
-   <span data-ttu-id="5684a-140">O botão 3 é da lista de imagens zero (ahim \[ 0 \] ) com um índice de 2.</span><span class="sxs-lookup"><span data-stu-id="5684a-140">Button 3 is from image list zero (ahim\[0\]) with an index of 2.</span></span>
-   <span data-ttu-id="5684a-141">O botão 4 é da lista de imagens um (ahim \[ 1 \] ) com um índice de 3.</span><span class="sxs-lookup"><span data-stu-id="5684a-141">Button 4 is from image list one (ahim\[1\]) with an index of 3.</span></span>

<span data-ttu-id="5684a-142">Por fim, os botões são adicionados ao controle barra de ferramentas com uma mensagem de [**\_ hiperbotãos de TB**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="5684a-142">Finally, the buttons are added to the toolbar control with a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>


```
//Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 2, (LPARAM)ahiml[2]);

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



## <a name="requirements"></a><span data-ttu-id="5684a-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5684a-143">Requirements</span></span>



| <span data-ttu-id="5684a-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="5684a-144">Requirement</span></span> | <span data-ttu-id="5684a-145">Valor</span><span class="sxs-lookup"><span data-stu-id="5684a-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5684a-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5684a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5684a-147">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5684a-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5684a-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5684a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5684a-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5684a-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5684a-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5684a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="5684a-151"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5684a-151"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5684a-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="5684a-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="5684a-153">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5684a-153">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span></span>
</dt> </dl>

 

