---
title: Associando ícones a uma categoria
description: Associando ícones a uma categoria
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c7a662ab3aaf578f037ff246207d03e4fcd688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005045"
---
# <a name="associating-icons-with-a-category"></a><span data-ttu-id="9a67e-103">Associando ícones a uma categoria</span><span class="sxs-lookup"><span data-stu-id="9a67e-103">Associating Icons with a Category</span></span>

<span data-ttu-id="9a67e-104">A criação de uma interface do usuário que permite ao usuário selecionar categorias de componentes em uma categoria requer a capacidade de exibir uma imagem significativa para uma determinada categoria.</span><span class="sxs-lookup"><span data-stu-id="9a67e-104">Building a user interface that allows the user to select component categories within a category requires the ability to display a meaningful image for a particular category.</span></span> <span data-ttu-id="9a67e-105">Para associar um ícone a uma categoria de componente, crie uma chave para o CATID da categoria e preencha essa chave com uma subchave [DefaultIcon](defaulticon.md) .</span><span class="sxs-lookup"><span data-stu-id="9a67e-105">To associate an icon with a component category, create a key for the category's CATID and populate that key with a [DefaultIcon](defaulticon.md) subkey.</span></span> <span data-ttu-id="9a67e-106">A entrada do registro é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="9a67e-106">The registry entry is as follows:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

<span data-ttu-id="9a67e-107">O nome de arquivo referenciado pela chave DefaultIcon pode ser um executável ou um arquivos DLL (DLL somente de recursos).</span><span class="sxs-lookup"><span data-stu-id="9a67e-107">The filename referenced by the DefaultIcon key can be either an EXE or a DLL file (resource-only DLL).</span></span>

<span data-ttu-id="9a67e-108">Para associar um pequeno "bitmap de caixa de ferramentas" 16x16 a uma categoria de componente, crie uma chave em **\_ classe HKEY \_ raiz \\ CLSID** para o CATID da categoria e preencha essa chave com uma subchave [ToolBoxBitmap32](toolboxbitmap32.md) , conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="9a67e-108">To associate a small 16x16 "toolbox bitmap" with a component category, create a key in **HKEY\_CLASSES\_ROOT\\CLSID** for the category's CATID and populate that key with a [ToolBoxBitmap32](toolboxbitmap32.md) subkey, as shown in the following example:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

<span data-ttu-id="9a67e-109">O nome de arquivo referenciado pela chave [ToolBoxBitmap32](toolboxbitmap32.md) também pode ser um arquivos exe ou DLL (DLL somente de recursos).</span><span class="sxs-lookup"><span data-stu-id="9a67e-109">The filename referenced by the [ToolBoxBitmap32](toolboxbitmap32.md) key can also be an EXE or DLL file (resource-only DLL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a67e-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a67e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a67e-111">Categorizando por recursos de componente</span><span class="sxs-lookup"><span data-stu-id="9a67e-111">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="9a67e-112">Categorizando por recursos de contêiner</span><span class="sxs-lookup"><span data-stu-id="9a67e-112">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="9a67e-113">Classes e associações padrão</span><span class="sxs-lookup"><span data-stu-id="9a67e-113">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="9a67e-114">Definindo categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="9a67e-114">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="9a67e-115">**ICatInformation**</span><span class="sxs-lookup"><span data-stu-id="9a67e-115">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[<span data-ttu-id="9a67e-116">**ICatRegister**</span><span class="sxs-lookup"><span data-stu-id="9a67e-116">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[<span data-ttu-id="9a67e-117">O Gerenciador de categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="9a67e-117">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




