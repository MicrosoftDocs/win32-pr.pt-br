---
description: Cria uma cópia do IAnalysisRegion.
ms.assetid: eb94e1ce-7801-409d-9ae6-e7db0a9b861f
title: 'Método IAnalysisRegion:: clone (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.Clone
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fb069ddb461ab4422f8cbbc8990fb6d735808e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811389"
---
# <a name="ianalysisregionclone-method"></a>Método IAnalysisRegion:: clone

Cria uma cópia do [**IAnalysisRegion**](ianalysisregion.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] IAnalysisRegion **pClonedRegion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pClonedRegion* \[ fora\]
</dt> <dd>

Um ponteiro para uma cópia do [**IAnalysisRegion**](ianalysisregion.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Esse método é eqivalent para o método System. Windows. Ink. AnalysisCore. AnalysisRegionBase. Clone no .NET Framework.

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *pClonedRegion* quando você não precisar mais usar a região de análise clonada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

