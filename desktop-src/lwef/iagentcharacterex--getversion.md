---
title: GetVersion do IAgentCharacterEx
description: GetVersion do IAgentCharacterEx
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c72d9304aa689cda83117d57f26c2da776c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005331"
---
# <a name="iagentcharacterexgetversion"></a><span data-ttu-id="d8eb8-103">IAgentCharacterEx:: GetVersion</span><span class="sxs-lookup"><span data-stu-id="d8eb8-103">IAgentCharacterEx::GetVersion</span></span>

<span data-ttu-id="d8eb8-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d8eb8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

<span data-ttu-id="d8eb8-105">Recupera o número de versão do conjunto de animações padrão de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8eb8-105">Retrieves the version number of the character standard animation set.</span></span>

-   <span data-ttu-id="d8eb8-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d8eb8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d8eb8-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span><span class="sxs-lookup"><span data-stu-id="d8eb8-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span></span>
</dt> <dd>

<span data-ttu-id="d8eb8-108">Endereço de uma variável que recebe a versão principal.</span><span class="sxs-lookup"><span data-stu-id="d8eb8-108">Address of a variable that receives the major version.</span></span>

</dd> <dt>

<span data-ttu-id="d8eb8-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span><span class="sxs-lookup"><span data-stu-id="d8eb8-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span></span>
</dt> <dd>

<span data-ttu-id="d8eb8-110">Endereço de uma variável que recebe a versão secundária.</span><span class="sxs-lookup"><span data-stu-id="d8eb8-110">Address of a variable that receives the minor version.</span></span>

</dd> </dl>

<span data-ttu-id="d8eb8-111">O número de versão do conjunto de animações padrão é definido automaticamente quando você o cria com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d8eb8-111">The standard animation set version number is automatically set when you build it with the Microsoft Agent Character Editor.</span></span>

 

 




