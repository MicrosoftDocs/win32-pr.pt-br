---
description: Considerações sobre programação para trabalhar com links simbólicos.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Considerações sobre programação (sistemas de arquivos locais)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5d63c231c88da95efc0e5078506bf9fc0d6d9a
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "105775749"
---
# <a name="programming-considerations-local-file-systems"></a><span data-ttu-id="59560-103">Considerações sobre programação (sistemas de arquivos locais)</span><span class="sxs-lookup"><span data-stu-id="59560-103">Programming Considerations (Local File Systems)</span></span>

<span data-ttu-id="59560-104">Lembre-se das seguintes considerações de programação ao trabalhar com links simbólicos:</span><span class="sxs-lookup"><span data-stu-id="59560-104">Keep the following programming considerations in mind when working with symbolic links:</span></span>

-   <span data-ttu-id="59560-105">Links simbólicos podem apontar para um destino não existente.</span><span class="sxs-lookup"><span data-stu-id="59560-105">Symbolic links can point to a non-existent target.</span></span>
-   <span data-ttu-id="59560-106">Ao criar um link simbólico, o sistema operacional não verifica se o destino existe.</span><span class="sxs-lookup"><span data-stu-id="59560-106">When creating a symbolic link, the operating system does not check to see if the target exists.</span></span>
-   <span data-ttu-id="59560-107">Se um aplicativo tentar abrir um destino não existente, o **arquivo de \_ erro \_ não \_ encontrado** será retornado.</span><span class="sxs-lookup"><span data-stu-id="59560-107">If an application tries to open a non-existent target, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>
-   <span data-ttu-id="59560-108">Links simbólicos são pontos de nova análise.</span><span class="sxs-lookup"><span data-stu-id="59560-108">Symbolic links are reparse points.</span></span> <span data-ttu-id="59560-109">Para obter mais informações, consulte [determinando se um diretório é uma pasta montada](determining-whether-a-directory-is-a-volume-mount-point.md).</span><span class="sxs-lookup"><span data-stu-id="59560-109">For more information, see [Determining Whether a Directory Is a Mounted Folder](determining-whether-a-directory-is-a-volume-mount-point.md).</span></span>
-   <span data-ttu-id="59560-110">Há um máximo de 63 pontos de nova análise (e, portanto, links simbólicos) permitidos em um caminho específico.</span><span class="sxs-lookup"><span data-stu-id="59560-110">There is a maximum of 63 reparse points (and therefore symbolic links) allowed in a particular path.</span></span>

    <span data-ttu-id="59560-111">**Windows Server 2003 e Windows XP:** Há um limite de 31 pontos de nova análise em qualquer caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="59560-111">**Windows Server 2003 and Windows XP:** There is a limit of 31 reparse points on any given path.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59560-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="59560-112">Related topics</span></span>

<dl> <span data-ttu-id="59560-113"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="59560-113"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="59560-114">Links físicos e junções</span><span class="sxs-lookup"><span data-stu-id="59560-114">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> </dl>

 

 



