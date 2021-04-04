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
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008824"
---
# <a name="systemmonitorbrowsecounters-method"></a>Método SystemMonitor:: BrowseCounters

Exibe a caixa de diálogo **Adicionar contadores** .

## <a name="syntax"></a>Sintaxe


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

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

 

 





