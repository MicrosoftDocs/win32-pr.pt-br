---
title: Mensagem de UDM_SETPOS (commctrl. h)
description: Define a posição atual para um controle de cima para baixo com precisão de 16 bits.
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- Controles de UDM_SETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085916"
---
# <a name="udm_setpos-message"></a><span data-ttu-id="727c6-104">\_Mensagem de SETPOS UDM</span><span class="sxs-lookup"><span data-stu-id="727c6-104">UDM\_SETPOS message</span></span>

<span data-ttu-id="727c6-105">Define a posição atual para um controle de cima para baixo com precisão de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="727c6-105">Sets the current position for an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="727c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="727c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="727c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="727c6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="727c6-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="727c6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="727c6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="727c6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="727c6-110">Nova posição para o controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="727c6-110">New position for the up-down control.</span></span> <span data-ttu-id="727c6-111">Se o parâmetro estiver fora do intervalo especificado do controle, *lParam* será definido como o valor válido mais próximo.</span><span class="sxs-lookup"><span data-stu-id="727c6-111">If the parameter is outside the control's specified range, *lParam* will be set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="727c6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="727c6-112">Return value</span></span>

<span data-ttu-id="727c6-113">O valor de retorno é a posição anterior.</span><span class="sxs-lookup"><span data-stu-id="727c6-113">The return value is the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="727c6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="727c6-114">Remarks</span></span>

<span data-ttu-id="727c6-115">Esta mensagem dá suporte apenas a posições de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="727c6-115">This message only supports 16-bit positions.</span></span> <span data-ttu-id="727c6-116">Se os valores de 32 bits tiverem sido habilitados para um controle de cima para baixo com o [**UDM \_ SETRANGE32**](udm-setrange32.md), use o [**UDM \_ SETPOS32**](udm-setpos32.md).</span><span class="sxs-lookup"><span data-stu-id="727c6-116">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), use [**UDM\_SETPOS32**](udm-setpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="727c6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="727c6-117">Requirements</span></span>



| <span data-ttu-id="727c6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="727c6-118">Requirement</span></span> | <span data-ttu-id="727c6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="727c6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="727c6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="727c6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="727c6-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="727c6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="727c6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="727c6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="727c6-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="727c6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="727c6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="727c6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="727c6-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="727c6-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="727c6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="727c6-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="727c6-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="727c6-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="727c6-128">**GetRange do UDM \_**</span><span class="sxs-lookup"><span data-stu-id="727c6-128">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="727c6-129">**\_GETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="727c6-129">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> </dl>

 

 





