---
description: Um provedor de serviços de mídia deve implementar um subconjunto mínimo de interfaces MSPI ITMSPAddress ITTerminalSupport ITStreamControl e ITStream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Escrevendo um provedor de serviços de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f99cc8a52b7362caa01d9743fea7fc848faec2ae451b96ec916f4f3aa5c287
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739016"
---
# <a name="writing-a-media-service-provider"></a>Escrevendo um provedor de serviços de mídia

Um provedor de serviços de mídia deve implementar um subconjunto mínimo de interfaces MSPI: [**ITMSPAddress,**](/windows/desktop/api/msp/nn-msp-itmspaddress) [**ITTerminalSupport,**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream). O suporte a SubStream é opcional. Além disso, um determinado MSP pode implementar métodos adicionais, como controles necessários para hardware especializado.

Os seguintes documentos de material:

-   As classes base do [TAPI 3 MSP,](tapi-3-msp-base-classes.md)que são um conjunto de classes C++ projetadas para simplificar a tarefa de criação de um MSP DirectShow baseado em DirectShow. As classes base implementam todas as interfaces MSPI de maneira genérica. Diferentes MSPs podem substituir funções específicas do MSP e fornecer suas próprias implementações.
-   O [Gerenciador de Terminal tapi 3,](tapi-3-terminal-manager.md)que fornece interfaces e métodos usados por um MSP para controlar terminais.
-   [Terminais plugáveis](writing-a-pluggable-terminal.md), que permitem que um aplicativo em vez de um MSP crie terminais. Os desenvolvedores que já têm experiência em escrever provedores de serviços serão os principais criadores de terminais que podem ser conectados. A versão inicial implementada para esta versão destina-se a conferência de aplicativos de servidor que precisam adicionar clientes não Windows 2000 ou não multicast a conferências multicast SDP/IP de tapi 3.

 

 
