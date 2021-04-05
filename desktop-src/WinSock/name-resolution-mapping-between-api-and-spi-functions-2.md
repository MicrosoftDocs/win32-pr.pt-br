---
description: A instalação de classes de serviço, o registro de instâncias de serviço e as operações básicas de consulta todos mapeiam diretamente da API para o SPI.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Mapeamento de resolução de nomes entre as funções API e SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a031ea8af72bb2733fc647c817a850ab7f311b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827108"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>Mapeamento de resolução de nomes entre as funções API e SPI

A instalação de classes de serviço, o registro de instâncias de serviço e as operações básicas de consulta todos mapeiam diretamente da API para o SPI. A função [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) não tem uma função correspondente no SPI, pois essa função é implementada em Ws2 \_32.dll fazendo uma chamada para [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).

As funções auxiliares [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) e [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) são mapeadas para as funções correspondentes na API de transporte, já que apenas um provedor de transporte saberá, necessariamente, como executar a tradução em uma estrutura [**SOCKADDR**](sockaddr-2.md) .

 

 



