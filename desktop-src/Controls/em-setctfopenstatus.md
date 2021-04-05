---
title: Mensagem de EM_SETCTFOPENSTATUS (RichEdit. h)
description: Abre ou fecha o teclado do TSF (estrutura de serviços de texto).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- Controles de EM_SETCTFOPENSTATUS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009659"
---
# <a name="em_setctfopenstatus-message"></a><span data-ttu-id="daade-104">\_Mensagem em SETCTFOPENSTATUS</span><span class="sxs-lookup"><span data-stu-id="daade-104">EM\_SETCTFOPENSTATUS message</span></span>

<span data-ttu-id="daade-105">Abre ou fecha o teclado do TSF (estrutura de serviços de texto).</span><span class="sxs-lookup"><span data-stu-id="daade-105">Opens or closes the Text Services Framework (TSF) keyboard.</span></span>

## <a name="parameters"></a><span data-ttu-id="daade-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="daade-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daade-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="daade-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="daade-108">Para ativar o teclado TSF, use **true**.</span><span class="sxs-lookup"><span data-stu-id="daade-108">To turn on the TSF keyboard, use **TRUE**.</span></span> <span data-ttu-id="daade-109">Para desligar o teclado TSF, use **false**.</span><span class="sxs-lookup"><span data-stu-id="daade-109">To turn off the TSF keyboard, use **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="daade-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="daade-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="daade-111">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="daade-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daade-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="daade-112">Return value</span></span>

<span data-ttu-id="daade-113">Se for bem-sucedida, essa mensagem retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="daade-113">If successful, this message returns **TRUE**.</span></span> <span data-ttu-id="daade-114">Se não for bem-sucedida, essa mensagem retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="daade-114">If unsuccessful, this message returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="daade-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daade-115">Requirements</span></span>



| <span data-ttu-id="daade-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="daade-116">Requirement</span></span> | <span data-ttu-id="daade-117">Valor</span><span class="sxs-lookup"><span data-stu-id="daade-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="daade-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="daade-118">Minimum supported client</span></span><br/> | <span data-ttu-id="daade-119">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="daade-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="daade-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="daade-120">Minimum supported server</span></span><br/> | <span data-ttu-id="daade-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="daade-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="daade-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="daade-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="daade-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="daade-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daade-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="daade-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daade-125">**em \_ GETCTFOPENSTATUS**</span><span class="sxs-lookup"><span data-stu-id="daade-125">**EM\_GETCTFOPENSTATUS**</span></span>](em-getctfopenstatus.md)
</dt> </dl>

 

 





