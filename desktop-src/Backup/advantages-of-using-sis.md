---
title: Vantagens do uso do SIS
description: As vantagens de usar o SIS e a arquitetura de backup do SIS são as seguintes.
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- Backup de armazenamento de instância única (SIS), vantagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd1856ce54e817c25830f15f133c7d76c6a80fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004973"
---
# <a name="advantages-of-using-sis"></a><span data-ttu-id="4d79e-104">Vantagens do uso do SIS</span><span class="sxs-lookup"><span data-stu-id="4d79e-104">Advantages of Using SIS</span></span>

<span data-ttu-id="4d79e-105">As vantagens de usar o SIS e a arquitetura de backup do SIS são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="4d79e-105">The advantages of using SIS and the SIS backup architecture are the following:</span></span>

-   <span data-ttu-id="4d79e-106">As conexões entre os links do SIS e os arquivos de backup são mantidas automaticamente pela arquitetura do SIS à medida que os aplicativos de backup chamam as funções da API de backup do SIS.</span><span class="sxs-lookup"><span data-stu-id="4d79e-106">The connections between the SIS links and the backing files are automatically maintained by the SIS architecture as your backup applications call the SIS backup API functions.</span></span>
-   <span data-ttu-id="4d79e-107">O conteúdo dos pontos de nova análise do SIS é opaco para seus aplicativos de backup e restauração, garantindo que as atualizações para os internos do SIS não exigirão uma alteração na API do SIS ou nos aplicativos de backup e restauração que chamam funções de API do SIS.</span><span class="sxs-lookup"><span data-stu-id="4d79e-107">The contents of the SIS reparse points are opaque to your backup and restore applications, ensuring that upgrades to the SIS internals will not require a change in the SIS API or your backup and restore applications that call SIS API functions.</span></span> <span data-ttu-id="4d79e-108">Você precisa apenas recompilar seu aplicativo com uma nova versão da DLL do SIS, chamada Sisbkup.dll.</span><span class="sxs-lookup"><span data-stu-id="4d79e-108">You need only recompile your application with a new version of the SIS DLL, named Sisbkup.dll.</span></span>
-   <span data-ttu-id="4d79e-109">Como o SIS é implementado como um driver de filtro do sistema de arquivos, ele rastreia constantemente as conexões entre os links do SIS e os arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="4d79e-109">Because SIS is implemented as a file system filter driver, it constantly tracks the connections between the SIS links and the backing files.</span></span> <span data-ttu-id="4d79e-110">Quando os arquivos são armazenados em backup e restaurados, o backup do SIS garante que apenas uma instância do arquivo de backup será armazenada em backup e restaurada, independentemente do número de links do SIS que apontam para ele.</span><span class="sxs-lookup"><span data-stu-id="4d79e-110">When the files are backed up and restored, SIS backup ensures that only one instance of the backing file will be backed up and restored, regardless of the number of SIS links that point to it.</span></span>

 

 




