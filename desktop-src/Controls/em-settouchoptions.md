---
title: Mensagem de EM_SETTOUCHOPTIONS (RichEdit. h)
description: Define as opções de toque associadas a um controle de edição rico.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- Controles de EM_SETTOUCHOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455343"
---
# <a name="em_settouchoptions-message"></a><span data-ttu-id="520ff-104">\_Mensagem em SETtouchoptions</span><span class="sxs-lookup"><span data-stu-id="520ff-104">EM\_SETTOUCHOPTIONS message</span></span>

<span data-ttu-id="520ff-105">Define as opções de toque associadas a um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="520ff-105">Sets the touch options associated with a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="520ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="520ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="520ff-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="520ff-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="520ff-108">A opção de toque a ser definida.</span><span class="sxs-lookup"><span data-stu-id="520ff-108">The touch option to set.</span></span> <span data-ttu-id="520ff-109">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="520ff-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="520ff-110">Valor</span><span class="sxs-lookup"><span data-stu-id="520ff-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="520ff-111">Significado</span><span class="sxs-lookup"><span data-stu-id="520ff-111">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="520ff-112"><dt>**indisponibilidades de RTO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="520ff-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="520ff-113">Mostre ou oculte os identificadores de garra de toque, dependendo do valor de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="520ff-113">Show or hide the touch gripper handles, depending on the value of *lParam*.</span></span><br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="520ff-114"><dt>**\_DISABLEHANDLES RTO**</dt></span><span class="sxs-lookup"><span data-stu-id="520ff-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="520ff-115">Habilite ou desabilite os identificadores de garra de toque, dependendo do valor de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="520ff-115">Enable or disable the touch gripper handles, depending on the value of *lParam*.</span></span> <span data-ttu-id="520ff-116">Quando os identificadores estiverem desabilitados, eles ficarão ocultos se estiverem visíveis e permanecerão ocultos até que uma mensagem em **\_ settouchoptions** altere seu status.</span><span class="sxs-lookup"><span data-stu-id="520ff-116">When handles are disabled, they are hidden if they are visible and remain hidden until an **EM\_SETTOUCHOPTIONS** message changes their status.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="520ff-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="520ff-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="520ff-118">Defina como **true** para mostrar/habilitar as alças de seleção de toque ou **false** para ocultar/desabilitar as alças de seleção de toque.</span><span class="sxs-lookup"><span data-stu-id="520ff-118">Set to **TRUE** to show/enable the touch selection handles, or **FALSE** to hide/disable the touch selection handles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="520ff-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="520ff-119">Return value</span></span>

<span data-ttu-id="520ff-120">Essa mensagem retorna zero.</span><span class="sxs-lookup"><span data-stu-id="520ff-120">This message returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="520ff-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="520ff-121">Requirements</span></span>



| <span data-ttu-id="520ff-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="520ff-122">Requirement</span></span> | <span data-ttu-id="520ff-123">Valor</span><span class="sxs-lookup"><span data-stu-id="520ff-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="520ff-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="520ff-124">Minimum supported client</span></span><br/> | <span data-ttu-id="520ff-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="520ff-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="520ff-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="520ff-126">Minimum supported server</span></span><br/> | <span data-ttu-id="520ff-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="520ff-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="520ff-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="520ff-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="520ff-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="520ff-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="520ff-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="520ff-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="520ff-131">**em \_ GETtouchoptions**</span><span class="sxs-lookup"><span data-stu-id="520ff-131">**EM\_GETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 





