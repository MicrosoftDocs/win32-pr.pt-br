---
description: As sequências de ação sugeridas para uma tabela InstalUISequence básica em um banco de dados Windows Installer.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: InstallUISequence sugerido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751626"
---
# <a name="suggested-installuisequence"></a><span data-ttu-id="f486f-103">InstallUISequence sugerido</span><span class="sxs-lookup"><span data-stu-id="f486f-103">Suggested InstallUISequence</span></span>



| <span data-ttu-id="f486f-104">Ação</span><span class="sxs-lookup"><span data-stu-id="f486f-104">Action</span></span>                                          | <span data-ttu-id="f486f-105">Condição</span><span class="sxs-lookup"><span data-stu-id="f486f-105">Condition</span></span>                                                                                                  | <span data-ttu-id="f486f-106">Sequência</span><span class="sxs-lookup"><span data-stu-id="f486f-106">Sequence</span></span> |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="f486f-107">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="f486f-107">FatalErrorDlg</span></span>                                   |                                                                                                            | <span data-ttu-id="f486f-108">-3</span><span class="sxs-lookup"><span data-stu-id="f486f-108">-3</span></span>       |
| <span data-ttu-id="f486f-109">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="f486f-109">UserExitDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="f486f-110">-2</span><span class="sxs-lookup"><span data-stu-id="f486f-110">-2</span></span>       |
| <span data-ttu-id="f486f-111">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="f486f-111">ExitDlg</span></span>                                         |                                                                                                            | <span data-ttu-id="f486f-112">-1</span><span class="sxs-lookup"><span data-stu-id="f486f-112">-1</span></span>       |
| [<span data-ttu-id="f486f-113">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="f486f-113">LaunchConditions</span></span>](launchconditions-action.md) |                                                                                                            | <span data-ttu-id="f486f-114">100</span><span class="sxs-lookup"><span data-stu-id="f486f-114">100</span></span>      |
| <span data-ttu-id="f486f-115">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="f486f-115">PrepareDlg</span></span>                                      |                                                                                                            | <span data-ttu-id="f486f-116">140</span><span class="sxs-lookup"><span data-stu-id="f486f-116">140</span></span>      |
| [<span data-ttu-id="f486f-117">AppSearch</span><span class="sxs-lookup"><span data-stu-id="f486f-117">AppSearch</span></span>](appsearch-action.md)               |                                                                                                            | <span data-ttu-id="f486f-118">400</span><span class="sxs-lookup"><span data-stu-id="f486f-118">400</span></span>      |
| [<span data-ttu-id="f486f-119">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="f486f-119">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="f486f-120">Não [ **instalado**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="f486f-120">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="f486f-121">500</span><span class="sxs-lookup"><span data-stu-id="f486f-121">500</span></span>      |
| [<span data-ttu-id="f486f-122">RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="f486f-122">RMCCPSearch</span></span>](rmccpsearch-action.md)           | <span data-ttu-id="f486f-123">Não [ **instalado**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="f486f-123">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="f486f-124">600</span><span class="sxs-lookup"><span data-stu-id="f486f-124">600</span></span>      |
| [<span data-ttu-id="f486f-125">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="f486f-125">CostInitialize</span></span>](costinitialize-action.md)     |                                                                                                            | <span data-ttu-id="f486f-126">800</span><span class="sxs-lookup"><span data-stu-id="f486f-126">800</span></span>      |
| [<span data-ttu-id="f486f-127">Custo de</span><span class="sxs-lookup"><span data-stu-id="f486f-127">FileCost</span></span>](filecost-action.md)                 |                                                                                                            | <span data-ttu-id="f486f-128">900</span><span class="sxs-lookup"><span data-stu-id="f486f-128">900</span></span>      |
| [<span data-ttu-id="f486f-129">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="f486f-129">CostFinalize</span></span>](costfinalize-action.md)         |                                                                                                            | <span data-ttu-id="f486f-130">1000</span><span class="sxs-lookup"><span data-stu-id="f486f-130">1000</span></span>     |
| <span data-ttu-id="f486f-131">WelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="f486f-131">WelcomeDlg</span></span>                                      | <span data-ttu-id="f486f-132">Não [ **instalado**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="f486f-132">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="f486f-133">1230</span><span class="sxs-lookup"><span data-stu-id="f486f-133">1230</span></span>     |
| <span data-ttu-id="f486f-134">ResumeDlg</span><span class="sxs-lookup"><span data-stu-id="f486f-134">ResumeDlg</span></span>                                       | <span data-ttu-id="f486f-135">[**Instalado**](installed.md) E ( [**retomar**](resume.md) ou [**selecionável**](preselected.md))</span><span class="sxs-lookup"><span data-stu-id="f486f-135">[**Installed**](installed.md) AND ( [**RESUME**](resume.md) OR [**Preselected**](preselected.md))</span></span>       | <span data-ttu-id="f486f-136">1240</span><span class="sxs-lookup"><span data-stu-id="f486f-136">1240</span></span>     |
| <span data-ttu-id="f486f-137">MaintenanceWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="f486f-137">MaintenanceWelcomeDlg</span></span>                           | <span data-ttu-id="f486f-138">[**Instalado**](installed.md) E não [**retomar**](resume.md) e não [**selecionável**](preselected.md)</span><span class="sxs-lookup"><span data-stu-id="f486f-138">[**Installed**](installed.md) AND NOT [**RESUME**](resume.md) AND NOT [**Preselected**](preselected.md)</span></span> | <span data-ttu-id="f486f-139">1250</span><span class="sxs-lookup"><span data-stu-id="f486f-139">1250</span></span>     |
| <span data-ttu-id="f486f-140">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="f486f-140">ProgressDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="f486f-141">1280</span><span class="sxs-lookup"><span data-stu-id="f486f-141">1280</span></span>     |
| [<span data-ttu-id="f486f-142">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="f486f-142">ExecuteAction</span></span>](executeaction-action.md)       |                                                                                                            | <span data-ttu-id="f486f-143">1300</span><span class="sxs-lookup"><span data-stu-id="f486f-143">1300</span></span>     |



 

 

 



