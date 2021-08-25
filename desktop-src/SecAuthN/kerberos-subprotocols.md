---
description: O protocolo Kerberos é composto por três subprotocols.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Subprotocoles kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ea1ababaf1ec7fe4e80112d4c1f69dc8bfc242a40cea56675d08198188a130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013356"
---
# <a name="kerberos-subprotocols"></a>Subprotocoles kerberos

O [*protocolo Kerberos*](../secgloss/k-gly.md) é composto por três subprotocols.



| Subprotocol                                                                         | Significado                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Troca de serviços de autenticação](authentication-service-exchange.md)<br/>   | Neste subprotocol, o [*KDC (centro de distribuição de chaves)*](../secgloss/k-gly.md) fornece ao cliente uma chave de sessão de [*logon*](../secgloss/s-gly.md) e um TGT (tíquete de concessão de tíquete).<br/> |
| [Troca de serviços de concessão de tíquete](ticket-granting-service-exchange.md)<br/> | Neste subprotocol, o KDC distribui uma chave de sessão de serviço e um tíquete para o serviço.<br/>                                                                                                                                                                                                            |
| [Cliente/servidor Exchange](client-server-exchange.md)<br/>                     | Neste subprotocol, o cliente apresenta o tíquete para admissão em um serviço.<br/>                                                                                                                                                                                                                         |



 

 

 
