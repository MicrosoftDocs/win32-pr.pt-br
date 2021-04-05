---
description: A interface IMonitorEventer fornece métodos para enviar eventos e alocar e liberar recursos de monitor.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Interface IMonitorEventer (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827035"
---
# <a name="imonitoreventer-interface"></a>Interface IMonitorEventer

A interface **IMonitorEventer** fornece métodos para enviar eventos e alocar e liberar recursos de monitor.

## <a name="members"></a>Membros

A interface **IMonitorEventer** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMonitorEventer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMonitorEventer** tem esses métodos.



| Método                                                 | Descrição                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [**FreeEventData**](imonitoreventer-freeeventdata.md) | Libera espaço alocado para monitorar dados.<br/> |
| [**GetEventData**](imonitoreventer-geteventdata.md)   | Aloca espaço para monitorar dados.<br/>       |
| [**SendNMEvent**](imonitoreventer-sendnmevent.md)     | Envia eventos para o WMI.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

