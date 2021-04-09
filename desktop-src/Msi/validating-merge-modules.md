---
description: Os autores devem executar a validação em todos os módulos de mesclagem novos ou modificados recentemente antes de tentar mesclar o módulo em um banco de dados de instalação pela primeira vez.
ms.assetid: 8d6794af-403a-416e-8ace-1af3f193414b
title: Validando módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8bbe7f1c1ea32baa39cadd7c729f3a8ca3ac17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090767"
---
# <a name="validating-merge-modules"></a><span data-ttu-id="d483c-103">Validando módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="d483c-103">Validating Merge Modules</span></span>

<span data-ttu-id="d483c-104">Os autores devem executar a validação em todos os módulos de mesclagem novos ou modificados recentemente antes de tentar mesclar o módulo em um banco de dados de instalação pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="d483c-104">Authors should run validation on every new, or newly modified, merge module before attempting to merge the module into an installation database for the first time.</span></span> <span data-ttu-id="d483c-105">A validação do módulo de mesclagem funciona da mesma maneira que a [validação do pacote](package-validation.md) , mas usa um conjunto diferente de [avaliadores de consistência internos](internal-consistency-evaluators-ices.md) (ICES) específicos para módulos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="d483c-105">Merge module validation works in the same way as [package validation](package-validation.md) but uses a different set of [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) (ICEs) specific to merge modules.</span></span> <span data-ttu-id="d483c-106">Para obter mais informações sobre este módulo de mesclagem ICEs, consulte [referência de Ice do módulo de mesclagem](merge-module-ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d483c-106">For more information about these merge module ICEs, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

<span data-ttu-id="d483c-107">O módulo de mesclagem ICEs é armazenado no arquivo. Cub do módulo de mesclagem, Mergemod. cub.</span><span class="sxs-lookup"><span data-stu-id="d483c-107">Merge module ICEs are stored in the merge module .cub file, Mergemod.cub.</span></span> <span data-ttu-id="d483c-108">A instalação da ferramenta Orca ou msival2 também fornece os arquivos logo. Cub, Darice. Cub e Mergemod. cub.</span><span class="sxs-lookup"><span data-stu-id="d483c-108">The installation of the Orca tool or msival2 also provides the Logo.cub, Darice.cub, and Mergemod.cub files.</span></span>

<span data-ttu-id="d483c-109">Para obter mais informações, consulte [referência de Ice do módulo de mesclagem](merge-module-ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d483c-109">For more information, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

 

 



