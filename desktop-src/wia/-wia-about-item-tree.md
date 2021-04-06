---
description: Com o Windows Vista, a árvore de itens de aquisição de imagens do Windows (WIA) mudou significativamente.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Sobre a árvore de itens do IWiaItem2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828458"
---
# <a name="about-the-iwiaitem2-item-tree"></a><span data-ttu-id="63dc3-103">Sobre a árvore de itens do IWiaItem2</span><span class="sxs-lookup"><span data-stu-id="63dc3-103">About the IWiaItem2 Item Tree</span></span>

<span data-ttu-id="63dc3-104">Com o Windows Vista, a árvore de itens de aquisição de imagens do Windows (WIA) mudou significativamente.</span><span class="sxs-lookup"><span data-stu-id="63dc3-104">With Windows Vista, the Windows Image Acquisition (WIA) item tree has changed significantly.</span></span> <span data-ttu-id="63dc3-105">Os itens [**IWiaItem2**](-wia-iwiaitem2.md) são usados para representar os atributos do dispositivo e os dados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63dc3-105">[**IWiaItem2**](-wia-iwiaitem2.md) items are used to represent device attributes and device data.</span></span> <span data-ttu-id="63dc3-106">Os aplicativos de geração de imagens veem um dispositivo de aquisição de imagem do Windows (WIA) 2,0 como uma árvore hierárquica de itens, com o item raiz que representa o próprio dispositivo e os itens filho que representam coisas como fontes de dados programáveis, imagens ou pastas que contêm imagens.</span><span class="sxs-lookup"><span data-stu-id="63dc3-106">Imaging applications see a Windows Image Acquisition (WIA) 2.0 device as a hierarchical tree of items, with the root item representing the device itself and the child items representing things like programmable data sources, images, or folders that contain images.</span></span>

-   [<span data-ttu-id="63dc3-107">Itens de aplicativo</span><span class="sxs-lookup"><span data-stu-id="63dc3-107">Application Items</span></span>](#application-items)
-   [<span data-ttu-id="63dc3-108">Sinalizadores de item</span><span class="sxs-lookup"><span data-stu-id="63dc3-108">Item Flags</span></span>](#item-flags)
-   [<span data-ttu-id="63dc3-109">Categorias de item</span><span class="sxs-lookup"><span data-stu-id="63dc3-109">Item Categories</span></span>](#item-categories)
-   [<span data-ttu-id="63dc3-110">Item raiz</span><span class="sxs-lookup"><span data-stu-id="63dc3-110">Root Item</span></span>](#root-item)
-   [<span data-ttu-id="63dc3-111">Item de dados</span><span class="sxs-lookup"><span data-stu-id="63dc3-111">Data Item</span></span>](#data-item)
-   [<span data-ttu-id="63dc3-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63dc3-112">Related topics</span></span>](#related-topics)

## <a name="application-items"></a><span data-ttu-id="63dc3-113">Itens de aplicativo</span><span class="sxs-lookup"><span data-stu-id="63dc3-113">Application Items</span></span>

<span data-ttu-id="63dc3-114">A árvore de itens WIA 2,0 que um aplicativo pode ver é separada da árvore criada e mantida por uma minidriver WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="63dc3-114">The WIA 2.0 item tree that an application can see is separate from the tree created and maintained by a WIA 2.0 minidriver.</span></span> <span data-ttu-id="63dc3-115">Quando um minidriver cria uma árvore, o serviço WIA 2,0 usa essa árvore de itens WIA 2,0 como um guia para criar uma cópia da árvore que pode ser exibida por aplicativos de geração de imagens.</span><span class="sxs-lookup"><span data-stu-id="63dc3-115">When a minidriver creates a tree, the WIA 2.0 service uses this WIA 2.0 item tree as a guide to create a copy of the tree that can be viewed by imaging applications.</span></span> <span data-ttu-id="63dc3-116">Os itens na árvore copiada são chamados de itens de *aplicativo* .</span><span class="sxs-lookup"><span data-stu-id="63dc3-116">Items in the copied tree are called *application* items.</span></span> <span data-ttu-id="63dc3-117">Os itens na árvore criados por um minidriver são chamados de itens de *Driver* .</span><span class="sxs-lookup"><span data-stu-id="63dc3-117">Items in the tree created by a minidriver are called *driver* items.</span></span>

<span data-ttu-id="63dc3-118">Um item WIA pode representar uma fonte de dados programável para o alimentador de documentos de um scanner ou os dados armazenados nesse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63dc3-118">A WIA item can represent a programmable data source for a scanner's document feeder or the data stored on that device.</span></span> <span data-ttu-id="63dc3-119">Um dispositivo WIA deve ser dividido em itens individuais que descrevem diferentes dados produzidos por esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63dc3-119">A WIA device should be divided into individual items that describe different data produced by that device.</span></span>

<span data-ttu-id="63dc3-120">Por exemplo, um scanner WIA que dá suporte à verificação de mesa e à verificação do alimentador de documentos pode ser dividido em dois itens filho.</span><span class="sxs-lookup"><span data-stu-id="63dc3-120">For example, a WIA scanner that supports both flatbed scanning and document feeder scanning might be divided into two child items.</span></span> <span data-ttu-id="63dc3-121">Uma representa a funcionalidade de digitalização de mesa e a outra representa a funcionalidade de verificação do alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="63dc3-121">One represents the flatbed scanning functionality and the other represents the document feeder scanning functionality.</span></span>

<span data-ttu-id="63dc3-122">Várias imagens dispostas em um scanner de mesa e verificadas ao mesmo tempo podem ser colocadas em uma única pasta.</span><span class="sxs-lookup"><span data-stu-id="63dc3-122">Multiple images laid out on a flatbed scanner and scanned at the same time can be placed in one folder.</span></span> <span data-ttu-id="63dc3-123">Usando o filtro de segmentação ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), cada imagem ou subregião pode ser criada como um item filho da pasta.</span><span class="sxs-lookup"><span data-stu-id="63dc3-123">Using the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), each image or subregion can then be created as a child item of the folder.</span></span>

<span data-ttu-id="63dc3-124">A árvore WIA para um dispositivo de câmera que armazena fotos ("filme") pode ser dividida em itens que representam pastas, subpastas e fotos.</span><span class="sxs-lookup"><span data-stu-id="63dc3-124">The WIA tree for a camera device that stores photos ("Film") can be divided into items that represent folders, subfolders, and photos.</span></span>

## <a name="item-flags"></a><span data-ttu-id="63dc3-125">Sinalizadores de item</span><span class="sxs-lookup"><span data-stu-id="63dc3-125">Item Flags</span></span>

<span data-ttu-id="63dc3-126">Os sinalizadores de item WIA ajudam a classificar o conteúdo ou o comportamento com suporte de um determinado item WIA.</span><span class="sxs-lookup"><span data-stu-id="63dc3-126">WIA item flags help classify the content or supported behavior of a particular WIA item.</span></span> <span data-ttu-id="63dc3-127">Os sinalizadores de item WIA se enquadram em dois grupos.</span><span class="sxs-lookup"><span data-stu-id="63dc3-127">WIA item flags fall into two groups.</span></span>

1.  <span data-ttu-id="63dc3-128">Sinalizadores de status do item relatam o estado atual do item WIA, por exemplo, [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted** e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="63dc3-128">Item status flags report the current state of the WIA item, for example, [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted**, and so forth.</span></span>
2.  <span data-ttu-id="63dc3-129">Sinalizadores de uso/representação de dados do item relatam os dados que o item WIA representa ou que podem produzir se transferidos.</span><span class="sxs-lookup"><span data-stu-id="63dc3-129">Item data representation/usage flags report the data that the WIA item represents or can produce if transferred.</span></span> <span data-ttu-id="63dc3-130">Por exemplo, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) é um sinalizador de representação de dados que informa ao aplicativo que os dados associados ao item WIA atual são dados de imagem e devem ter propriedades de dados de imagem.</span><span class="sxs-lookup"><span data-stu-id="63dc3-130">For example, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) is a data representation flag that tells the application the data associated with the current WIA item is image data and should have image data properties.</span></span> <span data-ttu-id="63dc3-131">**WIA \_ \_ \_ Sinalizadores de item de IPA** é um sinalizador de uso de item que informa ao aplicativo que o item WIA é configurável e segue um conjunto de regras de configuração predefinidas com base na [**\_ \_ \_ categoria de item IPA WIA**](-wia-wiaitempropcommonitem.md) e que a configuração pode, possivelmente, alterar o resultado para cada transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="63dc3-131">**WIA\_IPA\_ITEM\_FLAGS** is an item usage flag that tells the application that the WIA item is configurable and follows a set of predefined configuration rules based on the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) and that the configuration can possibly change the result for each data transfer.</span></span> <span data-ttu-id="63dc3-132">(Para obter mais informações sobre definições de categoria, consulte categorias de item [categorias de item](#item-categories) .)</span><span class="sxs-lookup"><span data-stu-id="63dc3-132">(For more information about category definitions, see [Item Categories](#item-categories) item categories.)</span></span>

<span data-ttu-id="63dc3-133">O gráfico a seguir mostra um exemplo de uma árvore de itens WIA e os vários sinalizadores que podem ser associados a cada item.</span><span class="sxs-lookup"><span data-stu-id="63dc3-133">The following graphic shows an example of a WIA item tree and the various flags that might be associated with each item.</span></span>

![exemplos de sinalizadores de item para itens em uma árvore](images/scannertree1.jpg)

## <a name="item-categories"></a><span data-ttu-id="63dc3-135">Categorias de item</span><span class="sxs-lookup"><span data-stu-id="63dc3-135">Item Categories</span></span>

<span data-ttu-id="63dc3-136">Os itens WIA são agrupados em categorias usando os valores de propriedade de [**\_ \_ \_ categoria do item IPA WIA**](-wia-wiaitempropcommonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="63dc3-136">WIA items are grouped into categories using the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) property values.</span></span> <span data-ttu-id="63dc3-137">Essas categorias definem como um item WIA deve ser tratado ou usado.</span><span class="sxs-lookup"><span data-stu-id="63dc3-137">These categories define how a WIA item is to be treated or used.</span></span> <span data-ttu-id="63dc3-138">Por exemplo, se o item representa um arquivo concluído ( \_ arquivo de categoria WIA \_ concluído \_ ), um aplicativo WIA deve assumir que os dados são estáticos e localizados no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63dc3-138">For example, if the item represents a finished file (WIA\_CATEGORY\_FINISHED\_FILE), a WIA application should assume that the data is static and located on the device.</span></span> <span data-ttu-id="63dc3-139">Se o item representa um alimentador ( \_ alimentador de categoria WIA \_ ), o aplicativo deve esperar que ele contenha as propriedades necessárias do alimentador de documentos e opere como um alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="63dc3-139">If the item represents a feeder (WIA\_CATEGORY\_FEEDER), the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span>

<span data-ttu-id="63dc3-140">As categorias definidas por WIA são:</span><span class="sxs-lookup"><span data-stu-id="63dc3-140">The categories defined by WIA are:</span></span>

-   <span data-ttu-id="63dc3-141">\_automático da categoria WIA \_</span><span class="sxs-lookup"><span data-stu-id="63dc3-141">WIA\_CATEGORY\_AUTO</span></span>
-   <span data-ttu-id="63dc3-142">\_alimentador de categoria WIA \_</span><span class="sxs-lookup"><span data-stu-id="63dc3-142">WIA\_CATEGORY\_FEEDER</span></span>
-   <span data-ttu-id="63dc3-143">\_filme de categoria WIA \_</span><span class="sxs-lookup"><span data-stu-id="63dc3-143">WIA\_CATEGORY\_FILM</span></span>
-   <span data-ttu-id="63dc3-144">\_arquivo de categoria WIA \_ concluído \_</span><span class="sxs-lookup"><span data-stu-id="63dc3-144">WIA\_CATEGORY\_FINISHED\_FILE</span></span>
-   <span data-ttu-id="63dc3-145">\_superfície da categoria WIA \_</span><span class="sxs-lookup"><span data-stu-id="63dc3-145">WIA\_CATEGORY\_FLATBED</span></span>

<span data-ttu-id="63dc3-146">Por exemplo, o item de mesa de um scanner pode ter os [**\_ \_ \_ sinalizadores de item IPA WIA**](-wia-wiaitempropcommonitem.md) definidos como [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer** e **WiaItemTypeProgrammableDataSource**, e a propriedade de **categoria de \_ item de IPA \_ \_ WIA** definida como a \_ superfície de categoria WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="63dc3-146">For example, a scanner's flatbed item may have the [**WIA\_IPA\_ITEM\_FLAGS**](-wia-wiaitempropcommonitem.md) set to [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer**, and **WiaItemTypeProgrammableDataSource**, and the **WIA\_IPA\_ITEM\_CATEGORY** property set to WIA\_CATEGORY\_FLATBED.</span></span>

<span data-ttu-id="63dc3-147">A tabela a seguir mostra o agrupamento de categorias WIA com sinalizadores de item e itens WIA.</span><span class="sxs-lookup"><span data-stu-id="63dc3-147">The following table shows WIA category grouping with item flags and WIA items.</span></span> <span data-ttu-id="63dc3-148">Esta tabela não inclui uma lista completa dos sinalizadores de item WIA definidos pelo WIA.</span><span class="sxs-lookup"><span data-stu-id="63dc3-148">This table does not include a full list of the WIA item flags defined by WIA.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63dc3-149">Categoria WIA</span><span class="sxs-lookup"><span data-stu-id="63dc3-149">WIA Category</span></span></th>
<th><span data-ttu-id="63dc3-150">Sinalizadores de item WIA válidos</span><span class="sxs-lookup"><span data-stu-id="63dc3-150">Valid WIA Item Flags</span></span></th>
<th><span data-ttu-id="63dc3-151">Conjunto de propriedades WIA</span><span class="sxs-lookup"><span data-stu-id="63dc3-151">WIA Property Set</span></span></th>
<th><span data-ttu-id="63dc3-152">Itens WIA</span><span class="sxs-lookup"><span data-stu-id="63dc3-152">WIA Items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63dc3-153">WIA_CATEGORY_AUTO</span><span class="sxs-lookup"><span data-stu-id="63dc3-153">WIA_CATEGORY_AUTO</span></span></td>
<td><ul>
<li><span data-ttu-id="63dc3-154"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-154"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-155"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-155"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-156"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-156"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-157"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-157"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="63dc3-158">O conjunto de propriedades inclui propriedades de scanner configuradas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="63dc3-158">Property set includes auto-configured scanner properties.</span></span></td>
<td><span data-ttu-id="63dc3-159">O item automático WIA que representa as configurações de verificação automáticas do verificador.</span><span class="sxs-lookup"><span data-stu-id="63dc3-159">WIA auto item that represents the scanner's auto-configured scanning settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63dc3-160">WIA_CATEGORY_FEEDER</span><span class="sxs-lookup"><span data-stu-id="63dc3-160">WIA_CATEGORY_FEEDER</span></span></td>
<td><ul>
<li><span data-ttu-id="63dc3-161"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-161"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-162"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-162"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-163"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-163"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-164"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-164"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-165"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-165"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="63dc3-166">O conjunto de propriedades inclui propriedades do controle do scanner do Feeder (geralmente imagem e conjunto de propriedades específicas do documento).</span><span class="sxs-lookup"><span data-stu-id="63dc3-166">Property set includes feeder scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="63dc3-167">Itens do alimentador WIA, incluindo itens filho que representam as páginas de frente e de trás de um documento.</span><span class="sxs-lookup"><span data-stu-id="63dc3-167">WIA Feeder items, including child items that represent the front and back pages of a document.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63dc3-168">WIA_CATEGORY_FILM</span><span class="sxs-lookup"><span data-stu-id="63dc3-168">WIA_CATEGORY_FILM</span></span></td>
<td><ul>
<li><span data-ttu-id="63dc3-169"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-169"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-170"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-170"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-171"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-171"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-172"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-172"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="63dc3-173">O conjunto de propriedades inclui propriedades de controle de scanner de filme (geralmente imagem e conjunto de propriedades específicas de documento).</span><span class="sxs-lookup"><span data-stu-id="63dc3-173">Property set includes film scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="63dc3-174">Itens de filme WIA, incluindo itens filho que representam os quadros de verificação individuais.</span><span class="sxs-lookup"><span data-stu-id="63dc3-174">WIA Film items, including child items that represent the individual scanning frames.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63dc3-175">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="63dc3-175">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><ul>
<li><span data-ttu-id="63dc3-176"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-176"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-177"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-177"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-178"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-178"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-179"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-179"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-180"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-180"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-181"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-181"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="63dc3-182">A propriedade definida neste item depende do tipo de item relatado.</span><span class="sxs-lookup"><span data-stu-id="63dc3-182">The property set on this item depends on the item type reported.</span></span> <span data-ttu-id="63dc3-183">Por exemplo, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> deve incluir algumas propriedades de item de imagem, como bits por pixel e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="63dc3-183">For example, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> should include some image item properties, like bits per pixel and so forth.</span></span></td>
<td><span data-ttu-id="63dc3-184">Itens de armazenamento WIA, incluindo itens filho que representam o conteúdo do arquivo concluído (arquivos de dados como JPEG, HTML, TXT e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="63dc3-184">WIA storage items, including child items that represent finished file content (data files like JPEG, HTML, TXT, and so forth).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63dc3-185">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="63dc3-185">WIA_CATEGORY_FLATBED</span></span></td>
<td><ul>
<li><span data-ttu-id="63dc3-186"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-186"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-187"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-187"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-188"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-188"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-189"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="63dc3-189"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="63dc3-190"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>— pode estar presente se o verificador oferecer suporte à verificação de vários itens.</span><span class="sxs-lookup"><span data-stu-id="63dc3-190"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>—may be present if the scanner supports multi-item scanning.</span></span></li>
<li><span data-ttu-id="63dc3-191"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>— pode estar presente se o aplicativo gerar um item WIA durante uma sessão de verificação de vários itens.</span><span class="sxs-lookup"><span data-stu-id="63dc3-191"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>—may be present if the application generates a WIA item during a multi-item scanning session.</span></span></li>
</ul></td>
<td><span data-ttu-id="63dc3-192">O conjunto de propriedades inclui as propriedades do controle do scanner de mesa (geralmente imagem e conjunto de propriedades específicas do documento).</span><span class="sxs-lookup"><span data-stu-id="63dc3-192">The property set includes flatbed scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="63dc3-193">Itens de mesa WIA, incluindo itens filho que representam regiões sendo examinadas no cilindro de mesa do scanner.</span><span class="sxs-lookup"><span data-stu-id="63dc3-193">WIA flatbed items, including child items that represent regions being scanned on the scanner's flatbed platen.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="63dc3-194">O gráfico a seguir mostra um exemplo de uma árvore de itens WIA e as várias categorias que podem ser associadas a cada item.</span><span class="sxs-lookup"><span data-stu-id="63dc3-194">The following graphic shows an example of a WIA item tree and the various categories that might be associated with each item.</span></span>

![exemplos de categorias de item para itens em uma árvore](images/scannertree2.jpg)

## <a name="root-item"></a><span data-ttu-id="63dc3-196">Item raiz</span><span class="sxs-lookup"><span data-stu-id="63dc3-196">Root Item</span></span>

<span data-ttu-id="63dc3-197">Um item raiz WIA é um item de pasta marcado com sinalizadores [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) e **WiaItemTypeDevice** que representa o próprio dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63dc3-197">A WIA root item is a folder item marked with [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) and **WiaItemTypeDevice** flags that represents the device itself.</span></span> <span data-ttu-id="63dc3-198">Ele contém atributos de dispositivo, como fabricante, nome do dispositivo e atributos de driver, como versão do driver e identificador de classe de interface do usuário (CLSID).</span><span class="sxs-lookup"><span data-stu-id="63dc3-198">It contains device attributes like manufacturer, device name, and driver attributes like driver version and user interface class identifier (CLSID).</span></span> <span data-ttu-id="63dc3-199">Os aplicativos de geração de imagens obtêm a raiz para a árvore de itens WIA chamando o método [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="63dc3-199">Imaging applications get the root to the WIA item tree by calling [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md) method.</span></span> <span data-ttu-id="63dc3-200">O aplicativo usa o item raiz para obter acesso aos itens WIA filho individuais enumerando a árvore (consulte [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span><span class="sxs-lookup"><span data-stu-id="63dc3-200">The application uses the root item to gain access to the individual child WIA items by enumerating the tree (see [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span></span>

## <a name="data-item"></a><span data-ttu-id="63dc3-201">Item de Dados</span><span class="sxs-lookup"><span data-stu-id="63dc3-201">Data Item</span></span>

<span data-ttu-id="63dc3-202">Qualquer item que possa ser usado para transferir dados é considerado um item de dados.</span><span class="sxs-lookup"><span data-stu-id="63dc3-202">Any item that can be use to transfer data is considered a data item.</span></span> <span data-ttu-id="63dc3-203">Isso inclui itens marcados com o sinalizador [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="63dc3-203">This includes items marked with the [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) flag.</span></span>

<span data-ttu-id="63dc3-204">Itens de pasta e itens não de pasta podem expor a capacidade de transferir dados, sendo marcados com o sinalizador [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="63dc3-204">Folder items and nonfolder items can expose the ability to transfer data by being marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag.</span></span> <span data-ttu-id="63dc3-205">Qualquer item com esse sinalizador definido deve fornecer as seguintes propriedades de item WIA:</span><span class="sxs-lookup"><span data-stu-id="63dc3-205">Any item with this flag set has to provide the following WIA item properties:</span></span>

-   [<span data-ttu-id="63dc3-206">**\_direitos de \_ acesso \_ IPA WIA**</span><span class="sxs-lookup"><span data-stu-id="63dc3-206">**WIA\_IPA\_ACCESS\_RIGHTS**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="63dc3-207">**\_tamanho do \_ item \_ IPA WIA**</span><span class="sxs-lookup"><span data-stu-id="63dc3-207">**WIA\_IPA\_ITEM\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="63dc3-208">**\_tamanho do \_ buffer \_ IPA WIA**</span><span class="sxs-lookup"><span data-stu-id="63dc3-208">**WIA\_IPA\_BUFFER\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="63dc3-209">**\_formato IPA \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="63dc3-209">**WIA\_IPA\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="63dc3-210">**\_ \_ formato preferencial IPA \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="63dc3-210">**WIA\_IPA\_PREFERRED\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="63dc3-211">**\_TYMED IPA \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="63dc3-211">**WIA\_IPA\_TYMED**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="63dc3-212">**\_extensão de \_ nome de arquivo WIA IPA \_**</span><span class="sxs-lookup"><span data-stu-id="63dc3-212">**WIA\_IPA\_FILENAME\_EXTENSION**</span></span>](-wia-wiaitempropcommonitem.md)

<span data-ttu-id="63dc3-213">Itens de fonte de dados programáveis marcados com o sinalizador [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) também devem fornecer o conjunto de propriedades de item de dados necessário.</span><span class="sxs-lookup"><span data-stu-id="63dc3-213">Programmable data source items marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag must also supply the data item required property set.</span></span>

<span data-ttu-id="63dc3-214">Os itens de dados WIA podem ter propriedades adicionais, dependendo das configurações de sinalizador do item.</span><span class="sxs-lookup"><span data-stu-id="63dc3-214">WIA data items may have additional properties depending on the item's flag settings.</span></span> <span data-ttu-id="63dc3-215">Por exemplo, os itens WIA marcados com o sinalizador [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) devem ter propriedades de informações específicas da imagem, como a [**\_ \_ profundidade IPA do WIA**](-wia-wiaitempropcommonitem.md) e o **\_ \_ número \_ de \_ linhas IPA do WIA**.</span><span class="sxs-lookup"><span data-stu-id="63dc3-215">For example, WIA items marked with the [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) flag should have image specific information properties, like [**WIA\_IPA\_DEPTH**](-wia-wiaitempropcommonitem.md) and **WIA\_IPA\_NUMBER\_OF\_LINES**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63dc3-216">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63dc3-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="63dc3-217">**Referência**</span><span class="sxs-lookup"><span data-stu-id="63dc3-217">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="63dc3-218">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="63dc3-218">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="63dc3-219">**IEnumWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="63dc3-219">**IEnumWiaItem2**</span></span>](-wia-ienumwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="63dc3-220">**IWiaDevMgr2**</span><span class="sxs-lookup"><span data-stu-id="63dc3-220">**IWiaDevMgr2**</span></span>](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 



