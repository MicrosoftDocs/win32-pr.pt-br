---
description: Executa a análise de tinta assíncrona.
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'Método IInkAnalyzer:: BackgroundAnalyze (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501806"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a>Método IInkAnalyzer:: BackgroundAnalyze

Executa a análise de tinta assíncrona.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Quando esse método é chamado, o [**IInkAnalyzer**](iinkanalyzer.md) executa a análise de tinta em um thread em segundo plano.

Esse método retorna **S \_ false** e não inicia uma nova operação de análise em segundo plano nas seguintes circunstâncias.

-   No momento, o [**IInkAnalyzer**](iinkanalyzer.md) está executando a análise em segundo plano.
-   a região suja (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) representa uma área vazia.

O [**IInkAnalyzer**](iinkanalyzer.md) analisa a tinta em sua região suja durante uma chamada para o método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) ou **IInkAnalyzer:: BackgroundAnalyze**. No entanto, o **IInkAnalyzer** pode expandir a operação de análise para incluir regiões vizinhas.

Esse método define a região suja para uma região vazia.

Se os dados de traço tiverem sido adicionados ao [**IInkAnalyzer**](iinkanalyzer.md) após a chamada para o **método IInkAnalyzer:: BackgroundAnalyze**, o **IInkAnalyzer** poderá atualizar a região suja durante a fase reconciliar da análise de tinta.

A configuração de modos de análise (consulte o [**método IInkAnalyzer:: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)) especifica como o [**IInkAnalyzer**](iinkanalyzer.md) executa a análise em segundo plano. Para obter mais informações sobre a análise de tinta, consulte [visão geral da análise de tinta](ink-analysis-overview.md).

Esse método retorna um código de erro sob as circunstâncias a seguir.

-   Seu aplicativo definiu o valor de [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ IntermediateResults** no [**IInkAnalyzer**](iinkanalyzer.md) (consulte o [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)) e não trata o evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) .
-   Seu aplicativo limpou o valor de [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ AutomaticReconciliation** no [**IInkAnalyzer**](iinkanalyzer.md) (consulte o [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)) e não trata o evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .
-   Seu aplicativo não manipula o evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .
-   Seu aplicativo não manipula o evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir verifica a região suja do Ink Analyzer e inicia a análise de tinta em segundo plano se a região suja não estiver vazia.


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
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

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**Método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




