---
description: Os controles do Call Center estendem o modelo de objeto TAPI 3 para dar suporte aos requisitos de sistemas AD (distribuição de chamada automática).
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Usando controles do Call Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f166658cce86faa0003b762ec697286a434a06b36b18ae92a861d1f6757fa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991536"
---
# <a name="using-call-center-controls"></a>Usando controles do Call Center

Os controles do Call Center estendem o modelo de objeto TAPI 3 para dar suporte aos requisitos de sistemas AD (distribuição de chamada automática). Uma central de atendimento é um local com agentes ou operadores em bancos de telefones, fazendo chamadas telefônicas de saída ou campos de entrada. Por exemplo, um banco ou uma empresa de cartão de crédito usará um Call Center para processar consultas de conta.

Os aplicativos de Call Center são divididos em três tipos básicos:

-   [Proxy ad](acd-proxy.md): trata as sessões de entrada ou saída no servidor, que podem ser qualquer coisa de um comutador telefônico proprietário para um gateway de Internet.
-   [Cliente do agente do AD](acd-agent-client.md): serviços um agente individual que está recebendo ou fazendo chamadas.
-   Cliente do supervisor do AD: fornece uma visão geral das operações do agente e do AD.

> [!Note]  
> para Windows 2000, a funcionalidade de proxy está disponível usando a TAPI 2,2, e as funções de supervisor não são implementadas.

 

a seção de exemplos do SDK do Windows contém exemplos de código ad em Netds \\ tapi \\ Tapi2 \\ ad e Netds \\ tapi \\ Tapi3 \\ ad.

 

 



