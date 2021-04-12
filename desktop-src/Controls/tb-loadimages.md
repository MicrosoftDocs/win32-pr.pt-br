---
title: Mensagem de TB_LOADIMAGES (commctrl. h)
description: Carrega imagens de botão definidas pelo sistema em uma lista de imagens de controle da barra de ferramentas.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- Controles de TB_LOADIMAGES de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455604"
---
# <a name="tb_loadimages-message"></a><span data-ttu-id="1f874-104">\_Mensagem de LOADimages TB</span><span class="sxs-lookup"><span data-stu-id="1f874-104">TB\_LOADIMAGES message</span></span>

<span data-ttu-id="1f874-105">Carrega imagens de botão definidas pelo sistema em uma lista de imagens de controle da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="1f874-105">Loads system-defined button images into a toolbar control's image list.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f874-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f874-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f874-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f874-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f874-108">Identificador de uma lista de imagens de botões definida pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="1f874-108">Identifier of a system-defined button image list.</span></span> <span data-ttu-id="1f874-109">Esse parâmetro pode ser definido como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f874-109">This parameter can be set to one of the following values.</span></span>



| <span data-ttu-id="1f874-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1f874-110">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="1f874-111">Significado</span><span class="sxs-lookup"><span data-stu-id="1f874-111">Meaning</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <span data-ttu-id="1f874-112"><dt>**\_ \_ cor grande do sua de idb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f874-112"><dt>**IDB\_HIST\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="1f874-113">Bitmaps do Windows Explorer em tamanho grande.</span><span class="sxs-lookup"><span data-stu-id="1f874-113">Windows Explorer bitmaps in large size.</span></span><br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <span data-ttu-id="1f874-114"><dt>**\_ \_ cor pequena do sua de idb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f874-114"><dt>**IDB\_HIST\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="1f874-115">Bitmaps do Windows Explorer em tamanho pequeno.</span><span class="sxs-lookup"><span data-stu-id="1f874-115">Windows Explorer bitmaps in small size.</span></span><br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <span data-ttu-id="1f874-116"><dt>**\_ \_ cor grande do idb padrão \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f874-116"><dt>**IDB\_STD\_LARGE\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="1f874-117">Bitmaps padrão em tamanho grande.</span><span class="sxs-lookup"><span data-stu-id="1f874-117">Standard bitmaps in large size.</span></span><br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <span data-ttu-id="1f874-118"><dt>**cor do IDB \_ std \_ Small \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f874-118"><dt>**IDB\_STD\_SMALL\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="1f874-119">Bitmaps padrão em tamanho pequeno.</span><span class="sxs-lookup"><span data-stu-id="1f874-119">Standard bitmaps in small size.</span></span><br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <span data-ttu-id="1f874-120"><dt>**\_ \_ cor grande de exibição de idb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f874-120"><dt>**IDB\_VIEW\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="1f874-121">Exibir bitmaps em tamanho grande.</span><span class="sxs-lookup"><span data-stu-id="1f874-121">View bitmaps in large size.</span></span><br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <span data-ttu-id="1f874-122"><dt>**\_ \_ cor pequena da exibição idb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f874-122"><dt>**IDB\_VIEW\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="1f874-123">Exibir bitmaps em tamanho pequeno.</span><span class="sxs-lookup"><span data-stu-id="1f874-123">View bitmaps in small size.</span></span><br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <span data-ttu-id="1f874-124"><dt>**sua de IDB \_ \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="1f874-124"><dt>**IDB\_HIST\_NORMAL**</dt></span></span> </dl>                 | <span data-ttu-id="1f874-125">Os botões de viagem do Windows Explorer e os bitmaps de favoritos em estado normal.</span><span class="sxs-lookup"><span data-stu-id="1f874-125">Windows Explorer travel buttons and favorites bitmaps in normal state.</span></span><br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <span data-ttu-id="1f874-126"><dt>**sua de IDB \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f874-126"><dt>**IDB\_HIST\_HOT**</dt></span></span> </dl>                          | <span data-ttu-id="1f874-127">Os botões de viagem do Windows Explorer e os bitmaps de favoritos estão em estado ativo.</span><span class="sxs-lookup"><span data-stu-id="1f874-127">Windows Explorer travel buttons and favorites bitmaps in hot state.</span></span><br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <span data-ttu-id="1f874-128"><dt>**sua de IDB \_ \_ desabilitado**</dt></span><span class="sxs-lookup"><span data-stu-id="1f874-128"><dt>**IDB\_HIST\_DISABLED**</dt></span></span> </dl>           | <span data-ttu-id="1f874-129">Os botões de viagem do Windows Explorer e os bitmaps de favoritos no estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1f874-129">Windows Explorer travel buttons and favorites bitmaps in disabled state.</span></span><br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <span data-ttu-id="1f874-130"><dt>**sua de IDB \_ \_ pressionado**</dt></span><span class="sxs-lookup"><span data-stu-id="1f874-130"><dt>**IDB\_HIST\_PRESSED**</dt></span></span> </dl>              | <span data-ttu-id="1f874-131">Os botões de viagem do Windows Explorer e os bitmaps de favoritos no estado pressionado.</span><span class="sxs-lookup"><span data-stu-id="1f874-131">Windows Explorer travel buttons and favorites bitmaps in pressed state.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="1f874-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f874-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f874-133">Identificador de instância.</span><span class="sxs-lookup"><span data-stu-id="1f874-133">Instance handle.</span></span> <span data-ttu-id="1f874-134">Esse parâmetro deve ser definido como HINST \_ COMMCTRL.</span><span class="sxs-lookup"><span data-stu-id="1f874-134">This parameter must be set to HINST\_COMMCTRL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f874-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f874-135">Return value</span></span>

<span data-ttu-id="1f874-136">A contagem de imagens na lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="1f874-136">The count of images in the image list.</span></span> <span data-ttu-id="1f874-137">Retornará zero se a barra de ferramentas não tiver nenhuma lista de imagens ou se a lista de imagens existente estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="1f874-137">Returns zero if the toolbar has no image list or if the existing image list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f874-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f874-138">Remarks</span></span>

<span data-ttu-id="1f874-139">Você deve usar os valores de índice de imagem apropriados ao preparar estruturas [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) antes de enviar a mensagem de [**\_ hiperbotãos de TB**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="1f874-139">You must use the proper image index values when you prepare [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures prior to sending the [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="1f874-140">Para obter uma lista de valores de índice de imagem para esses bitmaps predefinidos, consulte [valores de índice de imagem de botão padrão da barra de ferramentas](toolbar-standard-button-image-index-values.md).</span><span class="sxs-lookup"><span data-stu-id="1f874-140">For a list of image index values for these preset bitmaps, see [Toolbar Standard Button Image Index Values](toolbar-standard-button-image-index-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1f874-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f874-141">Examples</span></span>

<span data-ttu-id="1f874-142">O código de exemplo a seguir carrega as imagens de cores pequenas do sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="1f874-142">The following sample code loads the system standard small color images.</span></span>


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a><span data-ttu-id="1f874-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f874-143">Requirements</span></span>



| <span data-ttu-id="1f874-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f874-144">Requirement</span></span> | <span data-ttu-id="1f874-145">Valor</span><span class="sxs-lookup"><span data-stu-id="1f874-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f874-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f874-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1f874-147">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f874-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f874-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f874-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1f874-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f874-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f874-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f874-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f874-151"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f874-151"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f874-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f874-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f874-153">**rebitmap de TB \_**</span><span class="sxs-lookup"><span data-stu-id="1f874-153">**TB\_ADDBITMAP**</span></span>](tb-addbitmap.md)
</dt> </dl>

 

 





