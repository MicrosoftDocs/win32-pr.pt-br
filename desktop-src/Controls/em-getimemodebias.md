---
title: Mensagem de EM_GETIMEMODEBIAS (RichEdit. h)
description: Recupera o ajuste do modo IME (editor de método de entrada) para um controle de edição rico da Microsoft.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- Controles de EM_GETIMEMODEBIAS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009564"
---
# <a name="em_getimemodebias-message"></a><span data-ttu-id="b0d8a-104">\_Mensagem em GETIMEMODEBIAS</span><span class="sxs-lookup"><span data-stu-id="b0d8a-104">EM\_GETIMEMODEBIAS message</span></span>

<span data-ttu-id="b0d8a-105">Recupera o ajuste do modo IME (editor de método de entrada) para um controle de edição rico da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b0d8a-105">Retrieves the Input Method Editor (IME) mode bias for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0d8a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0d8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0d8a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0d8a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0d8a-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b0d8a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b0d8a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0d8a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0d8a-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b0d8a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0d8a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0d8a-111">Return value</span></span>

<span data-ttu-id="b0d8a-112">Essa mensagem retorna a configuração de ajuste do modo IME atual.</span><span class="sxs-lookup"><span data-stu-id="b0d8a-112">This message returns the current IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0d8a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0d8a-113">Remarks</span></span>

<span data-ttu-id="b0d8a-114">Para obter a tendência do modo de estrutura de serviços de texto, use em [**\_ GETCTFMODEBIAS**](em-getctfmodebias.md).</span><span class="sxs-lookup"><span data-stu-id="b0d8a-114">To get the Text Services Framework mode bias, use [**EM\_GETCTFMODEBIAS**](em-getctfmodebias.md).</span></span>

<span data-ttu-id="b0d8a-115">O aplicativo deve chamar [**em \_ ISIME**](em-isime.md) antes de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="b0d8a-115">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0d8a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0d8a-116">Requirements</span></span>



| <span data-ttu-id="b0d8a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0d8a-117">Requirement</span></span> | <span data-ttu-id="b0d8a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b0d8a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d8a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0d8a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b0d8a-120">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="b0d8a-120">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0d8a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0d8a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b0d8a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b0d8a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0d8a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0d8a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0d8a-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0d8a-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0d8a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0d8a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="b0d8a-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b0d8a-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b0d8a-127">**em \_ ISIME**</span><span class="sxs-lookup"><span data-stu-id="b0d8a-127">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="b0d8a-128">**em \_ GETCTFMODEBIAS**</span><span class="sxs-lookup"><span data-stu-id="b0d8a-128">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> </dl>

 

 





