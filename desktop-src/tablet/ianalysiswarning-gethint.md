---
description: Recupera a dica de análise que causou este aviso.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'Método IAnalysisWarning:: gethint (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51eb76839b157c2ac9611ef9be978ea967c8e9b3506513a23b0ca70906dd32b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940506"
---
# <a name="ianalysiswarninggethint-method"></a>Método IAnalysisWarning:: gethint

Recupera a dica de análise que causou este aviso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAnalysisHint* \[ fora\]
</dt> <dd>

O nó de contexto de dica de análise que causou este aviso ou **nulo** se uma dica de análise não causar esse aviso.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *pAnalysisHint* quando você não precisar mais usar o nó de contexto de dica de análise.

 

Um exemplo de uma dica de análise que gera um [**IAnalysisWarning**](ianalysiswarning.md) é uma dica de análise que contém um facto grafado incorretamente. Nesse caso, a análise de tinta retorna um [**IAnalysisStatus**](ianalysisstatus.md) que contém um **IAnalysisWarning** que faz referência ao nó de contexto de dica de análise com o factor digitado incorretamente. Além disso, nesse caso, o método [**IAnalysisWarning:: GetWarningCode**](ianalysiswarning-getwarningcode.md) do aviso de análise retorna um valor [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ FactoidNotSupported**.

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

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

