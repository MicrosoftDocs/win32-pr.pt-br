---
title: Mensagem de TVM_GETIMAGELIST (commctrl. h)
description: Recupera o identificador para a lista de imagens normal ou de estado associada a um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro do TreeView \_ GetImageList.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- Controles de TVM_GETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4e2503d9c6d57743059ee1da3049a36ed17f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645122"
---
# <a name="tvm_getimagelist-message"></a><span data-ttu-id="649e9-105">\_Mensagem TVM GETimagelist</span><span class="sxs-lookup"><span data-stu-id="649e9-105">TVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="649e9-106">Recupera o identificador para a lista de imagens normal ou de estado associada a um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="649e9-106">Retrieves the handle to the normal or state image list associated with a tree-view control.</span></span> <span data-ttu-id="649e9-107">Você pode enviar essa mensagem explicitamente ou usando a macro do [**TreeView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="649e9-107">You can send this message explicitly or by using the [**TreeView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="649e9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="649e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="649e9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="649e9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="649e9-110">Tipo de lista de imagens a recuperar.</span><span class="sxs-lookup"><span data-stu-id="649e9-110">Type of image list to retrieve.</span></span> <span data-ttu-id="649e9-111">Esse parâmetro pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="649e9-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="649e9-112">Valor</span><span class="sxs-lookup"><span data-stu-id="649e9-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="649e9-113">Significado</span><span class="sxs-lookup"><span data-stu-id="649e9-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="649e9-114"><dt>**TVSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="649e9-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="649e9-115">Indica a lista de imagens normal, que contém imagens selecionadas, não selecionadas e sobreposição para os itens de um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="649e9-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="649e9-116"><dt>**\_estado TVSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="649e9-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="649e9-117">Indica a lista de imagens de estado.</span><span class="sxs-lookup"><span data-stu-id="649e9-117">Indicates the state image list.</span></span> <span data-ttu-id="649e9-118">Você pode usar imagens de estado para indicar os Estados de itens definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="649e9-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="649e9-119">Uma imagem de estado é exibida à esquerda da imagem selecionada ou não marcada de um item.</span><span class="sxs-lookup"><span data-stu-id="649e9-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="649e9-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="649e9-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="649e9-121">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="649e9-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="649e9-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="649e9-122">Return value</span></span>

<span data-ttu-id="649e9-123">Retorna um identificador HIMAGELIST para a lista de imagens especificada.</span><span class="sxs-lookup"><span data-stu-id="649e9-123">Returns an HIMAGELIST handle to the specified image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="649e9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="649e9-124">Requirements</span></span>



| <span data-ttu-id="649e9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="649e9-125">Requirement</span></span> | <span data-ttu-id="649e9-126">Valor</span><span class="sxs-lookup"><span data-stu-id="649e9-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="649e9-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="649e9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="649e9-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="649e9-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="649e9-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="649e9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="649e9-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="649e9-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="649e9-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="649e9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="649e9-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="649e9-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="649e9-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="649e9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="649e9-134">**TVM \_ SETimagelist**</span><span class="sxs-lookup"><span data-stu-id="649e9-134">**TVM\_SETIMAGELIST**</span></span>](tvm-setimagelist.md)
</dt> </dl>

 

 





