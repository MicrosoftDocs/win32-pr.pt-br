---
title: Mensagem de HDM_SETIMAGELIST (commctrl. h)
description: Atribui uma lista de imagens a um controle de cabeçalho existente. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetImageList ou header \_ SetStateImageList do cabeçalho.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- Controles de HDM_SETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918390"
---
# <a name="hdm_setimagelist-message"></a><span data-ttu-id="9c1d7-105">\_Mensagem HDM SETimagelist</span><span class="sxs-lookup"><span data-stu-id="9c1d7-105">HDM\_SETIMAGELIST message</span></span>

<span data-ttu-id="9c1d7-106">Atribui uma lista de imagens a um controle de cabeçalho existente.</span><span class="sxs-lookup"><span data-stu-id="9c1d7-106">Assigns an image list to an existing header control.</span></span> <span data-ttu-id="9c1d7-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) ou [**header \_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="9c1d7-107">You can send this message explicitly or use the [**Header\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) or [**Header\_SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c1d7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c1d7-108">Parameters</span></span>

<dl> <span data-ttu-id="9c1d7-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="9c1d7-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="9c1d7-110">Um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="9c1d7-110">One of the following values:</span></span>

| <span data-ttu-id="9c1d7-111">Valor</span><span class="sxs-lookup"><span data-stu-id="9c1d7-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="9c1d7-112">Significado</span><span class="sxs-lookup"><span data-stu-id="9c1d7-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="9c1d7-113"><dt>**HDSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="9c1d7-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="9c1d7-114">Indica que esta é uma lista de imagens normal.</span><span class="sxs-lookup"><span data-stu-id="9c1d7-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="9c1d7-115"><dt>**\_estado HDSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="9c1d7-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="9c1d7-116">Indica que esta é uma lista de imagens de estado.</span><span class="sxs-lookup"><span data-stu-id="9c1d7-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="9c1d7-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c1d7-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c1d7-118">Um identificador para uma lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="9c1d7-118">A handle to an image list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c1d7-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c1d7-119">Return value</span></span>

<span data-ttu-id="9c1d7-120">Retorna o identificador para a lista de imagens associada anteriormente ao controle.</span><span class="sxs-lookup"><span data-stu-id="9c1d7-120">Returns the handle to the image list previously associated with the control.</span></span> <span data-ttu-id="9c1d7-121">Retorna **NULL** após a falha ou se nenhuma lista de imagens foi definida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9c1d7-121">Returns **NULL** upon failure or if no image list was set previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c1d7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c1d7-122">Requirements</span></span>



| <span data-ttu-id="9c1d7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c1d7-123">Requirement</span></span> | <span data-ttu-id="9c1d7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9c1d7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c1d7-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c1d7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9c1d7-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c1d7-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c1d7-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c1d7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9c1d7-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c1d7-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c1d7-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c1d7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c1d7-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c1d7-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





