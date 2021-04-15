---
title: Mensagem de EM_GETENDOFLINE (commctrl. h)
description: Recupera o caractere de fim de linha usado quando um LineBreak é inserido. Envie essa mensagem explicitamente ou usando a macro Edit \_ GetEndOfLine.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Controles de EM_GETENDOFLINE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 98d537d2ea4239ab3f511666aeba46be93a2b881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454765"
---
# <a name="em_getendofline-message"></a><span data-ttu-id="ccd27-105">\_Mensagem em GETENDOFLINE</span><span class="sxs-lookup"><span data-stu-id="ccd27-105">EM\_GETENDOFLINE message</span></span>

<span data-ttu-id="ccd27-106">Recupera o caractere de fim de linha para um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="ccd27-106">Retrieves the end-of-line character for an edit control.</span></span> <span data-ttu-id="ccd27-107">Envie essa mensagem explicitamente ou usando a macro [**Edit \_ GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) .</span><span class="sxs-lookup"><span data-stu-id="ccd27-107">Send this message explicitly or by using the [**Edit\_GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccd27-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccd27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd27-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccd27-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ccd27-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ccd27-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ccd27-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccd27-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ccd27-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ccd27-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd27-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccd27-113">Return value</span></span>

<span data-ttu-id="ccd27-114">Retorna o caractere de fim de linha usado pelo controle de edição.</span><span class="sxs-lookup"><span data-stu-id="ccd27-114">Returns the end-of-line character used by the edit control.</span></span> <span data-ttu-id="ccd27-115">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccd27-115">This can be one of the following values.</span></span>

| <span data-ttu-id="ccd27-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ccd27-116">Value</span></span>                                                                                                                                                   | <span data-ttu-id="ccd27-117">Significado</span><span class="sxs-lookup"><span data-stu-id="ccd27-117">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="ccd27-118"><dt>**ENDOFLINE da EC \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd27-118"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl> | <span data-ttu-id="ccd27-119">O caractere de final de linha usado para o novo quebras é o retorno de carro seguido por linha de alimentação (CRLF).</span><span class="sxs-lookup"><span data-stu-id="ccd27-119">The end-of-line character used for new linebreaks is carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="ccd27-120"><dt>**EC \_ ENDOFLINE \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd27-120"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>       | <span data-ttu-id="ccd27-121">O caractere de final de linha usado para New quebras é retorno de carro (CR).</span><span class="sxs-lookup"><span data-stu-id="ccd27-121">The end-of-line character used for new linebreaks is carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="ccd27-122"><dt>**EC \_ ENDOFLINE \_ LF**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd27-122"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>       | <span data-ttu-id="ccd27-123">O caractere de fim de linha usado para o novo quebras é o LF (alimentação de linhas).</span><span class="sxs-lookup"><span data-stu-id="ccd27-123">The end-of-line character used for new linebreaks is linefeed (LF).</span></span><br/>                               |

## <a name="remarks"></a><span data-ttu-id="ccd27-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccd27-124">Remarks</span></span>

<span data-ttu-id="ccd27-125">Quando o caractere de final de linha usado é definido como **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** usando [**Editar \_ SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), essa mensagem retornará o caractere de fim de linha detectado.</span><span class="sxs-lookup"><span data-stu-id="ccd27-125">When the end-of-line character used is set to **EC\_ENDOFLINE\_DETECTFROMCONTENT** using [**Edit\_SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), this message will return the detected end-of-line character.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd27-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccd27-126">Requirements</span></span>



| <span data-ttu-id="ccd27-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccd27-127">Requirement</span></span> | <span data-ttu-id="ccd27-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ccd27-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd27-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccd27-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd27-130">\[Somente aplicativos da área de trabalho do Windows 10, versão 1809\]</span><span class="sxs-lookup"><span data-stu-id="ccd27-130">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ccd27-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccd27-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd27-132">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="ccd27-132">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ccd27-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ccd27-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccd27-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccd27-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccd27-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccd27-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd27-136">\**em \_ SETENDOFLINE*</span><span class="sxs-lookup"><span data-stu-id="ccd27-136">\**EM\_SETENDOFLINE*</span></span>](em-setendofline.md)
</dt> </dl>
 

 





