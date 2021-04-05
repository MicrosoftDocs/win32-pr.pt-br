---
title: Categorizando por recursos de contêiner
description: Os componentes geralmente exigem determinada funcionalidade do contêiner e não funcionarão com um contêiner que não forneça o suporte.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006086"
---
# <a name="categorizing-by-container-capabilities"></a><span data-ttu-id="7330f-103">Categorizando por recursos de contêiner</span><span class="sxs-lookup"><span data-stu-id="7330f-103">Categorizing by Container Capabilities</span></span>

<span data-ttu-id="7330f-104">Os componentes geralmente exigem determinada funcionalidade do contêiner e não funcionarão com um contêiner que não forneça o suporte.</span><span class="sxs-lookup"><span data-stu-id="7330f-104">Components often require certain functionality from the container and will not work with a container that does not provide the support.</span></span> <span data-ttu-id="7330f-105">A interface do usuário deve filtrar os componentes que exigem a funcionalidade para a qual o contêiner não dá suporte.</span><span class="sxs-lookup"><span data-stu-id="7330f-105">The user interface should filter out components that require functionality the container does not support.</span></span> <span data-ttu-id="7330f-106">Para fazer isso, os componentes podem ser categorizados pela funcionalidade de contêiner necessária.</span><span class="sxs-lookup"><span data-stu-id="7330f-106">To accomplish this, components can be categorized by the required container functionality.</span></span>

<span data-ttu-id="7330f-107">Um exemplo de componentes que exigem funcionalidade do contêiner e não funcionam em contêineres que não dão suporte a essa funcionalidade são controles OLE de quadro simples.</span><span class="sxs-lookup"><span data-stu-id="7330f-107">An example of components that require functionality from the container and do not work in containers that do not support that functionality are simple frame OLE controls.</span></span> <span data-ttu-id="7330f-108">A categorização por recursos de contêiner é realizada por uma chave de registro adicional na chave CLSID do componente:</span><span class="sxs-lookup"><span data-stu-id="7330f-108">Categorizing by container capabilities is accomplished by an additional registry key within the component's CLSID key:</span></span>

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

<span data-ttu-id="7330f-109">Como mostrado neste exemplo, um componente pode pertencer a categorias de componentes que indicam a funcionalidade com suporte, bem como categorias de componentes que indicam a funcionalidade necessária.</span><span class="sxs-lookup"><span data-stu-id="7330f-109">As shown in this example, a component can belong to component categories that indicate supported functionality as well as to component categories that indicate required functionality.</span></span>

<span data-ttu-id="7330f-110">No exemplo a seguir, o controle Button é um controle OLE genérico que não dá suporte a nenhuma funcionalidade adicional.</span><span class="sxs-lookup"><span data-stu-id="7330f-110">In the following example, the button control is a generic OLE control that supports no additional functionality.</span></span> <span data-ttu-id="7330f-111">Ele funcionará em qualquer contêiner de controle OLE.</span><span class="sxs-lookup"><span data-stu-id="7330f-111">It will work in any OLE control container.</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

<span data-ttu-id="7330f-112">Compare o exemplo anterior com o próximo exemplo no qual o MyDBControl pode usar Visual Basic vinculação de dados se o contêiner oferecer suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="7330f-112">Compare the preceding example with the next example in which the MyDBControl can use Visual Basic data binding if the container supports it.</span></span> <span data-ttu-id="7330f-113">No entanto, ele foi definido para que funcione em contêineres que não suportam Visual Basic Associação de dados (talvez por uma API de banco de dado diferente):</span><span class="sxs-lookup"><span data-stu-id="7330f-113">However, it has been defined so that it will work in containers that do not support Visual Basic data binding (perhaps by a different database API):</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

<span data-ttu-id="7330f-114">O controle GroupBox é um controle Frame simples.</span><span class="sxs-lookup"><span data-stu-id="7330f-114">The GroupBox control is a simple frame control.</span></span> <span data-ttu-id="7330f-115">Ele se baseia no contêiner que implementa a interface [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) e funcionará corretamente apenas nesses contêineres:</span><span class="sxs-lookup"><span data-stu-id="7330f-115">It relies on the container implementing the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface and will work correctly only in such containers:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

<span data-ttu-id="7330f-116">Um contêiner que dá suporte a Visual Basic controles associados a dados, mas não dá suporte a controles de quadro simples especificaria \_ o controle CATID e \_ o CATID VBDatabound para a interface do usuário do controle de inserção.</span><span class="sxs-lookup"><span data-stu-id="7330f-116">A container that supports Visual Basic data bound controls but does not support simple frame controls would specify CATID\_Control and CATID\_VBDatabound to the insert control user interface.</span></span> <span data-ttu-id="7330f-117">A lista de controles exibida para o usuário contém o botão CLSID \_ e CLSID \_ MyDBControl.</span><span class="sxs-lookup"><span data-stu-id="7330f-117">The list of controls displayed to the user would contain the CLSID\_Button and CLSID\_MyDBControl.</span></span> <span data-ttu-id="7330f-118">A caixa de caixa do CLSID \_ não seria exibida.</span><span class="sxs-lookup"><span data-stu-id="7330f-118">CLSID\_GroupBox would not be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7330f-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7330f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7330f-120">Associando ícones a uma categoria</span><span class="sxs-lookup"><span data-stu-id="7330f-120">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="7330f-121">Categorizando por recursos de componente</span><span class="sxs-lookup"><span data-stu-id="7330f-121">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="7330f-122">Classes e associações padrão</span><span class="sxs-lookup"><span data-stu-id="7330f-122">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="7330f-123">Definindo categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="7330f-123">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="7330f-124">O Gerenciador de categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="7330f-124">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




