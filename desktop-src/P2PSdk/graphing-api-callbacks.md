---
description: 'A API de gráfico usa os seguintes retornos de chamada:'
ms.assetid: a8e083ab-b5e3-4186-99fb-cbb536e9d529
title: Retornos de chamada da API de gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11f4f559307e457822cd0e7ce18ef4b44119697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011026"
---
# <a name="graphing-api-callbacks"></a>Retornos de chamada da API de gráfico

A API de gráfico usa os seguintes retornos de chamada:



| Callback                                                          | Descrição                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*PFNPEER \_ \_ dados de segurança gratuitos \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_free_security_data) | Especifica a função que a infraestrutura de grafo de pares chama para liberar dados retornados [*pelo \_ \_ registro seguro de PFNPEER*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) e retornos de chamada de [*PFNPEER \_ Validate \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) . |
| [*\_registro seguro do PFNPEER \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record)            | Especifica a função que a infraestrutura de gráfico de pares chama para proteger registros.                                                                                                                                        |
| [*PFNPEER \_ validar \_ registro*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record)        | Especifica a função que a infraestrutura de grafo de pares chama para validar registros.                                                                                                                                      |



 

 

 



