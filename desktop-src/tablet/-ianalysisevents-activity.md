---
description: 'Ocorre quando o método IInkAnalyzer:: Analyze ou IInkAnalyzer:: BackgroundAnalyze é chamado.'
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: 'Evento _IAnalysisEvents:: Activity (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f235d3414b0d514f32b4ebd197c04a8721968a2a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104298012"
---
# <a name="_ianalysiseventsactivity-event"></a>\_Evento IAnalysisEvents:: Activity

Ocorre quando o método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) ou [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) é chamado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Activity();
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Esse evento indica que o [**IInkAnalyzer**](iinkanalyzer.md) está executando a análise de tinta. Esse evento não indica o progresso da operação de análise de tinta.

Para executar qualquer um dos procedimentos a seguir, implemente um manipulador de eventos **\_ IAnalysisEvents:: Activity** :

-   Indique ao usuário que o analisador de tinta está executando a análise de tinta.
-   Processar a entrada do usuário durante a análise síncrona.
-   Receber notificação de solicitações do sistema, como repintura da janela do aplicativo, durante a análise de tinta.

O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento com frequência durante a fase de análise de layout e a fase de classificação de escrita e desenho da análise de tinta. O **IInkAnalyzer** gera esse evento durante a fase de reconhecimento de manuscrito antes e depois de acessar um reconhecedor de tinta.

O número de eventos de atividade que um [**IInkAnalyzer**](iinkanalyzer.md) gera é afetado por:

-   O reconhecedor de tinta que o [**IInkAnalyzer**](iinkanalyzer.md) se aplica ao reconhecimento de tinta.
-   O número e o comprimento dos traços que o [**IInkAnalyzer**](iinkanalyzer.md) está analisando.
-   O número de traços que são classificados como gravação.

Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




