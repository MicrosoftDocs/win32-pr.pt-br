---
title: Tutorial
description: Este tutorial orienta você pelas etapas necessárias para criar um aplicativo distribuído simples, de único cliente e de servidor único a partir de um aplicativo autônomo existente.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- RPC de chamada de procedimento remoto, tutorial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005883"
---
# <a name="tutorial"></a><span data-ttu-id="11260-104">Tutorial</span><span class="sxs-lookup"><span data-stu-id="11260-104">Tutorial</span></span>

<span data-ttu-id="11260-105">Este tutorial orienta você pelas etapas necessárias para criar um aplicativo distribuído simples, de único cliente e de servidor único a partir de um aplicativo autônomo existente.</span><span class="sxs-lookup"><span data-stu-id="11260-105">This tutorial takes you through the steps required to create a simple, single-client, single-server distributed application from an existing standalone application.</span></span> <span data-ttu-id="11260-106">Estas etapas são:</span><span class="sxs-lookup"><span data-stu-id="11260-106">These steps are:</span></span>

-   <span data-ttu-id="11260-107">Criar definição de interface e arquivos de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11260-107">Create interface definition and application configuration files.</span></span>
-   <span data-ttu-id="11260-108">Use o compilador MIDL para gerar cabeçalhos e stubs de cliente e de servidor C-Language a partir desses arquivos.</span><span class="sxs-lookup"><span data-stu-id="11260-108">Use the MIDL compiler to generate C-language client and server stubs and headers from those files.</span></span>
-   <span data-ttu-id="11260-109">Grave um aplicativo cliente que gerencia sua conexão com o servidor.</span><span class="sxs-lookup"><span data-stu-id="11260-109">Write a client application that manages its connection to the server.</span></span>
-   <span data-ttu-id="11260-110">Escreva um aplicativo de servidor que contenha os procedimentos remotos reais.</span><span class="sxs-lookup"><span data-stu-id="11260-110">Write a server application that contains the actual remote procedures.</span></span>
-   <span data-ttu-id="11260-111">Compile e vincule esses arquivos à biblioteca de tempo de execução RPC para produzir o aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="11260-111">Compile and link these files to the RPC run-time library to produce the distributed application.</span></span>

<span data-ttu-id="11260-112">O aplicativo cliente passa uma cadeia de caracteres para o servidor em uma chamada de procedimento remoto e o servidor imprime a cadeia de caracteres "Olá, mundo" para a saída padrão.</span><span class="sxs-lookup"><span data-stu-id="11260-112">The client application passes a character string to the server in a remote procedure call, and the server prints the string "Hello, World" to its standard output.</span></span>

<span data-ttu-id="11260-113">Os arquivos de origem completos para este aplicativo de exemplo, com código adicional para lidar com a entrada de linha de comando e para gerar várias mensagens de status para o usuário, estão no \\ diretório de saudação RPC do SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="11260-113">The complete source files for this example application, with additional code to handle command-line input and to output various status messages to the user, are in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="11260-114">Esta seção apresenta sua discussão nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="11260-114">This section presents its discussion in the following topics:</span></span>

-   [<span data-ttu-id="11260-115">O aplicativo autônomo</span><span class="sxs-lookup"><span data-stu-id="11260-115">The Standalone Application</span></span>](the-standalone-application.md)
-   [<span data-ttu-id="11260-116">Definindo a interface</span><span class="sxs-lookup"><span data-stu-id="11260-116">Defining the Interface</span></span>](defining-the-interface.md)
-   [<span data-ttu-id="11260-117">Gerando o UUID</span><span class="sxs-lookup"><span data-stu-id="11260-117">Generating the UUID</span></span>](generating-the-uuid.md)
-   [<span data-ttu-id="11260-118">O arquivo IDL</span><span class="sxs-lookup"><span data-stu-id="11260-118">The IDL File</span></span>](the-idl-file.md)
-   [<span data-ttu-id="11260-119">O arquivo ACF</span><span class="sxs-lookup"><span data-stu-id="11260-119">The ACF File</span></span>](the-acf-file.md)
-   [<span data-ttu-id="11260-120">Gerando os arquivos stub</span><span class="sxs-lookup"><span data-stu-id="11260-120">Generating the Stub Files</span></span>](generating-the-stub-files.md)
-   [<span data-ttu-id="11260-121">O aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="11260-121">The Client Application</span></span>](the-client-application.md)
-   [<span data-ttu-id="11260-122">O aplicativo de servidor</span><span class="sxs-lookup"><span data-stu-id="11260-122">The Server Application</span></span>](the-server-application.md)
-   [<span data-ttu-id="11260-123">Parando o aplicativo de servidor</span><span class="sxs-lookup"><span data-stu-id="11260-123">Stopping the Server Application</span></span>](stopping-the-server-application.md)
-   [<span data-ttu-id="11260-124">Compilando e vinculando</span><span class="sxs-lookup"><span data-stu-id="11260-124">Compiling and Linking</span></span>](compiling-and-linking.md)
-   [<span data-ttu-id="11260-125">Executando o aplicativo</span><span class="sxs-lookup"><span data-stu-id="11260-125">Running the Application</span></span>](running-the-application.md)

 

 




