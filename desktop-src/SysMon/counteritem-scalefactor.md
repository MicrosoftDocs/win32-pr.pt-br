---
title: Propriedade MyItem. ScaleFactor
description: Recupera ou define o fator de escala usado para grafar o valor do contador.
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Propriedade ScaleFactor SysMon
- Propriedade ScaleFactor SysMon, classe de coitem
- Classe monoitem SysMon, propriedade ScaleFactor
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9a04df634fe54c82230ade679afb3259519173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755773"
---
# <a name="counteritemscalefactor-property"></a>Propriedade MyItem. ScaleFactor

Recupera ou define o fator de escala usado para grafar o valor do contador.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a>Valor da propriedade

Fator de escala usado na exibição dos valores do contador grafado. Os valores válidos variam de-9 a 9 (os valores correspondem a 0, 1-100000000,0).

**Antes do Windows Vista:** Os valores válidos variam de-7 a 7 (os valores correspondem a 0, 1-1000000,0).

## <a name="remarks"></a>Comentários

Defina essa propriedade somente se desejar alterar o fator de escala padrão do contador (cada contador define seu próprio fator de escala). O valor dessa propriedade é definido como Integer. MaxValue se o contador estiver usando seu fator de escala padrão para grafar os valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Item**](counteritem.md)
</dt> <dt>

[**SystemMonitor.ScaleToFit**](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





