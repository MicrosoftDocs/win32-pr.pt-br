---
description: Obtém o retângulo delimitador do IAnalysisRegion.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: 'Método IAnalysisRegion:: GetBounds (IACom. h)'
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
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647243"
---
# <a name="ianalysisregiongetbounds-method"></a>Método IAnalysisRegion:: GetBounds

Obtém o retângulo delimitador do [**IAnalysisRegion**](ianalysisregion.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBoundingRectangle* \[ fora\]
</dt> <dd>

O retângulo delimitador do [**IAnalysisRegion**](ianalysisregion.md) nas coordenadas de espaço de tinta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Os limites estão em coordenadas de espaço de tinta.

Se [**IAnalysisRegion**](ianalysisregion.md) representar uma área infinita, os limites esquerdo e superior serão **int \_ min**; e os limites direito e inferior serão **int \_ Max**.

Se [**IAnalysisRegion**](ianalysisregion.md) representar uma área vazia, todos os limites do retângulo serão 0.

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

[**Método IAnalysisRegion:: GetRegionScans**](ianalysisregion-getregionscans.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




