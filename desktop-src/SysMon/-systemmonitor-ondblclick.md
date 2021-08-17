---
title: Evento SystemMonitor.OnDblClick
description: Notifica você quando um usuário clica duas vezes na linha do grafo, na barra de histograma ou no item de relatório com o botão esquerdo do mouse.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- Evento OnDblClick SysMon
- Evento OnDblClick SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon , evento OnDblClick
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef829fad368e7d8cf3b65ab70db4600f6d635b1d36bcc5e3f50fcdbaf429a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883950"
---
# <a name="systemmonitorondblclick-event"></a>Evento SystemMonitor.OnDblClick

Notifica você quando um usuário clica duas vezes na linha do grafo, na barra de histograma ou no item de relatório com o botão esquerdo do mouse.

## <a name="syntax"></a>Sintaxe


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ in, out\]
</dt> <dd>

Índice do contador selecionado no objeto [**de coleção**](counters.md) Contadores. Um valor de índice de 0 será retornado se nenhum contador tiver sido selecionado; caso contrário, o índice do contador selecionado será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Quando esse evento é disparado, o contador que o usuário selecionou no grafo de linha e no histograma também é selecionado no painel Legenda. Isso facilita para o usuário do Monitor do Sistema ver qual contador é selecionado quando vários valores de contador são exibidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





