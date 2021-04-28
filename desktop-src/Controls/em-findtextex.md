---
title: Mensagem de EM_FINDTEXTEX (RichEdit. h)
description: Mensagem de EM_FINDTEXTEX-localiza o texto em um controle de edição rico.
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- Controles de EM_FINDTEXTEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2158dabf9ea17d1bd4cac48454bdbb4056765752
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109834"
---
# <a name="em_findtextex-message"></a><span data-ttu-id="6524a-104">\_Mensagem em FINDTEXTEX</span><span class="sxs-lookup"><span data-stu-id="6524a-104">EM\_FINDTEXTEX message</span></span>

<span data-ttu-id="6524a-105">Localiza texto em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="6524a-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6524a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6524a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6524a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6524a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6524a-108">Especifica o comportamento da operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6524a-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="6524a-109">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6524a-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="6524a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6524a-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="6524a-111">Significado</span><span class="sxs-lookup"><span data-stu-id="6524a-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="6524a-112"><dt>**FR \_ para baixo**</dt></span><span class="sxs-lookup"><span data-stu-id="6524a-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="6524a-113">Microsoft rich edit 2,0 e posterior: se definido, a pesquisa será encaminhada de **FINDTEXTEX. chrg. cpMin**; Se não estiver definido, a pesquisa será regressiva de **FINDTEXTEX. chrg. cpMin**.</span><span class="sxs-lookup"><span data-stu-id="6524a-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="6524a-114">Microsoft Rich Edit 1,0: o \_ sinalizador fr down é ignorado.</span><span class="sxs-lookup"><span data-stu-id="6524a-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="6524a-115">A pesquisa está sempre em frente.</span><span class="sxs-lookup"><span data-stu-id="6524a-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="6524a-116"><dt>**\_MATCHALEFHAMZA fr**</dt></span><span class="sxs-lookup"><span data-stu-id="6524a-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="6524a-117">Microsoft Rich Edit 3,0 e posterior: se definido, a pesquisa diferencia entre os Alef árabe e Hebraico com acentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="6524a-117">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic and Hebrew alefs with different accents.</span></span> <span data-ttu-id="6524a-118">Se não estiver definido, todos os Alef serão correspondidos apenas pelo Alef caractere.</span><span class="sxs-lookup"><span data-stu-id="6524a-118">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="6524a-119"><dt>**\_MATCHCASE fr**</dt></span><span class="sxs-lookup"><span data-stu-id="6524a-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="6524a-120">Se definido, a operação de pesquisa diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6524a-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="6524a-121">Se não for definido, a operação de pesquisa não diferenciará maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6524a-121">If not set, the search operation is case-insensitive.</span></span> <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="6524a-122"><dt>**\_MATCHDIAC fr**</dt></span><span class="sxs-lookup"><span data-stu-id="6524a-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="6524a-123">Microsoft Rich Edit 3,0 e posterior: se definido, a operação de pesquisa considerará as marcas de diacríticos árabe e Hebraico.</span><span class="sxs-lookup"><span data-stu-id="6524a-123">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="6524a-124">Se não estiver definido, as marcas de diacríticos serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="6524a-124">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="6524a-125"><dt>**\_MATCHKASHIDA fr**</dt></span><span class="sxs-lookup"><span data-stu-id="6524a-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="6524a-126">Microsoft Rich Edit 3,0 e posterior: se definido, a operação de pesquisa considerará os kashidas árabe e Hebraico.</span><span class="sxs-lookup"><span data-stu-id="6524a-126">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew kashidas.</span></span> <span data-ttu-id="6524a-127">Se não estiver definido, os kashidas serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="6524a-127">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="6524a-128"><dt>**\_WHOLEWORD fr**</dt></span><span class="sxs-lookup"><span data-stu-id="6524a-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="6524a-129">Se definido, a operação pesquisa apenas palavras inteiras que correspondam à cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6524a-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="6524a-130">Se não for definido, a operação também pesquisará fragmentos de palavras que correspondam à cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6524a-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="6524a-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6524a-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6524a-132">Uma estrutura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) que contém informações sobre a operação Find.</span><span class="sxs-lookup"><span data-stu-id="6524a-132">A [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6524a-133">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6524a-133">Return value</span></span>

<span data-ttu-id="6524a-134">Se a cadeia de caracteres de destino for encontrada, o valor de retorno será a posição baseada em zero do primeiro caractere da correspondência.</span><span class="sxs-lookup"><span data-stu-id="6524a-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="6524a-135">Se o destino não for encontrado, o valor de retorno será-1.</span><span class="sxs-lookup"><span data-stu-id="6524a-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="6524a-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="6524a-136">Remarks</span></span>

<span data-ttu-id="6524a-137">Use esta mensagem para localizar cadeias de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="6524a-137">Use this message to find ANSI strings.</span></span> <span data-ttu-id="6524a-138">Para Unicode, use [**em \_ FINDTEXTEXW**](em-findtextexw.md).</span><span class="sxs-lookup"><span data-stu-id="6524a-138">For Unicode, use [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span>

<span data-ttu-id="6524a-139">O membro **cpMin** de **FINDTEXTEX. chrg** sempre especifica o ponto de partida da pesquisa e **cpMax** especifica o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="6524a-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="6524a-140">Ao pesquisar em retrocesso, **cpMin** deve ser igual ou maior que **cpMax**.</span><span class="sxs-lookup"><span data-stu-id="6524a-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="6524a-141">Ao pesquisar em frente, um valor de-1 em **cpMax** estende o intervalo de pesquisa até o final do texto.</span><span class="sxs-lookup"><span data-stu-id="6524a-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="6524a-142">Se a operação de pesquisa encontrar uma correspondência, o membro **chrgText** da estrutura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) retornará o intervalo de posições de caracteres que contém o texto correspondente.</span><span class="sxs-lookup"><span data-stu-id="6524a-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

## <a name="requirements"></a><span data-ttu-id="6524a-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6524a-143">Requirements</span></span>



| <span data-ttu-id="6524a-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="6524a-144">Requirement</span></span> | <span data-ttu-id="6524a-145">Valor</span><span class="sxs-lookup"><span data-stu-id="6524a-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6524a-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6524a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6524a-147">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6524a-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6524a-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6524a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6524a-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6524a-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6524a-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6524a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="6524a-151"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6524a-151"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6524a-152">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6524a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6524a-153">**em \_ LocalizarTexto**</span><span class="sxs-lookup"><span data-stu-id="6524a-153">**EM\_FINDTEXT**</span></span>](em-findtext.md)
</dt> </dl>

 

 





