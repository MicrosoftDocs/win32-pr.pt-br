---
title: Mensagem de EM_FORMATRANGE (RichEdit. h)
description: Formata um intervalo de texto em um controle de edição rico para um dispositivo específico.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- Controles de EM_FORMATRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f235fb054643623510ea23e73001aaeb070be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824478"
---
# <a name="em_formatrange-message"></a><span data-ttu-id="284d4-104">\_Mensagem em FORMATRANGE</span><span class="sxs-lookup"><span data-stu-id="284d4-104">EM\_FORMATRANGE message</span></span>

<span data-ttu-id="284d4-105">Formata um intervalo de texto em um controle de edição rico para um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="284d4-105">Formats a range of text in a rich edit control for a specific device.</span></span>

## <a name="parameters"></a><span data-ttu-id="284d4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="284d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="284d4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="284d4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="284d4-108">Especifica se o texto deve ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="284d4-108">Specifies whether to render the text.</span></span> <span data-ttu-id="284d4-109">Se esse parâmetro não for zero, o texto será renderizado.</span><span class="sxs-lookup"><span data-stu-id="284d4-109">If this parameter is not zero, the text is rendered.</span></span> <span data-ttu-id="284d4-110">Caso contrário, o texto é apenas medido.</span><span class="sxs-lookup"><span data-stu-id="284d4-110">Otherwise, the text is just measured.</span></span>

</dd> <dt>

<span data-ttu-id="284d4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="284d4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="284d4-112">Uma estrutura [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) que contém informações sobre o dispositivo de saída ou **NULL** para liberar informações armazenadas em cache pelo controle.</span><span class="sxs-lookup"><span data-stu-id="284d4-112">A [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure containing information about the output device, or **NULL** to free information cached by the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="284d4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="284d4-113">Return value</span></span>

<span data-ttu-id="284d4-114">Essa mensagem retorna o índice do último caractere que se ajusta à região, mais 1.</span><span class="sxs-lookup"><span data-stu-id="284d4-114">This message returns the index of the last character that fits in the region, plus 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="284d4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="284d4-115">Remarks</span></span>

<span data-ttu-id="284d4-116">Essa mensagem é normalmente usada para formatar o conteúdo do controle de edição rico para um dispositivo de saída, como uma impressora.</span><span class="sxs-lookup"><span data-stu-id="284d4-116">This message is typically used to format the content of rich edit control for an output device such as a printer.</span></span>

<span data-ttu-id="284d4-117">Depois de usar essa mensagem para formatar um intervalo de texto, é importante que você libere informações armazenadas em cache enviando **em \_ FORMATRANGE** novamente, mas com *lParam* definido como **NULL**; caso contrário, ocorrerá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="284d4-117">After using this message to format a range of text, it is important that you free cached information by sending **EM\_FORMATRANGE** again, but with *lParam* set to **NULL**; otherwise, a memory leak will occur.</span></span> <span data-ttu-id="284d4-118">Além disso, depois de usar essa mensagem para um dispositivo, você deve liberar as informações em cache antes de usá-las novamente para um dispositivo diferente.</span><span class="sxs-lookup"><span data-stu-id="284d4-118">Also, after using this message for one device, you must free cached information before using it again for a different device.</span></span>

## <a name="requirements"></a><span data-ttu-id="284d4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="284d4-119">Requirements</span></span>



| <span data-ttu-id="284d4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="284d4-120">Requirement</span></span> | <span data-ttu-id="284d4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="284d4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="284d4-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="284d4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="284d4-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="284d4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="284d4-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="284d4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="284d4-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="284d4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="284d4-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="284d4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="284d4-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="284d4-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="284d4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="284d4-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="284d4-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="284d4-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="284d4-130">**em \_ DISPLAYBAND**</span><span class="sxs-lookup"><span data-stu-id="284d4-130">**EM\_DISPLAYBAND**</span></span>](em-displayband.md)
</dt> <dt>

<span data-ttu-id="284d4-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="284d4-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="284d4-132">Imprimindo controles de edição avançada</span><span class="sxs-lookup"><span data-stu-id="284d4-132">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

 





