---
title: Vários controles em uma DLL
description: Vários controles em uma DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e11c91faa26420f37df330ad7f1d9eff4587f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004950"
---
# <a name="multiple-controls-in-one-dll"></a><span data-ttu-id="e82f2-103">Vários controles em uma DLL</span><span class="sxs-lookup"><span data-stu-id="e82f2-103">Multiple Controls in One DLL</span></span>

<span data-ttu-id="e82f2-104">Uma única DLL. ocx pode contêinerar qualquer número de controles ActiveX, simplificando assim a distribuição e o uso de um conjunto de controles relacionados.</span><span class="sxs-lookup"><span data-stu-id="e82f2-104">A single .ocx DLL can container any number of ActiveX controls, thus simplifying the distribution and use of a set of related controls.</span></span>

<span data-ttu-id="e82f2-105">Se você enviar vários controles em uma única DLL, certifique-se de incluir o nome do fornecedor em cada nome de controle no pacote.</span><span class="sxs-lookup"><span data-stu-id="e82f2-105">If you ship multiple controls in a single DLL, be sure to include the vendor name in each control name in the package.</span></span> <span data-ttu-id="e82f2-106">A inclusão dos nomes dos fornecedores em cada nome de controle permitirá que os usuários identifiquem facilmente os controles em um pacote.</span><span class="sxs-lookup"><span data-stu-id="e82f2-106">Including the vendors' names in each control name will enable users to easily identify controls within a package.</span></span> <span data-ttu-id="e82f2-107">Por exemplo, se você enviar uma DLL que implemente três controles, Con1, Con2 e Con3, os nomes de controle deverão ser:</span><span class="sxs-lookup"><span data-stu-id="e82f2-107">For example, if you ship a DLL that implements three controls, Con1, Con2, and Con3, then the control names should be:</span></span>

-   <span data-ttu-id="e82f2-108">*O nome da sua empresa* Controle Con1</span><span class="sxs-lookup"><span data-stu-id="e82f2-108">*Your company name* Con1 Control</span></span>

-   <span data-ttu-id="e82f2-109">*O nome da sua empresa* Controle Con2</span><span class="sxs-lookup"><span data-stu-id="e82f2-109">*Your company name* Con2 Control</span></span>

-   <span data-ttu-id="e82f2-110">*O nome da sua empresa* Controle Con3</span><span class="sxs-lookup"><span data-stu-id="e82f2-110">*Your company name* Con3 Control</span></span>

 

 




