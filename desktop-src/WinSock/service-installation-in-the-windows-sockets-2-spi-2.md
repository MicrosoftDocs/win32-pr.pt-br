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
# <a name="service-installation-in-the-windows-sockets-2-spi"></a>Instalação de serviço no SPI do Windows Sockets 2

-   [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

Quando a classe de serviço necessária ainda não existir, um cliente SPI de namespace usará [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) para instalar uma nova classe de serviço fornecendo um nome de classe de serviço, um GUID para o identificador de classe de serviço e uma série de estruturas [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) . Essas estruturas são específicas para um namespace específico e fornecem valores comuns, como números de porta TCP recomendados ou identificadores SAP do NetWare. Uma classe de serviço pode ser removida chamando [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) e fornecendo o GUID correspondente ao identificador de classe.

Quando existe uma classe de serviço, as instâncias específicas de um serviço podem ser instaladas ou removidas por meio de [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice). Essa função usa uma estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como um parâmetro de entrada junto com um código de operação e sinalizadores de operação. O código da operação indica se o serviço está sendo instalado ou removido. A estrutura **WSAQUERYSET** fornece todas as informações relevantes sobre o serviço, incluindo o identificador de classe de serviço, o nome do serviço (para essa instância), o identificador de namespace aplicável e as informações de protocolo e um conjunto de endereços de transporte para os quais o serviço escuta.

 

 



