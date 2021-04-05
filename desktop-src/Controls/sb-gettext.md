---
title: Mensagem de SB_GETTEXT (commctrl. h)
description: Recupera o texto da parte especificada de uma janela de status.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- Controles de SB_GETTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90b132c3f934188aea36afd86d53ab8f75bdadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009605"
---
# <a name="sb_gettext-message"></a><span data-ttu-id="70376-104">\_Mensagem GETTEXT SB</span><span class="sxs-lookup"><span data-stu-id="70376-104">SB\_GETTEXT message</span></span>

<span data-ttu-id="70376-105">Recupera o texto da parte especificada de uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="70376-105">Retrieves the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="70376-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70376-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70376-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70376-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70376-108">Índice de base zero da parte da qual recuperar o texto.</span><span class="sxs-lookup"><span data-stu-id="70376-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="70376-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70376-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70376-110">Ponteiro para o buffer que recebe o texto como uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="70376-110">Pointer to the buffer that receives the text as a null-terminated string.</span></span> <span data-ttu-id="70376-111">Use a [**mensagem \_ GETTEXTLENGTH do SB**](sb-gettextlength.md) para determinar o tamanho necessário do buffer.</span><span class="sxs-lookup"><span data-stu-id="70376-111">Use the [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message to determine the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70376-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70376-112">Return value</span></span>

<span data-ttu-id="70376-113">Retorna um valor de 32 bits que consiste em valores de 2 16 bits.</span><span class="sxs-lookup"><span data-stu-id="70376-113">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="70376-114">A palavra inferior Especifica o comprimento, em caracteres, do texto.</span><span class="sxs-lookup"><span data-stu-id="70376-114">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="70376-115">A palavra alta especifica o tipo de operação usado para desenhar o texto.</span><span class="sxs-lookup"><span data-stu-id="70376-115">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="70376-116">O tipo pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="70376-116">The type can be one of the following values.</span></span>



| <span data-ttu-id="70376-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="70376-117">Return code</span></span>                                                                                    | <span data-ttu-id="70376-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="70376-118">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="70376-119"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="70376-119"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="70376-120">O texto é desenhado com uma borda para aparecer menor do que o plano da janela.</span><span class="sxs-lookup"><span data-stu-id="70376-120">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>  |
| <dl> <span data-ttu-id="70376-121"><dt>**SBT \_ NObordas**</dt></span><span class="sxs-lookup"><span data-stu-id="70376-121"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="70376-122">O texto é desenhado sem bordas.</span><span class="sxs-lookup"><span data-stu-id="70376-122">The text is drawn without borders.</span></span><br/>                                             |
| <dl> <span data-ttu-id="70376-123"><dt>**SBT \_ POPOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="70376-123"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="70376-124">O texto é desenhado com uma borda para aparecer maior do que o plano da janela.</span><span class="sxs-lookup"><span data-stu-id="70376-124">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/> |
| <dl> <span data-ttu-id="70376-125"><dt>**SBT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="70376-125"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="70376-126">O texto é exibido na direção oposta do texto na janela pai.</span><span class="sxs-lookup"><span data-stu-id="70376-126">The text displays in the opposite direction of the text in the parent window.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="70376-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="70376-127">Remarks</span></span>

<span data-ttu-id="70376-128">**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="70376-128">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="70376-129">Essa mensagem não fornece uma maneira de saber o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="70376-129">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="70376-130">Se você usar essa mensagem, primeiro chame [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obter o número de caracteres necessários e, em seguida, chame a mensagem para recuperar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="70376-130">If you use this message, first call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="70376-131">Se você aguardar antes de chamar **SB \_ gettext** , o texto poderá ser alterado, invalidando o valor de retorno de **SB \_ GETTEXTLENGTH**.</span><span class="sxs-lookup"><span data-stu-id="70376-131">If you wait before calling **SB\_GETTEXT** the text could change, thereby invalidating the return value of **SB\_GETTEXTLENGTH**.</span></span> <span data-ttu-id="70376-132">Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="70376-132">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="70376-133">Essa mensagem retorna um máximo de 65.535 caracteres.</span><span class="sxs-lookup"><span data-stu-id="70376-133">This message returns a maximum of 65,535 characters.</span></span> <span data-ttu-id="70376-134">Se a cadeia de texto for maior que isso, ela será truncada.</span><span class="sxs-lookup"><span data-stu-id="70376-134">If the text string is longer than that, it is truncated.</span></span>

<span data-ttu-id="70376-135">Se o texto tiver o \_ tipo de desenho SBT OWNERDRAW, essa mensagem retornará o valor de 32 bits associado ao texto em vez do comprimento e do tipo de operação.</span><span class="sxs-lookup"><span data-stu-id="70376-135">If the text has the SBT\_OWNERDRAW drawing type, this message returns the 32-bit value associated with the text instead of the length and operation type.</span></span>

<span data-ttu-id="70376-136">Texto de exibição normal do Windows da esquerda para a direita (EPD).</span><span class="sxs-lookup"><span data-stu-id="70376-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="70376-137">O Windows pode ser *espelhado* para exibir idiomas como hebraico ou árabe que são lidos da direita para a esquerda (RTL).</span><span class="sxs-lookup"><span data-stu-id="70376-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="70376-138">Se SBT \_ RTLREADING for definido, a cadeia de caracteres *lParam* lerá na direção oposta do texto na janela pai.</span><span class="sxs-lookup"><span data-stu-id="70376-138">If SBT\_RTLREADING is set, the *lParam* string reads in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="70376-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70376-139">Requirements</span></span>



| <span data-ttu-id="70376-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="70376-140">Requirement</span></span> | <span data-ttu-id="70376-141">Valor</span><span class="sxs-lookup"><span data-stu-id="70376-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70376-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70376-142">Minimum supported client</span></span><br/> | <span data-ttu-id="70376-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70376-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70376-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70376-144">Minimum supported server</span></span><br/> | <span data-ttu-id="70376-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="70376-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70376-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70376-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="70376-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="70376-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="70376-148">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="70376-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="70376-149">**SB \_ GETTEXTW** (Unicode) e **SB \_ gettexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="70376-149">**SB\_GETTEXTW** (Unicode) and **SB\_GETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="70376-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="70376-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70376-151">**SB \_ SETtext**</span><span class="sxs-lookup"><span data-stu-id="70376-151">**SB\_SETTEXT**</span></span>](sb-settext.md)
</dt> </dl>

 

 





