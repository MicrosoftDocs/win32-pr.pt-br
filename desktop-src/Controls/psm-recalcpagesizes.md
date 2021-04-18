---
title: Mensagem de PSM_RECALCPAGESIZES (Prsht. h)
description: Recalcula o tamanho da página de uma folha de propriedades padrão ou do assistente depois que as páginas são adicionadas ou removidas. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet RecalcPageSizes.
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- Controles de PSM_RECALCPAGESIZES de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752941"
---
# <a name="psm_recalcpagesizes-message"></a><span data-ttu-id="b8595-105">Mensagem de PSM \_ RECALCPAGESIZES</span><span class="sxs-lookup"><span data-stu-id="b8595-105">PSM\_RECALCPAGESIZES message</span></span>

<span data-ttu-id="b8595-106">Recalcula o tamanho da página de uma folha de propriedades padrão ou do assistente depois que as páginas são adicionadas ou removidas.</span><span class="sxs-lookup"><span data-stu-id="b8595-106">Recalculates the page size of a standard or wizard property sheet after pages have been added or removed.</span></span> <span data-ttu-id="b8595-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) .</span><span class="sxs-lookup"><span data-stu-id="b8595-107">You can send this message explicitly or use the [**PropSheet\_RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8595-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8595-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8595-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8595-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8595-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b8595-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b8595-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8595-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8595-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b8595-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8595-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8595-113">Return value</span></span>

<span data-ttu-id="b8595-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b8595-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8595-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8595-115">Remarks</span></span>

<span data-ttu-id="b8595-116">Quando uma folha de propriedades é criada, ela é dimensionada para se ajustar à coleção inicial de páginas.</span><span class="sxs-lookup"><span data-stu-id="b8595-116">When a property sheet is created, it is sized to fit its initial collection of pages.</span></span> <span data-ttu-id="b8595-117">Para manter a compatibilidade com versões anteriores dos controles comuns, as folhas de propriedades e os assistentes não são automaticamente redimensionados quando as páginas são adicionadas ou removidas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="b8595-117">In order to maintain compatibility with previous versions of the common controls, property sheets and wizards do not automatically resize themselves when pages are subsequently added or removed.</span></span> <span data-ttu-id="b8595-118">Com os controles comuns [versão 5,80](common-control-versions.md), os aplicativos devem enviar uma mensagem de **PSM \_ RECALCPAGESIZES** depois de adicionar ou remover páginas com [**PSM \_ ADDPAGE**](psm-addpage.md), [**PSM \_ INSERTPAGE**](psm-insertpage.md), [**PSM \_ REMOVEPAGE**](psm-removepage.md)ou suas macros equivalentes.</span><span class="sxs-lookup"><span data-stu-id="b8595-118">With common controls [version 5.80](common-control-versions.md), applications should send a **PSM\_RECALCPAGESIZES** message after adding or removing pages with [**PSM\_ADDPAGE**](psm-addpage.md), [**PSM\_INSERTPAGE**](psm-insertpage.md), [**PSM\_REMOVEPAGE**](psm-removepage.md), or their equivalent macros.</span></span> <span data-ttu-id="b8595-119">Ele garante que a folha de propriedades seja dimensionada corretamente para sua coleção atual de páginas.</span><span class="sxs-lookup"><span data-stu-id="b8595-119">It ensures that the property sheet is properly sized for its current collection of pages.</span></span> <span data-ttu-id="b8595-120">Se essa mensagem não for enviada, algumas páginas da folha de propriedades poderão ser truncadas ou muito grandes.</span><span class="sxs-lookup"><span data-stu-id="b8595-120">If this message is not sent, some property sheet pages may be truncated or too large.</span></span>

> [!Note]  
> <span data-ttu-id="b8595-121">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="b8595-121">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b8595-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8595-122">Requirements</span></span>



| <span data-ttu-id="b8595-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8595-123">Requirement</span></span> | <span data-ttu-id="b8595-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b8595-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8595-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8595-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b8595-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8595-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b8595-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8595-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b8595-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8595-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b8595-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8595-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8595-130"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8595-130"><dt>Prsht.h</dt></span></span> </dl> |



 

 





