---
description: Recupera o objeto IAnalysisAlternate no índice especificado dentro da coleção.
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: 'Método IAnalysisAlternates:: GetAnalysisAlternate (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 122bccc4985ed7ba5617e9d373ecdf3d0c84dac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788838"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a>Método IAnalysisAlternates:: GetAnalysisAlternate

Recupera o objeto [**IAnalysisAlternate**](ianalysisalternate.md) no índice especificado dentro da coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulIndex* \[ no\]
</dt> <dd>

O índice de base zero do objeto [**IAnalysisAlternate**](ianalysisalternate.md) a ser obtido.

</dd> <dt>

*ppAlternate* \[ fora\]
</dt> <dd>

Um ponteiro para o objeto [**IAnalysisAlternate**](ianalysisalternate.md) no índice especificado dentro da coleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppAlternate* quando você não precisar mais usar a alternativa de análise.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

