---
title: Arquivos gerados para uma interface COM
description: Para interfaces COM, o compilador MIDL combina todos os dados e rotinas auxiliares do servidor de objetos e do cliente em um único arquivo de proxy de interface.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- MIDL do compilador MIDL, MIDL e COM
- MIDL COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917228"
---
# <a name="files-generated-for-a-com-interface"></a><span data-ttu-id="760b0-105">Arquivos gerados para uma interface COM</span><span class="sxs-lookup"><span data-stu-id="760b0-105">Files Generated for a COM Interface</span></span>

<span data-ttu-id="760b0-106">Para interfaces COM, o compilador MIDL combina todos os dados e rotinas auxiliares do servidor de objetos e do cliente em um único arquivo de proxy de interface.</span><span class="sxs-lookup"><span data-stu-id="760b0-106">For COM interfaces, the MIDL compiler combines all client and object server auxiliary routines and data into a single interface proxy file.</span></span> <span data-ttu-id="760b0-107">Esse arquivo inclui os pontos de entrada substitutos para clientes e servidores.</span><span class="sxs-lookup"><span data-stu-id="760b0-107">This file includes the surrogate entry points for both clients and servers.</span></span> <span data-ttu-id="760b0-108">Além disso, o compilador MIDL gera um arquivo de cabeçalho de interface, um arquivo UUID de interface e um arquivo de registro de interface.</span><span class="sxs-lookup"><span data-stu-id="760b0-108">In addition, the MIDL compiler generates an interface header file, an interface UUID file and an interface registration file.</span></span> <span data-ttu-id="760b0-109">Você usará todos esses arquivos ao criar uma DLL de proxy que contém o código para dar suporte ao uso da interface por aplicativos cliente e servidores de objetos.</span><span class="sxs-lookup"><span data-stu-id="760b0-109">You will use all these files when creating a proxy DLL that contains the code to support the use of the interface by both client applications and object servers.</span></span> <span data-ttu-id="760b0-110">Você também usará o arquivo de cabeçalho da interface e o arquivo UUID da interface ao criar o arquivo executável para um aplicativo cliente que usa a interface.</span><span class="sxs-lookup"><span data-stu-id="760b0-110">You will also use the interface header file and the interface UUID file when creating the executable file for a client application that uses the interface.</span></span>

<span data-ttu-id="760b0-111">Os tópicos a seguir descrevem cada um dos arquivos gerados para uma interface COM personalizada, que você identifica, incluindo o **\[** [](object.md) **\]** atributo Object na lista atributo de interface do arquivo IDL:</span><span class="sxs-lookup"><span data-stu-id="760b0-111">The following topics describe each of the files generated for a custom COM interface, which you identify by including the **\[**[**object**](object.md)**\]** attribute in the interface attribute list of the IDL file:</span></span>

-   [<span data-ttu-id="760b0-112">O arquivo de proxy da interface</span><span class="sxs-lookup"><span data-stu-id="760b0-112">The Interface Proxy File</span></span>](the-interface-proxy-file.md)
-   [<span data-ttu-id="760b0-113">Os arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="760b0-113">The Header Files</span></span>](the-header-files.md)
-   [<span data-ttu-id="760b0-114">O arquivo UUID de interface</span><span class="sxs-lookup"><span data-stu-id="760b0-114">The Interface UUID File</span></span>](the-interface-uuid-file.md)
-   [<span data-ttu-id="760b0-115">O arquivo de registro da interface</span><span class="sxs-lookup"><span data-stu-id="760b0-115">The Interface Registration File</span></span>](the-interface-registration-file.md)

<span data-ttu-id="760b0-116">Para obter mais informações, consulte [arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md), [**\_ configuração de/App**](-app-config.md), arquivo de definição de [interface (IDL)](interface-definition-idl-file.md)e [compilando e registrando uma DLL de proxy](../com/building-and-registering-a-proxy-dll.md).</span><span class="sxs-lookup"><span data-stu-id="760b0-116">For more information, see [Application Configuration File (ACF)](application-configuration-file-acf-.md), [**/app\_config**](-app-config.md), [Interface Definition (IDL) File](interface-definition-idl-file.md), and [Building and Registering a Proxy DLL](../com/building-and-registering-a-proxy-dll.md).</span></span>

 

 