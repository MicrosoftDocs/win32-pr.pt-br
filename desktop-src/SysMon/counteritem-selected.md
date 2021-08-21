---
title: Propriedade CounterItem.Selected
description: Recupera ou define um valor que indica se o contador está selecionado.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Propriedade selecionada SysMon
- Propriedade selecionada SysMon , objeto CounterItem
- Objeto CounterItem SysMon, propriedade selecionada
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e5cfcc65c54f882f10e87a0f2aaebad0e1a55c94b6581031b034799987bc6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956955"
---
# <a name="counteritemselected-property"></a>Propriedade CounterItem.Selected

Recupera ou define um valor que indica se o contador está selecionado.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Property Selected As Boolean
```



## <a name="property-value"></a>Valor da propriedade

True se o contador estiver selecionado; caso contrário, false.

## <a name="remarks"></a>Comentários

Você pode selecionar um ou mais contadores da coleção de contadores. Selecionar um contador, seleciona o contador na Legenda, torna o contador visível na Legenda e gera um [**evento OnCounterSelected.**](-systemmonitor-oncounterselected.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





