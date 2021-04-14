---
title: Mensagem de EM_FMTLINES (WinUser. h)
description: Define um sinalizador que determina se um controle de edição de várias linhas inclui caracteres de quebra de linha flexível. Uma quebra de linha suave consiste em dois retornos de carro e um feed de linha e é inserido no final de uma linha quebrada por causa de wordwrapping.
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- Controles de EM_FMTLINES de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c12a22ee8c30ffa74705f670a16caa3651e9b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455280"
---
# <a name="em_fmtlines-message"></a><span data-ttu-id="8f68f-105">\_Mensagem em FMTLINES</span><span class="sxs-lookup"><span data-stu-id="8f68f-105">EM\_FMTLINES message</span></span>

<span data-ttu-id="8f68f-106">Define um sinalizador que determina se um controle de edição de várias linhas inclui caracteres de quebra de linha flexível.</span><span class="sxs-lookup"><span data-stu-id="8f68f-106">Sets a flag that determines whether a multiline edit control includes soft line-break characters.</span></span> <span data-ttu-id="8f68f-107">Uma quebra de linha suave consiste em dois retornos de carro e um feed de linha e é inserido no final de uma linha quebrada por causa de wordwrapping.</span><span class="sxs-lookup"><span data-stu-id="8f68f-107">A soft line break consists of two carriage returns and a line feed and is inserted at the end of a line that is broken because of wordwrapping.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f68f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f68f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f68f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f68f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f68f-110">Especifica se os caracteres de quebra de linha flexível devem ser inseridos.</span><span class="sxs-lookup"><span data-stu-id="8f68f-110">Specifies whether soft line-break characters are to be inserted.</span></span> <span data-ttu-id="8f68f-111">Um valor **true** insere os caracteres; um valor **false** remove-os.</span><span class="sxs-lookup"><span data-stu-id="8f68f-111">A value of **TRUE** inserts the characters; a value of **FALSE** removes them.</span></span>

</dd> <dt>

<span data-ttu-id="8f68f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f68f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f68f-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="8f68f-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f68f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f68f-114">Return value</span></span>

<span data-ttu-id="8f68f-115">O valor de retorno é idêntico ao parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="8f68f-115">The return value is identical to the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f68f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f68f-116">Remarks</span></span>

<span data-ttu-id="8f68f-117">Essa mensagem afeta apenas o buffer retornado pela mensagem [**em \_ GetHandle**](em-gethandle.md) e o texto retornado pela mensagem de [**\_ gettext do WM**](/windows/desktop/winmsg/wm-gettext) .</span><span class="sxs-lookup"><span data-stu-id="8f68f-117">This message affects only the buffer returned by the [**EM\_GETHANDLE**](em-gethandle.md) message and the text returned by the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext) message.</span></span> <span data-ttu-id="8f68f-118">Ele não tem nenhum efeito na exibição do texto dentro do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="8f68f-118">It has no effect on the display of the text within the edit control.</span></span>

<span data-ttu-id="8f68f-119">A mensagem em **\_ FMTLINES** não afeta uma linha que termina com uma quebra de linha rígida.</span><span class="sxs-lookup"><span data-stu-id="8f68f-119">The **EM\_FMTLINES** message does not affect a line that ends with a hard line break.</span></span> <span data-ttu-id="8f68f-120">Uma quebra de linha rígida consiste em um retorno de carro e um feed de linha.</span><span class="sxs-lookup"><span data-stu-id="8f68f-120">A hard line break consists of one carriage return and a line feed.</span></span>

> [!Note]  
> <span data-ttu-id="8f68f-121">O tamanho do texto é alterado quando essa mensagem é processada.</span><span class="sxs-lookup"><span data-stu-id="8f68f-121">The size of the text changes when this message is processed.</span></span>

 

<span data-ttu-id="8f68f-122">**Edição avançada:** Não há suporte para a mensagem em **\_ FMTLINES** .</span><span class="sxs-lookup"><span data-stu-id="8f68f-122">**Rich Edit:** The **EM\_FMTLINES** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f68f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f68f-123">Requirements</span></span>



| <span data-ttu-id="8f68f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f68f-124">Requirement</span></span> | <span data-ttu-id="8f68f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8f68f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f68f-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f68f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8f68f-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f68f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8f68f-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f68f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8f68f-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8f68f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8f68f-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f68f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f68f-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f68f-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f68f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f68f-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="8f68f-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="8f68f-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8f68f-134">**em \_ GEThandle**</span><span class="sxs-lookup"><span data-stu-id="8f68f-134">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

<span data-ttu-id="8f68f-135">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="8f68f-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8f68f-136">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="8f68f-136">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

