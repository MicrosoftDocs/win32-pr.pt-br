---
title: Mensagem de UDM_GETPOS (commctrl. h)
description: Recupera a posição atual de um controle de cima para baixo com precisão de 16 bits.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- Controles de UDM_GETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e78ad19289d85b93ebcb39a244a896ddb4f33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748248"
---
# <a name="udm_getpos-message"></a><span data-ttu-id="cf546-104">\_Mensagem de GETPOS UDM</span><span class="sxs-lookup"><span data-stu-id="cf546-104">UDM\_GETPOS message</span></span>

<span data-ttu-id="cf546-105">Recupera a posição atual de um controle de cima para baixo com precisão de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="cf546-105">Retrieves the current position of an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf546-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf546-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf546-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf546-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cf546-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cf546-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cf546-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf546-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cf546-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cf546-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf546-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf546-111">Return value</span></span>

<span data-ttu-id="cf546-112">Se for bem-sucedido, o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) será definido como zero e o [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) será definido como a posição atual do controle.</span><span class="sxs-lookup"><span data-stu-id="cf546-112">If successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is set to zero and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is set to the control's current position.</span></span> <span data-ttu-id="cf546-113">Se ocorrer um erro, o **HIWORD** será definido como um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="cf546-113">If an error occurs, the **HIWORD** is set to a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf546-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf546-114">Remarks</span></span>

<span data-ttu-id="cf546-115">Ao processar essa mensagem, o controle de cima para baixo atualiza sua posição atual com base na legenda da janela Buddy.</span><span class="sxs-lookup"><span data-stu-id="cf546-115">When processing this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="cf546-116">O controle de cima para baixo retornará um erro se não houver nenhuma janela Buddy ou se a legenda especificar um valor inválido ou fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="cf546-116">The up-down control returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span> <span data-ttu-id="cf546-117">Além disso, um sinalizador de erro é definido no HIWORD do retorno se o controle for criado sem o estilo [**UDS \_ SETBUDDYINT**](up-down-control-styles.md) , embora ele retorne um valor de posição válido no LOWORD do retorno.</span><span class="sxs-lookup"><span data-stu-id="cf546-117">Also, an error flag is set in the HIWORD of the return if the control is created without the [**UDS\_SETBUDDYINT**](up-down-control-styles.md) style, even though it returns a valid position value in the LOWORD of the return.</span></span>

<span data-ttu-id="cf546-118">Se os valores de 32 bits tiverem sido habilitados para um controle de cima para baixo com o [**UDM \_ SETRANGE32**](udm-setrange32.md), essa mensagem retornará apenas 16 bits inferiores da posição.</span><span class="sxs-lookup"><span data-stu-id="cf546-118">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), this message returns only the lower 16 bits of the position.</span></span> <span data-ttu-id="cf546-119">Para recuperar a posição completa de 32 bits, use o [**UDM \_ GETPOS32**](udm-getpos32.md).</span><span class="sxs-lookup"><span data-stu-id="cf546-119">To retrieve the full 32-bit position, use [**UDM\_GETPOS32**](udm-getpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf546-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf546-120">Requirements</span></span>



| <span data-ttu-id="cf546-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf546-121">Requirement</span></span> | <span data-ttu-id="cf546-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cf546-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf546-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf546-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cf546-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf546-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf546-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf546-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cf546-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf546-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf546-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf546-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf546-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf546-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf546-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf546-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf546-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="cf546-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cf546-131">**GetRange do UDM \_**</span><span class="sxs-lookup"><span data-stu-id="cf546-131">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="cf546-132">**\_GETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="cf546-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)
</dt> <dt>

[<span data-ttu-id="cf546-133">**\_SETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="cf546-133">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="cf546-134">**\_SETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="cf546-134">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)
</dt> </dl>

 

