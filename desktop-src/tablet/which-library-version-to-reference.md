---
description: Este tópico descreve as diferenças entre as versões binárias da biblioteca do Tablet PC.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Qual versão da biblioteca deve ser referenciada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781556"
---
# <a name="which-library-version-to-reference"></a><span data-ttu-id="2e853-103">Qual versão da biblioteca deve ser referenciada</span><span class="sxs-lookup"><span data-stu-id="2e853-103">Which Library Version to Reference</span></span>

<span data-ttu-id="2e853-104">Este tópico descreve as diferenças entre as versões binárias da biblioteca do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="2e853-104">This topic describes the differences between the Tablet PC library binary versions.</span></span>

## <a name="tablet-pc-library-versions"></a><span data-ttu-id="2e853-105">Versões da biblioteca do Tablet PC</span><span class="sxs-lookup"><span data-stu-id="2e853-105">Tablet PC Library Versions</span></span>

<span data-ttu-id="2e853-106">Os binários da biblioteca do Tablet PC (Microsoft.Ink.dll) foram atualizados no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2e853-106">The Tablet PC library binaries (Microsoft.Ink.dll) have been updated in Windows Vista.</span></span> <span data-ttu-id="2e853-107">Esses binários são chamados de "versão 6,0" para incide com a versão do Windows na qual estão sendo lançados.</span><span class="sxs-lookup"><span data-stu-id="2e853-107">Theses binaries are referred to as "version 6.0" to co-incide with the version of Windows in which they are being released.</span></span>

<span data-ttu-id="2e853-108">A versão mais recente dos binários que são compatíveis com o Windows XP é conhecida como "versão 1,7".</span><span class="sxs-lookup"><span data-stu-id="2e853-108">The most recent release of the binaries that are compatible with Windows XP is referred to as "version 1.7".</span></span>

<span data-ttu-id="2e853-109">O SDK do Windows pode ser instalado em computadores com vista e XP, e o SDK do Windows inclui as duas versões do Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="2e853-109">The Windows SDK can be installed on both Vista and XP machines, and the Windows SDK includes both versions of Microsoft.Ink.dll.</span></span>

<span data-ttu-id="2e853-110">Eles são instalados em:</span><span class="sxs-lookup"><span data-stu-id="2e853-110">These are installed in:</span></span>

1. <span data-ttu-id="2e853-111">% ProgramFiles% \\ Reference Assemblies \\ Microsoft \\ Tablet PC \\ v 1.7 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="2e853-111">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v1.7\\Microsoft.Ink.dll</span></span>

2. <span data-ttu-id="2e853-112">% ProgramFiles% \\ Reference Assemblies \\ Microsoft \\ Tablet PC \\ v 6.0 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="2e853-112">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v6.0\\Microsoft.Ink.dll</span></span>

<span data-ttu-id="2e853-113">Os binários da versão 6,0 são compatíveis apenas com o Windows Vista, e os aplicativos escritos neles só devem ser executados no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2e853-113">The version 6.0 binaries are only compatible with Windows Vista, and applications written against them should only ever be run on Windows Vista.</span></span>

<span data-ttu-id="2e853-114">Um aplicativo escrito em relação aos binários da versão 1,7 deve ser executado sem modificação quando instalado no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2e853-114">An application written against the version 1.7 binaries should run without modification when installed on Windows Vista.</span></span>

 

 



