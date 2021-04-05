---
title: Mensagem de EM_GETCTFMODEBIAS (RichEdit. h)
description: Obtém os valores de tendência do modo de estrutura de serviços de texto para um controle de edição rico da Microsoft.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- Controles de EM_GETCTFMODEBIAS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085676"
---
# <a name="em_getctfmodebias-message"></a><span data-ttu-id="4f68c-104">\_Mensagem em GETCTFMODEBIAS</span><span class="sxs-lookup"><span data-stu-id="4f68c-104">EM\_GETCTFMODEBIAS message</span></span>

<span data-ttu-id="4f68c-105">Obtém os valores de tendência do modo de estrutura de serviços de texto para um controle de edição rico da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4f68c-105">Gets the Text Services Framework mode bias values for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f68c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f68c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f68c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f68c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f68c-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4f68c-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4f68c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f68c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f68c-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4f68c-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f68c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f68c-111">Return value</span></span>

<span data-ttu-id="4f68c-112">O valor de tendência do modo de estrutura de serviços de texto atual.</span><span class="sxs-lookup"><span data-stu-id="4f68c-112">The current Text Services Framework mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f68c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f68c-113">Remarks</span></span>

<span data-ttu-id="4f68c-114">Para obter a tendência do modo IME, chame em [**\_ GETIMEMODEBIAS**](em-getimemodebias.md).</span><span class="sxs-lookup"><span data-stu-id="4f68c-114">To get the IME mode bias, call [**EM\_GETIMEMODEBIAS**](em-getimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f68c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f68c-115">Requirements</span></span>



| <span data-ttu-id="4f68c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f68c-116">Requirement</span></span> | <span data-ttu-id="4f68c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4f68c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f68c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f68c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4f68c-119">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="4f68c-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f68c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f68c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4f68c-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4f68c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f68c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f68c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f68c-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f68c-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f68c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f68c-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="4f68c-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4f68c-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4f68c-126">**em \_ SETCTFMODEBIAS**</span><span class="sxs-lookup"><span data-stu-id="4f68c-126">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="4f68c-127">**em \_ GETIMEMODEBIAS**</span><span class="sxs-lookup"><span data-stu-id="4f68c-127">**EM\_GETIMEMODEBIAS**</span></span>](em-getimemodebias.md)
</dt> </dl>

 

 





