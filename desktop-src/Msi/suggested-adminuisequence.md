---
description: As sequências de ação sugeridas para uma tabela AdminUISequence básica em um banco de dados Windows Installer.
ms.assetid: a5371133-7d55-4041-8e1f-ecc8245c8d3a
title: AdminUISequence sugerido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af34c0662d19070b1d97b88e8942b2276cc64a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661856"
---
# <a name="suggested-adminuisequence"></a><span data-ttu-id="147d9-103">AdminUISequence sugerido</span><span class="sxs-lookup"><span data-stu-id="147d9-103">Suggested AdminUISequence</span></span>



| <span data-ttu-id="147d9-104">Ação</span><span class="sxs-lookup"><span data-stu-id="147d9-104">Action</span></span>                                      | <span data-ttu-id="147d9-105">Condição</span><span class="sxs-lookup"><span data-stu-id="147d9-105">Condition</span></span> | <span data-ttu-id="147d9-106">Sequência</span><span class="sxs-lookup"><span data-stu-id="147d9-106">Sequence</span></span> |
|---------------------------------------------|-----------|----------|
| <span data-ttu-id="147d9-107">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="147d9-107">FatalErrorDlg</span></span>                               |           | <span data-ttu-id="147d9-108">-3</span><span class="sxs-lookup"><span data-stu-id="147d9-108">-3</span></span>       |
| <span data-ttu-id="147d9-109">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="147d9-109">UserExitDlg</span></span>                                 |           | <span data-ttu-id="147d9-110">-2</span><span class="sxs-lookup"><span data-stu-id="147d9-110">-2</span></span>       |
| <span data-ttu-id="147d9-111">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="147d9-111">ExitDlg</span></span>                                     |           | <span data-ttu-id="147d9-112">-1</span><span class="sxs-lookup"><span data-stu-id="147d9-112">-1</span></span>       |
| <span data-ttu-id="147d9-113">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="147d9-113">PrepareDlg</span></span>                                  |           | <span data-ttu-id="147d9-114">140</span><span class="sxs-lookup"><span data-stu-id="147d9-114">140</span></span>      |
| [<span data-ttu-id="147d9-115">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="147d9-115">CostInitialize</span></span>](costinitialize-action.md) |           | <span data-ttu-id="147d9-116">800</span><span class="sxs-lookup"><span data-stu-id="147d9-116">800</span></span>      |
| [<span data-ttu-id="147d9-117">Custo de</span><span class="sxs-lookup"><span data-stu-id="147d9-117">FileCost</span></span>](filecost-action.md)             |           | <span data-ttu-id="147d9-118">900</span><span class="sxs-lookup"><span data-stu-id="147d9-118">900</span></span>      |
| [<span data-ttu-id="147d9-119">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="147d9-119">CostFinalize</span></span>](costfinalize-action.md)     |           | <span data-ttu-id="147d9-120">1000</span><span class="sxs-lookup"><span data-stu-id="147d9-120">1000</span></span>     |
| <span data-ttu-id="147d9-121">AdminWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="147d9-121">AdminWelcomeDlg</span></span>                             |           | <span data-ttu-id="147d9-122">1230</span><span class="sxs-lookup"><span data-stu-id="147d9-122">1230</span></span>     |
| <span data-ttu-id="147d9-123">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="147d9-123">ProgressDlg</span></span>                                 |           | <span data-ttu-id="147d9-124">1280</span><span class="sxs-lookup"><span data-stu-id="147d9-124">1280</span></span>     |
| [<span data-ttu-id="147d9-125">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="147d9-125">ExecuteAction</span></span>](executeaction-action.md)   |           | <span data-ttu-id="147d9-126">1300</span><span class="sxs-lookup"><span data-stu-id="147d9-126">1300</span></span>     |



 

 

 



