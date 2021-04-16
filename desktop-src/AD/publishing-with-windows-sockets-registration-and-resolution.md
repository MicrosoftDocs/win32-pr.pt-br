---
title: Publicando com a resolução de & de registro do Windows Sockets
description: O Windows Sockets Services pode usar as APIs de RnR (registro e resolução) para publicar serviços e Pesquisar serviços publicados com o RnR.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- ANÚNCIO de registro e resolução do Windows Sockets, publicando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/04/2019
ms.locfileid: "104453808"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a><span data-ttu-id="d1b75-104">Publicando com a resolução de & de registro do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="d1b75-104">Publishing with Windows Sockets Registration & Resolution</span></span>

<span data-ttu-id="d1b75-105">O Windows Sockets Services pode usar as APIs de RnR (registro e resolução) para publicar serviços e Pesquisar serviços publicados com o RnR.</span><span class="sxs-lookup"><span data-stu-id="d1b75-105">Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services and look up services published with RnR.</span></span> <span data-ttu-id="d1b75-106">A publicação RnR ocorre em duas etapas.</span><span class="sxs-lookup"><span data-stu-id="d1b75-106">RnR publication occurs in two steps.</span></span> <span data-ttu-id="d1b75-107">A primeira etapa instala uma classe de serviço que associa um GUID com um nome para o serviço.</span><span class="sxs-lookup"><span data-stu-id="d1b75-107">The first step installs a service class that associates a GUID with a name for the service.</span></span> <span data-ttu-id="d1b75-108">A classe de serviço pode manter dados de configuração específicos do serviço.</span><span class="sxs-lookup"><span data-stu-id="d1b75-108">The service class can hold service-specific configuration data.</span></span> <span data-ttu-id="d1b75-109">Os serviços podem, então, se publicar como instâncias da classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="d1b75-109">Services can then publish themselves as instances of the service class.</span></span> <span data-ttu-id="d1b75-110">Quando publicado, os clientes podem consultar o serviço de diretório em busca de instâncias de uma determinada classe usando as APIs RnR e selecionar uma instância à qual associar.</span><span class="sxs-lookup"><span data-stu-id="d1b75-110">When published, clients can query the directory service for instances of a given class using the RnR APIs and select an instance to bind to.</span></span> <span data-ttu-id="d1b75-111">Quando uma classe não é mais necessária, ela pode ser removida.</span><span class="sxs-lookup"><span data-stu-id="d1b75-111">When a class is no longer required, it can be removed.</span></span>

 

 




