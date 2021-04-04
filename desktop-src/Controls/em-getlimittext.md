---
title: Mensagem de EM_GETLIMITTEXT (WinUser. h)
description: Obtém o limite de texto atual para um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- Controles de EM_GETLIMITTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53da76f43716fd7934011a96d449ffa37c254cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824202"
---
# <a name="em_getlimittext-message"></a><span data-ttu-id="1550d-105">\_Mensagem em GETLIMITTEXT</span><span class="sxs-lookup"><span data-stu-id="1550d-105">EM\_GETLIMITTEXT message</span></span>

<span data-ttu-id="1550d-106">Obtém o limite de texto atual para um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="1550d-106">Gets the current text limit for an edit control.</span></span> <span data-ttu-id="1550d-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="1550d-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1550d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1550d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1550d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1550d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1550d-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1550d-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1550d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1550d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1550d-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1550d-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1550d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1550d-113">Return value</span></span>

<span data-ttu-id="1550d-114">O valor de retorno é o limite de texto.</span><span class="sxs-lookup"><span data-stu-id="1550d-114">The return value is the text limit.</span></span>

## <a name="remarks"></a><span data-ttu-id="1550d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1550d-115">Remarks</span></span>

<span data-ttu-id="1550d-116">**Edite controles, edição avançada 2,0 e posterior:** O limite de texto é a quantidade máxima de texto, em **TCHAR** s, que o controle pode conter.</span><span class="sxs-lookup"><span data-stu-id="1550d-116">**Edit controls, Rich Edit 2.0 and later:** The text limit is the maximum amount of text, in **TCHAR** s, that the control can contain.</span></span> <span data-ttu-id="1550d-117">Para texto ANSI, este é o número de bytes; para texto Unicode, este é o número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1550d-117">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="1550d-118">Dois documentos com o mesmo limite de caracteres resultarão no mesmo limite de texto, mesmo se um for ANSI e o outro for Unicode.</span><span class="sxs-lookup"><span data-stu-id="1550d-118">Two documents with the same character limit will yield the same text limit, even if one is ANSI and the other is Unicode.</span></span>

<span data-ttu-id="1550d-119">**Edição avançada 1,0:** O limite de texto é a quantidade máxima de texto, em bytes, que o controle de edição rico pode conter.</span><span class="sxs-lookup"><span data-stu-id="1550d-119">**Rich Edit 1.0:** The text limit is the maximum amount of text, in bytes, that the rich edit control can contain.</span></span>

<span data-ttu-id="1550d-120">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="1550d-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="1550d-121">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="1550d-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1550d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1550d-122">Requirements</span></span>



| <span data-ttu-id="1550d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1550d-123">Requirement</span></span> | <span data-ttu-id="1550d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1550d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1550d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1550d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1550d-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1550d-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1550d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1550d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1550d-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1550d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1550d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1550d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1550d-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1550d-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1550d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1550d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1550d-132">**em \_ SETLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="1550d-132">**EM\_SETLIMITTEXT**</span></span>](em-setlimittext.md)
</dt> </dl>

 

 





