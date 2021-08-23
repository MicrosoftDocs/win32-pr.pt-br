---
description: Determina se o IAnalysisRegion especificado contém o mesmo valor que o objeto IAnalysisRegion atual.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: Método IAnalysisRegion::EqualsRegion (IACom.h)
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
ms.openlocfilehash: aecf7bd065c2da0c507c2424c0305526510c9d4f64844dfa229183cf43d5554a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596796"
---
# <a name="ianalysisregionequalsregion-method"></a>Método IAnalysisRegion::EqualsRegion

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

*pOtherRegion* \[ Em\]
</dt> <dd>

O [**objeto IAnalysisRegion**](ianalysisregion.md) a ser comparado com **o IAnalysisRegion atual.**

</dd> <dt>

*pfRegionsEqual* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** se o [**IAnalysisRegion especificado**](ianalysisregion.md) contiver o mesmo valor que o IAnalysisRegion atual; caso contrário, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> </dl>

 

 




