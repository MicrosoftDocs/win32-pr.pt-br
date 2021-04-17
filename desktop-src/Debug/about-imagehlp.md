---
description: As funções de ImageHlp são usadas principalmente por ferramentas de programação, utilitários de instalação de aplicativos e outros programas que precisam de acesso aos dados contidos em uma imagem PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: Sobre o ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76da517a396536640df0e9bfcfa05368e4d0b76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756225"
---
# <a name="about-imagehlp"></a><span data-ttu-id="7d316-103">Sobre o ImageHlp</span><span class="sxs-lookup"><span data-stu-id="7d316-103">About ImageHlp</span></span>

<span data-ttu-id="7d316-104">As funções de ImageHlp são usadas principalmente por ferramentas de programação, utilitários de instalação de aplicativos e outros programas que precisam de acesso aos dados contidos em uma imagem PE.</span><span class="sxs-lookup"><span data-stu-id="7d316-104">The ImageHlp functions are used mostly by programming tools, application setup utilities, and other programs that need access to the data contained in a PE image.</span></span> <span data-ttu-id="7d316-105">Todas as funções de ImageHlp são thread único.</span><span class="sxs-lookup"><span data-stu-id="7d316-105">All ImageHlp functions are single threaded.</span></span> <span data-ttu-id="7d316-106">Portanto, as chamadas de mais de um thread para essa função provavelmente resultarão em um comportamento inesperado ou corrupção de memória.</span><span class="sxs-lookup"><span data-stu-id="7d316-106">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="7d316-107">Para evitar isso, você deve sincronizar todas as chamadas simultâneas de mais de um thread para essa função.</span><span class="sxs-lookup"><span data-stu-id="7d316-107">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

<span data-ttu-id="7d316-108">Os tópicos a seguir descrevem as imagens do PE e a funcionalidade fornecida pelas funções do ImageHlp.</span><span class="sxs-lookup"><span data-stu-id="7d316-108">The following topics describe PE images and the functionality provided by the ImageHlp functions.</span></span>

-   [<span data-ttu-id="7d316-109">Formato PE</span><span class="sxs-lookup"><span data-stu-id="7d316-109">PE Format</span></span>](pe-format.md)
-   [<span data-ttu-id="7d316-110">Funções de acesso a imagens</span><span class="sxs-lookup"><span data-stu-id="7d316-110">Image Access Functions</span></span>](image-access-functions.md)
-   [<span data-ttu-id="7d316-111">Funções de integridade da imagem</span><span class="sxs-lookup"><span data-stu-id="7d316-111">Image Integrity Functions</span></span>](image-integrity-functions.md)
-   [<span data-ttu-id="7d316-112">Funções de modificação de imagem</span><span class="sxs-lookup"><span data-stu-id="7d316-112">Image Modification Functions</span></span>](image-modification-functions.md)

 

 



