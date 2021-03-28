---
description: Demonstra como criar uma pesquisa com restrições de consulta usando o modelo de programação shell.
title: Exemplo da pasta de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.assetid: DF3432AB-39DF-44c6-9A08-4630408D6B9B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c86a29c4a7d01fad3b91db20035cb84751e0b78a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170474"
---
# <a name="search-folder-sample"></a><span data-ttu-id="fa2f2-103">Exemplo da pasta de pesquisa</span><span class="sxs-lookup"><span data-stu-id="fa2f2-103">Search Folder Sample</span></span>

<span data-ttu-id="fa2f2-104">Demonstra como criar uma pesquisa com restrições de consulta usando o modelo de programação shell.</span><span class="sxs-lookup"><span data-stu-id="fa2f2-104">Demonstrates how to create a search with query constraints using the Shell programming model.</span></span>

<span data-ttu-id="fa2f2-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="fa2f2-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="fa2f2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa2f2-106">Description</span></span>](#description)
-   [<span data-ttu-id="fa2f2-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa2f2-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="fa2f2-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fa2f2-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="fa2f2-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fa2f2-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="fa2f2-110">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fa2f2-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="fa2f2-111">Description</span><span class="sxs-lookup"><span data-stu-id="fa2f2-111">Description</span></span>

<span data-ttu-id="fa2f2-112">Este exemplo mostra como criar uma pesquisa restrita usando a interface [**ISearchFolderItemFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) para construir um item de Shell de pasta (um contêiner) que representa a consulta.</span><span class="sxs-lookup"><span data-stu-id="fa2f2-112">This sample shows how to create a constrained search by using the [**ISearchFolderItemFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) interface to construct a folder Shell item (a container) that represents the query.</span></span> <span data-ttu-id="fa2f2-113">Os resultados são exibidos usando a caixa de diálogo abrir arquivo.</span><span class="sxs-lookup"><span data-stu-id="fa2f2-113">The results are displayed using the file open dialog.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa2f2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa2f2-114">Requirements</span></span>



| <span data-ttu-id="fa2f2-115">Produto</span><span class="sxs-lookup"><span data-stu-id="fa2f2-115">Product</span></span>                                | <span data-ttu-id="fa2f2-116">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="fa2f2-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="fa2f2-117">Windows</span><span class="sxs-lookup"><span data-stu-id="fa2f2-117">Windows</span></span>                                | <span data-ttu-id="fa2f2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa2f2-118">Windows Vista</span></span>           |
| <span data-ttu-id="fa2f2-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="fa2f2-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="fa2f2-120">7.0</span><span class="sxs-lookup"><span data-stu-id="fa2f2-120">7.0</span></span>                     |



 

<span data-ttu-id="fa2f2-121">Para obter requisitos adicionais, consulte o arquivo Leiame incluído com o exemplo.</span><span class="sxs-lookup"><span data-stu-id="fa2f2-121">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="fa2f2-122">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fa2f2-122">Downloading the Sample</span></span>

| <span data-ttu-id="fa2f2-123">Localização</span><span class="sxs-lookup"><span data-stu-id="fa2f2-123">Location</span></span>      | <span data-ttu-id="fa2f2-124">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="fa2f2-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2f2-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="fa2f2-125">GitHub</span></span>  | [<span data-ttu-id="fa2f2-126">Exemplo de SearchFolder</span><span class="sxs-lookup"><span data-stu-id="fa2f2-126">SearchFolder sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/searchfolder) |

## <a name="building-the-sample"></a><span data-ttu-id="fa2f2-127">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fa2f2-127">Building the Sample</span></span>

<span data-ttu-id="fa2f2-128">Para obter instruções sobre como criar o exemplo, consulte o arquivo Leiame incluído com o exemplo.</span><span class="sxs-lookup"><span data-stu-id="fa2f2-128">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="fa2f2-129">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fa2f2-129">Running the Sample</span></span>

<span data-ttu-id="fa2f2-130">Para obter instruções sobre como criar o exemplo, consulte o arquivo Leiame incluído com o exemplo.</span><span class="sxs-lookup"><span data-stu-id="fa2f2-130">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



