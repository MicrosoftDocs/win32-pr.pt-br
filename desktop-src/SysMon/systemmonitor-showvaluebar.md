---
title: Propriedade SystemMonitor. ShowValueBar
description: Recupera ou define um valor que determina se a barra de valores (o conjunto de valores estatísticos abaixo do grafo) é exibida no controle.
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- Propriedade ShowValueBar SysMon
- Propriedade ShowValueBar SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade ShowValueBar
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644430"
---
# <a name="systemmonitorshowvaluebar-property"></a>Propriedade SystemMonitor. ShowValueBar

Recupera ou define um valor que determina se a barra de valores (o conjunto de valores estatísticos abaixo do grafo) é exibida no controle.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Verdadeiro indica que a barra de valores é exibida no controle; caso contrário, false. O valor padrão para essa propriedade é true.

## <a name="remarks"></a>Comentários

As estatísticas exibidas incluem o último valor, o valor médio e os valores mínimo e máximo do contador selecionado no momento durante o intervalo de tempo exibido. Para selecionar os valores do contador a serem exibidos, o usuário deve selecionar o contador no painel Legenda do controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





