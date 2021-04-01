---
title: Mensagem de EM_FINDTEXT (RichEdit. h)
description: Localiza texto em um controle de edição rico.
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- Controles de EM_FINDTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e50034337f05d2df17af777986136881c503d05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918625"
---
# <a name="em_findtext-message"></a><span data-ttu-id="3de12-104">\_Mensagem em LocalizarTexto</span><span class="sxs-lookup"><span data-stu-id="3de12-104">EM\_FINDTEXT message</span></span>

<span data-ttu-id="3de12-105">Localiza texto em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="3de12-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3de12-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3de12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de12-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3de12-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3de12-108">Especifique os parâmetros da operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3de12-108">Specify the parameters of the search operation.</span></span> <span data-ttu-id="3de12-109">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3de12-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="3de12-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3de12-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="3de12-111">Significado</span><span class="sxs-lookup"><span data-stu-id="3de12-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="3de12-112"><dt>**FR \_ para baixo**</dt></span><span class="sxs-lookup"><span data-stu-id="3de12-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="3de12-113">Microsoft rich edit 2,0 e posterior: se definido, a pesquisa é do final da seleção atual até o final do documento.</span><span class="sxs-lookup"><span data-stu-id="3de12-113">Microsoft Rich Edit 2.0 and later: If set, the search is from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="3de12-114">Se não estiver definido, a pesquisa será do final da seleção atual até o início do documento.</span><span class="sxs-lookup"><span data-stu-id="3de12-114">If not set, the search is from the end of the current selection to the beginning of the document.</span></span> <br/> <span data-ttu-id="3de12-115">Microsoft Rich Edit 1,0: o \_ sinalizador fr down é ignorado.</span><span class="sxs-lookup"><span data-stu-id="3de12-115">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="3de12-116">A pesquisa é sempre do final da seleção atual até o fim do documento.</span><span class="sxs-lookup"><span data-stu-id="3de12-116">The search is always from the end of the current selection to the end of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="3de12-117"><dt>**\_MATCHALEFHAMZA fr**</dt></span><span class="sxs-lookup"><span data-stu-id="3de12-117"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="3de12-118">Microsoft Rich Edit 3,0 e posterior: se definido, a pesquisa diferencia entre os Alef árabes com acentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="3de12-118">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic alefs with different accents.</span></span> <span data-ttu-id="3de12-119">Se não estiver definido, todos os Alef serão correspondidos apenas pelo Alef caractere.</span><span class="sxs-lookup"><span data-stu-id="3de12-119">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="3de12-120"><dt>**\_MATCHDIAC fr**</dt></span><span class="sxs-lookup"><span data-stu-id="3de12-120"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="3de12-121">Microsoft Rich Edit 3,0 e posterior: se definido, a operação de pesquisa considerará as marcas de diacríticos árabe e Hebraico.</span><span class="sxs-lookup"><span data-stu-id="3de12-121">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="3de12-122">Se não estiver definido, as marcas de diacríticos serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="3de12-122">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="3de12-123"><dt>**\_MATCHKASHIDA fr**</dt></span><span class="sxs-lookup"><span data-stu-id="3de12-123"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="3de12-124">Microsoft Rich Edit 3,0 e posterior: se definido, a operação de pesquisa considerará kashidas árabes.</span><span class="sxs-lookup"><span data-stu-id="3de12-124">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic kashidas.</span></span> <span data-ttu-id="3de12-125">Se não estiver definido, os kashidas serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="3de12-125">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <span data-ttu-id="3de12-126"><dt>**\_MATCHWIDTH fr**</dt></span><span class="sxs-lookup"><span data-stu-id="3de12-126"><dt>**FR\_MATCHWIDTH**</dt></span></span> </dl>             | <span data-ttu-id="3de12-127">Windows 8: se definido, as versões de byte único e de byte duplo do mesmo caractere são consideradas como não iguais.</span><span class="sxs-lookup"><span data-stu-id="3de12-127">Windows 8: If set, single-byte and double-byte versions of the same character are considered to be not equal.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="3de12-128"><dt>**\_WHOLEWORD fr**</dt></span><span class="sxs-lookup"><span data-stu-id="3de12-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="3de12-129">Se definido, a operação pesquisa apenas palavras inteiras que correspondam à cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3de12-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="3de12-130">Se não for definido, a operação também pesquisará fragmentos de palavras que correspondam à cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3de12-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="3de12-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3de12-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3de12-132">Uma estrutura [**LocalizarTexto**](/windows/win32/api/richedit/ns-richedit-findtexta) que contém informações sobre a operação de localização.</span><span class="sxs-lookup"><span data-stu-id="3de12-132">A [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de12-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3de12-133">Return value</span></span>

<span data-ttu-id="3de12-134">Se a cadeia de caracteres de destino for encontrada, o valor de retorno será a posição baseada em zero do primeiro caractere da correspondência.</span><span class="sxs-lookup"><span data-stu-id="3de12-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="3de12-135">Se o destino não for encontrado, o valor de retorno será-1.</span><span class="sxs-lookup"><span data-stu-id="3de12-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="3de12-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="3de12-136">Remarks</span></span>

<span data-ttu-id="3de12-137">O membro **cpMin** de **LocalizarTexto. chrg** sempre especifica o ponto de partida da pesquisa e **cpMax** especifica o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="3de12-137">The **cpMin** member of **FINDTEXT.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="3de12-138">Ao pesquisar em retrocesso, **cpMin** deve ser igual ou maior que **cpMax**.</span><span class="sxs-lookup"><span data-stu-id="3de12-138">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="3de12-139">Ao pesquisar em frente, um valor de-1 em **cpMax** estende o intervalo de pesquisa até o final do texto.</span><span class="sxs-lookup"><span data-stu-id="3de12-139">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="3de12-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3de12-140">Requirements</span></span>



| <span data-ttu-id="3de12-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="3de12-141">Requirement</span></span> | <span data-ttu-id="3de12-142">Valor</span><span class="sxs-lookup"><span data-stu-id="3de12-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3de12-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3de12-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3de12-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3de12-144">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3de12-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3de12-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3de12-146">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3de12-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3de12-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3de12-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="3de12-148"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3de12-148"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de12-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="3de12-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de12-150">**FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="3de12-150">**FINDTEXT**</span></span>](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





