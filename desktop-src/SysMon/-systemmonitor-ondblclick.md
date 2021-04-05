---
title: Evento SystemMonitor. AoClicarDuasVezes
description: Notifica quando um usuário clica duas vezes na linha do gráfico, na barra de histograma ou no item de relatório com o botão esquerdo do mouse.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- Evento de AoClicarDuasVezes do SysMon
- Evento AoClicarDuasVezes SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, evento AoClicarDuasVezes
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
ms.openlocfilehash: f5f21c6d67468ecb07bbe0fe83bec7b48a086571
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085608"
---
# <a name="systemmonitorondblclick-event"></a>Evento SystemMonitor. AoClicarDuasVezes

Notifica quando um usuário clica duas vezes na linha do gráfico, na barra de histograma ou no item de relatório com o botão esquerdo do mouse.

## <a name="syntax"></a>Sintaxe


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do entrada, saída\]
</dt> <dd>

Índice do contador selecionado no objeto da coleção de [**contadores**](counters.md) . Um valor de índice 0 será retornado se nenhum contador tiver sido selecionado; caso contrário, o índice do contador selecionado será retornado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Quando esse evento é disparado, o contador que o usuário selecionou no grafo de linha e no histograma também é selecionado no painel Legenda. Isso torna mais fácil para o usuário do monitor do sistema ver qual contador é selecionado quando vários valores de contador são exibidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





