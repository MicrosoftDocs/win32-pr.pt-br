---
description: Especifica o conjunto de avisos disponíveis que podem ocorrer durante a análise de tinta.
ms.assetid: 52676f1d-8d67-4bdb-9d4f-3e409ffa8332
title: Enumeração AnalysisWarningCode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisWarningCode
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 651408678daa64788952b2706980968ca315abf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749177"
---
# <a name="analysiswarningcode-enumeration"></a><span data-ttu-id="b447b-103">Enumeração AnalysisWarningCode</span><span class="sxs-lookup"><span data-stu-id="b447b-103">AnalysisWarningCode enumeration</span></span>

<span data-ttu-id="b447b-104">Especifica o conjunto de avisos disponíveis que podem ocorrer durante a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="b447b-104">Specifies the set of available warnings that can occur during ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="b447b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b447b-105">Syntax</span></span>


```C++
typedef enum AnalysisWarningCode { 
  AnalysisWarningCode_Aborted                                    = 0,
  AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound       = 1,
  AnalysisWarningCode_FactoidNotSupported                        = 2,
  AnalysisWarningCode_FactoidCoercionNotSupported                = 3,
  AnalysisWarningCode_GuideNotSupported                          = 4,
  AnalysisWarningCode_WordlistNotSupported                       = 5,
  AnalysisWarningCode_WordModeNotSupported                       = 6,
  AnalysisWarningCode_PartialDictionaryTermsNotSupported         = 7,
  AnalysisWarningCode_TextRecognitionProcessFailed               = 8,
  AnalysisWarningCode_AddInkToRecognizerFailed                   = 9,
  AnalysisWarningCode_SetPrefixSuffixFailed                      = 10,
  AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed  = 11,
  AnalysisWarningCode_ConfirmedWithoutInkRecognition             = 12,
  AnalysisWarningCode_BackgroundException                        = 13,
  AnalysisWarningCode_ContextNodeLocationNotSet                  = 14,
  AnalysisWarningCode_LanguageIdNotRespected                     = 15,
  AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported   = 16,
  AnalysisWarningCode_TopInkBreaksOnlyNotSupported               = 17,
  AnalysisWarningCode_AnalysisAlreadyRunning                     = 18
} AnalysisWarningCode;
```



## <a name="constants"></a><span data-ttu-id="b447b-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b447b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b447b-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode \_ anulado**</span><span class="sxs-lookup"><span data-stu-id="b447b-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode\_Aborted**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-108">A operação de análise foi anulada.</span><span class="sxs-lookup"><span data-stu-id="b447b-108">The analysis operation was aborted.</span></span>

<span data-ttu-id="b447b-109">Retornado somente quando a operação de análise síncrona é chamada.</span><span class="sxs-lookup"><span data-stu-id="b447b-109">Returned only when the synchronous analysis operation is called.</span></span> <span data-ttu-id="b447b-110">Anular uma operação assíncrona não gerará um evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="b447b-110">Aborting an asynchronous operation will not raise an [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="b447b-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**</span><span class="sxs-lookup"><span data-stu-id="b447b-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-112">O [**IInkAnalyzer**](iinkanalyzer.md) não pode encontrar um reconhecedor de tinta que atenda aos requisitos de idioma ou capacidade necessários para executar a operação de análise.</span><span class="sxs-lookup"><span data-stu-id="b447b-112">The [**IInkAnalyzer**](iinkanalyzer.md) cannot find an ink recognizer that meets language or capability requirements needed to perform the analysis operation.</span></span>

</dd> <dt>

<span data-ttu-id="b447b-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidNotSupported**</span><span class="sxs-lookup"><span data-stu-id="b447b-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-114">O reconhecedor de tinta não pôde respeitar o factor especificado definido no nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [Propriedades de dica de análise](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="b447b-114">The ink recognizer was unable to respect the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b447b-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidCoercionNotSupported**</span><span class="sxs-lookup"><span data-stu-id="b447b-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidCoercionNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-116">O reconhecedor de tinta não pôde forçar seus resultados para o factor especificado definido no nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [Propriedades de dica de análise](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="b447b-116">The ink recognizer was unable to coerce its results to the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b447b-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode \_ GuideNotSupported**</span><span class="sxs-lookup"><span data-stu-id="b447b-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode\_GuideNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-118">O reconhecedor de tinta não pôde respeitar o conjunto de guias especificado no nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [Propriedades de dica de análise](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="b447b-118">The ink recognizer was unable to respect the specified guide set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b447b-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode \_ WordlistNotSupported**</span><span class="sxs-lookup"><span data-stu-id="b447b-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode\_WordlistNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-120">O reconhecedor de tinta não pôde respeitar o conjunto de listas de palavras especificado no nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [Propriedades de dica de análise](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="b447b-120">The ink recognizer was unable to respect the specified word list set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b447b-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode \_ WordModeNotSupported**</span><span class="sxs-lookup"><span data-stu-id="b447b-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode\_WordModeNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-122">O reconhecedor de tinta não pôde respeitar o modo de palavra especificado definido no nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [Propriedades de dica de análise](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="b447b-122">The ink recognizer was unable to respect the specified word mode set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b447b-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode \_ PartialDictionaryTermsNotSupported**</span><span class="sxs-lookup"><span data-stu-id="b447b-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode\_PartialDictionaryTermsNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-124">Indica que os termos do dicionário parcial não puderam ser retornados do [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="b447b-124">Indicates that partial dictionary terms could not be returned from the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="b447b-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode \_ TextRecognitionProcessFailed**</span><span class="sxs-lookup"><span data-stu-id="b447b-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode\_TextRecognitionProcessFailed**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-126">Indica que o processo de reconhecimento de texto falhou.</span><span class="sxs-lookup"><span data-stu-id="b447b-126">Indicates the text recognition process failed.</span></span>

</dd> <dt>

<span data-ttu-id="b447b-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode \_ AddInkToRecognizerFailed**</span><span class="sxs-lookup"><span data-stu-id="b447b-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode\_AddInkToRecognizerFailed**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-128">Não foi possível adicionar a tinta ao [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="b447b-128">The ink could not be added to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="b447b-129">Por exemplo, a adição de traços coletados de um mouse em um reconhecedor de gesto falhará, pois o reconhecedor de gesto requer traços coletados de um digitalizador.</span><span class="sxs-lookup"><span data-stu-id="b447b-129">For example, adding strokes collected from a mouse on a gesture recognizer will fail, as the gesture recognizer requires strokes collected from a digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="b447b-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode \_ SetPrefixSuffixFailed**</span><span class="sxs-lookup"><span data-stu-id="b447b-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode\_SetPrefixSuffixFailed**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-131">O [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) não pôde respeitar o prefixo especificado ou o texto do sufixo de um nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [Propriedades de dica de análise](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="b447b-131">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) was unable to respect the specified prefix or suffix text of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b447b-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed**</span><span class="sxs-lookup"><span data-stu-id="b447b-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-133">O [**IInkAnalyzer**](iinkanalyzer.md) não pôde criar uma instância, clonar ou definir traços no [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="b447b-133">The [**IInkAnalyzer**](iinkanalyzer.md) was not able to instantiate, clone, or set strokes on the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="b447b-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode \_ ConfirmedWithoutInkRecognition**</span><span class="sxs-lookup"><span data-stu-id="b447b-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode\_ConfirmedWithoutInkRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-135">Indica que um objeto [**IContextNode**](icontextnode.md) foi confirmado pelo usuário sem nenhum valor de reconhecimento calculado para o nó.</span><span class="sxs-lookup"><span data-stu-id="b447b-135">Indicates that an [**IContextNode**](icontextnode.md) object has been confirmed by the user without having any recognition values computed for the node.</span></span>

</dd> <dt>

<span data-ttu-id="b447b-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ em segundo planoexception**</span><span class="sxs-lookup"><span data-stu-id="b447b-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode\_BackgroundException**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-137">A operação em segundo plano não foi concluída devido a uma exceção.</span><span class="sxs-lookup"><span data-stu-id="b447b-137">The background operation did not complete due to an exception.</span></span> <span data-ttu-id="b447b-138">Esse é um erro fatal e requer que o [**IInkAnalyzer**](iinkanalyzer.md) seja instanciado novamente antes de ser usado.</span><span class="sxs-lookup"><span data-stu-id="b447b-138">This is a fatal error and requires that the [**IInkAnalyzer**](iinkanalyzer.md) is re-instantiated before further use.</span></span>

</dd> <dt>

<span data-ttu-id="b447b-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode \_ ContextNodeLocationNotSet**</span><span class="sxs-lookup"><span data-stu-id="b447b-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode\_ContextNodeLocationNotSet**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-140">Indica que um objeto [**IContextNode**](icontextnode.md) não tem um conjunto de locais adequado (consulte [**IContextNode:: SetLocation**](icontextnode-setlocation.md)).</span><span class="sxs-lookup"><span data-stu-id="b447b-140">Indicates that an [**IContextNode**](icontextnode.md) object does not have a proper location set (see [**IContextNode::SetLocation**](icontextnode-setlocation.md)).</span></span> <span data-ttu-id="b447b-141">O método [**IContextNode:: getLocation**](icontextnode-getlocation.md) deve retornar um valor não vazio, a menos que o objeto **IContextNode** seja marcado como parcialmente preenchido.</span><span class="sxs-lookup"><span data-stu-id="b447b-141">The [**IContextNode::GetLocation**](icontextnode-getlocation.md) method must return a non-empty value unless the **IContextNode** object is marked as partially populated.</span></span>

</dd> <dt>

<span data-ttu-id="b447b-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode \_ LanguageIdNotRespected**</span><span class="sxs-lookup"><span data-stu-id="b447b-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode\_LanguageIdNotRespected**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-143">O identificador de idioma definido em um traço associado a um nó de reconhecedor personalizado (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)) não correspondeu ao identificador de idioma do [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) usado.</span><span class="sxs-lookup"><span data-stu-id="b447b-143">The language identifier set on a stroke associated with a custom recognizer node (see [**IContextNode::GetType**](icontextnode-gettype.md)) did not match the language identifier of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) used.</span></span> <span data-ttu-id="b447b-144">A tinta ainda foi reconhecida com o **IInkAnalysisRecognizer** especificado.</span><span class="sxs-lookup"><span data-stu-id="b447b-144">The ink was still recognized with the specified **IInkAnalysisRecognizer**.</span></span>

</dd> <dt>

<span data-ttu-id="b447b-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode \_ EnableUnicodeCharacterRangesNotSupported**</span><span class="sxs-lookup"><span data-stu-id="b447b-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode\_EnableUnicodeCharacterRangesNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-146">O [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) não dá suporte à habilitação de intervalos de caracteres Unicode, conforme especificado.</span><span class="sxs-lookup"><span data-stu-id="b447b-146">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support enabling Unicode character ranges as specified.</span></span>

</dd> <dt>

<span data-ttu-id="b447b-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode \_ TopInkBreaksOnlyNotSupported**</span><span class="sxs-lookup"><span data-stu-id="b447b-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode\_TopInkBreaksOnlyNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-148">O [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) não dá suporte a TopInkBreaks apenas, embora as dicas contivessem apenas a solicitação de TopInkBreaks.</span><span class="sxs-lookup"><span data-stu-id="b447b-148">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support TopInkBreaks only even though the hints contained the request for TopInkBreaks only.</span></span>

</dd> <dt>

<span data-ttu-id="b447b-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode \_ AnalysisAlreadyRunning**</span><span class="sxs-lookup"><span data-stu-id="b447b-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode\_AnalysisAlreadyRunning**</span></span>
</dt> <dd>

<span data-ttu-id="b447b-150">O [**IInkAnalyzer**](iinkanalyzer.md) já está executando a análise em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b447b-150">The [**IInkAnalyzer**](iinkanalyzer.md) is already performing background analysis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b447b-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="b447b-151">Remarks</span></span>

<span data-ttu-id="b447b-152">**AnalysisWarningCode \_ BackgroundException** é o único valor de código de aviso que requer que o objeto [**IInkAnalyzer**](iinkanalyzer.md) seja instanciado novamente antes de ser usado.</span><span class="sxs-lookup"><span data-stu-id="b447b-152">**AnalysisWarningCode\_BackgroundException** is the only warning code value that requires that the [**IInkAnalyzer**](iinkanalyzer.md) object is re-instantiated before further use.</span></span>

<span data-ttu-id="b447b-153">Outros valores de código de avisos, como **AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed** e **AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**, podem exigir que o objeto [**IInkAnalyzer**](iinkanalyzer.md) use um reconhecedor diferente.</span><span class="sxs-lookup"><span data-stu-id="b447b-153">Other warnings code values, such as **AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed** and **AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**, might require that the [**IInkAnalyzer**](iinkanalyzer.md) object use a different recognizer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b447b-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b447b-154">Requirements</span></span>



| <span data-ttu-id="b447b-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="b447b-155">Requirement</span></span> | <span data-ttu-id="b447b-156">Valor</span><span class="sxs-lookup"><span data-stu-id="b447b-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b447b-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b447b-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b447b-158">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b447b-158">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b447b-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b447b-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b447b-160">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b447b-160">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b447b-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b447b-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="b447b-162"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b447b-162"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b447b-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="b447b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b447b-164">**IAnalysisWarning::GetWarningCode**</span><span class="sxs-lookup"><span data-stu-id="b447b-164">**IAnalysisWarning::GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[<span data-ttu-id="b447b-165">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="b447b-165">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




