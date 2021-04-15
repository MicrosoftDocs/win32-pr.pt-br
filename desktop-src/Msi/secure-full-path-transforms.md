---
description: Seguras-as transformações de caminho completo devem ter uma origem localizada no caminho completo especificado na propriedade transformações.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Alta segurança – transformações de caminho completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8a60cf30beffe3831ed6489ea3827124ae319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506277"
---
# <a name="secure-full-path-transforms"></a><span data-ttu-id="a0469-103">Alta segurança – transformações de caminho completo</span><span class="sxs-lookup"><span data-stu-id="a0469-103">Secure-Full-Path Transforms</span></span>

<span data-ttu-id="a0469-104">Seguras-as transformações de caminho completo devem ter uma origem localizada no caminho completo especificado na propriedade [**TRANSformações**](transforms.md) .</span><span class="sxs-lookup"><span data-stu-id="a0469-104">Secure-full-path transforms must have a source located at the full path specified in the [**TRANSFORMS**](transforms.md) property.</span></span> <span data-ttu-id="a0469-105">Quando o pacote é instalado ou anunciado, o instalador salva as transformações em um cache em que, em um sistema de arquivos seguro, o usuário não tem acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="a0469-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="a0469-106">Se a cópia local da transformação ficar indisponível, ela só poderá restaurar o cache usando o caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="a0469-106">If the local copy of the transform becomes unavailable, it may only restore the cache using the specified path.</span></span> <span data-ttu-id="a0469-107">A remoção de um produto por qualquer usuário remove todas as transformações seguras desse produto do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="a0469-107">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="a0469-108">Para aplicar transformações de caminhos completos seguros na instalação de um pacote, defina a [política TransformsSecure](transformssecure-policy.md) ou a propriedade [**TransformsSecure**](transformssecure.md) ou faça com que \| o primeiro caractere seja passado na lista de transformação.</span><span class="sxs-lookup"><span data-stu-id="a0469-108">To apply secure-full-paths transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property or make \| the first character passed in the transform list.</span></span> <span data-ttu-id="a0469-109">Os caminhos completos para a origem de cada transformação devem ser passados na cadeia de caracteres de transformações.</span><span class="sxs-lookup"><span data-stu-id="a0469-109">The full paths to the source of each transform must be passed in the transforms string.</span></span> <span data-ttu-id="a0469-110">Se algum caminho relativo estiver na lista, a instalação falhará.</span><span class="sxs-lookup"><span data-stu-id="a0469-110">If any relative paths are in the list, the installation fails.</span></span> <span data-ttu-id="a0469-111">A origem da transformação não precisa estar localizada com a origem do pacote.</span><span class="sxs-lookup"><span data-stu-id="a0469-111">The transform source does not have to be located with the source of the package.</span></span>

 

 



