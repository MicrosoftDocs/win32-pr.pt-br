---
title: Mensagem de HDM_GETIMAGELIST (commctrl. h)
description: Obtém o identificador para a lista de imagens que foi definida para um controle de cabeçalho existente. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetImageList ou header \_ GetStateImageList do cabeçalho.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- Controles de HDM_GETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644844"
---
# <a name="hdm_getimagelist-message"></a><span data-ttu-id="004d1-105">\_Mensagem HDM GETimagelist</span><span class="sxs-lookup"><span data-stu-id="004d1-105">HDM\_GETIMAGELIST message</span></span>

<span data-ttu-id="004d1-106">Obtém o identificador para a lista de imagens que foi definida para um controle de cabeçalho existente.</span><span class="sxs-lookup"><span data-stu-id="004d1-106">Gets the handle to the image list that has been set for an existing header control.</span></span> <span data-ttu-id="004d1-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) ou [**header \_ GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="004d1-107">You can send this message explicitly or use the [**Header\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) or [**Header\_GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="004d1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="004d1-108">Parameters</span></span>

<dl> <span data-ttu-id="004d1-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="004d1-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="004d1-110">Um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="004d1-110">One of the following values:</span></span>

| <span data-ttu-id="004d1-111">Valor</span><span class="sxs-lookup"><span data-stu-id="004d1-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="004d1-112">Significado</span><span class="sxs-lookup"><span data-stu-id="004d1-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="004d1-113"><dt>**HDSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="004d1-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="004d1-114">Indica que esta é uma lista de imagens normal.</span><span class="sxs-lookup"><span data-stu-id="004d1-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="004d1-115"><dt>**\_estado HDSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="004d1-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="004d1-116">Indica que esta é uma lista de imagens de estado.</span><span class="sxs-lookup"><span data-stu-id="004d1-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="004d1-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="004d1-117">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="004d1-118">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="004d1-118">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="004d1-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="004d1-119">Return value</span></span>

<span data-ttu-id="004d1-120">Retorna um identificador para a lista de imagens definida para o controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="004d1-120">Returns a handle to the image list set for the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="004d1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="004d1-121">Requirements</span></span>



| <span data-ttu-id="004d1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="004d1-122">Requirement</span></span> | <span data-ttu-id="004d1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="004d1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="004d1-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="004d1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="004d1-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="004d1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="004d1-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="004d1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="004d1-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="004d1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="004d1-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="004d1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="004d1-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="004d1-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





