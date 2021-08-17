---
description: Recupera a região do documento que corresponde às alterações feitas na árvore de nós de contexto do objeto IInkAnalyzer como resultado da análise de tinta.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'Método IAnalysisStatus:: GetAppliedChangesRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d3b2fec2528cbf961956e8b41f9eb6c985bd745d5dad097eb05544e64c42d122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044989"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a>Método IAnalysisStatus:: GetAppliedChangesRegion

Recupera a região do documento que corresponde às alterações feitas na árvore de nós de contexto do objeto [**IInkAnalyzer**](iinkanalyzer.md) como resultado da análise de tinta.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAppliedChangesRegion* \[ fora\]
</dt> <dd>

Um ponteiro para a [**IAnalysisRegion**](ianalysisregion.md) do documento em que foram feitas alterações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *pAppliedChangesRegion* quando você não precisar mais usar a região de análise.

 

Esse método é usado com mais frequência quando o aplicativo recebe informações para fins de depuração e precisa invalidar a área onde as alterações podem ocorrer para que as informações de depuração sejam pintadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

