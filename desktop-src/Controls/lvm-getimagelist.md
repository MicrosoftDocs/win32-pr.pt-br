---
title: Mensagem de LVM_GETIMAGELIST (commctrl. h)
description: Recupera o identificador para uma lista de imagens usada para desenhar itens de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetImageList de ListView.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- Controles de LVM_GETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085813"
---
# <a name="lvm_getimagelist-message"></a><span data-ttu-id="5ed94-105">Mensagem do LVM \_ GETimagelist</span><span class="sxs-lookup"><span data-stu-id="5ed94-105">LVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="5ed94-106">Recupera o identificador para uma lista de imagens usada para desenhar itens de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="5ed94-106">Retrieves the handle to an image list used for drawing list-view items.</span></span> <span data-ttu-id="5ed94-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetImageList de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="5ed94-107">You can send this message explicitly or by using the [**ListView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ed94-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ed94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed94-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ed94-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ed94-110">Lista de imagens a recuperar.</span><span class="sxs-lookup"><span data-stu-id="5ed94-110">Image list to retrieve.</span></span> <span data-ttu-id="5ed94-111">Esse parâmetro pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5ed94-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="5ed94-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5ed94-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="5ed94-113">Significado</span><span class="sxs-lookup"><span data-stu-id="5ed94-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="5ed94-114"><dt>**LVSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed94-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="5ed94-115">Lista de imagens com ícones grandes.</span><span class="sxs-lookup"><span data-stu-id="5ed94-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="5ed94-116"><dt>**LVSIL \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed94-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="5ed94-117">Lista de imagens com ícones pequenos.</span><span class="sxs-lookup"><span data-stu-id="5ed94-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="5ed94-118"><dt>**\_estado LVSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed94-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="5ed94-119">Lista de imagem com imagens de estado.</span><span class="sxs-lookup"><span data-stu-id="5ed94-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="5ed94-120"><dt>**\_GROUPHEADER LVSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed94-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="5ed94-121">Lista de imagens para cabeçalho de grupo.</span><span class="sxs-lookup"><span data-stu-id="5ed94-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="5ed94-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ed94-122">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5ed94-123">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5ed94-123">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ed94-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ed94-124">Return value</span></span>

<span data-ttu-id="5ed94-125">Retorna o identificador para a lista de imagens especificada, se for bem-sucedido, ou **NULL** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="5ed94-125">Returns the handle to the specified image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed94-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ed94-126">Requirements</span></span>



| <span data-ttu-id="5ed94-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ed94-127">Requirement</span></span> | <span data-ttu-id="5ed94-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5ed94-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed94-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ed94-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed94-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ed94-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5ed94-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ed94-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed94-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5ed94-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5ed94-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed94-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ed94-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ed94-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





