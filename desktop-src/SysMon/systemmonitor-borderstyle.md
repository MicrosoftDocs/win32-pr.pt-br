---
title: Propriedade SystemMonitor. BorderStyle
description: Recupera ou define o estilo de borda do controle.
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- Propriedade BorderStyle SysMon
- Propriedade BorderStyle SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriedade BorderStyle
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824358"
---
# <a name="systemmonitorborderstyle-property"></a>Propriedade SystemMonitor. BorderStyle

Recupera ou define o estilo de borda do controle.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a>Valor da propriedade

Estilo de borda do controle.

Você pode definir essa propriedade como um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                                                                                                                                   | Significado                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <dt>**System. Windows. Forms. FormBorderStyle. VbBSNone**</dt> <dt>0</dt> </dl>                     | Sem borda. Esse é o valor padrão.<br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <dt>**System. Windows. Forms. FormBorderStyle. VbFixedSingle**</dt> <dt>1</dt> </dl> | Fixo, borda única.<br/>                 |



 

## <a name="exceptions"></a>Exceções



| Tipo de exceção               | Condição                                |
|------------------------------|------------------------------------------|
| **System. ArgumentException** | O estilo de borda especificado não é válido. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





