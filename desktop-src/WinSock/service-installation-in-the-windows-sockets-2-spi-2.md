---
description: Instalação do serviço na SPI Windows Sockets 2 (Winsock).
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Instalação do serviço na SPI Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faad2431add9b20ebd3358c48469f382596b658de1339525b147b094a7c3786c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740520"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a>Instalação do serviço na SPI Windows Sockets 2

-   [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

Quando a classe de serviço necessária ainda não existe, um cliente SPI de namespace usa [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) para instalar uma nova classe de serviço fornecendo um nome de classe de serviço, um GUID para o identificador de classe de serviço e uma série de [**estruturas WSANSCLASSINFO.**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) Essas estruturas são específicas de um namespace específico e fornecem valores comuns, como números de porta TCP recomendados ou Identificadores SAP do NetWare. Uma classe de serviço pode ser removida chamando [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) e fornecendo o GUID correspondente ao identificador de classe.

Depois que uma classe de serviço existir, instâncias específicas de um serviço poderão ser instaladas ou removidas por [**meio de NSPSetService.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice) Essa função aceita uma [**estrutura WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como um parâmetro de entrada junto com um código de operação e sinalizadores de operação. O código de operação indica se o serviço está sendo instalado ou removido. A estrutura **WSAQUERYSET** fornece todas as informações relevantes sobre o serviço, incluindo identificador de classe de serviço, nome do serviço (para esta instância), identificador de namespace e informações de protocolo aplicáveis e um conjunto de endereços de transporte aos quais o serviço escuta.

 

 



