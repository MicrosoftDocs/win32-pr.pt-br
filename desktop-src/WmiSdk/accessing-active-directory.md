---
description: Active Directory é o serviço de diretório do Windows e é a base das redes distribuídas do Windows.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Acessando Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171457"
---
# <a name="accessing-active-directory"></a><span data-ttu-id="7bb2d-103">Acessando Active Directory</span><span class="sxs-lookup"><span data-stu-id="7bb2d-103">Accessing Active Directory</span></span>

<span data-ttu-id="7bb2d-104">Active Directory é o serviço de diretório do Windows e é a base das redes distribuídas do Windows.</span><span class="sxs-lookup"><span data-stu-id="7bb2d-104">Active Directory is the directory service for Windows and is the foundation of Windows distributed networks.</span></span> <span data-ttu-id="7bb2d-105">Você pode usar Active Directory para localizar objetos em um domínio de rede de computador, como usuários, políticas de segurança, impressoras, componentes distribuídos e outros recursos.</span><span class="sxs-lookup"><span data-stu-id="7bb2d-105">You can use Active Directory to locate objects in a computer network domain, such as users, security policies, printers, distributed components, and other resources.</span></span> <span data-ttu-id="7bb2d-106">O nome Active Directory se refere ao serviço de diretório e ao próprio diretório.</span><span class="sxs-lookup"><span data-stu-id="7bb2d-106">The name Active Directory refers both to the directory service and the directory itself.</span></span>

> [!Note]  
> <span data-ttu-id="7bb2d-107">Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="7bb2d-107">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="7bb2d-108">O Windows torna Active Directory acessível por meio do WMI criando um conjunto de referências a cada classe e objeto contidos no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7bb2d-108">Windows makes Active Directory accessible through WMI by creating a set of references to every class and object contained in Active Directory.</span></span> <span data-ttu-id="7bb2d-109">Ao acessar o provedor de serviços de diretório por meio do WMI, você pode criar aplicativos habilitados para WMI que podem acessar a riqueza de informações contidas no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7bb2d-109">By accessing the Directory Services provider through WMI, you can create WMI-enabled applications that can access the wealth of information contained in Active Directory.</span></span>

<span data-ttu-id="7bb2d-110">Com essas interfaces, você pode:</span><span class="sxs-lookup"><span data-stu-id="7bb2d-110">With these interfaces, you can:</span></span>

-   <span data-ttu-id="7bb2d-111">Recupere classes e instâncias.</span><span class="sxs-lookup"><span data-stu-id="7bb2d-111">Retrieve classes and instances.</span></span>
-   <span data-ttu-id="7bb2d-112">Enumere classes e instâncias.</span><span class="sxs-lookup"><span data-stu-id="7bb2d-112">Enumerate classes and instances.</span></span>
-   <span data-ttu-id="7bb2d-113">Crie novas instâncias.</span><span class="sxs-lookup"><span data-stu-id="7bb2d-113">Create new instances.</span></span>
-   <span data-ttu-id="7bb2d-114">Modifique as instâncias existentes.</span><span class="sxs-lookup"><span data-stu-id="7bb2d-114">Modify existing instances.</span></span>
-   <span data-ttu-id="7bb2d-115">Excluir instâncias existentes.</span><span class="sxs-lookup"><span data-stu-id="7bb2d-115">Delete existing instances.</span></span>
-   <span data-ttu-id="7bb2d-116">Active Directory de consulta.</span><span class="sxs-lookup"><span data-stu-id="7bb2d-116">Query Active Directory.</span></span>

<span data-ttu-id="7bb2d-117">Os tópicos a seguir podem ajudá-lo a usar o Active Directory com o WMI:</span><span class="sxs-lookup"><span data-stu-id="7bb2d-117">The following topics can assist you in using Active Directory with WMI:</span></span>

-   [<span data-ttu-id="7bb2d-118">Usando a sintaxe de Active Directory apropriada</span><span class="sxs-lookup"><span data-stu-id="7bb2d-118">Using the Proper Active Directory Syntax</span></span>](using-the-proper-active-directory-syntax.md)
-   [<span data-ttu-id="7bb2d-119">Mapeando Active Directory para o WMI</span><span class="sxs-lookup"><span data-stu-id="7bb2d-119">Mapping Active Directory to WMI</span></span>](mapping-active-directory-to-wmi.md)

 

 



