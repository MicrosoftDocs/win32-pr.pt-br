---
title: O Gerenciador de categorias de componentes
description: O Gerenciador de categorias de componentes
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453590"
---
# <a name="the-component-categories-manager"></a><span data-ttu-id="3b858-103">O Gerenciador de categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="3b858-103">The Component Categories Manager</span></span>

<span data-ttu-id="3b858-104">Para facilitar o manuseio de categorias de componentes e garantir a consistência do registro, o sistema fornece o Gerenciador de categorias de componentes, um objeto COM com um CLSID de CLSID \_ StdComponentCategoriesMgr.</span><span class="sxs-lookup"><span data-stu-id="3b858-104">To facilitate the handling of component categories and to guarantee consistency of the registry, the system provides the Component Categories Manager, a COM object with a CLSID of CLSID\_StdComponentCategoriesMgr.</span></span> <span data-ttu-id="3b858-105">Este objeto COM fornece as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="3b858-105">This COM object provides the following interfaces:</span></span>

-   [<span data-ttu-id="3b858-106">**ICatInformation**</span><span class="sxs-lookup"><span data-stu-id="3b858-106">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [<span data-ttu-id="3b858-107">**ICatRegister**</span><span class="sxs-lookup"><span data-stu-id="3b858-107">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)

<span data-ttu-id="3b858-108">O [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) fornece métodos para obter informações sobre as categorias implementadas ou exigidas por uma determinada classe e fornece informações sobre as categorias registradas em determinado computador.</span><span class="sxs-lookup"><span data-stu-id="3b858-108">[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) provides methods for obtaining information about the categories implemented or required by a certain class and provides information about the categories registered on a given machine.</span></span>

<span data-ttu-id="3b858-109">O [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) fornece métodos para registrar e cancelar o registro de informações de categoria de componente no registro.</span><span class="sxs-lookup"><span data-stu-id="3b858-109">[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) provides methods for registering and unregistering component category information in the registry.</span></span> <span data-ttu-id="3b858-110">Isso inclui os nomes legíveis de categorias e as categorias implementadas ou exigidas por um determinado componente ou classe.</span><span class="sxs-lookup"><span data-stu-id="3b858-110">This includes both the human-readable names of categories and the categories implemented or required by a given component or class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b858-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b858-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b858-112">Associando ícones a uma categoria</span><span class="sxs-lookup"><span data-stu-id="3b858-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="3b858-113">Categorizando por recursos de componente</span><span class="sxs-lookup"><span data-stu-id="3b858-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="3b858-114">Categorizando por recursos de contêiner</span><span class="sxs-lookup"><span data-stu-id="3b858-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="3b858-115">Classes e associações padrão</span><span class="sxs-lookup"><span data-stu-id="3b858-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="3b858-116">Definindo categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="3b858-116">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> </dl>

 

 




