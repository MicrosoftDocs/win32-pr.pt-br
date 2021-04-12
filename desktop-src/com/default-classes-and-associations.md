---
title: Classes e associações padrão
description: Para determinadas categorias, uma única classe pode ser associada como a classe padrão.
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363672"
---
# <a name="default-classes-and-associations"></a><span data-ttu-id="3a3ea-103">Classes e associações padrão</span><span class="sxs-lookup"><span data-stu-id="3a3ea-103">Default Classes and Associations</span></span>

<span data-ttu-id="3a3ea-104">Para determinadas categorias, uma única classe pode ser associada como a classe padrão.</span><span class="sxs-lookup"><span data-stu-id="3a3ea-104">For certain categories, a single class can be associated as the default class.</span></span> <span data-ttu-id="3a3ea-105">A classe padrão é selecionada sempre que essa categoria de objeto em particular é necessária.</span><span class="sxs-lookup"><span data-stu-id="3a3ea-105">The default class is selected whenever that particular category of object is required.</span></span> <span data-ttu-id="3a3ea-106">Embora isso possa não ser útil para todas as categorias de componente, o estabelecimento de uma classe padrão pode ser útil quando uma determinada classe deve ser carregada de uma lista de classes possíveis sem intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="3a3ea-106">While this may not be useful for all component categories, establishing a default class can be helpful when a particular class must be loaded from a list of possible classes without user intervention.</span></span> <span data-ttu-id="3a3ea-107">Os administradores definem qual classe pode ser usada manipulando o registro.</span><span class="sxs-lookup"><span data-stu-id="3a3ea-107">Administrators define which class can be used by manipulating the registry.</span></span>

<span data-ttu-id="3a3ea-108">Para associar uma classe padrão a uma categoria, introduza uma chave CLSID com o mesmo CLSID que o CATID da categoria de componente escolhida como padrão.</span><span class="sxs-lookup"><span data-stu-id="3a3ea-108">To associate a default class with a category, introduce a CLSID key with the same CLSID as the CATID of the component category chosen as the default.</span></span> <span data-ttu-id="3a3ea-109">Em seguida, adicione uma chave Treats a essa chave, usando o valor para o CLSID da classe padrão para a categoria.</span><span class="sxs-lookup"><span data-stu-id="3a3ea-109">Then add a TreatAs key to this key, using the value for the CLSID of the default class for the category.</span></span> <span data-ttu-id="3a3ea-110">Para usar a classe padrão para uma categoria de componente, use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), especificando o CATID para o parâmetro CLSID.</span><span class="sxs-lookup"><span data-stu-id="3a3ea-110">To use the default class for a component category, use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), specifying the CATID for the CLSID parameter.</span></span> <span data-ttu-id="3a3ea-111">Isso redireciona automaticamente para o CLSID estabelecido como o padrão para essa categoria.</span><span class="sxs-lookup"><span data-stu-id="3a3ea-111">This automatically redirects to the CLSID established as the default for this category.</span></span> <span data-ttu-id="3a3ea-112">A entrada do registro é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="3a3ea-112">The registry entry is as follows:</span></span>

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

<span data-ttu-id="3a3ea-113">Durante a instalação, um componente pode verificar a existência de qualquer chave de classe padrão para suas categorias e apresentar ao usuário opções para substituir as configurações atuais.</span><span class="sxs-lookup"><span data-stu-id="3a3ea-113">During installation, a component can check for the existence of any default class keys for its categories and present the user with options for overriding the current settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a3ea-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a3ea-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a3ea-115">Associando ícones a uma categoria</span><span class="sxs-lookup"><span data-stu-id="3a3ea-115">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="3a3ea-116">Categorizando por recursos de componente</span><span class="sxs-lookup"><span data-stu-id="3a3ea-116">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="3a3ea-117">Categorizando por recursos de contêiner</span><span class="sxs-lookup"><span data-stu-id="3a3ea-117">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="3a3ea-118">Definindo categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="3a3ea-118">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="3a3ea-119">O Gerenciador de categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="3a3ea-119">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




