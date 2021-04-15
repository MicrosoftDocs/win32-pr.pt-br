---
title: Mensagem de UDM_GETPOS32 (commctrl. h)
description: Retorna a posição de 32 bits de um controle acima-abaixo.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- Controles de UDM_GETPOS32 de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454816"
---
# <a name="udm_getpos32-message"></a><span data-ttu-id="04f77-104">\_Mensagem de GETPOS32 UDM</span><span class="sxs-lookup"><span data-stu-id="04f77-104">UDM\_GETPOS32 message</span></span>

<span data-ttu-id="04f77-105">Retorna a posição de 32 bits de um controle acima-abaixo.</span><span class="sxs-lookup"><span data-stu-id="04f77-105">Returns the 32-bit position of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="04f77-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04f77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04f77-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04f77-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04f77-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="04f77-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="04f77-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04f77-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04f77-110">Ponteiro para um valor **bool** definido como zero se o valor for recuperado com êxito ou diferente de zero se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="04f77-110">Pointer to a **BOOL** value that is set to zero if the value is successfully retrieved or nonzero if an error occurs.</span></span> <span data-ttu-id="04f77-111">Se esse parâmetro for definido como **NULL**, os erros não serão relatados.</span><span class="sxs-lookup"><span data-stu-id="04f77-111">If this parameter is set to **NULL**, errors are not reported.</span></span>

<span data-ttu-id="04f77-112">Se o **UDM \_ GETPOS32** for usado em uma situação de processo cruzado, esse parâmetro deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="04f77-112">If **UDM\_GETPOS32** is used in a cross-process situation, this parameter must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04f77-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04f77-113">Return value</span></span>

<span data-ttu-id="04f77-114">Retorna a posição de um controle acima para baixo com precisão de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="04f77-114">Returns the position of an up-down control with 32-bit precision.</span></span> <span data-ttu-id="04f77-115">Os aplicativos devem verificar o valor de *lParam* para determinar se o valor de retorno é válido.</span><span class="sxs-lookup"><span data-stu-id="04f77-115">Applications must check the *lParam* value to determine whether the return value is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="04f77-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="04f77-116">Remarks</span></span>

<span data-ttu-id="04f77-117">Quando ele processa essa mensagem, o controle de cima para baixo atualiza sua posição atual com base na legenda da janela Buddy.</span><span class="sxs-lookup"><span data-stu-id="04f77-117">When it processes this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="04f77-118">Ele retornará um erro se não houver nenhuma janela Buddy ou se a legenda especificar um valor inválido ou fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="04f77-118">It returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span>

## <a name="requirements"></a><span data-ttu-id="04f77-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04f77-119">Requirements</span></span>



| <span data-ttu-id="04f77-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="04f77-120">Requirement</span></span> | <span data-ttu-id="04f77-121">Valor</span><span class="sxs-lookup"><span data-stu-id="04f77-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04f77-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04f77-122">Minimum supported client</span></span><br/> | <span data-ttu-id="04f77-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04f77-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04f77-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04f77-124">Minimum supported server</span></span><br/> | <span data-ttu-id="04f77-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="04f77-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04f77-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04f77-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="04f77-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="04f77-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04f77-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="04f77-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="04f77-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="04f77-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="04f77-130">**\_GETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="04f77-130">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="04f77-131">**\_SETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="04f77-131">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="04f77-132">**\_SETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="04f77-132">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)
</dt> </dl>

 

 





