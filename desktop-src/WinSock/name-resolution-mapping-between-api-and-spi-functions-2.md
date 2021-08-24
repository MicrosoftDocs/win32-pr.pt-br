---
description: A instalação de classes de serviço, o registro de instâncias de serviço e operações de consulta básicas são mapeado diretamente da API para a SPI.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Mapeamento de resolução de nomes entre funções API e SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad02896ea15fb1b7c7e2aa2e01d9ec0727492da43d0446819dd1f2e04ad591d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733620"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>Mapeamento de resolução de nomes entre funções API e SPI

A instalação de classes de serviço, o registro de instâncias de serviço e operações de consulta básicas são mapeado diretamente da API para a SPI. A [**função WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) não tem uma função correspondente na SPI, pois essa função é implementada no Ws232.dll fazendo uma chamada para \_ [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).

As funções auxiliares [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) e [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) são mapeadas para as funções correspondentes na API de transporte, pois apenas um provedor de transporte necessariamente sabe como executar a tradução em uma estrutura [**sockaddr.**](sockaddr-2.md)

 

 



