---
description: O exemplo de código PropertyEdit demonstra como converter o nome da propriedade canônica em um PROPERTYKEY, definir o valor do repositório de propriedades para o do item e gravar os dados de volta no fluxo de arquivos.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826913"
---
# <a name="propertyedit"></a><span data-ttu-id="e5144-103">PropertyEdit</span><span class="sxs-lookup"><span data-stu-id="e5144-103">PropertyEdit</span></span>

<span data-ttu-id="e5144-104">O exemplo de código PropertyEdit demonstra como converter o nome da propriedade canônica em um PROPERTYKEY, definir o valor do repositório de propriedades para o do item e gravar os dados de volta no fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e5144-104">The PropertyEdit code sample demonstrates how to convert the canonical property name to a PROPERTYKEY, set the value of the property store to that of the item, and write the data back to the file stream.</span></span>

<span data-ttu-id="e5144-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e5144-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e5144-106">Requirements</span><span class="sxs-lookup"><span data-stu-id="e5144-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e5144-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e5144-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="e5144-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e5144-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="e5144-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e5144-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="e5144-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5144-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="e5144-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5144-111">Requirements</span></span>



| <span data-ttu-id="e5144-112">Produto</span><span class="sxs-lookup"><span data-stu-id="e5144-112">Product</span></span>     | <span data-ttu-id="e5144-113">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="e5144-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="e5144-114">Windows</span><span class="sxs-lookup"><span data-stu-id="e5144-114">Windows</span></span>     | <span data-ttu-id="e5144-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e5144-115">Windows 7</span></span>               |
| <span data-ttu-id="e5144-116">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="e5144-116">Windows SDK</span></span> | <span data-ttu-id="e5144-117">7.0</span><span class="sxs-lookup"><span data-stu-id="e5144-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="e5144-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e5144-118">Downloading the Sample</span></span>

<span data-ttu-id="e5144-119">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="e5144-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="e5144-120">Local</span><span class="sxs-lookup"><span data-stu-id="e5144-120">Location</span></span>      | <span data-ttu-id="e5144-121">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="e5144-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="e5144-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="e5144-122">GitHub</span></span>  | [<span data-ttu-id="e5144-123">Exemplo de PropertyEdit</span><span class="sxs-lookup"><span data-stu-id="e5144-123">PropertyEdit sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> <span data-ttu-id="e5144-124">Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.</span><span class="sxs-lookup"><span data-stu-id="e5144-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="e5144-125">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e5144-125">Building the Sample</span></span>

<span data-ttu-id="e5144-126">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="e5144-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="e5144-127">Abra a janela do prompt de comando e navegue até o diretório do projeto **PropertyEdit** .</span><span class="sxs-lookup"><span data-stu-id="e5144-127">Open the Command Prompt window and navigate to the **PropertyEdit** project directory.</span></span> 
2.  <span data-ttu-id="e5144-128">Digite `msbuild PropertyEdit.sln`.</span><span class="sxs-lookup"><span data-stu-id="e5144-128">Enter `msbuild PropertyEdit.sln`.</span></span>

<span data-ttu-id="e5144-129">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="e5144-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="e5144-130">Abra o Windows Explorer e navegue até o diretório do projeto **PropertyEdit** .</span><span class="sxs-lookup"><span data-stu-id="e5144-130">Open Windows Explorer and navigate to the **PropertyEdit** project directory.</span></span>
2.  <span data-ttu-id="e5144-131">Clique duas vezes no ícone do arquivo PropertyEdit. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e5144-131">Double-click the icon for the PropertyEdit.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="e5144-132">A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="e5144-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="e5144-133">Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".</span><span class="sxs-lookup"><span data-stu-id="e5144-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="e5144-134">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="e5144-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="e5144-135">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e5144-135">Running the Sample</span></span>

1.  <span data-ttu-id="e5144-136">Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="e5144-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="e5144-137">No prompt de comando, digite `PropertyEdit.exe` ou, no Windows Explorer, clique duas vezes no ícone para PropertyEdit.exe.</span><span class="sxs-lookup"><span data-stu-id="e5144-137">At the command prompt, enter `PropertyEdit.exe`, or from Windows Explorer, double-click the icon for PropertyEdit.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5144-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5144-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e5144-139">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="e5144-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e5144-140">Exemplos de código de pesquisa</span><span class="sxs-lookup"><span data-stu-id="e5144-140">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="e5144-141">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="e5144-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e5144-142">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="e5144-142">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[<span data-ttu-id="e5144-143">Sobre manipuladores de propriedade e propriedades</span><span class="sxs-lookup"><span data-stu-id="e5144-143">About Properties and Property Handlers</span></span>](../properties/building-property-handlers-properties.md)
</dt> <dt>

<span data-ttu-id="e5144-144">[Esquema de descrição da propriedade](/previous-versions//cc144127(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e5144-144">[Property Description Schema](/previous-versions//cc144127(v=vs.85))</span></span>
</dt> </dl>

 

 
