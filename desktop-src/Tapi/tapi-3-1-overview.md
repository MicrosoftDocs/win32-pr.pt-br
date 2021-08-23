---
description: A TAPI versão 3.1 é uma API baseada em COM que mescla telefonia IP e clássica. Os aplicativos possíveis variam de chamadas de voz simples pela PSTN (Rede pública de telefone comutado) até a conferência de IP multimídia multicast com QOS (qualidade de serviço).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: Visão geral do TAPI 3.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55aff75690894cc8c8a0d5e692b0c9b019a39116a617dbf2a4ae050200f6892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139889"
---
# <a name="tapi-31-overview"></a>Visão geral do TAPI 3.1

A TAPI versão 3.1 é uma API baseada em COM que mescla telefonia IP e clássica. Os aplicativos possíveis variam de chamadas de voz simples pela PSTN (Rede pública de telefone comutado) até a conferência de IP multimídia multicast com QOS (qualidade de serviço).

Para obter informações adicionais sobre os recursos de Telefonia IP da TAPI 3.1, consulte o white paper "Telefonia IP com TAPI 3", que pode ser encontrado no site da Microsoft.

Há quatro componentes principais do TAPI 3.1:

-   COM API
-   Servidor TAPI
-   TSPs (Provedores de Serviços de Telefonia)
-   Provedores de Fluxo de Mídia (MSPs)

O diagrama a seguir ilustra a arquitetura tapi 3.1:

![arquitetura tapi 3](images/callarc-gif-1.png)

A API é implementada como um conjunto de objetos COMPONENT OBJECT MODEL (COM). Mover a TAPI para o modelo COM orientado a objeto permite que os desenvolvedores escrevam aplicativos habilitados para TAPI em muitas linguagens, como Java, Visual Basic ou C/C++. O uso de COM permite atualizações de componentes de recursos tapi.

O processo do tapi server (TAPISRV) abstrai a TSPI (Interface do Provedor de Serviços) TAPI do TAPI 3.x e TAPI 2.x, permitindo que os Provedores de Serviços de Telefonia TAPI 2.x sejam usados com TAPI 3.x, mantendo o estado interno da TAPI. TAPISRV é implementado como um processo de serviço no SVCHOST.

[Provedores de Serviços abstraem](./tapi-service-providers.md) mecanismos de transporte de mídia específicos do provedor. Normalmente, eles existem em pares – um TSP (Provedor de Serviços de Telefonia) para controle de chamada e um MSP (Provedor de Serviços de Mídia) para controle de mídia.

[Os TSPs (Provedores](./telephony-service-providers-start-page.md) de Serviços de Telefonia) são responsáveis por resolver o modelo de chamada independente de protocolo da TAPI em mecanismos de controle de chamada específicos do protocolo. O TAPI 3.1 fornece compatibilidade com TAPI 2.1 TSPs. Dois provedores de serviços de Telefonia IP (e seus MSPs associados) são fornecidas por padrão com TAPI 3.1: o TSP H.323 e o TSP de Conferência multicast de IP.

[](media-service-providers-start-page.md) Os MSPs (Provedores de Serviços de Mídia) fornecem uma maneira uniforme de acessar os fluxos de mídia em uma chamada, dando suporte à API DirectShow<sup>TM</sup> como o manipulador de fluxo de mídia primário. Os MSPs tapi implementam DirectShow interfaces para um TSP específico e são necessários para qualquer serviço de telefonia que use DirectShow streaming. Fluxos genéricos são manipulados pelo aplicativo.

 

 
