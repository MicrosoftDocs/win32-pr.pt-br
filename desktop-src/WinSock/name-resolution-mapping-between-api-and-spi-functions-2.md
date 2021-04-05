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
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a><span data-ttu-id="00b63-103">Mapeamento de resolução de nomes entre as funções API e SPI</span><span class="sxs-lookup"><span data-stu-id="00b63-103">Name Resolution Mapping Between API and SPI Functions</span></span>

<span data-ttu-id="00b63-104">A instalação de classes de serviço, o registro de instâncias de serviço e as operações básicas de consulta todos mapeiam diretamente da API para o SPI.</span><span class="sxs-lookup"><span data-stu-id="00b63-104">The installation of service classes, registration of service instances and basic query operations all map fairly directly from the API to the SPI.</span></span> <span data-ttu-id="00b63-105">A função [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) não tem uma função correspondente no SPI, pois essa função é implementada em Ws2 \_32.dll fazendo uma chamada para [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).</span><span class="sxs-lookup"><span data-stu-id="00b63-105">The [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) function does not have a corresponding function in the SPI, as this function is implemented in Ws2\_32.dll by making a call to [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).</span></span>

<span data-ttu-id="00b63-106">As funções auxiliares [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) e [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) são mapeadas para as funções correspondentes na API de transporte, já que apenas um provedor de transporte saberá, necessariamente, como executar a tradução em uma estrutura [**SOCKADDR**](sockaddr-2.md) .</span><span class="sxs-lookup"><span data-stu-id="00b63-106">The helper functions [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) and [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) are mapped to the corresponding functions in the transport API, as only a transport provider will necessarily know how to perform the translation on a [**sockaddr**](sockaddr-2.md) structure.</span></span>

 

 



