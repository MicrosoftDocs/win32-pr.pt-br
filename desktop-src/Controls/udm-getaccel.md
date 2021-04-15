---
title: Mensagem de UDM_GETACCEL (commctrl. h)
description: Recupera informações de aceleração para um controle de cima para baixo.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- Controles de UDM_GETACCEL de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454819"
---
# <a name="udm_getaccel-message"></a><span data-ttu-id="0e7fe-104">\_Mensagem de GETACCEL UDM</span><span class="sxs-lookup"><span data-stu-id="0e7fe-104">UDM\_GETACCEL message</span></span>

<span data-ttu-id="0e7fe-105">Recupera informações de aceleração para um controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="0e7fe-105">Retrieves acceleration information for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e7fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e7fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e7fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e7fe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e7fe-108">Número de elementos na matriz especificada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="0e7fe-108">Number of elements in the array specified by *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="0e7fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e7fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e7fe-110">Ponteiro para uma matriz de estruturas [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) que recebem informações de aceleração.</span><span class="sxs-lookup"><span data-stu-id="0e7fe-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that receive acceleration information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e7fe-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e7fe-111">Return value</span></span>

<span data-ttu-id="0e7fe-112">O valor de retorno é o número de aceleradores definidos atualmente para o controle.</span><span class="sxs-lookup"><span data-stu-id="0e7fe-112">The return value is the number of accelerators currently set for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e7fe-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e7fe-113">Requirements</span></span>



| <span data-ttu-id="0e7fe-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e7fe-114">Requirement</span></span> | <span data-ttu-id="0e7fe-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0e7fe-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e7fe-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e7fe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0e7fe-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e7fe-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e7fe-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e7fe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0e7fe-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0e7fe-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e7fe-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e7fe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e7fe-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e7fe-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e7fe-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e7fe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e7fe-123">**\_SETACCEL UDM**</span><span class="sxs-lookup"><span data-stu-id="0e7fe-123">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)
</dt> </dl>

 

 





