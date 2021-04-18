---
description: Os controles do Call Center estendem o modelo de objeto TAPI 3 para dar suporte aos requisitos de sistemas AD (distribuição de chamada automática).
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Usando controles do Call Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc01cac4b068c5ec17ff5794e2e7ffff46dbf95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760322"
---
# <a name="using-call-center-controls"></a>Usando controles do Call Center

Os controles do Call Center estendem o modelo de objeto TAPI 3 para dar suporte aos requisitos de sistemas AD (distribuição de chamada automática). Uma central de atendimento é um local com agentes ou operadores em bancos de telefones, fazendo chamadas telefônicas de saída ou campos de entrada. Por exemplo, um banco ou uma empresa de cartão de crédito usará um Call Center para processar consultas de conta.

Os aplicativos de Call Center são divididos em três tipos básicos:

-   [Proxy ad](acd-proxy.md): trata as sessões de entrada ou saída no servidor, que podem ser qualquer coisa de um comutador telefônico proprietário para um gateway de Internet.
-   [Cliente do agente do AD](acd-agent-client.md): serviços um agente individual que está recebendo ou fazendo chamadas.
-   Cliente do supervisor do AD: fornece uma visão geral das operações do agente e do AD.

> [!Note]  
> Para o Windows 2000, a funcionalidade de proxy está disponível usando a TAPI 2,2, e as funções de supervisor não são implementadas.

 

A seção de exemplos do SDK do Windows contém exemplos de código AD em Netds \\ TAPI \\ Tapi2 \\ AD e Netds \\ TAPI \\ Tapi3 \\ AD.

 

 



