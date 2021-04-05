---
title: Mensagem de PSM_SETHEADERSUBTITLE (Prsht. h)
description: Define o texto do subtítulo para o cabeçalho da página interior de um assistente. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet SetHeaderSubTitle.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- Controles de PSM_SETHEADERSUBTITLE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d73376b5ed35f20b43c743b31a4a78d3a4fa809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918388"
---
# <a name="psm_setheadersubtitle-message"></a><span data-ttu-id="0d8ab-105">Mensagem de PSM \_ SETHEADERSUBTITLE</span><span class="sxs-lookup"><span data-stu-id="0d8ab-105">PSM\_SETHEADERSUBTITLE message</span></span>

<span data-ttu-id="0d8ab-106">Define o texto do subtítulo para o cabeçalho da página interior de um assistente.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-106">Sets the subtitle text for the header of a wizard's interior page.</span></span> <span data-ttu-id="0d8ab-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) .</span><span class="sxs-lookup"><span data-stu-id="0d8ab-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d8ab-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d8ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d8ab-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d8ab-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d8ab-110">Índice de base zero da página do assistente.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="0d8ab-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d8ab-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d8ab-112">Novo subtítulo do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d8ab-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d8ab-113">Return value</span></span>

<span data-ttu-id="0d8ab-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d8ab-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d8ab-115">Remarks</span></span>

<span data-ttu-id="0d8ab-116">Se você especificar a página atual, ela será repintada imediatamente para exibir o novo subtítulo.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-116">If you specify the current page, it will immediately be repainted to display the new subtitle.</span></span>

> [!Note]  
> <span data-ttu-id="0d8ab-117">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="0d8ab-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d8ab-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d8ab-118">Requirements</span></span>



| <span data-ttu-id="0d8ab-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d8ab-119">Requirement</span></span> | <span data-ttu-id="0d8ab-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0d8ab-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d8ab-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d8ab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d8ab-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d8ab-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0d8ab-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d8ab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d8ab-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0d8ab-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0d8ab-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d8ab-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d8ab-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d8ab-126"><dt>Prsht.h</dt></span></span> </dl>      |
| <span data-ttu-id="0d8ab-127">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0d8ab-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0d8ab-128">**PSM \_ SETHEADERSUBTITLEW** (Unicode) e **PSM \_ SETHEADERSUBTITLEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0d8ab-128">**PSM\_SETHEADERSUBTITLEW** (Unicode) and **PSM\_SETHEADERSUBTITLEA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d8ab-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d8ab-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="0d8ab-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0d8ab-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0d8ab-131">**HWNDTOINDEX de PSM \_**</span><span class="sxs-lookup"><span data-stu-id="0d8ab-131">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="0d8ab-132">**IDTOINDEX de PSM \_**</span><span class="sxs-lookup"><span data-stu-id="0d8ab-132">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="0d8ab-133">**PAGETOINDEX de PSM \_**</span><span class="sxs-lookup"><span data-stu-id="0d8ab-133">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 





