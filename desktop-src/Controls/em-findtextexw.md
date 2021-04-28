---
title: Mensagem de EM_FINDTEXTEXW (RichEdit. h)
description: Mensagem de EM_FINDTEXTEXW-localiza o texto Unicode dentro de um controle de edição rico.
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- Controles de EM_FINDTEXTEXW de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5278726ca4d3e4748e96d8095a411bcebd5637ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109804"
---
# <a name="em_findtextexw-message"></a><span data-ttu-id="3c7d0-104">\_Mensagem em FINDTEXTEXW</span><span class="sxs-lookup"><span data-stu-id="3c7d0-104">EM\_FINDTEXTEXW message</span></span>

<span data-ttu-id="3c7d0-105">Localiza o texto Unicode dentro de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c7d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c7d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c7d0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c7d0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c7d0-108">Especifica o comportamento da operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="3c7d0-109">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="3c7d0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3c7d0-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="3c7d0-111">Significado</span><span class="sxs-lookup"><span data-stu-id="3c7d0-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="3c7d0-112"><dt>**FR \_ para baixo**</dt></span><span class="sxs-lookup"><span data-stu-id="3c7d0-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="3c7d0-113">Microsoft rich edit 2,0 e posterior: se definido, a pesquisa será encaminhada de **FINDTEXTEX. chrg. cpMin**; Se não estiver definido, a pesquisa será regressiva de **FINDTEXTEX. chrg. cpMin**.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="3c7d0-114">Microsoft Rich Edit 1,0: o \_ sinalizador fr down é ignorado.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="3c7d0-115">A pesquisa está sempre em frente.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="3c7d0-116"><dt>**\_MATCHALEFHAMZA fr**</dt></span><span class="sxs-lookup"><span data-stu-id="3c7d0-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="3c7d0-117">Se definido, a pesquisa é diferenciada entre os Alef com acentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-117">If set, the search differentiates between alefs with different accents.</span></span> <span data-ttu-id="3c7d0-118">Se não for definido, os Alef Arábico e Hebraico com acentos diferentes serão todos correspondidos pelo caractere Alef.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-118">If not set, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="3c7d0-119"><dt>**\_MATCHCASE fr**</dt></span><span class="sxs-lookup"><span data-stu-id="3c7d0-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="3c7d0-120">Se definido, a operação de pesquisa diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="3c7d0-121">Se não for definido, a operação de pesquisa não diferenciará maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-121">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="3c7d0-122"><dt>**\_MATCHDIAC fr**</dt></span><span class="sxs-lookup"><span data-stu-id="3c7d0-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="3c7d0-123">Se definido, a operação de pesquisa considerará as marcas de sinais diacríticos.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-123">If set, the search operation considers diacritical marks.</span></span> <span data-ttu-id="3c7d0-124">Se não estiver definido, as marcas de diacríticos árabe e Hebraico serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-124">If not set, Arabic and Hebrew diacritical marks are ignored.</span></span> <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="3c7d0-125"><dt>**\_MATCHKASHIDA fr**</dt></span><span class="sxs-lookup"><span data-stu-id="3c7d0-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="3c7d0-126">Se definido, a operação de pesquisa considerará kashidas.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-126">If set, the search operation considers kashidas.</span></span> <span data-ttu-id="3c7d0-127">Se não for definido, os kashidas árabe e Hebraico serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-127">If not set, Arabic and Hebrew kashidas are ignored.</span></span> <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="3c7d0-128"><dt>**\_WHOLEWORD fr**</dt></span><span class="sxs-lookup"><span data-stu-id="3c7d0-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="3c7d0-129">Se definido, a operação pesquisa apenas palavras inteiras que correspondam à cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="3c7d0-130">Se não for definido, a operação também pesquisará fragmentos de palavras que correspondam à cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="3c7d0-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c7d0-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c7d0-132">Uma estrutura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) que contém informações sobre a operação Find.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-132">A [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c7d0-133">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3c7d0-133">Return value</span></span>

<span data-ttu-id="3c7d0-134">Se a cadeia de caracteres de destino for encontrada, o valor de retorno será a posição baseada em zero do primeiro caractere da correspondência.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="3c7d0-135">Se o destino não for encontrado, o valor de retorno será-1.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c7d0-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c7d0-136">Remarks</span></span>

<span data-ttu-id="3c7d0-137">Use esta mensagem para localizar cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-137">Use this message to find Unicode strings.</span></span> <span data-ttu-id="3c7d0-138">Para ANSI;, use [**em \_ FINDTEXTEX**](em-findtextex.md).</span><span class="sxs-lookup"><span data-stu-id="3c7d0-138">For ANSI;, use [**EM\_FINDTEXTEX**](em-findtextex.md).</span></span>

<span data-ttu-id="3c7d0-139">O membro **cpMin** de **FINDTEXTEX. chrg** sempre especifica o ponto de partida da pesquisa e **cpMax** especifica o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="3c7d0-140">Ao pesquisar em retrocesso, **cpMin** deve ser igual ou maior que **cpMax**.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="3c7d0-141">Ao pesquisar em frente, um valor de-1 em **cpMax** estende o intervalo de pesquisa até o final do texto.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="3c7d0-142">Se a operação de pesquisa encontrar uma correspondência, o membro **chrgText** da estrutura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) retornará o intervalo de posições de caracteres que contém o texto correspondente.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

<span data-ttu-id="3c7d0-143">**Em \_ FINDTEXTEXW** usa a estrutura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , enquanto [**em \_ FINDTEXTW**](em-findtextw.md) usa a estrutura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) .</span><span class="sxs-lookup"><span data-stu-id="3c7d0-143">**EM\_FINDTEXTEXW** uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, while [**EM\_FINDTEXTW**](em-findtextw.md) uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure.</span></span> <span data-ttu-id="3c7d0-144">A diferença é que **em \_ FINDTEXTEXW** relata o intervalo de texto que foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-144">The difference is that **EM\_FINDTEXTEXW** reports the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c7d0-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c7d0-145">Requirements</span></span>



| <span data-ttu-id="3c7d0-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c7d0-146">Requirement</span></span> | <span data-ttu-id="3c7d0-147">Valor</span><span class="sxs-lookup"><span data-stu-id="3c7d0-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c7d0-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c7d0-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3c7d0-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c7d0-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c7d0-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c7d0-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3c7d0-151">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3c7d0-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c7d0-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c7d0-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c7d0-153"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c7d0-153"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c7d0-154">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3c7d0-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c7d0-155">**em \_ FINDTEXTW**</span><span class="sxs-lookup"><span data-stu-id="3c7d0-155">**EM\_FINDTEXTW**</span></span>](em-findtextw.md)
</dt> </dl>

 

 





