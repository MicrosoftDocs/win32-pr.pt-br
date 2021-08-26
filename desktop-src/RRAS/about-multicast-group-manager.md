---
title: Sobre o Gerenciador de Grupos multicast
description: Esta documentação descreve a tecnologia MGM (Multicast Group Manager).
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- RRAS do Gerenciador de Grupos multicast
- RRAS do Gerenciador de Grupos multicast, descrito
- RRAS do Serviço de Roteamento e Acesso Remoto, Gerenciador de Grupos multicast
- RRAS do Serviço de Roteamento e Acesso Remoto, Gerenciador de Grupos multicast, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f83dc2b212f7d70d04b4a3ec08bf07e664fa2d67d9c638233a4e8e914369c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030926"
---
# <a name="about-multicast-group-manager"></a>Sobre o Gerenciador de Grupos multicast

Esta documentação descreve a tecnologia MGM (Multicast Group Manager).

Multicasting permite que um host envie dados somente para os destinos que solicitam especificamente receber os dados. Dessa forma, o multicast é diferente do envio de dados de difusão, pois os dados de difusão são enviados para todos os hosts.

O multicast economiza largura de banda de rede porque os dados multicast são recebidos apenas pelos hosts que solicitam os dados e os dados percorrem qualquer link apenas uma vez. O multicasting salva a largura de banda do servidor porque um servidor precisa enviar apenas uma mensagem multicast por rede, em vez de uma mensagem unicast por receptor. Exemplos de aplicativos multicast populares são reuniões online e rádio via Internet.

A API do MGM permite que os desenvolvedores escrevam protocolos de roteamento multicast que interoperam com roteadores que executam o gerenciador de grupos multicast.

Quando mais de um protocolo de roteamento multicast está habilitado em um roteador, o gerenciador de grupos multicast coordena as operações entre todos os protocolos de roteamento. O gerenciador de grupos multicast informa cada protocolo de roteamento quando ocorrem alterações de associação de grupo e quando dados multicast de uma nova fonte ou destinados a um novo grupo são recebidos.

A API do MGM fornece os seguintes recursos:

-   Registro de protocolo
-   Gerenciamento de grupos
-   Enumeração MFE (entrada de encaminhamento multicast)
-   Definições de retorno de chamada para protocolos de roteamento multicast

Esta visão geral descreve os componentes da arquitetura multicast, os cenários de cliente usados para interoperar com o gerenciador de grupos multicast e considerações de programação para usar a API do MGM.

 

 




