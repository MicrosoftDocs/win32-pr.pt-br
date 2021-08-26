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
ms.openlocfilehash: aa8c9c3c60f51ffd854ccdfebb6538337e7676a8c63e45899737333c41d99aad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057956"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a>Método IAnalysisWarning:: GetBackgroundError

Recupera o código de erro para a operação de análise de tinta em segundo plano se ocorreu um erro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Se ocorrer um erro dentro de uma operação de análise em segundo plano, o [**IInkAnalyzer**](iinkanalyzer.md) não poderá retornar o código de erro porque ele está ocorrendo em um thread diferente. Em vez disso, o manipulador de eventos [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) recebe um [**IAnalysisStatus**](ianalysisstatus.md) que contém um [**IAnalysisWarning**](ianalysiswarning.md) com um [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ BackgroundException**. Este **IAnalysisWarning** contém o código de erro para a operação de análise em segundo plano. Em geral, o manipulador de eventos **\_ IAnalysisEvents:: Results** retornará esse código de erro para que ele possa ser tratado em outro lugar em seu aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
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

 

