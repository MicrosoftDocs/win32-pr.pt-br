---
description: Os assemblies privados lado a lado podem ser usados para criar componentes que podem ser facilmente atualizados, sem Atualizar também o aplicativo de hospedagem.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Atualizando componentes do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba559323c3272db96f0cd106f0fc61624519b770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920827"
---
# <a name="updating-application-components"></a><span data-ttu-id="d37ca-103">Atualizando componentes do aplicativo</span><span class="sxs-lookup"><span data-stu-id="d37ca-103">Updating Application Components</span></span>

<span data-ttu-id="d37ca-104">Os assemblies privados lado a lado podem ser usados para criar componentes que podem ser facilmente atualizados, sem Atualizar também o aplicativo de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="d37ca-104">Side-by-side private assemblies can be used to create components that can be easily updated without also updating the hosting application.</span></span> <span data-ttu-id="d37ca-105">Isso permite que um serviço de atualização instale os componentes atualizados do aplicativo, reinicie o aplicativo e faça com que o aplicativo use as alterações.</span><span class="sxs-lookup"><span data-stu-id="d37ca-105">This allows an updating service to install the application's updated components, restart the application, and have the application use the changes.</span></span> <span data-ttu-id="d37ca-106">Ao usar manifestos de aplicativo, a funcionalidade dos componentes hospedados por um aplicativo pode ser atualizada sem a necessidade de alterar o código do aplicativo de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="d37ca-106">When using application manifests, the functionality of components hosted by an application can be updated without having to change the hosting application's code.</span></span>

<span data-ttu-id="d37ca-107">Esse método pode ser usado para atualizar a versão dos recursos de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d37ca-107">This method can be used to update the version of an application's resources.</span></span> <span data-ttu-id="d37ca-108">Por exemplo, se um aplicativo contiver um assembly, o manifesto do aplicativo poderá especificar uma dependência nesse assembly.</span><span class="sxs-lookup"><span data-stu-id="d37ca-108">For example, if an application contains an assembly, the application's manifest can specify a dependency on this assembly.</span></span> <span data-ttu-id="d37ca-109">O aplicativo pode obter o assembly chamando [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) para localizar e carregar os arquivos necessários.</span><span class="sxs-lookup"><span data-stu-id="d37ca-109">The application can get the assembly by calling [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) to find and load the files it requires.</span></span> <span data-ttu-id="d37ca-110">Um atualizador simplesmente precisa desativar os bits mais novos para o assembly, que pode existir lado a lado com uma versão anterior do assembly.</span><span class="sxs-lookup"><span data-stu-id="d37ca-110">An updater simply has to bring down the newest bits for the assembly, which can exist side-by-side with an earlier version of the assembly.</span></span>

 

 
