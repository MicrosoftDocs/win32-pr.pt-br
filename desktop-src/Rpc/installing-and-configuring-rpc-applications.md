---
title: Instalando e Configurando aplicativos RPC
description: Quando o sistema operacional Microsoft Windows é instalado em um servidor ou cliente, a instalação instala automaticamente os arquivos de tempo de execução RPC.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- Chamada de procedimento remoto RPC, tarefas, instalação e configuração de aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90837261c571276a74bb3a5354c7b9a5db2da6cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453725"
---
# <a name="installing-and-configuring-rpc-applications"></a>Instalando e Configurando aplicativos RPC

Quando o sistema operacional Microsoft Windows é instalado em um servidor ou cliente, a instalação instala automaticamente os arquivos de tempo de execução RPC. Nenhuma outra instalação de RPC é necessária. No entanto, você deve garantir que a versão do Windows instalada ofereça suporte a todos os recursos usados em seu aplicativo distribuído.

Ao usar um aplicativo RPC em um sistema operacional Windows 3. x ou Microsoft MS-DOS, você deve copiar os arquivos executáveis de tempo de execução RPC para os computadores com Windows 3. x ou MS-DOS que usarão o aplicativo. O diretório \\ mstools \\ RPC \_ rt16 no CD do SDK (Software Development Kit) da plataforma contém uma imagem de disco desses arquivos junto com um programa de instalação para instalar os arquivos. Use esta imagem de disco para criar um disco de instalação para distribuição com seu aplicativo RPC. Você também pode usar aplicativos cliente de 16 bits direcionados para o MS-DOS ou Windows em um sistema operacional Windows de 32 bits/64 bits. No entanto, o programa de instalação do aplicativo deve instalar os arquivos executáveis contidos nesta imagem de disco.

Ao criar um aplicativo RPC para um cliente Macintosh, você deve vincular os arquivos necessários ao aplicativo no momento da compilação. Nenhuma instalação adicional de RPC é necessária.

Para obter mais detalhes sobre os arquivos redistribuíveis e contratos de licenciamento, consulte \\ licença \\Redist.txt e \\ \\License.txt de licença no CD do Platform SDK.

Esta seção contém informações sobre como configurar aplicativos RPC em uma variedade de plataformas de hardware e software. Ele apresenta a discussão nas seguintes seções:

-   [Configurando o provedor de serviços de nome](configuring-the-name-service-provider.md)
-   [Informações do registro](registry-information.md)
-   [Usando RPC com proxy Winsock](using-rpc-with-winsock-proxy.md)
-   [Instalação de SPX/IPX](spx-ipx-installation.md)
-   [Configurando o servidor de segurança](configuring-the-security-server.md)

 

 




