---
description: O protocolo Kerberos é composto por três subprotocolos.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Subprotocolos Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c06c26013e065254458ad403cdff99fbb2edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169829"
---
# <a name="kerberos-subprotocols"></a>Subprotocolos Kerberos

O [*protocolo Kerberos*](../secgloss/k-gly.md) é composto por três subprotocolos.



| Subprotocolo                                                                         | Significado                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Troca de serviços de autenticação](authentication-service-exchange.md)<br/>   | Nesse subprotocolo, o [*centro de distribuição de chaves*](../secgloss/k-gly.md) (KDC) fornece ao cliente uma chave de [*sessão*](../secgloss/s-gly.md) de logon e um tíquete de concessão de tíquete (TGT).<br/> |
| [Troca de serviços de concessão de tíquete](ticket-granting-service-exchange.md)<br/> | Nesse subprotocolo, o KDC distribui uma chave de sessão de serviço e um tíquete para o serviço.<br/>                                                                                                                                                                                                            |
| [Troca de cliente/servidor](client-server-exchange.md)<br/>                     | Nesse subprotocolo, o cliente apresenta o tíquete para a admissão a um serviço.<br/>                                                                                                                                                                                                                         |



 

 

 
