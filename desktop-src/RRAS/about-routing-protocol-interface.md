---
title: Sobre a interface de protocolo de roteamento
description: A documentação a seguir descreve a integração de protocolos de roteamento de terceiros ao RRAS (Serviço de Roteamento e Acesso Remoto).
ms.assetid: 593e3b8a-6f26-47c6-aa93-520d36db7a6f
keywords:
- Roteamento e RRAS do Serviço de Acesso Remoto, Interface de Protocolo de Roteamento
- Roteamento e RRAS do Serviço de Acesso Remoto, Interface de Protocolo de Roteamento, descrito
- Interface de protocolo de roteamento RRAS
- Interface de protocolo de roteamento RRAS , descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76689e0e7ca40c2677491fc0673c596c902a73ee85b677161c208fe71d090367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792113"
---
# <a name="about-routing-protocol-interface"></a>Sobre a interface de protocolo de roteamento

A documentação a seguir descreve a integração de protocolos de roteamento de terceiros ao RRAS (Serviço de Roteamento e Acesso Remoto). O RRAS é um recurso de Windows que atua como um roteador de vários protocolos. O RRAS define a interface entre o gerenciador de roteador e o protocolo de roteamento. O protocolo de roteamento é implementado em uma DLL (biblioteca de vínculo dinâmico).

Use essa interface para implementar protocolos de roteamento, como IGRP, NLSP e BGP, como DLLs de modo de usuário que funcionam com RRAS.

Esta documentação descreve os seguintes tópicos:

-   [Adaptadores](adapters.md)
-   [Interfaces](interfaces.md)
-   [Rotas estáticas e estáticas](static-and-autostatic-routes.md)

 

 




