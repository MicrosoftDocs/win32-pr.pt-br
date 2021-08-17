---
description: A ordem na qual os provedores de serviços de transporte são inicialmente instalados rege a ordem na qual eles são enumerados por meio de WSCEnumProtocols e WSCEnumProtocols32 na interface do provedor de serviços ou por meio de WSAEnumProtocols na interface do aplicativo. Mais importante, essa ordem também rege a ordem na qual protocolos e provedores de serviços são considerados quando um cliente solicita a criação de um soquete com base em sua família de endereços, tipo e identificador de protocolo.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Ordenação do provedor de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445fcc0cadafae8fd61ee2e34a872485b67466037c1dc71e34ab173156c8d9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740577"
---
# <a name="service-provider-ordering"></a>Ordenação do provedor de serviços

A ordem na qual os provedores de serviços de transporte são inicialmente instalados rege a ordem na qual eles são enumerados por meio de [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) e [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) na interface do provedor de serviços ou por meio [**de WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) na interface do aplicativo. Mais importante, essa ordem também rege a ordem na qual protocolos e provedores de serviços são considerados quando um cliente solicita a criação de um soquete com base em sua família de endereços, tipo e identificador de protocolo.

Windows Os soquetes 2 incluem um applet chamado Sporder.exe que permite que o catálogo de protocolos instalados seja reordenado interativamente depois que os protocolos já foram instalados. O Winsock também inclui uma DLL auxiliar, Sporder.dll, que exporta uma interface de procedimento para reordenar protocolos. Essa interface de procedimento consiste em um único procedimento chamado [**WSCWriteProviderOrder.**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder)

A definição da interface pode ser importada para um programa C ou C++ por meio do arquivo de inclusão Sporder.h. O ponto de entrada pode ser vinculado por meio do arquivo lib Sporder.lib.

 

 



