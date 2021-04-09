---
description: As transformações de origem segura devem ter uma origem localizada na raiz da origem do pacote.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Transformações de origem segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec59d551489fa1699c20c24d09b7ecbff99f8ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837401"
---
# <a name="secure-at-source-transforms"></a><span data-ttu-id="d9d9b-103">Transformações de origem segura</span><span class="sxs-lookup"><span data-stu-id="d9d9b-103">Secure-At-Source Transforms</span></span>

<span data-ttu-id="d9d9b-104">As transformações de origem segura devem ter uma origem localizada na raiz da origem do pacote.</span><span class="sxs-lookup"><span data-stu-id="d9d9b-104">Secure-at-source transforms must have a source located at the root of the source for the package.</span></span> <span data-ttu-id="d9d9b-105">Quando o pacote é instalado ou anunciado, o instalador salva as transformações em um cache em que, em um sistema de arquivos seguro, o usuário não tem acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="d9d9b-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="d9d9b-106">Se a cópia local da transformação ficar indisponível, o instalador procurará uma origem para restaurar o cache.</span><span class="sxs-lookup"><span data-stu-id="d9d9b-106">If the local copy of the transform becomes unavailable, the installer searches for a source to restore the cache.</span></span> <span data-ttu-id="d9d9b-107">O método é o mesmo que pesquisar a lista de origem de um arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="d9d9b-107">The method is the same as searching the source list for an .msi file.</span></span> <span data-ttu-id="d9d9b-108">Para obter mais informações, consulte [resiliência de origem](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="d9d9b-108">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="d9d9b-109">A remoção de um produto por qualquer usuário remove todas as transformações seguras desse produto do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="d9d9b-109">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="d9d9b-110">Para aplicar transformações de origem segura na instalação de um pacote, defina a [política TransformsSecure](transformssecure-policy.md) ou a propriedade [**TransformsSecure**](transformssecure.md) ou torne @ o primeiro caractere passado na lista de transformação.</span><span class="sxs-lookup"><span data-stu-id="d9d9b-110">To apply secure-at-source transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property, or make @ the first character passed in the transform list.</span></span> <span data-ttu-id="d9d9b-111">Cada transformação deve ser indicada por um nome de arquivo e deve estar localizada na raiz da origem do pacote.</span><span class="sxs-lookup"><span data-stu-id="d9d9b-111">Each transform must be indicated by a file name and must be located at the root of the source for the package.</span></span> <span data-ttu-id="d9d9b-112">Se qualquer uma das transformações não estiver localizada na raiz da origem do pacote, a instalação falhará.</span><span class="sxs-lookup"><span data-stu-id="d9d9b-112">If any of the transforms are not located at the root of the package source, the installation fails.</span></span> <span data-ttu-id="d9d9b-113">Para obter mais informações, consulte [aplicando transformações](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="d9d9b-113">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



