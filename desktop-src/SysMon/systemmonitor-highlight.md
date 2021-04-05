---
title: Propriedade SystemMonitor. Highlight
description: Recupera ou define um valor que indica se os valores dos contadores selecionados são realçados no grafo.
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- Realçar a propriedade SysMon
- Realçar a propriedade SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriedade de realce
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824430"
---
# <a name="systemmonitorhighlight-property"></a>Propriedade SystemMonitor. Highlight

Recupera ou define um valor que indica se os valores dos contadores selecionados são realçados no grafo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Verdadeiro indica que os valores dos contadores selecionados são realçados no grafo; caso contrário, false. O valor padrão é False.

## <a name="remarks"></a>Comentários

Para selecionar um ou mais contadores, você pode definir [**MyItem. Selected**](counteritem-selected.md) como true ou o usuário pode selecionar os contadores na lista de contadores mostrados na legenda.

**Antes do Windows Vista:** Não é possível selecionar contadores de forma programática e o usuário pode selecionar apenas um contador na lista de contadores mostrados na legenda.

O realce pode ser preto ou branco, dependendo do valor da propriedade [**BackColor**](systemmonitor-backcolor.md) . O realce é definido automaticamente com a cor que fornecerá contraste suficiente entre a cor de realce e a cor do plano de fundo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**Coitem. selecionado**](counteritem-selected.md)
</dt> </dl>

 

 





