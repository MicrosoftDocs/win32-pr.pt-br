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
# <a name="installing-and-configuring-rpc-applications"></a><span data-ttu-id="97c51-104">Instalando e Configurando aplicativos RPC</span><span class="sxs-lookup"><span data-stu-id="97c51-104">Installing and Configuring RPC Applications</span></span>

<span data-ttu-id="97c51-105">Quando o sistema operacional Microsoft Windows é instalado em um servidor ou cliente, a instalação instala automaticamente os arquivos de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="97c51-105">When the Microsoft Windows operating system is installed on a server or client, setup automatically installs the RPC run-time files.</span></span> <span data-ttu-id="97c51-106">Nenhuma outra instalação de RPC é necessária.</span><span class="sxs-lookup"><span data-stu-id="97c51-106">No further RPC installation is required.</span></span> <span data-ttu-id="97c51-107">No entanto, você deve garantir que a versão do Windows instalada ofereça suporte a todos os recursos usados em seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="97c51-107">You must ensure, however, that the version of Windows you install supports all the features used in your distributed application.</span></span>

<span data-ttu-id="97c51-108">Ao usar um aplicativo RPC em um sistema operacional Windows 3. x ou Microsoft MS-DOS, você deve copiar os arquivos executáveis de tempo de execução RPC para os computadores com Windows 3. x ou MS-DOS que usarão o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97c51-108">When you use an RPC application on a Windows 3.x or Microsoft MS-DOS operating system, you must copy the RPC run-time executable files to the Windows 3.x or MS-DOS computers that will be using the application.</span></span> <span data-ttu-id="97c51-109">O diretório \\ mstools \\ RPC \_ rt16 no CD do SDK (Software Development Kit) da plataforma contém uma imagem de disco desses arquivos junto com um programa de instalação para instalar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="97c51-109">The directory \\mstools\\rpc\_rt16 on the Platform Software Development Kit (SDK) CD contains a disk image of these files along with a setup program to install the files.</span></span> <span data-ttu-id="97c51-110">Use esta imagem de disco para criar um disco de instalação para distribuição com seu aplicativo RPC.</span><span class="sxs-lookup"><span data-stu-id="97c51-110">Use this disk image to create an install disk for distribution with your RPC application.</span></span> <span data-ttu-id="97c51-111">Você também pode usar aplicativos cliente de 16 bits direcionados para o MS-DOS ou Windows em um sistema operacional Windows de 32 bits/64 bits.</span><span class="sxs-lookup"><span data-stu-id="97c51-111">You can also use 16-bit client applications targeted toward MS-DOS or Windows on a 32-bit/64-bit Windows operating system.</span></span> <span data-ttu-id="97c51-112">No entanto, o programa de instalação do aplicativo deve instalar os arquivos executáveis contidos nesta imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="97c51-112">However, your application's installation program must install the executable files contained in this disk image.</span></span>

<span data-ttu-id="97c51-113">Ao criar um aplicativo RPC para um cliente Macintosh, você deve vincular os arquivos necessários ao aplicativo no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="97c51-113">When you build an RPC application for a Macintosh client, you must link the necessary files to the application at build time.</span></span> <span data-ttu-id="97c51-114">Nenhuma instalação adicional de RPC é necessária.</span><span class="sxs-lookup"><span data-stu-id="97c51-114">No additional RPC installation is needed.</span></span>

<span data-ttu-id="97c51-115">Para obter mais detalhes sobre os arquivos redistribuíveis e contratos de licenciamento, consulte \\ licença \\Redist.txt e \\ \\License.txt de licença no CD do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="97c51-115">For more details about redistributable files and licensing agreements, see \\LICENSE\\Redist.txt and \\LICENSE\\License.txt on the Platform SDK CD.</span></span>

<span data-ttu-id="97c51-116">Esta seção contém informações sobre como configurar aplicativos RPC em uma variedade de plataformas de hardware e software.</span><span class="sxs-lookup"><span data-stu-id="97c51-116">This section contains information about setting up RPC applications on a variety of hardware and software platforms.</span></span> <span data-ttu-id="97c51-117">Ele apresenta a discussão nas seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="97c51-117">It presents the discussion in the following sections:</span></span>

-   [<span data-ttu-id="97c51-118">Configurando o provedor de serviços de nome</span><span class="sxs-lookup"><span data-stu-id="97c51-118">Configuring the Name Service Provider</span></span>](configuring-the-name-service-provider.md)
-   [<span data-ttu-id="97c51-119">Informações do registro</span><span class="sxs-lookup"><span data-stu-id="97c51-119">Registry Information</span></span>](registry-information.md)
-   [<span data-ttu-id="97c51-120">Usando RPC com proxy Winsock</span><span class="sxs-lookup"><span data-stu-id="97c51-120">Using RPC with Winsock Proxy</span></span>](using-rpc-with-winsock-proxy.md)
-   [<span data-ttu-id="97c51-121">Instalação de SPX/IPX</span><span class="sxs-lookup"><span data-stu-id="97c51-121">SPX/IPX Installation</span></span>](spx-ipx-installation.md)
-   [<span data-ttu-id="97c51-122">Configurando o servidor de segurança</span><span class="sxs-lookup"><span data-stu-id="97c51-122">Configuring the Security Server</span></span>](configuring-the-security-server.md)

 

 




