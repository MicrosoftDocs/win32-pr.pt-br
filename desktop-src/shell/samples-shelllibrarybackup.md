---
description: Demonstra como enumerar bibliotecas como contêineres.
title: Exemplo de backup da biblioteca de shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 206356B2-3998-4a19-BC4D-F6A043AFDBD3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e1b4746d2e559b567adb4cbd2305ea474b03129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968202"
---
# <a name="shell-library-backup-sample"></a><span data-ttu-id="f02ca-103">Exemplo de backup da biblioteca de shell</span><span class="sxs-lookup"><span data-stu-id="f02ca-103">Shell Library Backup Sample</span></span>

<span data-ttu-id="f02ca-104">Demonstra como enumerar bibliotecas como contêineres.</span><span class="sxs-lookup"><span data-stu-id="f02ca-104">Demonstrates how to enumerate libraries as containers.</span></span> <span data-ttu-id="f02ca-105">As bibliotecas são o novo paradigma de armazenamento para arquivos de usuário e são introduzidas no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f02ca-105">Libraries are the new storage paradigm for user files and are introduced in Windows 7.</span></span>

<span data-ttu-id="f02ca-106">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="f02ca-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f02ca-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f02ca-107">Description</span></span>](#description)
-   [<span data-ttu-id="f02ca-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f02ca-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f02ca-109">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f02ca-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="f02ca-110">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f02ca-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f02ca-111">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f02ca-111">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="f02ca-112">Description</span><span class="sxs-lookup"><span data-stu-id="f02ca-112">Description</span></span>

<span data-ttu-id="f02ca-113">Este exemplo é um aplicativo de backup fictício que mostra como escolher bibliotecas por meio da caixa de diálogo arquivo comum.</span><span class="sxs-lookup"><span data-stu-id="f02ca-113">This sample is a fictional backup application that shows how to pick libraries through the common file dialog.</span></span> <span data-ttu-id="f02ca-114">Ele também demonstra como fazer backup de bibliotecas usando o Shell namespace Walker.</span><span class="sxs-lookup"><span data-stu-id="f02ca-114">It also demonstrates how to back up libraries using the Shell namespace walker.</span></span>

## <a name="requirements"></a><span data-ttu-id="f02ca-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f02ca-115">Requirements</span></span>



| <span data-ttu-id="f02ca-116">Produto</span><span class="sxs-lookup"><span data-stu-id="f02ca-116">Product</span></span>                                | <span data-ttu-id="f02ca-117">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="f02ca-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="f02ca-118">Windows</span><span class="sxs-lookup"><span data-stu-id="f02ca-118">Windows</span></span>                                | <span data-ttu-id="f02ca-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f02ca-119">Windows 7</span></span>               |
| <span data-ttu-id="f02ca-120">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="f02ca-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="f02ca-121">7.0</span><span class="sxs-lookup"><span data-stu-id="f02ca-121">7.0</span></span>                     |



 

<span data-ttu-id="f02ca-122">Para obter requisitos adicionais, consulte o arquivo Leiame incluído com o exemplo.</span><span class="sxs-lookup"><span data-stu-id="f02ca-122">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="f02ca-123">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f02ca-123">Downloading the Sample</span></span>

| <span data-ttu-id="f02ca-124">Localização</span><span class="sxs-lookup"><span data-stu-id="f02ca-124">Location</span></span>      | <span data-ttu-id="f02ca-125">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="f02ca-125">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f02ca-126">GitHub</span><span class="sxs-lookup"><span data-stu-id="f02ca-126">GitHub</span></span>  | [<span data-ttu-id="f02ca-127">Exemplo de ShellLibraryBackup</span><span class="sxs-lookup"><span data-stu-id="f02ca-127">ShellLibraryBackup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ShellLibraryBackup) |

## <a name="building-the-sample"></a><span data-ttu-id="f02ca-128">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f02ca-128">Building the Sample</span></span>

<span data-ttu-id="f02ca-129">Para obter instruções sobre como criar o exemplo, consulte o arquivo Leiame incluído com o exemplo.</span><span class="sxs-lookup"><span data-stu-id="f02ca-129">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="f02ca-130">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f02ca-130">Running the Sample</span></span>

<span data-ttu-id="f02ca-131">Para obter instruções sobre como criar o exemplo, consulte o arquivo Leiame incluído com o exemplo.</span><span class="sxs-lookup"><span data-stu-id="f02ca-131">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



