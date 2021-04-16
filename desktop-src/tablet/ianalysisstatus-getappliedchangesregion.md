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
ms.openlocfilehash: 08f6690091207b648c39cded161de64585e44b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501820"
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

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *pAppliedChangesRegion* quando você não precisar mais usar a região de análise.

 

Esse método é usado com mais frequência quando o aplicativo recebe informações para fins de depuração e precisa invalidar a área onde as alterações podem ocorrer para que as informações de depuração sejam pintadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

