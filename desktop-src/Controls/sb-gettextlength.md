---
title: Mensagem de SB_GETTEXTLENGTH (commctrl. h)
description: Recupera o comprimento, em caracteres, do texto da parte especificada de uma janela de status.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- Controles de SB_GETTEXTLENGTH de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b08dd3b870c3c59e5aafbeb9d53baef3816a726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918869"
---
# <a name="sb_gettextlength-message"></a><span data-ttu-id="dc246-104">\_Mensagem de GETTEXTLENGTH SB</span><span class="sxs-lookup"><span data-stu-id="dc246-104">SB\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="dc246-105">Recupera o comprimento, em caracteres, do texto da parte especificada de uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="dc246-105">Retrieves the length, in characters, of the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc246-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc246-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc246-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc246-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc246-108">Índice de base zero da parte da qual recuperar o texto.</span><span class="sxs-lookup"><span data-stu-id="dc246-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="dc246-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc246-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dc246-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dc246-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc246-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc246-111">Return value</span></span>

<span data-ttu-id="dc246-112">Retorna um valor de 32 bits que consiste em valores de 2 16 bits.</span><span class="sxs-lookup"><span data-stu-id="dc246-112">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="dc246-113">A palavra inferior Especifica o comprimento, em caracteres, do texto.</span><span class="sxs-lookup"><span data-stu-id="dc246-113">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="dc246-114">A palavra alta especifica o tipo de operação usado para desenhar o texto.</span><span class="sxs-lookup"><span data-stu-id="dc246-114">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="dc246-115">O tipo pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="dc246-115">The type can be one of the following values:</span></span>



| <span data-ttu-id="dc246-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dc246-116">Return code</span></span>                                                                                    | <span data-ttu-id="dc246-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc246-117">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc246-118"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="dc246-118"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="dc246-119">O texto é desenhado com uma borda para aparecer menor do que o plano da janela.</span><span class="sxs-lookup"><span data-stu-id="dc246-119">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>          |
| <dl> <span data-ttu-id="dc246-120"><dt>**SBT \_ NObordas**</dt></span><span class="sxs-lookup"><span data-stu-id="dc246-120"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="dc246-121">O texto é desenhado sem bordas.</span><span class="sxs-lookup"><span data-stu-id="dc246-121">The text is drawn without borders.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="dc246-122"><dt>**SBT \_ OWNERDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="dc246-122"><dt>**SBT\_OWNERDRAW**</dt></span></span> </dl>  | <span data-ttu-id="dc246-123">O texto é desenhado pela janela pai.</span><span class="sxs-lookup"><span data-stu-id="dc246-123">The text is drawn by the parent window.</span></span><br/>                                                |
| <dl> <span data-ttu-id="dc246-124"><dt>**SBT \_ POPOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="dc246-124"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="dc246-125">O texto é desenhado com uma borda para aparecer maior do que o plano da janela.</span><span class="sxs-lookup"><span data-stu-id="dc246-125">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/>         |
| <dl> <span data-ttu-id="dc246-126"><dt>**SBT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="dc246-126"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="dc246-127">O texto será exibido na direção oposta ao texto na janela pai.</span><span class="sxs-lookup"><span data-stu-id="dc246-127">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc246-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc246-128">Remarks</span></span>

<span data-ttu-id="dc246-129">Texto de exibição normal do Windows da esquerda para a direita (EPD).</span><span class="sxs-lookup"><span data-stu-id="dc246-129">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="dc246-130">O Windows pode ser *espelhado* para exibir idiomas como hebraico ou árabe que são lidos da direita para a esquerda (RTL).</span><span class="sxs-lookup"><span data-stu-id="dc246-130">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="dc246-131">Se SBT \_ RTLREADING for definido, o texto da janela de status especificado lerá na direção oposta do texto na janela pai.</span><span class="sxs-lookup"><span data-stu-id="dc246-131">If SBT\_RTLREADING is set, the specified status window text will read in the opposite direction from the text in the parent window.</span></span>

<span data-ttu-id="dc246-132">Esta mensagem retorna um tamanho máximo de cadeia de caracteres de 65.535 caracteres.</span><span class="sxs-lookup"><span data-stu-id="dc246-132">This message returns a maximum string length of 65,535 characters.</span></span> <span data-ttu-id="dc246-133">Se a cadeia de caracteres de texto real for maior que isso, a mensagem [**SB \_ gettext**](sb-gettext.md) truncará.</span><span class="sxs-lookup"><span data-stu-id="dc246-133">If the actual text string is longer than that, the [**SB\_GETTEXT**](sb-gettext.md) message truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc246-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc246-134">Requirements</span></span>



| <span data-ttu-id="dc246-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc246-135">Requirement</span></span> | <span data-ttu-id="dc246-136">Valor</span><span class="sxs-lookup"><span data-stu-id="dc246-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc246-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc246-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dc246-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc246-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc246-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc246-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dc246-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dc246-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc246-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc246-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc246-142"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc246-142"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="dc246-143">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="dc246-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dc246-144">**SB \_ GETTEXTLENGTHW** (Unicode) e **SB \_ GETTEXTLENGTHA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="dc246-144">**SB\_GETTEXTLENGTHW** (Unicode) and **SB\_GETTEXTLENGTHA** (ANSI)</span></span><br/>         |



 

 





