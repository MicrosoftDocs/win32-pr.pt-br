---
description: Demonstra como usar a interface Manipuladordeminiaturai para extrair a miniatura de um item do sistema de cache de miniaturas do Windows.
title: Usar exemplo de provedores de miniatura
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B5E4145A-AF9D-4b83-923A-2DC064B66E8E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e0cab8db27ddfdca0db5a7a08b6329c44776fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968072"
---
# <a name="using-thumbnail-providers-sample"></a><span data-ttu-id="9d6c0-103">Usar exemplo de provedores de miniatura</span><span class="sxs-lookup"><span data-stu-id="9d6c0-103">Using Thumbnail Providers Sample</span></span>

<span data-ttu-id="9d6c0-104">Demonstra como usar a interface [**manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) para extrair a miniatura de um item do sistema de cache de miniaturas do Windows.</span><span class="sxs-lookup"><span data-stu-id="9d6c0-104">Demonstrates how to use the [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface to extract the thumbnail for an item from the Windows thumbnail cache system.</span></span>

<span data-ttu-id="9d6c0-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d6c0-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9d6c0-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d6c0-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9d6c0-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="9d6c0-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="9d6c0-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="9d6c0-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="9d6c0-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="9d6c0-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="9d6c0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d6c0-110">Requirements</span></span>



| <span data-ttu-id="9d6c0-111">Produto</span><span class="sxs-lookup"><span data-stu-id="9d6c0-111">Product</span></span>                                | <span data-ttu-id="9d6c0-112">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="9d6c0-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="9d6c0-113">Windows</span><span class="sxs-lookup"><span data-stu-id="9d6c0-113">Windows</span></span>                                | <span data-ttu-id="9d6c0-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d6c0-114">Windows Vista</span></span>           |
| <span data-ttu-id="9d6c0-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="9d6c0-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="9d6c0-116">6.1</span><span class="sxs-lookup"><span data-stu-id="9d6c0-116">6.1</span></span>                     |



 

<span data-ttu-id="9d6c0-117">Para obter requisitos adicionais, consulte o arquivo Leiame incluído com o exemplo.</span><span class="sxs-lookup"><span data-stu-id="9d6c0-117">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="9d6c0-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="9d6c0-118">Downloading the Sample</span></span>

| <span data-ttu-id="9d6c0-119">Localização</span><span class="sxs-lookup"><span data-stu-id="9d6c0-119">Location</span></span>      | <span data-ttu-id="9d6c0-120">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="9d6c0-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d6c0-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="9d6c0-121">GitHub</span></span>  | [<span data-ttu-id="9d6c0-122">Exemplo de UsingThumbnailProviders</span><span class="sxs-lookup"><span data-stu-id="9d6c0-122">UsingThumbnailProviders sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/UsingThumbnailProviders) |

## <a name="building-the-sample"></a><span data-ttu-id="9d6c0-123">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="9d6c0-123">Building the Sample</span></span>

<span data-ttu-id="9d6c0-124">Para obter instruções sobre como criar o exemplo, consulte o arquivo Leiame incluído com o exemplo.</span><span class="sxs-lookup"><span data-stu-id="9d6c0-124">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="9d6c0-125">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="9d6c0-125">Running the Sample</span></span>

<span data-ttu-id="9d6c0-126">Para obter instruções sobre como criar o exemplo, consulte o arquivo Leiame incluído com o exemplo.</span><span class="sxs-lookup"><span data-stu-id="9d6c0-126">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



