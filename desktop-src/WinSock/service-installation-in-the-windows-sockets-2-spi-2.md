---
description: Instalação do serviço no SPI do Windows Sockets 2 (Winsock).
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Instalação de serviço no SPI do Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9028f35c21cc7055e8b8dde060c1c178dbf76715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813328"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a><span data-ttu-id="a32f4-103">Instalação de serviço no SPI do Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="a32f4-103">Service Installation in the Windows Sockets 2 SPI</span></span>

-   [<span data-ttu-id="a32f4-104">**NSPInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="a32f4-104">**NSPInstallServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [<span data-ttu-id="a32f4-105">**NSPRemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="a32f4-105">**NSPRemoveServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [<span data-ttu-id="a32f4-106">**NSPSetService**</span><span class="sxs-lookup"><span data-stu-id="a32f4-106">**NSPSetService**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

<span data-ttu-id="a32f4-107">Quando a classe de serviço necessária ainda não existir, um cliente SPI de namespace usará [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) para instalar uma nova classe de serviço fornecendo um nome de classe de serviço, um GUID para o identificador de classe de serviço e uma série de estruturas [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) .</span><span class="sxs-lookup"><span data-stu-id="a32f4-107">When the required service class does not already exist, a namespace SPI client uses [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="a32f4-108">Essas estruturas são específicas para um namespace específico e fornecem valores comuns, como números de porta TCP recomendados ou identificadores SAP do NetWare.</span><span class="sxs-lookup"><span data-stu-id="a32f4-108">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="a32f4-109">Uma classe de serviço pode ser removida chamando [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) e fornecendo o GUID correspondente ao identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="a32f4-109">A service class can be removed by calling [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="a32f4-110">Quando existe uma classe de serviço, as instâncias específicas de um serviço podem ser instaladas ou removidas por meio de [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice).</span><span class="sxs-lookup"><span data-stu-id="a32f4-110">Once a service class exists, specific instances of a service can be installed or removed via [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice).</span></span> <span data-ttu-id="a32f4-111">Essa função usa uma estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como um parâmetro de entrada junto com um código de operação e sinalizadores de operação.</span><span class="sxs-lookup"><span data-stu-id="a32f4-111">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="a32f4-112">O código da operação indica se o serviço está sendo instalado ou removido.</span><span class="sxs-lookup"><span data-stu-id="a32f4-112">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="a32f4-113">A estrutura **WSAQUERYSET** fornece todas as informações relevantes sobre o serviço, incluindo o identificador de classe de serviço, o nome do serviço (para essa instância), o identificador de namespace aplicável e as informações de protocolo e um conjunto de endereços de transporte para os quais o serviço escuta.</span><span class="sxs-lookup"><span data-stu-id="a32f4-113">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses to which the service listens.</span></span>

 

 



