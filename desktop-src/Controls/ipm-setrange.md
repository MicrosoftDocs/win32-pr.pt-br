---
title: Mensagem de IPM_SETRANGE (commctrl. h)
description: Define o intervalo válido para o campo especificado no controle de endereço IP.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- Controles de IPM_SETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e70df7b2b8f76f514d9a0cc6101aba2ee7cf4ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009616"
---
# <a name="ipm_setrange-message"></a><span data-ttu-id="19f6d-104">\_Mensagem IPM SETRANGE</span><span class="sxs-lookup"><span data-stu-id="19f6d-104">IPM\_SETRANGE message</span></span>

<span data-ttu-id="19f6d-105">Define o intervalo válido para o campo especificado no controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="19f6d-105">Sets the valid range for the specified field in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="19f6d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19f6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19f6d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19f6d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19f6d-108">Um índice de campo baseado em zero ao qual o intervalo será aplicado.</span><span class="sxs-lookup"><span data-stu-id="19f6d-108">A zero-based field index to which the range will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="19f6d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19f6d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19f6d-110">Um valor de **palavra** que contém o limite inferior do intervalo no byte de ordem inferior e o limite superior no byte de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="19f6d-110">A **WORD** value that contains the lower limit of the range in the low-order byte and the upper limit in the high-order byte.</span></span> <span data-ttu-id="19f6d-111">Esses dois valores são inclusivos.</span><span class="sxs-lookup"><span data-stu-id="19f6d-111">Both of these values are inclusive.</span></span> <span data-ttu-id="19f6d-112">A macro [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) também pode ser usada para criar o intervalo.</span><span class="sxs-lookup"><span data-stu-id="19f6d-112">The [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) macro can also be used to create the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19f6d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19f6d-113">Return value</span></span>

<span data-ttu-id="19f6d-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="19f6d-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="19f6d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="19f6d-115">Remarks</span></span>

<span data-ttu-id="19f6d-116">Se o usuário inserir um valor no campo que está fora desse intervalo, o controle enviará a notificação [ \_ FieldChanged IPN](ipn-fieldchanged.md) com o valor inserido.</span><span class="sxs-lookup"><span data-stu-id="19f6d-116">If the user enters a value in the field that is outside of this range, the control will send the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification with the entered value.</span></span> <span data-ttu-id="19f6d-117">Se o valor ainda estiver fora do intervalo após o envio da notificação, o controle tentará alterar o valor inserido para o limite de intervalo mais próximo.</span><span class="sxs-lookup"><span data-stu-id="19f6d-117">If the value is still outside of the range after sending the notification, the control will attempt to change the entered value to the closest range limit.</span></span>

## <a name="requirements"></a><span data-ttu-id="19f6d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19f6d-118">Requirements</span></span>



| <span data-ttu-id="19f6d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="19f6d-119">Requirement</span></span> | <span data-ttu-id="19f6d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="19f6d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19f6d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19f6d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="19f6d-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19f6d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19f6d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19f6d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="19f6d-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19f6d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19f6d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19f6d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="19f6d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="19f6d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





