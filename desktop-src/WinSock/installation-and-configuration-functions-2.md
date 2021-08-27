---
description: As funções a seguir são implementadas no Ws232.dll e devem ser usadas por aplicativos que instalam provedores de serviço de namespace e transporte Windows Sockets em um \_ computador.
ms.assetid: 3289737a-77b6-45d1-9c0a-3ed05b3475c2
title: Funções de instalação e configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0731eff882c614c19c20d8323d012a7656fc2d8c15072aaafef3d7c91e46e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097856"
---
# <a name="installation-and-configuration-functions"></a>Funções de instalação e configuração

As funções a seguir são implementadas no Ws232.dll e devem ser usadas por aplicativos que instalam provedores de serviço de namespace e transporte Windows Sockets em um \_ computador. Essas funções não afetam os aplicativos em execução no momento, nem as alterações feitas por essas funções são visíveis para aplicativos em execução no momento.

Para todos os provedores, um identificador de provedor é um GUID que é gerado pelo desenvolvedor do provedor (usando o utilitário Uuidgen.exe) e fornecido ao Ws2 \_32.dll.



| Função                                                                      | Descrição                                                                                                                                              |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)                        | Remove um provedor de serviços de transporte do Registro.                                                                                                  |
| [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32)                      | Remove o provedor de serviços de transporte de 32 bits especificado do Registro em uma plataforma de 64 bits.                                                          |
| [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)                                | Recupera informações sobre protocolos de transporte disponíveis.                                                                                               |
| [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)                              | Recupera informações sobre protocolos de transporte disponíveis no catálogo de 32 bits em plataformas de 64 bits.                                                     |
| [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider)                            | Registra um novo provedor de serviços de transporte.                                                                                                              |
| [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32)                   | Registra um novo provedor de serviços de transporte nos bancos de dados de configuração do sistema de 32 bits e 64 bits em uma plataforma de 64 bits.                               |
| [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)            | Registra um novo provedor de serviços de transporte de 32 bits, bem como suas cadeias de protocolo específicas no banco de dados de configuração do sistema em uma plataforma de 32 bits.   |
| [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32) | Registra um novo provedor de transporte e suas cadeias de protocolo específicas nos bancos de dados de configuração do sistema de 32 bits e 64 bits em uma plataforma de 64 bits. |



 

 

 



