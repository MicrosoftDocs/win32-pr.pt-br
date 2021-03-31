---
description: A ordem na qual os provedores de serviço de transporte são instalados inicialmente controla a ordem na qual eles são enumerados por meio de WSCEnumProtocols e WSCEnumProtocols32 na interface do provedor de serviço ou por meio de WSAEnumProtocols na interface do aplicativo. O mais importante é que essa ordem também governa a ordem em que os protocolos e provedores de serviço são considerados quando um cliente solicita a criação de um soquete com base em sua família de endereços, tipo e identificador de protocolo.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Ordenação do provedor de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c23d9357d30c94b084bf6288013c38a2d46a4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827735"
---
# <a name="service-provider-ordering"></a>Ordenação do provedor de serviço

A ordem na qual os provedores de serviço de transporte são instalados inicialmente controla a ordem na qual eles são enumerados por meio de [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) e [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) na interface do provedor de serviço ou por meio de [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) na interface do aplicativo. O mais importante é que essa ordem também governa a ordem em que os protocolos e provedores de serviço são considerados quando um cliente solicita a criação de um soquete com base em sua família de endereços, tipo e identificador de protocolo.

O Windows Sockets 2 inclui um applet chamado Sporder.exe que permite que o catálogo de protocolos instalados seja reordenado interativamente depois que os protocolos já tiverem sido instalados. O Winsock também inclui uma DLL auxiliar, Sporder.dll, que exporta uma interface de procedimento para reordenar protocolos. Essa interface de procedimento consiste em um único procedimento chamado [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

A definição de interface pode ser importada para um programa C ou C++ por meio da inclusão de arquivo de seqüência. h. O ponto de entrada pode ser vinculado por meio do arquivo lib de enorder. lib.

 

 



