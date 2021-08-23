---
title: Propriedade MyItem. LineStyle
description: Recupera ou define o estilo de linha usado para grafar o valor do contador.
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- Propriedade LineStyle SysMon
- Propriedade LineStyle SysMon, classe de coitem
- Classe monoitem SysMon, Propriedade LineStyle
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a60ce0c96f9e3eb25639cad9251d8cf3969d022001962e14ec9c3ef4d157ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883701"
---
# <a name="counteritemlinestyle-property"></a>Propriedade MyItem. LineStyle

Recupera ou define o estilo de linha usado para grafar o valor do contador.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Property LineStyle As Long
```



## <a name="property-value"></a>Valor da propriedade

O estilo de linha usado para grafar o valor do contador. Os valores correspondem às constantes do sistema mostradas na tabela a seguir.



| Valor                                                                                                                                                                                                                                                                                                                                                                               | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. sólido**</dt> <dt>0</dt> </dl>                     | Linha sólida. Esse é o valor padrão.<br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. Dash**</dt> <dt>1</dt> </dl>                         | Linha pontilhada com segmentos longos e espaços estreitos.<br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. dot**</dt> <dt>2</dt> </dl>                             | Linha pontilhada com segmentos e espaços uniformes.<br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. travessão ponto**</dt> <dt>3</dt> </dl>             | Linha pontilhada com segmentos curtos e longos alternados.<br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. travessão ponto ponto**</dt> <dt>4</dt> </dl> | Linha pontilhada com traços alternados e pontilhados duplos.<br/>  |



 

## <a name="exceptions"></a>Exceções



| Tipo de exceção               | Condição                              |
|------------------------------|----------------------------------------|
| **System.ArgumentException** | O estilo de linha especificado não é válido. |



 

## <a name="remarks"></a>Comentários

Para especificar um valor diferente de DashStyle. Solid, [**MyItem. Width**](counteritem-width.md) deve ser definido como 1. Se a largura for maior que 1, o SYSMON ignorará o estilo de linha especificado e usará DashStyle. Solid.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Item**](counteritem.md)
</dt> </dl>

 

 





