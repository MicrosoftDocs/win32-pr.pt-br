---
title: Mensagem de EM_FINDTEXTW (RichEdit. h)
description: Localiza o texto Unicode dentro de um controle de edição rico.
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- Controles de EM_FINDTEXTW de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bae60269ab3ddb84a17c285c243e00d8117c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644981"
---
# <a name="em_findtextw-message"></a><span data-ttu-id="e1d3d-104">\_Mensagem em FINDTEXTW</span><span class="sxs-lookup"><span data-stu-id="e1d3d-104">EM\_FINDTEXTW message</span></span>

<span data-ttu-id="e1d3d-105">Localiza o texto Unicode dentro de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1d3d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1d3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1d3d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1d3d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1d3d-108">Especifica os parâmetros da operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-108">Specifies the parameters of the search operation.</span></span> <span data-ttu-id="e1d3d-109">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="e1d3d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e1d3d-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="e1d3d-111">Significado</span><span class="sxs-lookup"><span data-stu-id="e1d3d-111">Meaning</span></span>                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="e1d3d-112"><dt>**FR \_ para baixo**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d3d-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="e1d3d-113">Se definido, a operação pesquisa do final da seleção atual até o final do documento.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-113">If set, the operation searches from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="e1d3d-114">Se não estiver definido, a operação pesquisa do final da seleção atual para o início do documento.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-114">If not set, the operation searches from the end of the current selection to the beginning of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="e1d3d-115"><dt>**\_MATCHALEFHAMZA fr**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d3d-115"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="e1d3d-116">Por padrão, os Alef Arábico e Hebraico com acentos diferentes são todos correspondidos pelo caractere Alef.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-116">By default, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <span data-ttu-id="e1d3d-117">Defina esse sinalizador se desejar que a pesquisa Diferencie entre os Alef com sotaques diferentes.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-117">Set this flag if you want the search to differentiate between alefs with different accents.</span></span><br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="e1d3d-118"><dt>**\_MATCHCASE fr**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d3d-118"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="e1d3d-119">Se definido, a operação de pesquisa diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-119">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="e1d3d-120">Se não for definido, a operação de pesquisa não diferenciará maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-120">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="e1d3d-121"><dt>**\_MATCHDIAC fr**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d3d-121"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="e1d3d-122">Por padrão, as marcas de diacríticos árabe e Hebraico são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-122">By default, Arabic and Hebrew diacritical marks are ignored.</span></span> <span data-ttu-id="e1d3d-123">Defina esse sinalizador se desejar que a operação de pesquisa considere as marcas de sinais diacríticos.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-123">Set this flag if you want the search operation to consider diacritical marks.</span></span><br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="e1d3d-124"><dt>**\_MATCHKASHIDA fr**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d3d-124"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="e1d3d-125">Por padrão, os kashidas árabe e Hebraico são ignorados.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-125">By default, Arabic and Hebrew kashidas are ignored.</span></span> <span data-ttu-id="e1d3d-126">Defina esse sinalizador se desejar que a operação de pesquisa considere os kashidas.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-126">Set this flag if you want the search operation to consider kashidas.</span></span><br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="e1d3d-127"><dt>**\_WHOLEWORD fr**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d3d-127"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="e1d3d-128">Se definido, a operação pesquisa apenas palavras inteiras que correspondam à cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-128">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="e1d3d-129">Se não for definido, a operação também pesquisará fragmentos de palavras que correspondam à cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-129">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                  |



 

</dd> <dt>

<span data-ttu-id="e1d3d-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1d3d-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1d3d-131">Uma estrutura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) que contém informações sobre a operação Find.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-131">A [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1d3d-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1d3d-132">Return value</span></span>

<span data-ttu-id="e1d3d-133">Se a cadeia de caracteres de destino for encontrada, o valor de retorno será a posição baseada em zero do primeiro caractere da correspondência.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-133">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="e1d3d-134">Se o destino não for encontrado, o valor de retorno será-1.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-134">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d3d-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1d3d-135">Remarks</span></span>

<span data-ttu-id="e1d3d-136">**Em \_ FINDTEXTW** usa a estrutura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) , enquanto [**em \_ FINDTEXTEXW**](em-findtextexw.md) usa a estrutura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) .</span><span class="sxs-lookup"><span data-stu-id="e1d3d-136">**EM\_FINDTEXTW** uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure, while [**EM\_FINDTEXTEXW**](em-findtextexw.md) uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure.</span></span> <span data-ttu-id="e1d3d-137">A diferença é que o **FINDTEXTEXW** relata o intervalo de texto que foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="e1d3d-137">The difference is that **FINDTEXTEXW** reports back the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d3d-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1d3d-138">Requirements</span></span>



| <span data-ttu-id="e1d3d-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1d3d-139">Requirement</span></span> | <span data-ttu-id="e1d3d-140">Valor</span><span class="sxs-lookup"><span data-stu-id="e1d3d-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d3d-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1d3d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e1d3d-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1d3d-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1d3d-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1d3d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e1d3d-144">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1d3d-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1d3d-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1d3d-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1d3d-146"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1d3d-146"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1d3d-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1d3d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d3d-148">**em \_ FINDTEXTEXW**</span><span class="sxs-lookup"><span data-stu-id="e1d3d-148">**EM\_FINDTEXTEXW**</span></span>](em-findtextexw.md)
</dt> </dl>

 

 





