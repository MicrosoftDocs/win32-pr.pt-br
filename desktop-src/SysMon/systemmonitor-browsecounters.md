---
title: Método SystemMonitor BrowseCounters
description: Exibe a caixa de diálogo Adicionar contadores.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Método BrowseCounters SysMon
- Método BrowseCounters SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, método BrowseCounters
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e88d493ea0e4e1a9312191533162c8eb5a94cfb4233d17d21bb7217a136d403
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882922"
---
# <a name="systemmonitorbrowsecounters-method"></a>Método SystemMonitor:: BrowseCounters

Exibe a caixa de diálogo **Adicionar contadores** .

## <a name="syntax"></a>Sintaxe


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa caixa de diálogo permite que o usuário selecione contadores de desempenho locais ou remotos de uma lista de objetos de desempenho. Os contadores selecionados são adicionados à coleção de [**contadores**](counters.md) e exibidos no gráfico ou relatório.

Para receber uma notificação quando um contador é adicionado, implemente o evento [**OnCounterAdded**](systemmonitor-oncounteradded.md) .

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

[**Counters. Add**](counters-add.md)
</dt> </dl>

 

 





