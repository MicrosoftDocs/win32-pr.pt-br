---
description: Depois de entender o modo de resultado da pesquisa, o modo de procura e os padrões de layout, você pode registrar uma lista de propriedades Personalizada para o tipo de arquivo. Para registrar uma lista de propriedades personalizadas e um padrão de layout para o tipo de arquivo, siga estas etapas.
ms.assetid: 29B863B3-E5FD-4E0A-B76B-4AFE5A6A76E3
title: Como registrar Propriedades personalizadas e layout para o tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da55d0a90d4dd0f3ca109a3ca9f628a3c0912520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988978"
---
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a><span data-ttu-id="03156-103">Como registrar Propriedades personalizadas e layout para o tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="03156-103">How to Register Custom Properties and Layout for Your File Type</span></span>

<span data-ttu-id="03156-104">Depois de entender o modo de resultado da pesquisa, o modo de procura e os padrões de layout, você pode registrar uma lista de propriedades Personalizada para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="03156-104">After you understand the Search Result mode, the Browse mode, and the layout patterns, you can register a custom property list for your file type.</span></span>

<span data-ttu-id="03156-105">Para registrar uma lista de propriedades personalizadas e um padrão de layout para o tipo de arquivo, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="03156-105">To register a custom property list and layout pattern for your file type, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="03156-106">Instruções</span><span class="sxs-lookup"><span data-stu-id="03156-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="03156-107">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="03156-107">Step 1:</span></span>

<span data-ttu-id="03156-108">Escolha entre os quatro padrões de layout: alfa, beta, gama ou Delta.</span><span class="sxs-lookup"><span data-stu-id="03156-108">Choose from the four layout patterns: Alpha, Beta, Gamma, or Delta.</span></span>

### <a name="step-2"></a><span data-ttu-id="03156-109">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="03156-109">Step 2:</span></span>

<span data-ttu-id="03156-110">Considere as seguintes regras de formatação, que se aplicam igualmente a todos os quatro padrões de layout:</span><span class="sxs-lookup"><span data-stu-id="03156-110">Consider the following formatting rules, which apply equally to all four layout patterns:</span></span>

-   <span data-ttu-id="03156-111">A propriedade 1 é sempre exibida em um tamanho de fonte maior.</span><span class="sxs-lookup"><span data-stu-id="03156-111">Property 1 is always displayed in a larger font size.</span></span> <span data-ttu-id="03156-112">O tamanho de fonte grande geralmente usado para o nome do item, mas também pode ser usado para a propriedade de âncora ou outro item.</span><span class="sxs-lookup"><span data-stu-id="03156-112">The large font size usually used for the item name, but can also be used for the anchor or other item property.</span></span>
-   <span data-ttu-id="03156-113">A propriedade 4 destina-se a trechos nos padrões de layout alfa, beta e gama.</span><span class="sxs-lookup"><span data-stu-id="03156-113">Property 4 is intended for excerpts in the Alpha, Beta, and Gamma layout patterns.</span></span> <span data-ttu-id="03156-114">Essa propriedade é alocada mais espaço nesses padrões e é exibida em uma cor de fonte cinza, em oposição a preto, como as outras propriedades, para ajudá-lo a destacar.</span><span class="sxs-lookup"><span data-stu-id="03156-114">This property is allotted more space in those patterns and is displayed in a gray font color, as opposed to black like the other properties, to help it stand out.</span></span>
-   <span data-ttu-id="03156-115">As medidas de pixel abaixo estão em pixels relativos e o tamanho inclui o ícone/miniatura à esquerda das propriedades e o espaço entre o ícone/miniatura e o retângulo de seleção.</span><span class="sxs-lookup"><span data-stu-id="03156-115">The pixel measurements below are in relative pixels, and the size includes the icon/thumbnail to the left of the properties and the space between the icon/thumbnail and the selection rectangle.</span></span>
-   <span data-ttu-id="03156-116">A maioria das propriedades tem um tamanho de exibição mínimo.</span><span class="sxs-lookup"><span data-stu-id="03156-116">Most properties have a minimum display size.</span></span> <span data-ttu-id="03156-117">Portanto, eles não serão exibidos se não houver espaço suficiente para eles em um tamanho de exibição específico.</span><span class="sxs-lookup"><span data-stu-id="03156-117">Therefore, they will not appear if there is not enough space for them at a particular view size.</span></span> <span data-ttu-id="03156-118">O tamanho mínimo geralmente é de 100 pixels de largura.</span><span class="sxs-lookup"><span data-stu-id="03156-118">The minimum size is usually 100 pixels wide.</span></span>
-   <span data-ttu-id="03156-119">Cada padrão de layout define o número de linhas e o número de propriedades em cada linha.</span><span class="sxs-lookup"><span data-stu-id="03156-119">Each layout pattern defines the number of rows and the number of properties in each row.</span></span>

### <a name="step-3"></a><span data-ttu-id="03156-120">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="03156-120">Step 3:</span></span>

<span data-ttu-id="03156-121">Decida quais propriedades você deseja exibir no layout e qual Propriedade deseja exibir em cada local.</span><span class="sxs-lookup"><span data-stu-id="03156-121">Decide which properties you want to display in the layout, and which property you want to display in each location.</span></span> <span data-ttu-id="03156-122">Ao decidir qual propriedade será exibida em cada posição no layout, considere o comprimento típico da propriedade, sua importância para o usuário e se ela deve ser descartada quando o tamanho da janela for muito pequeno para conter todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="03156-122">When deciding which property to display in each position in the layout, consider the typical length of the property, its importance to the user, and whether it should be dropped when the window size is too small to contain all properties.</span></span>

### <a name="step-4"></a><span data-ttu-id="03156-123">Etapa 4:</span><span class="sxs-lookup"><span data-stu-id="03156-123">Step 4:</span></span>

<span data-ttu-id="03156-124">Registre um padrão de layout e uma lista de propriedades para o tipo de arquivo ou tipo de item adicionando as seguintes chaves na chave do registro ProgID para o tipo de arquivo ou item (neste exemplo, para o tipo de arquivo. xyz).</span><span class="sxs-lookup"><span data-stu-id="03156-124">Register a layout pattern and a property list for your file type or item type by adding the following keys under the ProgID registry key for the file type or item (in this example, for the .xyz file type).</span></span>

```
HKEY_CLASSES_ROOT\*
   Contoso.xyzfile
      (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
      (ContentViewModeLayoutPatternForSearch) = <PropertyList>
```

### <a name="step-5"></a><span data-ttu-id="03156-125">Etapa 5:</span><span class="sxs-lookup"><span data-stu-id="03156-125">Step 5:</span></span>

<span data-ttu-id="03156-126">Observe as seguintes diretrizes de formatação para registrar Propriedades:</span><span class="sxs-lookup"><span data-stu-id="03156-126">Observe the following formatting guidelines for registering properties:</span></span>

-   <span data-ttu-id="03156-127">Cada registro começa com `prop:`</span><span class="sxs-lookup"><span data-stu-id="03156-127">Each registration starts with `prop:`</span></span>
-   <span data-ttu-id="03156-128">Cada propriedade requer o nome completo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="03156-128">Each property requires the full property name.</span></span>
-   <span data-ttu-id="03156-129">As propriedades são separadas por um ponto-e-vírgula sem espaço.</span><span class="sxs-lookup"><span data-stu-id="03156-129">Properties are separated by a semicolon with no space.</span></span>
-   <span data-ttu-id="03156-130">As propriedades são exibidas na ordem definida pelo padrão de layout selecionado.</span><span class="sxs-lookup"><span data-stu-id="03156-130">Properties are displayed in the order defined by the selected layout pattern.</span></span>
-   <span data-ttu-id="03156-131">`~` indica que o rótulo da propriedade não deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="03156-131">`~` indicates that the property label should not be displayed.</span></span>
-   <span data-ttu-id="03156-132">`~System.LayoutPattern.PlaceHolder` deve ser usado se você quiser deixar em branco uma propriedade especificada no padrão de layout.</span><span class="sxs-lookup"><span data-stu-id="03156-132">`~System.LayoutPattern.PlaceHolder` should be used if you want to leave blank a property that is specified in the layout pattern.</span></span>

<span data-ttu-id="03156-133">A chave do registro de exemplo a seguir ilustra essas diretrizes de formatação.</span><span class="sxs-lookup"><span data-stu-id="03156-133">The following sample registry key illustrates these formatting guidelines.</span></span>

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

<span data-ttu-id="03156-134">Os valores possíveis para (ContentViewModeForBrowse) incluem o seguinte: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`</span><span class="sxs-lookup"><span data-stu-id="03156-134">Possible values for (ContentViewModeForBrowse) include the following: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`</span></span>

 

 



