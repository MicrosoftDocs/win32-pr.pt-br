---
description: As funções a seguir são implementadas no \_32.dll Ws2 e destinam-se a serem usadas por aplicativos que instalam provedores de serviço de namespace e o transporte do Windows Sockets em um computador.
ms.assetid: 3289737a-77b6-45d1-9c0a-3ed05b3475c2
title: Funções de instalação e configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c72bb3ddaedb0b1d97c52d961293c161fe63c7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164469"
---
# <a name="installation-and-configuration-functions"></a>Funções de instalação e configuração

As funções a seguir são implementadas no \_32.dll Ws2 e destinam-se a serem usadas por aplicativos que instalam provedores de serviço de namespace e o transporte do Windows Sockets em um computador. Essas funções não afetam os aplicativos em execução no momento, nem as alterações feitas por essas funções são visíveis para os aplicativos em execução no momento.

Para todos os provedores, um identificador de provedor é um GUID que é gerado pelo desenvolvedor do provedor (usando o utilitário Uuidgen.exe) e fornecido para Ws2 \_32.dll.



| Função                                                                      | Descrição                                                                                                                                              |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)                        | Remove um provedor de serviço de transporte do registro.                                                                                                  |
| [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32)                      | Remove o provedor de serviço de transporte de 32 bits especificado do registro em uma plataforma de 64 bits.                                                          |
| [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)                                | Recupera informações sobre protocolos de transporte disponíveis.                                                                                               |
| [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)                              | Recupera informações sobre protocolos de transporte disponíveis no catálogo de 32 bits em plataformas de 64 bits.                                                     |
| [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider)                            | Registra um novo provedor de serviços de transporte.                                                                                                              |
| [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32)                   | Registra um novo provedor de serviços de transporte nos bancos de dados de configuração do sistema de 32 bits e 64 bits em uma plataforma de 64 bits.                               |
| [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)            | Registra um novo provedor de serviço de transporte de 32 bits, bem como suas cadeias de protocolo específicas no banco de dados de configuração do sistema em uma plataforma de 32 bits.   |
| [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32) | Registra um novo provedor de transporte e suas cadeias de protocolo específicas nos bancos de dados de configuração do sistema de 32 bits e 64 bits em uma plataforma de 64 bits. |



 

 

 



