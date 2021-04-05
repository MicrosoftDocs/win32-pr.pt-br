---
title: Propriedade MyItem. Selected
description: Recupera ou define um valor que indica se o contador está selecionado.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Propriedade selecionada SysMon
- Propriedade selecionada SysMon, objeto de coitem
- Objeto monoitem SysMon, propriedade selecionada
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
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918552"
---
# <a name="counteritemselected-property"></a>Propriedade MyItem. Selected

Recupera ou define um valor que indica se o contador está selecionado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Property Selected As Boolean
```



## <a name="property-value"></a>Valor da propriedade

True se o contador for selecionado; caso contrário, false.

## <a name="remarks"></a>Comentários

Você pode selecionar um ou mais contadores da coleção de contadores. Selecionar um contador, seleciona o contador na legenda, torna o contador visível na legenda e gera um evento [**OnCounterSelected**](-systemmonitor-oncounterselected.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Item**](counteritem.md)
</dt> </dl>

 

 





