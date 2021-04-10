---
description: Recupera um valor que indica se IAnalysisRegion representa uma região infinita.
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: 'Método IAnalysisRegion:: isFinite (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsInfinite
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f7d284c043f38a681b969f72d751f9acaa954c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164558"
---
# <a name="ianalysisregionisinfinite-method"></a>Método IAnalysisRegion:: isFinite

Recupera um valor que indica se [**IAnalysisRegion**](ianalysisregion.md) representa uma região infinita.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pfIsInfinite* \[ fora\]
</dt> <dd>

**Variante \_ TRUE** se a região representada for infinita; caso contrário, **Variant \_ false**.

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

[**Método IAnalysisRegion:: IsEmpty**](ianalysisregion-isempty.md)
</dt> <dt>

[**Método IAnalysisRegion:: MakeEmpty**](ianalysisregion-makeempty.md)
</dt> <dt>

[**Método IAnalysisRegion:: MakeInfinite**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




