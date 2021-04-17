---
description: As sequências de ação sugeridas para uma tabela AdvtExecuteSequence básica em um banco de dados Windows Installer.
ms.assetid: 42a55f8f-582a-499b-8a6b-c893da62a4d4
title: AdvtExecuteSequence sugerido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a672579a174a0cc242ac503225d81976de60d9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754342"
---
# <a name="suggested-advtexecutesequence"></a><span data-ttu-id="b3385-103">AdvtExecuteSequence sugerido</span><span class="sxs-lookup"><span data-stu-id="b3385-103">Suggested AdvtExecuteSequence</span></span>



| <span data-ttu-id="b3385-104">Ação</span><span class="sxs-lookup"><span data-stu-id="b3385-104">Action</span></span>                                                    | <span data-ttu-id="b3385-105">Condição</span><span class="sxs-lookup"><span data-stu-id="b3385-105">Condition</span></span> | <span data-ttu-id="b3385-106">Sequência</span><span class="sxs-lookup"><span data-stu-id="b3385-106">Sequence</span></span> |
|-----------------------------------------------------------|-----------|----------|
| [<span data-ttu-id="b3385-107">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="b3385-107">CostInitialize</span></span>](costinitialize-action.md)               |           | <span data-ttu-id="b3385-108">800</span><span class="sxs-lookup"><span data-stu-id="b3385-108">800</span></span>      |
| [<span data-ttu-id="b3385-109">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="b3385-109">CostFinalize</span></span>](costfinalize-action.md)                   |           | <span data-ttu-id="b3385-110">1000</span><span class="sxs-lookup"><span data-stu-id="b3385-110">1000</span></span>     |
| [<span data-ttu-id="b3385-111">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="b3385-111">InstallValidate</span></span>](installvalidate-action.md)             |           | <span data-ttu-id="b3385-112">1.400</span><span class="sxs-lookup"><span data-stu-id="b3385-112">1400</span></span>     |
| [<span data-ttu-id="b3385-113">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="b3385-113">InstallInitialize</span></span>](installinitialize-action.md)         |           | <span data-ttu-id="b3385-114">1500</span><span class="sxs-lookup"><span data-stu-id="b3385-114">1500</span></span>     |
| [<span data-ttu-id="b3385-115">Createatalhos</span><span class="sxs-lookup"><span data-stu-id="b3385-115">CreateShortcuts</span></span>](createshortcuts-action.md)             |           | <span data-ttu-id="b3385-116">4500</span><span class="sxs-lookup"><span data-stu-id="b3385-116">4500</span></span>     |
| [<span data-ttu-id="b3385-117">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="b3385-117">RegisterClassInfo</span></span>](registerclassinfo-action.md)         |           | <span data-ttu-id="b3385-118">4600</span><span class="sxs-lookup"><span data-stu-id="b3385-118">4600</span></span>     |
| [<span data-ttu-id="b3385-119">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="b3385-119">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md) |           | <span data-ttu-id="b3385-120">4700</span><span class="sxs-lookup"><span data-stu-id="b3385-120">4700</span></span>     |
| [<span data-ttu-id="b3385-121">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="b3385-121">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)       |           | <span data-ttu-id="b3385-122">4800</span><span class="sxs-lookup"><span data-stu-id="b3385-122">4800</span></span>     |
| [<span data-ttu-id="b3385-123">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="b3385-123">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)           |           | <span data-ttu-id="b3385-124">4900</span><span class="sxs-lookup"><span data-stu-id="b3385-124">4900</span></span>     |
| [<span data-ttu-id="b3385-125">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="b3385-125">PublishComponents</span></span>](publishcomponents-action.md)         |           | <span data-ttu-id="b3385-126">6200</span><span class="sxs-lookup"><span data-stu-id="b3385-126">6200</span></span>     |
| [<span data-ttu-id="b3385-127">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="b3385-127">PublishFeatures</span></span>](publishfeatures-action.md)             |           | <span data-ttu-id="b3385-128">6300</span><span class="sxs-lookup"><span data-stu-id="b3385-128">6300</span></span>     |
| [<span data-ttu-id="b3385-129">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="b3385-129">PublishProduct</span></span>](publishproduct-action.md)               |           | <span data-ttu-id="b3385-130">6400</span><span class="sxs-lookup"><span data-stu-id="b3385-130">6400</span></span>     |
| [<span data-ttu-id="b3385-131">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="b3385-131">InstallFinalize</span></span>](installfinalize-action.md)             |           | <span data-ttu-id="b3385-132">6600</span><span class="sxs-lookup"><span data-stu-id="b3385-132">6600</span></span>     |



 

 

 



