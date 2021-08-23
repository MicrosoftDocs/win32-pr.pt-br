---
description: Quando uma nova classe de serviço é instalada, uma estrutura WSASERVICECLASSINFO deve ser preparada e fornecida. Essa estrutura também consiste em subestruturas que contêm uma série de parâmetros que se aplicam a namespaces específicos.
ms.assetid: fb225e0c-a0c7-44e1-80fb-7b924b371afa
title: Estruturas de dados de classe de serviço na SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53eb2fd61c5ec6295b65128048bc9fe477ae63f78f89bfba4be73798002ead88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993557"
---
# <a name="service-class-data-structures-in-the-spi"></a>Estruturas de dados de classe de serviço na SPI

Quando uma nova classe de serviço é instalada, uma [**estrutura WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) deve ser preparada e fornecida. Essa estrutura também consiste em subestruturas que contêm uma série de parâmetros que se aplicam a namespaces específicos.

![Diagrama mostrando a estrutura WSASERVICECLASSINFO, subestruturas e parâmetros que se aplicam a namespaces específicos.](images/ovrvw3-3.png)

Para cada classe de serviço, há uma única [**estrutura WSASERVICECLASSINFO.**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) Dentro da estrutura **WSASERVICECLASSINFO,** o identificador exclusivo da classe de serviço está contido em **lpServiceClassId** e uma cadeia de caracteres de exibição associada é referenciada **por lpServiceClassName**.

O **membro lpClassInfos** na estrutura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) faz referência a uma matriz de estruturas [**WSANSCLASSINFO,**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) cada uma fornecendo um parâmetro nomeado e digitado que se aplica a um namespace especificado. Exemplos de valores para o **membro lpszName** incluem: SAPID, TCPPORT, UDPPORT, etc. Essas cadeias de caracteres geralmente são específicas para o namespace identificado **em dwNameSpace**. Os valores típicos **para dwValueType** podem ser REG \_ DWORD, REG \_ SZ etc. O **membro dwValueSize** indica o comprimento do item de dados apontado por **lpValue**.

Toda a coleção de dados representada em uma estrutura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) é fornecida para cada provedor de namespace por meio [**de NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass). Em seguida, cada provedor de namespace individual passa pela lista de estruturas [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) e mantém as informações aplicáveis a ele. Essa arquitetura também prevê a existência futura de um provedor de namespace especial que manteria todas as informações de esquema da classe de serviço para todos os namespaces. O Ws232.dll consultaria esse provedor para obter os dados \_ **WSASERVICECLASSINFO** necessários para fornecer aos provedores de namespace quando [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) for invocado para iniciar uma consulta e quando [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice) for invocado para registrar um serviço. O provedor de namespace não deve depender dessa funcionalidade por enquanto e, em vez disso, deve ter um meio específico do provedor para obter qualquer informação de esquema de classe de serviço necessária. Na ausência de um provedor que armazena todo o esquema de classe de serviço para todos os namespaces, o32.dll Ws2 usará \_ [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) para obter essas informações de cada provedor de namespace individual.

 

 



