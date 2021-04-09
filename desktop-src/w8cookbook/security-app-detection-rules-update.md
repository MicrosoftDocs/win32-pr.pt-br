---
title: Atualização de regras de detecção de aplicativo de segurança
description: Atualização de regras de detecção de aplicativo de segurança
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008497"
---
# <a name="security-app-detection-rules-update"></a><span data-ttu-id="cf776-103">Atualização de regras de detecção de aplicativo de segurança</span><span class="sxs-lookup"><span data-stu-id="cf776-103">Security app detection rules update</span></span>

## <a name="platforms"></a><span data-ttu-id="cf776-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="cf776-104">Platforms</span></span>

<span data-ttu-id="cf776-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="cf776-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="cf776-106">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf776-106">**Servers** – Windows Server 2012</span></span>  


### <a name="description"></a><span data-ttu-id="cf776-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf776-107">Description</span></span>

<span data-ttu-id="cf776-108">Os aplicativos da Windows Store que estão sendo adicionados ao Windows 8 estão sendo instalados em um local comum em "arquivos de programas" (% ProgramFiles%) chamados \\ arquivos de programas \\ WindowsApps.</span><span class="sxs-lookup"><span data-stu-id="cf776-108">The Windows Store apps being added in Windows 8 are all being installed to a common location under “Program Files” (%programfiles%) called \\program files\\WindowsApps.</span></span>

### <a name="manifestation"></a><span data-ttu-id="cf776-109">Manifestação</span><span class="sxs-lookup"><span data-stu-id="cf776-109">Manifestation</span></span>

<span data-ttu-id="cf776-110">Isso pode causar colisões com configurações existentes e alguns detectores antivírus/Antimalware veem esse local como um local potencial que é uma causa de preocupação.</span><span class="sxs-lookup"><span data-stu-id="cf776-110">This can cause collisions with existing configurations, and some antivirus/anti-malware detectors see this location as a potential location that is a cause for concern.</span></span>

### <a name="mitigation"></a><span data-ttu-id="cf776-111">Atenuação</span><span class="sxs-lookup"><span data-stu-id="cf776-111">Mitigation</span></span>

<span data-ttu-id="cf776-112">As recomendações atuais são:</span><span class="sxs-lookup"><span data-stu-id="cf776-112">The current recommendations are:</span></span>

-   <span data-ttu-id="cf776-113">Afastar-se dos \\ arquivos de programas \\ WindowsApps para armazenar aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="cf776-113">Move away from \\program files\\WindowsApps for storing any custom apps</span></span>
-   <span data-ttu-id="cf776-114">Fornecedores de antivírus/Antimalware devem atualizar sua heurística para que não identifiquem esse local como um local de malware</span><span class="sxs-lookup"><span data-stu-id="cf776-114">Antivirus/antimalware vendors should update their heuristics so they do not identify that location as a malware location</span></span>

 

 




