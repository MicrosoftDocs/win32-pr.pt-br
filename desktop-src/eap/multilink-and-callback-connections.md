---
title: Conexões Multilink e de retorno de chamada
description: Para o primeiro link em uma conexão de vínculos múltiplos, o serviço de autenticação define o sinalizador de \_ vínculo do sinalizador EAP RAS \_ \_ primeiro \_ no membro fFlags da \_ estrutura de entrada PPP EAP \_ .
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7493550863a755a87668c96dbe0ce600d524a111b7e7300b97c307f4d30c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852316"
---
# <a name="multilink-and-callback-connections"></a>Conexões Multilink e de retorno de chamada

Para o primeiro link em uma conexão de vínculos múltiplos, o serviço de autenticação define o sinalizador de \_ vínculo do sinalizador EAP RAS \_ \_ primeiro \_ no membro **FFlags** da estrutura de [**\_ \_ entrada PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) . O protocolo de autenticação pode usar a presença desse sinalizador para determinar se deve apresentar uma interface do usuário especificamente para o primeiro link de uma conexão de vínculos múltiplos.

Se a conexão estiver configurada para que o servidor chame de volta o computador cliente, o sinalizador de \_ \_ primeiro link do sinalizador EAP RAS \_ \_ não será definido no retorno de chamada.

Se o protocolo de autenticação definir o membro **fSaveConnectionData** da [**saída do PPP \_ \_ EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) como **true**, os links subsequentes na conexão Multilink receberão os novos dados específicos da conexão. No caso de dados específicos do usuário, no entanto, o protocolo de autenticação continua a obter os dados originais específicos do usuário, mesmo que ele defina o membro **fSaveUserData** da **saída do PPP \_ \_ EAP** como **true**.

O protocolo de autenticação pode usar uma [interface do usuário interativa](interactive-user-interface.md) para coletar dados de um link específico de uma conexão de vínculos múltiplos. Nesse caso, o serviço de autenticação disponibiliza os dados resultantes para o protocolo de autenticação durante os links subsequentes. No entanto, esses dados nunca são salvos no armazenamento persistente.

 

 




