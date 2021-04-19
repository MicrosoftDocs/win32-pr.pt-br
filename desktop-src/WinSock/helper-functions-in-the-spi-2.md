---
description: NSPGetServiceClassInfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: Funções auxiliares no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e687529bf1ede1598225708cf288e49bb7e9b5c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793297"
---
# <a name="helper-functions-in-the-spi"></a>Funções auxiliares no SPI

-   [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

A função [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) recupera informações de esquema de classe de serviço que foram retidas por um provedor de namespace. Ele também é usado pela DLL do Windows Sockets 2 em sua implementação de [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).

As macros a seguir definidas no arquivo de cabeçalho *Svcguid. h* e podem ajudar no mapeamento entre classes de serviço conhecidas e esses namespaces.

| Nome da macro                                                                              | Descrição                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **SVCID \_ TCP (porta)**<br/> **SVCID \_ UDP (porta)**<br/>                         | Dada uma porta TCP ou UDP para o protocolo de Internet, retorna o GUID.                                                                               |
| **é \_ SVCID \_ TCP (GUID)**<br/> **é \_ SVCID \_ UDP (GUID)**<br/>                 | Retornará **true** se o GUID para TCP ou UDP estiver dentro do intervalo permitido.                                                                         |
| **PORTA \_ de \_ SVCID \_ TCP (GUID)**<br/> **PORTA \_ do \_ SVCID \_ UDP (GUID)**<br/> | Retorna a porta TCP ou UDP associada ao GUID.                                                                                              |
| **SVCID \_ NetWare (SAPID)**<br/>                                                    | Dado o identificador do protocolo SAP, retorna o GUID. Essa macro é usada com o namespace do SAP em um ambiente do NetWare. |
| **SAPId \_ da \_ SVCID \_ NetWare (GUID)**<br/>                                        | Retorna o identificador SAP do NetWare associado ao GUID. Essa macro é usada com o namespace do SAP em um ambiente do NetWare.               |
| **é \_ SVCID \_ NetWare (GUID)**<br/>                                                 | Retornará **true** se o GUID para NetWare estiver dentro do intervalo permitido. Essa macro é usada com o namespace do SAP em um ambiente do NetWare.    |



 

> [!Note]  
> O arquivo de cabeçalho *Svcguid. h* não é incluído automaticamente pelo arquivo de cabeçalho *Winsock2. h* .

 

 

 




