---
title: Mensagem de PSM_CHANGED (Prsht. h)
description: Informa uma folha de propriedades de que as informações em uma página foram alteradas. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ Changed.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- Controles de PSM_CHANGED de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_CHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f931db5e25f816f7ea164ca5871a4e3e7757a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752942"
---
# <a name="psm_changed-message"></a><span data-ttu-id="2a6b3-105">Mensagem de alteração de PSM \_</span><span class="sxs-lookup"><span data-stu-id="2a6b3-105">PSM\_CHANGED message</span></span>

<span data-ttu-id="2a6b3-106">Informa uma folha de propriedades de que as informações em uma página foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-106">Informs a property sheet that information in a page has changed.</span></span> <span data-ttu-id="2a6b3-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) .</span><span class="sxs-lookup"><span data-stu-id="2a6b3-107">You can send this message explicitly or by using the [**PropSheet\_Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a6b3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a6b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a6b3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a6b3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a6b3-110">Identificador para a página que foi alterada.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-110">Handle to the page that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="2a6b3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a6b3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a6b3-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a6b3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a6b3-113">Return value</span></span>

<span data-ttu-id="2a6b3-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a6b3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a6b3-115">Remarks</span></span>

<span data-ttu-id="2a6b3-116">A folha de propriedades habilitará o botão **aplicar** .</span><span class="sxs-lookup"><span data-stu-id="2a6b3-116">The property sheet will enable the **Apply** button.</span></span>

> [!Note]  
> <span data-ttu-id="2a6b3-117">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="2a6b3-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2a6b3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a6b3-118">Requirements</span></span>



| <span data-ttu-id="2a6b3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a6b3-119">Requirement</span></span> | <span data-ttu-id="2a6b3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6b3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a6b3-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a6b3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2a6b3-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a6b3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2a6b3-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a6b3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2a6b3-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a6b3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2a6b3-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a6b3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a6b3-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a6b3-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





