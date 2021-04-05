---
title: Mensagem de UDM_SETPOS32 (commctrl. h)
description: Define a posição de um controle de cima para baixo com precisão de 32 bits.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- Controles de UDM_SETPOS32 de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0153305bb535a79dbed59e8d42a7c25157c30cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918772"
---
# <a name="udm_setpos32-message"></a><span data-ttu-id="86eda-104">\_Mensagem de SETPOS32 UDM</span><span class="sxs-lookup"><span data-stu-id="86eda-104">UDM\_SETPOS32 message</span></span>

<span data-ttu-id="86eda-105">Define a posição de um controle de cima para baixo com precisão de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="86eda-105">Sets the position of an up-down control with 32-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="86eda-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86eda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86eda-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86eda-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="86eda-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="86eda-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="86eda-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86eda-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86eda-110">Variável do tipo inteiro que especifica a nova posição para o controle acima-abaixo.</span><span class="sxs-lookup"><span data-stu-id="86eda-110">Variable of type integer that specifies the new position for the up-down control.</span></span> <span data-ttu-id="86eda-111">Se o parâmetro estiver fora do intervalo especificado do controle, *lParam* será definido como o valor válido mais próximo.</span><span class="sxs-lookup"><span data-stu-id="86eda-111">If the parameter is outside the control's specified range, *lParam* is set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86eda-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86eda-112">Return value</span></span>

<span data-ttu-id="86eda-113">Retorna a posição anterior.</span><span class="sxs-lookup"><span data-stu-id="86eda-113">Returns the previous position.</span></span>

## <a name="requirements"></a><span data-ttu-id="86eda-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86eda-114">Requirements</span></span>



| <span data-ttu-id="86eda-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="86eda-115">Requirement</span></span> | <span data-ttu-id="86eda-116">Valor</span><span class="sxs-lookup"><span data-stu-id="86eda-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86eda-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86eda-117">Minimum supported client</span></span><br/> | <span data-ttu-id="86eda-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86eda-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86eda-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86eda-119">Minimum supported server</span></span><br/> | <span data-ttu-id="86eda-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="86eda-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86eda-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86eda-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="86eda-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="86eda-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86eda-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="86eda-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="86eda-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="86eda-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="86eda-125">**\_GETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="86eda-125">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="86eda-126">**\_SETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="86eda-126">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="86eda-127">**\_GETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="86eda-127">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)
</dt> </dl>

 

 





