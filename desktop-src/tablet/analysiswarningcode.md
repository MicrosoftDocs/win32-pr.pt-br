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
# <a name="analysiswarningcode-enumeration"></a>Enumeração AnalysisWarningCode

Especifica o conjunto de avisos disponíveis que podem ocorrer durante a análise de tinta.

## <a name="syntax"></a>Sintaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode \_ anulado**
</dt> <dd>

A operação de análise foi anulada.

Retornado somente quando a operação de análise síncrona é chamada. Anular uma operação assíncrona não gerará um evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .

</dd> <dt>

<span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) não pode encontrar um reconhecedor de tinta que atenda aos requisitos de idioma ou capacidade necessários para executar a operação de análise.

</dd> <dt>

<span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidNotSupported**
</dt> <dd>

O reconhecedor de tinta não pôde respeitar o factor especificado definido no nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [Propriedades de dica de análise](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidCoercionNotSupported**
</dt> <dd>

O reconhecedor de tinta não pôde forçar seus resultados para o factor especificado definido no nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [Propriedades de dica de análise](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode \_ GuideNotSupported**
</dt> <dd>

O reconhecedor de tinta não pôde respeitar o conjunto de guias especificado no nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [Propriedades de dica de análise](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode \_ WordlistNotSupported**
</dt> <dd>

O reconhecedor de tinta não pôde respeitar o conjunto de listas de palavras especificado no nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [Propriedades de dica de análise](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode \_ WordModeNotSupported**
</dt> <dd>

O reconhecedor de tinta não pôde respeitar o modo de palavra especificado definido no nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [Propriedades de dica de análise](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode \_ PartialDictionaryTermsNotSupported**
</dt> <dd>

Indica que os termos do dicionário parcial não puderam ser retornados do [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode \_ TextRecognitionProcessFailed**
</dt> <dd>

Indica que o processo de reconhecimento de texto falhou.

</dd> <dt>

<span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode \_ AddInkToRecognizerFailed**
</dt> <dd>

Não foi possível adicionar a tinta ao [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md). Por exemplo, a adição de traços coletados de um mouse em um reconhecedor de gesto falhará, pois o reconhecedor de gesto requer traços coletados de um digitalizador.

</dd> <dt>

<span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode \_ SetPrefixSuffixFailed**
</dt> <dd>

O [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) não pôde respeitar o prefixo especificado ou o texto do sufixo de um nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [Propriedades de dica de análise](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed**
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) não pôde criar uma instância, clonar ou definir traços no [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode \_ ConfirmedWithoutInkRecognition**
</dt> <dd>

Indica que um objeto [**IContextNode**](icontextnode.md) foi confirmado pelo usuário sem nenhum valor de reconhecimento calculado para o nó.

</dd> <dt>

<span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ em segundo planoexception**
</dt> <dd>

A operação em segundo plano não foi concluída devido a uma exceção. Esse é um erro fatal e requer que o [**IInkAnalyzer**](iinkanalyzer.md) seja instanciado novamente antes de ser usado.

</dd> <dt>

<span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode \_ ContextNodeLocationNotSet**
</dt> <dd>

Indica que um objeto [**IContextNode**](icontextnode.md) não tem um conjunto de locais adequado (consulte [**IContextNode:: SetLocation**](icontextnode-setlocation.md)). O método [**IContextNode:: getLocation**](icontextnode-getlocation.md) deve retornar um valor não vazio, a menos que o objeto **IContextNode** seja marcado como parcialmente preenchido.

</dd> <dt>

<span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode \_ LanguageIdNotRespected**
</dt> <dd>

O identificador de idioma definido em um traço associado a um nó de reconhecedor personalizado (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)) não correspondeu ao identificador de idioma do [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) usado. A tinta ainda foi reconhecida com o **IInkAnalysisRecognizer** especificado.

</dd> <dt>

<span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode \_ EnableUnicodeCharacterRangesNotSupported**
</dt> <dd>

O [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) não dá suporte à habilitação de intervalos de caracteres Unicode, conforme especificado.

</dd> <dt>

<span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode \_ TopInkBreaksOnlyNotSupported**
</dt> <dd>

O [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) não dá suporte a TopInkBreaks apenas, embora as dicas contivessem apenas a solicitação de TopInkBreaks.

</dd> <dt>

<span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode \_ AnalysisAlreadyRunning**
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) já está executando a análise em segundo plano.

</dd> </dl>

## <a name="remarks"></a>Comentários

**AnalysisWarningCode \_ BackgroundException** é o único valor de código de aviso que requer que o objeto [**IInkAnalyzer**](iinkanalyzer.md) seja instanciado novamente antes de ser usado.

Outros valores de código de avisos, como **AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed** e **AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**, podem exigir que o objeto [**IInkAnalyzer**](iinkanalyzer.md) use um reconhecedor diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




