---
description: Recupera um valor que indica se IAnalysisRegion representa uma região vazia.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'Método IAnalysisRegion:: IsEmpty (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c1fb4ebbe487119c65f153f78e192de38e6393fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791072"
---
# <a name="ianalysisregionisempty-method"></a>Método IAnalysisRegion:: IsEmpty

Recupera um valor que indica se [**IAnalysisRegion**](ianalysisregion.md) representa uma região vazia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pfIsEmpty* \[ fora\]
</dt> <dd>

**Variante \_ TRUE** se a região representada estiver vazia; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

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

[**Método IAnalysisRegion:: isFinite**](ianalysisregion-isinfinite.md)
</dt> <dt>

[**Método IAnalysisRegion:: MakeEmpty**](ianalysisregion-makeempty.md)
</dt> <dt>

[**Método IAnalysisRegion:: MakeInfinite**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




