---
description: Obtém o retângulo delimitar da IAnalysisRegion.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: Método IAnalysisRegion::GetBounds (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8481ddda9d0d278d2f24873a0c7d8a993c924c816d58153c38de8ef1063e986b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092327"
---
# <a name="ianalysisregiongetbounds-method"></a>Método IAnalysisRegion::GetBounds

Obtém o retângulo delimitar [**do IAnalysisRegion.**](ianalysisregion.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBoundingRectangle* \[ out\]
</dt> <dd>

O retângulo delimitante da [**IAnalysisRegion em**](ianalysisregion.md) coordenadas de espaço de tinta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Os limites estão em coordenadas de espaço em tinta.

Se [**IAnalysisRegion**](ianalysisregion.md) representar uma área infinita, os limites esquerdo e superior serão **INT \_ MIN**; e os limites direito e inferior serão **INT \_ MAX.**

Se [**IAnalysisRegion representar**](ianalysisregion.md) uma área vazia, todos os limites do retângulo serão 0.

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
</dt> <dt>

[**Método IAnalysisRegion::GetRegionScans**](ianalysisregion-getregionscans.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




