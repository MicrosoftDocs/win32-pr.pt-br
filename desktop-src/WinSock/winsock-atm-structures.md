---
description: A lista a seguir fornece descrições concisas de cada estrutura de ATM do Winsock. Para obter informações adicionais sobre qualquer estrutura, clique no nome da estrutura.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Estruturas ATM do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f45cafef8bcf628f9172f2ad7ce3323d0d5b0c3e2c3912d195615ea2471501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612796"
---
# <a name="winsock-atm-structures"></a>Estruturas ATM do Winsock

A lista a seguir fornece descrições concisas de cada estrutura de ATM do Winsock. Para obter informações adicionais sobre qualquer estrutura, clique no nome da estrutura.



| Estrutura ATM                           | Descrição                                                |
|-----------------------------------------|------------------------------------------------------------|
| [**\_endereço ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | Armazena dados de endereço ATM para soquetes baseados em ATM.             |
| [**\_BHLI ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | Identifica informações de B-HLI para um Soquete ATM associado. |
| [**\_BLLI ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | Identifica informações de B-LLI para um Soquete ATM associado. |
| [**SOCKADDR \_ ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | Armazena informações de endereço de soquete para Soquetes ATM.         |



 

Para serviços ATM nativos, use \_ o ATM AF para a família de endereços e a estrutura de endereço de soquete [**\_ ATM SOCKADDR**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) . Para abrir um Soquete ATM nativo, passe AF \_ ATM, Sock \_ RAW e ATMPROTO \_ AAL5 ou ATMPROTO \_ AALUSER para a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , respectivamente.

 

 



