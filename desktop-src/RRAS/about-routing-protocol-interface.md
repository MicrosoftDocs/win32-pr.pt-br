---
title: Sobre a interface do protocolo de roteamento
description: A documentação a seguir descreve a integração de protocolos de roteamento de terceiros ao RRAS (serviço de roteamento e acesso remoto).
ms.assetid: 593e3b8a-6f26-47c6-aa93-520d36db7a6f
keywords:
- Serviço de roteamento e acesso remoto RRAS, interface do protocolo de roteamento
- Serviço de roteamento e acesso remoto RRAS, interface do protocolo de roteamento, descrito
- Interface do protocolo de roteamento RRAS
- Interface do protocolo de roteamento RRAS, descrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc663f249ca42ebbae509c164a828d603a9b968
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636348"
---
# <a name="about-routing-protocol-interface"></a>Sobre a interface do protocolo de roteamento

A documentação a seguir descreve a integração de protocolos de roteamento de terceiros ao RRAS (serviço de roteamento e acesso remoto). O RRAS é um recurso do Windows que funciona como um roteador de vários protocolos. O RRAS define a interface entre o Gerenciador de roteador e o protocolo de roteamento. O protocolo de roteamento é implementado em uma DLL (biblioteca de vínculo dinâmico).

Use essa interface para implementar protocolos de roteamento, como IGRP, NLSP e BGP, como DLLs de modo de usuário que funcionam com o RRAS.

Esta documentação descreve os seguintes tópicos:

-   [Adaptadores](adapters.md)
-   [Interfaces](interfaces.md)
-   [Rotas estáticas e auto-estáticas](static-and-autostatic-routes.md)

 

 




