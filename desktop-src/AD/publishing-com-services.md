---
title: Publicando serviços COM+
description: Os serviços baseados em COM fornecem um proxy de aplicativo na forma de um pacote do Windows Installer (MSI).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Publicando serviços COM+
- Active Directory, usando, publicando um serviço, serviços COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004904"
---
# <a name="publishing-com-services"></a><span data-ttu-id="13293-105">Publicando serviços COM+</span><span class="sxs-lookup"><span data-stu-id="13293-105">Publishing COM+ Services</span></span>

<span data-ttu-id="13293-106">Os serviços baseados em COM fornecem um proxy de aplicativo na forma de um pacote do Windows Installer (MSI).</span><span class="sxs-lookup"><span data-stu-id="13293-106">COM-based services provide an application-proxy in the form of a Windows installer (MSI) package.</span></span> <span data-ttu-id="13293-107">Esse arquivo. msi contém o nome do servidor a ser usado e outros elementos necessários, como proxy/stubs e bibliotecas de tipos necessários para o marshaling.</span><span class="sxs-lookup"><span data-stu-id="13293-107">This .msi file contains the server name to be used and other required elements, such as proxy/stubs and type libraries required for marshalling.</span></span> <span data-ttu-id="13293-108">O snap-in Serviços de componentes gera automaticamente esses proxies de aplicativo para aplicativos de servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="13293-108">The Component Services snap-in auto-generate these application proxies for COM+ Server applications.</span></span>

<span data-ttu-id="13293-109">Os proxies de aplicativo são publicados em objetos de política no Active Directory usando o editor de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="13293-109">The application proxies are published into policy objects in Active Directory using the Group Policy Editor.</span></span> <span data-ttu-id="13293-110">Nenhuma intervenção especial é necessária no aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="13293-110">No special intervention is required in the client application.</span></span> <span data-ttu-id="13293-111">A conta de computador/usuário no computador cliente deve estar em uma UO configurada para usar o objeto de política no qual os proxies de aplicativo são publicados.</span><span class="sxs-lookup"><span data-stu-id="13293-111">The computer/user account on the client computer must be in an OU configured to use the policy object in which the application proxies are published.</span></span> <span data-ttu-id="13293-112">O associador de COM localiza automaticamente o servidor por meio do diretório quando o cliente estabelece uma instância dos objetos preocupados.</span><span class="sxs-lookup"><span data-stu-id="13293-112">The COM binder automatically locates the server by means of the directory when the client establishes an instance of the objects concerned.</span></span>

 

 




