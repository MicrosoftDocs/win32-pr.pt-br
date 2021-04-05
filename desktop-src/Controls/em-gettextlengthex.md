---
title: Mensagem de EM_GETTEXTLENGTHEX (RichEdit. h)
description: Calcula o comprimento do texto de várias maneiras. Ele é geralmente chamado antes de criar um buffer para receber o texto do controle.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- Controles de EM_GETTEXTLENGTHEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824362"
---
# <a name="em_gettextlengthex-message"></a><span data-ttu-id="37110-105">\_Mensagem em GETTEXTLENGTHEX</span><span class="sxs-lookup"><span data-stu-id="37110-105">EM\_GETTEXTLENGTHEX message</span></span>

<span data-ttu-id="37110-106">Calcula o comprimento do texto de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="37110-106">Calculates text length in various ways.</span></span> <span data-ttu-id="37110-107">Ele é geralmente chamado antes de criar um buffer para receber o texto do controle.</span><span class="sxs-lookup"><span data-stu-id="37110-107">It is usually called before creating a buffer to receive the text from the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="37110-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37110-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37110-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37110-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37110-110">Ponteiro para uma estrutura [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) que recebe as informações de comprimento do texto.</span><span class="sxs-lookup"><span data-stu-id="37110-110">Pointer to a [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure that receives the text length information.</span></span>

</dd> <dt>

<span data-ttu-id="37110-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37110-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37110-112">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="37110-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37110-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37110-113">Return value</span></span>

<span data-ttu-id="37110-114">A mensagem retorna o número de **TCHAR** s no controle de edição, dependendo da configuração dos sinalizadores na estrutura [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) .</span><span class="sxs-lookup"><span data-stu-id="37110-114">The message returns the number of **TCHAR** s in the edit control, depending on the setting of the flags in the [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure.</span></span> <span data-ttu-id="37110-115">Se sinalizadores incompatíveis tiverem sido definidos no membro **flags** , a mensagem retornará E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="37110-115">If incompatible flags were set in the **flags** member, the message returns E\_INVALIDARG .</span></span>

## <a name="remarks"></a><span data-ttu-id="37110-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="37110-116">Remarks</span></span>

<span data-ttu-id="37110-117">Essa mensagem é uma maneira rápida e fácil de determinar o número de caracteres na versão Unicode do controle rich edit.</span><span class="sxs-lookup"><span data-stu-id="37110-117">This message is a fast and easy way to determine the number of characters in the Unicode version of the rich edit control.</span></span> <span data-ttu-id="37110-118">No entanto, para uma página de código de destino não-Unicode, você poderá converter potencialmente em uma combinação de caracteres de byte único e de byte duplo.</span><span class="sxs-lookup"><span data-stu-id="37110-118">However, for a non-Unicode target code page you will potentially be converting to a combination of single-byte and double-byte characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="37110-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37110-119">Requirements</span></span>



| <span data-ttu-id="37110-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="37110-120">Requirement</span></span> | <span data-ttu-id="37110-121">Valor</span><span class="sxs-lookup"><span data-stu-id="37110-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37110-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37110-122">Minimum supported client</span></span><br/> | <span data-ttu-id="37110-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37110-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37110-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37110-124">Minimum supported server</span></span><br/> | <span data-ttu-id="37110-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="37110-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37110-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37110-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="37110-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="37110-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37110-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="37110-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37110-129">**GETTEXTLENGTHEX**</span><span class="sxs-lookup"><span data-stu-id="37110-129">**GETTEXTLENGTHEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





