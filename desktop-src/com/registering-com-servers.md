---
title: Registrando servidores COM
description: Registrando servidores COM
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084912"
---
# <a name="registering-com-servers"></a><span data-ttu-id="d25ac-103">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="d25ac-103">Registering COM Servers</span></span>

<span data-ttu-id="d25ac-104">Depois de definir uma classe no código (garantindo que ela implemente [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) ou [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) e atribuída a ela um CLSID, você precisa colocar as informações no registro que permitirá com, na solicitação de um cliente com o CLSID, para criar instâncias de seus objetos.</span><span class="sxs-lookup"><span data-stu-id="d25ac-104">After you have defined a class in code (ensuring that it implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) and assigned it a CLSID, you need to put information in the registry that will allow COM, on request of a client with the CLSID, to create instances of its objects.</span></span> <span data-ttu-id="d25ac-105">Essas informações dizem ao sistema, para um determinado CLSID, onde o código DLL ou EXE para essa classe está localizado e como ele deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="d25ac-105">This information tells the system, for a given CLSID, where the DLL or EXE code for that class is located and how it is to be launched.</span></span>

<span data-ttu-id="d25ac-106">Há mais de uma maneira de registrar uma classe no registro.</span><span class="sxs-lookup"><span data-stu-id="d25ac-106">There is more than one way of registering a class in the registry.</span></span> <span data-ttu-id="d25ac-107">Além disso, há outras maneiras de "registrar" uma classe com o sistema quando ele está em execução, para que o sistema esteja ciente de que um objeto em execução está atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="d25ac-107">In addition, there are other ways of "registering" a class with the system when it is running, so that the system is aware that a running object is currently in the system.</span></span>

<span data-ttu-id="d25ac-108">Consulte os tópicos a seguir para obter mais informações sobre como registrar-se:</span><span class="sxs-lookup"><span data-stu-id="d25ac-108">See the following topics for more information about registering:</span></span>

-   [<span data-ttu-id="d25ac-109">Registrando uma classe na instalação</span><span class="sxs-lookup"><span data-stu-id="d25ac-109">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
-   [<span data-ttu-id="d25ac-110">Registrando um servidor EXE em execução</span><span class="sxs-lookup"><span data-stu-id="d25ac-110">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
-   [<span data-ttu-id="d25ac-111">Registrando objetos no corrompidos</span><span class="sxs-lookup"><span data-stu-id="d25ac-111">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
-   [<span data-ttu-id="d25ac-112">Registro automático</span><span class="sxs-lookup"><span data-stu-id="d25ac-112">Self-Registration</span></span>](self-registration.md)
-   [<span data-ttu-id="d25ac-113">Instalando como um aplicativo de serviço</span><span class="sxs-lookup"><span data-stu-id="d25ac-113">Installing as a Service Application</span></span>](installing-as-a-service-application.md)

## <a name="related-topics"></a><span data-ttu-id="d25ac-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d25ac-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d25ac-115">Responsabilidades do servidor COM</span><span class="sxs-lookup"><span data-stu-id="d25ac-115">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 