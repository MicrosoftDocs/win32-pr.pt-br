---
title: Mensagem de EM_LINEINDEX (WinUser. h)
description: Obtém o índice de caracteres do primeiro caractere de uma linha especificada em um controle de edição de várias linhas.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Controles de EM_LINEINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611d4ff892f95287c45166ae55ff2389f454512c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918282"
---
# <a name="em_lineindex-message-winuserh"></a><span data-ttu-id="75662-104">Mensagem de EM_LINEINDEX (WinUser. h)</span><span class="sxs-lookup"><span data-stu-id="75662-104">EM_LINEINDEX message (Winuser.h)</span></span>

<span data-ttu-id="75662-105">Obtém o índice de caracteres do primeiro caractere de uma linha especificada em um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="75662-105">Gets the character index of the first character of a specified line in a multiline edit control.</span></span> <span data-ttu-id="75662-106">Um índice de caracteres é o índice de base zero do caractere do início do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="75662-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="75662-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="75662-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="75662-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75662-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75662-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75662-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75662-110">O número de linha com base em zero.</span><span class="sxs-lookup"><span data-stu-id="75662-110">The zero-based line number.</span></span> <span data-ttu-id="75662-111">Um valor de-1 especifica o número de linha atual (a linha que contém o cursor).</span><span class="sxs-lookup"><span data-stu-id="75662-111">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="75662-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75662-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75662-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="75662-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75662-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75662-114">Return value</span></span>

<span data-ttu-id="75662-115">O valor de retorno é o índice de caracteres da linha especificada no parâmetro *wParam* ou é-1 se o número de linha especificado for maior que o número de linhas no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="75662-115">The return value is the character index of the line specified in the *wParam* parameter, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="75662-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="75662-116">Remarks</span></span>

<span data-ttu-id="75662-117">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="75662-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="75662-118">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="75662-118">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75662-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75662-119">Requirements</span></span>



| <span data-ttu-id="75662-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="75662-120">Requirement</span></span> | <span data-ttu-id="75662-121">Valor</span><span class="sxs-lookup"><span data-stu-id="75662-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75662-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75662-122">Minimum supported client</span></span><br/> | <span data-ttu-id="75662-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75662-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="75662-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75662-124">Minimum supported server</span></span><br/> | <span data-ttu-id="75662-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75662-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="75662-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75662-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="75662-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75662-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75662-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="75662-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75662-129">**em \_ LINEFROMCHAR**</span><span class="sxs-lookup"><span data-stu-id="75662-129">**EM\_LINEFROMCHAR**</span></span>](em-linefromchar.md)
</dt> </dl>

 

 





