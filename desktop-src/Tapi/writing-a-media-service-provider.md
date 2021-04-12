---
description: Um provedor de serviços de mídia deve implementar um subconjunto mínimo de interfaces MSPI ITMSPAddress ITTerminalSupport ITStreamControl e ITStream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Gravando um provedor de serviços de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782dddb9a87725bde7c104d459b71204a04de018
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297882"
---
# <a name="writing-a-media-service-provider"></a>Gravando um provedor de serviços de mídia

Um provedor de serviços de mídia deve implementar um subconjunto mínimo de interfaces MSPI: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream). O suporte a Subfluxo é opcional. Além disso, um determinado MSP pode implementar métodos adicionais, como os controles necessários para hardware especializado.

Os seguintes documentos materiais:

-   As [classes base TAPI 3 MSP](tapi-3-msp-base-classes.md), que são um conjunto de classes C++ projetadas para simplificar a tarefa de criar um MSP baseado em DirectShow. As classes base implementam todas as interfaces MSPI de maneira genérica. Diferentes MSPs podem substituir funções específicas do MSP e fornecer suas próprias implementações.
-   O [Gerenciador de terminal TAPI 3](tapi-3-terminal-manager.md), que fornece interfaces e métodos usados por um msp para controlar os terminais.
-   [Terminais conectáveis](writing-a-pluggable-terminal.md), que permitem a um aplicativo em vez de um MSP criar terminais. Os desenvolvedores que já tiverem experiência em escrever provedores de serviços serão os principais criadores de terminais conectáveis. A versão inicial implementada para esta versão destina-se a aplicativos de servidor de conferência que precisam adicionar clientes que não são do Windows 2000 ou não multicast a conferências multifuncionais de antivírus/IP de terceiros da TAPI 3.

 

 
