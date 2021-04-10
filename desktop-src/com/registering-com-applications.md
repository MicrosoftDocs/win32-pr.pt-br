---
title: Registrando aplicativos COM
description: Registrando aplicativos COM
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292641"
---
# <a name="registering-com-applications"></a><span data-ttu-id="9ca56-103">Registrando aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="9ca56-103">Registering COM Applications</span></span>

<span data-ttu-id="9ca56-104">O registro é um banco de dados do sistema que contém informações sobre a configuração de hardware e software do sistema, bem como sobre os usuários do sistema.</span><span class="sxs-lookup"><span data-stu-id="9ca56-104">The registry is a system database that contains information about the configuration of system hardware and software as well as about users of the system.</span></span> <span data-ttu-id="9ca56-105">Qualquer programa baseado no Windows pode adicionar informações ao registro e ler as informações do registro.</span><span class="sxs-lookup"><span data-stu-id="9ca56-105">Any Windows-based program can add information to the registry and read information back from the registry.</span></span> <span data-ttu-id="9ca56-106">Os clientes pesquisam no registro os componentes interessantes a serem usados.</span><span class="sxs-lookup"><span data-stu-id="9ca56-106">Clients search the registry for interesting components to use.</span></span>

<span data-ttu-id="9ca56-107">O registro mantém informações sobre todos os objetos COM instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="9ca56-107">The registry maintains information about all the COM objects installed in the system.</span></span> <span data-ttu-id="9ca56-108">Sempre que um aplicativo cria uma instância de um componente COM, o registro é consultado para resolver o CLSID ou ProgID do componente no nome do caminho da DLL do servidor ou do EXE que o contém.</span><span class="sxs-lookup"><span data-stu-id="9ca56-108">Whenever an application creates an instance of a COM component, the registry is consulted to resolve either the CLSID or ProgID of the component into the pathname of the server DLL or EXE that contains it.</span></span> <span data-ttu-id="9ca56-109">Depois de determinar o servidor do componente, o Windows carrega o servidor no espaço de processo do aplicativo cliente (componentes em processo) ou inicia o servidor em seu próprio espaço de processo (servidores locais e remotos).</span><span class="sxs-lookup"><span data-stu-id="9ca56-109">After determining the component's server, Windows either loads the server into the process space of the client application (in-process components) or starts the server in its own process space (local and remote servers).</span></span> <span data-ttu-id="9ca56-110">O servidor cria uma instância do componente e retorna ao cliente uma referência a uma das interfaces do componente.</span><span class="sxs-lookup"><span data-stu-id="9ca56-110">The server creates an instance of the component and returns to the client a reference to one of the component's interfaces.</span></span>

<span data-ttu-id="9ca56-111">Para obter mais informações sobre o registro do Windows, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="9ca56-111">For more information about the Windows registry, see the following topics:</span></span>

-   [<span data-ttu-id="9ca56-112">Hierarquia do registro</span><span class="sxs-lookup"><span data-stu-id="9ca56-112">Registry Hierarchy</span></span>](registry-hierarchy.md)
-   [<span data-ttu-id="9ca56-113">Classes e servidores</span><span class="sxs-lookup"><span data-stu-id="9ca56-113">Classes and Servers</span></span>](classes-and-servers.md)
-   [<span data-ttu-id="9ca56-114">Classificando componentes</span><span class="sxs-lookup"><span data-stu-id="9ca56-114">Classifying Components</span></span>](classifying-components.md)
-   [<span data-ttu-id="9ca56-115">Usando OleView</span><span class="sxs-lookup"><span data-stu-id="9ca56-115">Using OleView</span></span>](using-oleview.md)
-   [<span data-ttu-id="9ca56-116">Registrando componentes</span><span class="sxs-lookup"><span data-stu-id="9ca56-116">Registering Components</span></span>](registering-components.md)
-   [<span data-ttu-id="9ca56-117">Verificando registro</span><span class="sxs-lookup"><span data-stu-id="9ca56-117">Checking Registration</span></span>](checking-registration.md)
-   [<span data-ttu-id="9ca56-118">Tipos de usuário desconhecidos</span><span class="sxs-lookup"><span data-stu-id="9ca56-118">Unknown User Types</span></span>](unknown-user-types.md)
-   [<span data-ttu-id="9ca56-119">Chaves do registro COM</span><span class="sxs-lookup"><span data-stu-id="9ca56-119">COM Registry Keys</span></span>](com-registry-keys.md)

 

 




