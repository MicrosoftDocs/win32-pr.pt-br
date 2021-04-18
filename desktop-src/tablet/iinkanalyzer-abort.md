---
description: Cancela a operação de análise atual.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'Método IInkAnalyzer:: Abort (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eac96809bfbe41e7d6a070782da3ffd0f6407c60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793378"
---
# <a name="iinkanalyzerabort-method"></a>Método IInkAnalyzer:: Abort

Cancela a operação de análise atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppAbortedRegion* \[ fora\]
</dt> <dd>

Um ponteiro para um [**IAnalysisRegion**](ianalysisregion.md) que representa a região suja (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) da operação de análise atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAbortedRegion* quando você não precisar mais usar o objeto.

Esse método cancela a operação de análise atual.

Quando *ppAbortedRegion* é **NULL**, esse método executa a anulação como normal, porque isso indica que o chamador não tem interesse no valor de retorno.

O **método IInkAnalyzer:: Abort** silencia os eventos [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) e [**\_ IAnalysisEvents:: Activity**](-ianalysisevents-activity.md) para a operação de análise atual.

O **método IInkAnalyzer:: Abort** é executado de forma assíncrona até a operação de análise em segundo plano atual ser cancelada. Como o processo de cancelamento é assíncrono, o aplicativo pode executar outras tarefas enquanto o operações de análise atual é cancelado.

Se nenhuma operação de análise estiver em andamento, esse método retornará uma região de análise vazia.

Se uma operação de análise estiver em andamento, esse método cancelará a operação.

Se as operações de análise síncrona e assíncrona estiverem em andamento, esse método cancelará a operação síncrona.

Se esse método for chamado mais de uma vez para a mesma operação de análise, a primeira chamada retornará a região suja para a operação e as chamadas subsequentes retornarão uma região vazia.

Se seu aplicativo mantém sua própria estrutura de dados que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md), chamar o **método IInkAnalyzer:: Abort** pode deixar o documento com resultados parciais. Para evitar isso, não chame o **método IInkAnalyzer:: Abort** entre a hora em que o **IInkAnalyzer** recebe o evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) e a hora em que o **IInkAnalyzer** recebe o evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) ou [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .

Para obter mais informações sobre como sincronizar os dados do aplicativo com o Ink Analyzer, consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

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

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

