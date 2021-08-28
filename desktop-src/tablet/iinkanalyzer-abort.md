---
description: Cancela a operação de análise atual.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: Método IInkAnalyzer::Abort (IACom.h)
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
ms.openlocfilehash: 4f52b2037210e39533d1247cb338bb22a7785f354dbca6b615c6ada67eff3bb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773596"
---
# <a name="iinkanalyzerabort-method"></a>Método IInkAnalyzer::Abort

Cancela a operação de análise atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppAbortedRegion* \[ out\]
</dt> <dd>

Um ponteiro para [**uma IAnalysisRegion**](ianalysisregion.md) que representa a região suja (consulte [**Método IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) da operação de análise atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAbortedRegion* quando você não precisar mais usar o objeto .

Esse método cancela a operação de análise atual.

Quando *ppAbortedRegion* é **NULL,** esse método executa a anulação normalmente, porque isso indica que o chamador não tem interesse no valor de retorno.

**O método IInkAnalyzer::Abort** calam os eventos [**\_ IAnalysisEvents::Results**](-ianalysisevents-results.md) e [**\_ IAnalysisEvents::Activity**](-ianalysisevents-activity.md) para a operação de análise atual.

**O método IInkAnalyzer::Abort** é executado de forma assíncrona até que a operação de análise em segundo plano atual seja cancelada. Como o processo de cancelamento é assíncrono, o aplicativo pode executar outras tarefas enquanto as opertions de análise atuais são canceladas.

Se nenhuma operação de análise estiver em andamento, esse método retornará uma região de análise vazia.

Se uma operação de análise estiver em andamento, esse método cancelará a operação.

Se as operações de análise síncronas e assíncronas estão em andamento, esse método cancela a operação síncrona.

Se esse método for chamado mais de uma vez para a mesma operação de análise, a primeira chamada retornará a região suja para a operação e as chamadas subsequentes retornarão uma região vazia.

Se seu aplicativo mantiver sua própria estrutura de dados sincronizada com a do [**IInkAnalyzer,**](iinkanalyzer.md)chamar o **Método IInkAnalyzer::Abort** poderá deixar seu documento com resultados parciais. Para evitar isso, não chame o Método **IInkAnalyzer::Abort** entre o momento em que o **IInkAnalyzer** recebe o evento [**\_ IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) e a hora em que **o IInkAnalyzer** recebe o evento [**\_ IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) ou [**\_ IAnalysisEvents::Results.**](-ianalysisevents-results.md)

Para obter mais informações sobre como sincronizar os dados do aplicativo com o analisador de tinta, consulte [Proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Método IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Método IInkAnalyzer::SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

