---
title: Mensagem de PSM_SETHEADERTITLE (Prsht. h)
description: Define o texto do título do cabeçalho da página interior de um assistente. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet SetHeaderTitle.
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- Controles de PSM_SETHEADERTITLE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETHEADERTITLE
- PSM_SETHEADERTITLEA
- PSM_SETHEADERTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8140eef4aa09e9dd19d8baaf8193a836b105482e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811140"
---
# <a name="psm_setheadertitle-message"></a><span data-ttu-id="17df5-105">Mensagem de PSM \_ SETHEADERTITLE</span><span class="sxs-lookup"><span data-stu-id="17df5-105">PSM\_SETHEADERTITLE message</span></span>

<span data-ttu-id="17df5-106">Define o texto do título do cabeçalho da página interior de um assistente.</span><span class="sxs-lookup"><span data-stu-id="17df5-106">Sets the title text for the header of a wizard's interior page.</span></span> <span data-ttu-id="17df5-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) .</span><span class="sxs-lookup"><span data-stu-id="17df5-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="17df5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17df5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17df5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17df5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17df5-110">Índice de base zero da página do assistente.</span><span class="sxs-lookup"><span data-stu-id="17df5-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="17df5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17df5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17df5-112">Novo subtítulo do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="17df5-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17df5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17df5-113">Return value</span></span>

<span data-ttu-id="17df5-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="17df5-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17df5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="17df5-115">Remarks</span></span>

<span data-ttu-id="17df5-116">Se você especificar a página atual, ela será repintada imediatamente para exibir o novo título.</span><span class="sxs-lookup"><span data-stu-id="17df5-116">If you specify the current page, it will immediately be repainted to display the new title.</span></span>

## <a name="requirements"></a><span data-ttu-id="17df5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17df5-117">Requirements</span></span>



| <span data-ttu-id="17df5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="17df5-118">Requirement</span></span> | <span data-ttu-id="17df5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="17df5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17df5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17df5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="17df5-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17df5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="17df5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17df5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="17df5-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="17df5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="17df5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17df5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="17df5-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="17df5-125"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="17df5-126">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="17df5-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="17df5-127">**PSM \_ SETHEADERTITLEW** (Unicode) e **PSM \_ SETHEADERTITLEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="17df5-127">**PSM\_SETHEADERTITLEW** (Unicode) and **PSM\_SETHEADERTITLEA** (ANSI)</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="17df5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="17df5-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="17df5-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="17df5-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="17df5-130">**HWNDTOINDEX de PSM \_**</span><span class="sxs-lookup"><span data-stu-id="17df5-130">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="17df5-131">**IDTOINDEX de PSM \_**</span><span class="sxs-lookup"><span data-stu-id="17df5-131">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="17df5-132">**PAGETOINDEX de PSM \_**</span><span class="sxs-lookup"><span data-stu-id="17df5-132">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 





