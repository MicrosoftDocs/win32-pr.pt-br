---
description: Recupera o código de erro para a operação de análise de tinta em segundo plano se ocorreu um erro.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'Método IAnalysisWarning:: GetBackgroundError (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4367b1d52ee5d2a3bb65af0e4edd4922b8ae9a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164554"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a>Método IAnalysisWarning:: GetBackgroundError

Recupera o código de erro para a operação de análise de tinta em segundo plano se ocorreu um erro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Se ocorrer um erro dentro de uma operação de análise em segundo plano, o [**IInkAnalyzer**](iinkanalyzer.md) não poderá retornar o código de erro porque ele está ocorrendo em um thread diferente. Em vez disso, o manipulador de eventos [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) recebe um [**IAnalysisStatus**](ianalysisstatus.md) que contém um [**IAnalysisWarning**](ianalysiswarning.md) com um [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ BackgroundException**. Este **IAnalysisWarning** contém o código de erro para a operação de análise em segundo plano. Em geral, o manipulador de eventos **\_ IAnalysisEvents:: Results** retornará esse código de erro para que ele possa ser tratado em outro lugar em seu aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents:: resultados**](-ianalysisevents-results.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

