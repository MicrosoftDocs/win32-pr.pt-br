---
title: Considerações sobre implementação do IPropertySetStorage
description: Vários problemas surgem ao considerar como fornecer uma implementação da Interface IPropertySetStorage que lê e grava o formato de conjunto de propriedades COM. As seções a seguir descrevem essas considerações.
ms.assetid: 055da516-ed42-49ec-b20c-a5e98718bea8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f7532211668fa1ecf290484a707b19e1c263b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636648"
---
# <a name="ipropertysetstorage-implementation-considerations"></a><span data-ttu-id="5361a-104">Considerações sobre implementação do IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="5361a-104">IPropertySetStorage Implementation Considerations</span></span>

<span data-ttu-id="5361a-105">Vários problemas surgem ao considerar como fornecer uma implementação da interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) que lê e grava o formato de conjunto de propriedades com.</span><span class="sxs-lookup"><span data-stu-id="5361a-105">Several issues arise when considering how to provide an implementation of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface that reads and writes the COM property set format.</span></span> <span data-ttu-id="5361a-106">As seções a seguir descrevem essas considerações.</span><span class="sxs-lookup"><span data-stu-id="5361a-106">The following sections describe these considerations.</span></span>

-   [<span data-ttu-id="5361a-107">Nomes em IStorage</span><span class="sxs-lookup"><span data-stu-id="5361a-107">Names in IStorage</span></span>](names-in-istorage.md)
-   [<span data-ttu-id="5361a-108">Objetos de armazenamento e de fluxo para um conjunto de propriedades</span><span class="sxs-lookup"><span data-stu-id="5361a-108">Storage and Stream Objects for a Property Set</span></span>](storage-vs--stream-for-a-property-set.md)
-   [<span data-ttu-id="5361a-109">Definindo o identificador de classe do conjunto de propriedades</span><span class="sxs-lookup"><span data-stu-id="5361a-109">Setting the Property Set Class Identifier</span></span>](setting-the-property-set-class-identifier.md)
-   [<span data-ttu-id="5361a-110">Pontos de sincronização</span><span class="sxs-lookup"><span data-stu-id="5361a-110">Synchronization Points</span></span>](synchronization-points.md)
-   [<span data-ttu-id="5361a-111">Páginas de código e cadeias de caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="5361a-111">Code Pages and Unicode Strings</span></span>](code-pages-and-unicode-strings.md)
-   [<span data-ttu-id="5361a-112">Dicionário</span><span class="sxs-lookup"><span data-stu-id="5361a-112">Dictionary</span></span>](dictionary.md)
-   [<span data-ttu-id="5361a-113">Extensões</span><span class="sxs-lookup"><span data-stu-id="5361a-113">Extensions</span></span>](extensions.md)
-   [<span data-ttu-id="5361a-114">Serialização do conjunto de propriedades</span><span class="sxs-lookup"><span data-stu-id="5361a-114">Property Set Serialization</span></span>](version-0-vs--version-1-property-set-serialization.md)

<span data-ttu-id="5361a-115">Para obter mais informações, consulte [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) na seção de referência em interfaces.</span><span class="sxs-lookup"><span data-stu-id="5361a-115">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) in the Reference section under Interfaces.</span></span>

 

 




