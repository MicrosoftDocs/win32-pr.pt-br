---
title: Sobre o Gerenciador do grupo de multicast
description: Esta documentação descreve a tecnologia MGM (Gerenciador de grupos de multicast).
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- Gerenciador de grupos de multicast do RRAS
- Gerenciador de grupos multicast RRAS, descrito
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de grupo multicast
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de grupo multicast, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 034d37b99aaa9ca0139b5425cd5b85e7b3f280e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789737"
---
# <a name="about-multicast-group-manager"></a>Sobre o Gerenciador do grupo de multicast

Esta documentação descreve a tecnologia MGM (Gerenciador de grupos de multicast).

O multicast permite que um host envie dados somente para os destinos que solicitam a recepção dos dados. Dessa forma, o multicast difere do envio de dados de difusão, já que os dados de difusão são enviados para todos os hosts.

A difusão seletiva economiza largura de banda de rede porque os dados de multicast só são recebidos por esses hosts que solicitam os dados, e os dados viajam por qualquer link apenas uma vez. O multicast salva a largura de banda do servidor porque um servidor precisa enviar apenas uma mensagem de multicast por rede, em vez de uma mensagem unicast por destinatário. Exemplos de aplicativos multicast populares são reuniões online e rádio da Internet.

A API MGM permite que os desenvolvedores gravem protocolos de roteamento multicast que interoperam com roteadores que executam o Gerenciador de grupos de multicast.

Quando mais de um protocolo de roteamento multicast é habilitado em um roteador, o Gerenciador de grupo de multicast coordena as operações entre todos os protocolos de roteamento. O Gerenciador de grupos de multicast informa cada protocolo de roteamento quando ocorrerem alterações de associação de grupo e quando os dados de multicast de uma nova fonte ou destinados a um novo grupo são recebidos.

A API MGM fornece os seguintes recursos:

-   Registro de protocolo
-   Gerenciamento de grupos
-   Enumeração de entrada de encaminhamento de multicast (MFE)
-   Definições de retorno de chamada para protocolos de roteamento multicast

Esta visão geral descreve os componentes da arquitetura de multicast, os cenários de cliente que são usados para interoperar com o Gerenciador de grupo de multicast e considerações de programação para usar a API MGM.

 

 




