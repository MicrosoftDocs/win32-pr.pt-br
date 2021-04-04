---
title: Mensagem de EM_SETPAGEROTATE (RichEdit. h)
description: Define o layout de texto para um controle de edição rico.
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- Controles de EM_SETPAGEROTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918348"
---
# <a name="em_setpagerotate-message"></a><span data-ttu-id="eac98-104">\_Mensagem em SETPAGEROTATE</span><span class="sxs-lookup"><span data-stu-id="eac98-104">EM\_SETPAGEROTATE message</span></span>

<span data-ttu-id="eac98-105">\[**Em \_ O SETPAGEROTATE** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="eac98-105">\[**EM\_SETPAGEROTATE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eac98-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="eac98-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="eac98-107">Define o layout de texto para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="eac98-107">Sets the text layout for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="eac98-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eac98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eac98-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eac98-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eac98-110">Valor de layout do texto.</span><span class="sxs-lookup"><span data-stu-id="eac98-110">Text layout value.</span></span> <span data-ttu-id="eac98-111">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="eac98-111">This can be one of the following values.</span></span>



| <span data-ttu-id="eac98-112">Valor</span><span class="sxs-lookup"><span data-stu-id="eac98-112">Value</span></span>                                                                                                                                       | <span data-ttu-id="eac98-113">Significado</span><span class="sxs-lookup"><span data-stu-id="eac98-113">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <span data-ttu-id="eac98-114"><dt>**EPR \_ 0**</dt></span><span class="sxs-lookup"><span data-stu-id="eac98-114"><dt>**EPR\_0**</dt></span></span> </dl>       | <span data-ttu-id="eac98-115">O texto flui da esquerda para a direita e de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="eac98-115">Text flows from left to right and from top to bottom.</span></span><br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <span data-ttu-id="eac98-116"><dt>**EPR \_ 90**</dt></span><span class="sxs-lookup"><span data-stu-id="eac98-116"><dt>**EPR\_90**</dt></span></span> </dl>    | <span data-ttu-id="eac98-117">O texto flui de baixo para cima e da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="eac98-117">Text flows from bottom to top and from left to right.</span></span><br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <span data-ttu-id="eac98-118"><dt>**EPR \_ 180**</dt></span><span class="sxs-lookup"><span data-stu-id="eac98-118"><dt>**EPR\_180**</dt></span></span> </dl> | <span data-ttu-id="eac98-119">O texto flui da direita para a esquerda e de baixo para cima.</span><span class="sxs-lookup"><span data-stu-id="eac98-119">Text flows from right to left and from bottom to top.</span></span><br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <span data-ttu-id="eac98-120"><dt>**EPR \_ 270**</dt></span><span class="sxs-lookup"><span data-stu-id="eac98-120"><dt>**EPR\_270**</dt></span></span> </dl> | <span data-ttu-id="eac98-121">O texto flui de cima para baixo e da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="eac98-121">Text flows from top to bottom and from right to left.</span></span><br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <span data-ttu-id="eac98-122"><dt>**EPR \_ se**</dt></span><span class="sxs-lookup"><span data-stu-id="eac98-122"><dt>**EPR\_SE**</dt></span></span> </dl>    | <span data-ttu-id="eac98-123">**Windows 8:** O texto flui de cima para baixo e da esquerda para a direita (layout de texto mongol).</span><span class="sxs-lookup"><span data-stu-id="eac98-123">**Windows 8:** Text flows top to bottom and left to right (Mongolian text layout).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eac98-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eac98-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eac98-125">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="eac98-125">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eac98-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eac98-126">Return value</span></span>

<span data-ttu-id="eac98-127">Valor de retorno é o novo valor de layout de texto.</span><span class="sxs-lookup"><span data-stu-id="eac98-127">Return value is the new text layout value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eac98-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="eac98-128">Remarks</span></span>

<span data-ttu-id="eac98-129">Esta mensagem define o layout de texto para todo o documento.</span><span class="sxs-lookup"><span data-stu-id="eac98-129">This message sets the text layout for the entire document.</span></span> <span data-ttu-id="eac98-130">No entanto, o conteúdo inserido não é girado e deve ser girado separadamente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eac98-130">However, embedded contents are not rotated and must be rotated separately by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="eac98-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eac98-131">Requirements</span></span>



| <span data-ttu-id="eac98-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="eac98-132">Requirement</span></span> | <span data-ttu-id="eac98-133">Valor</span><span class="sxs-lookup"><span data-stu-id="eac98-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eac98-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eac98-134">Minimum supported client</span></span><br/> | <span data-ttu-id="eac98-135">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="eac98-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eac98-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eac98-136">Minimum supported server</span></span><br/> | <span data-ttu-id="eac98-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eac98-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eac98-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eac98-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="eac98-139"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="eac98-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eac98-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="eac98-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac98-141">**em \_ GETPAGEROTATE**</span><span class="sxs-lookup"><span data-stu-id="eac98-141">**EM\_GETPAGEROTATE**</span></span>](em-getpagerotate.md)
</dt> </dl>

 

 





