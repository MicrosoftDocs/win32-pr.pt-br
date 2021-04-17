---
description: Executa a análise de tinta síncrona.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'Método IInkAnalyzer:: Analyze (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768282"
---
# <a name="iinkanalyzeranalyze-method"></a>Método IInkAnalyzer:: Analyze

Executa a análise de tinta síncrona.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppStatus* \[ fora\]
</dt> <dd>

Um ponteiro para um [**IAnalysisStatus**](ianalysisstatus.md) que descreve o status da operação de análise.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppStatus* quando você não precisar mais usar o status da análise.

 

Esse método inicia uma operação de análise de tinta síncrona. A análise de tinta inclui análise de layout, gravação e classificação de desenho e reconhecimento de manuscrito. Esse método retorna após a conclusão da operação de análise.

Esse método retornará **o \_ ponteiro E** se *ppStatus* for **nulo**.

Durante uma chamada para o método **IInkAnalyzer:: Analyze** ou [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), o [**IInkAnalyzer**](iinkanalyzer.md) analisa a tinta em sua região suja (Confira o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)). No entanto, o **IInkAnalyzer** pode expandir a operação de análise para incluir regiões vizinhas.

Esse método define a região suja do objeto [**IInkAnalyzer**](iinkanalyzer.md) para uma região vazia. Se outro thread tiver adicionado dados de traço que não foram analisados, o **IInkAnalyzer** adicionará a caixa delimitadora dos traços não analisados à sua região suja durante a fase de reconciliação da análise.

Esse método retornará um erro se seu aplicativo não tratar o evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .

O [**IInkAnalyzer**](iinkanalyzer.md) não gera os eventos [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) e [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) em resposta a esse método.

Para modificar a maneira como a análise de tinta é executada, use o [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md).

Para obter mais informações sobre a análise de tinta, consulte [visão geral da análise de tinta](ink-analysis-overview.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir executa a análise de tinta em primeiro plano.


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 

