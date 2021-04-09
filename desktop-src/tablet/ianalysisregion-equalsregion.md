---
description: Determina se o IAnalysisRegion especificado contém o mesmo valor que o objeto IAnalysisRegion atual.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'Método IAnalysisRegion:: EqualsRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090558"
---
# <a name="ianalysisregionequalsregion-method"></a>Método IAnalysisRegion:: EqualsRegion

Determina se o [**IAnalysisRegion**](ianalysisregion.md) especificado contém o mesmo valor que o objeto **IAnalysisRegion** atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOtherRegion* \[ no\]
</dt> <dd>

O objeto [**IAnalysisRegion**](ianalysisregion.md) a ser comparado com o **IAnalysisRegion** atual.

</dd> <dt>

*pfRegionsEqual* \[ fora\]
</dt> <dd>

**Variante \_ TRUE** se o [**IAnalysisRegion**](ianalysisregion.md) especificado contiver o mesmo valor que o IAnalysisRegion atual; caso contrário, **Variant \_ false**.

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
</dt> </dl>

 

 




