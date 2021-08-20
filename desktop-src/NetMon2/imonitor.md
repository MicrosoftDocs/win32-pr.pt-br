---
description: A interface IMonitor fornece métodos que controlam a operação do monitor. Esses métodos são chamados pelo serviço de controle de monitor (MCSVC).
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Interface IMonitor (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 16199568473315fb61e53428d01c72032f3efff6ea0591bfd72ca2475f854fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133097"
---
# <a name="imonitor-interface"></a>Interface IMonitor

A interface **iMonitor** fornece métodos que controlam a operação do monitor. Esses métodos são chamados pelo [*serviço de controle de monitor*](m.md) (MCSVC).

## <a name="members"></a>Membros

A interface **iMonitor** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMonitor** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **iMonitor** tem esses métodos.



| Método                                        | Descrição                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**Configurar doconfigure**](imonitor-doconfigure.md)   | Atualiza a configuração do monitor.<br/>                                                                           |
| [**Doinitialize**](imonitor-doinitialize.md) | Inicializa um monitor.<br/>                                                                                   |
| [**Nos quadros**](imonitor-onframes.md)         | Indica o status de um evento de quadro.<br/>                                                                   |
| [**OnStart**](imonitor-onstart.md)           | Indica que o monitor foi configurado com êxito e que a captura de dados está prestes a começar.<br/> |
| [**OnStatus**](imonitor-onstatus.md)         | Indica um evento de status NPP.<br/>                                                                           |
| [**OnStop**](imonitor-onstop.md)             | Indica a conclusão da captura de dados.<br/>                                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

