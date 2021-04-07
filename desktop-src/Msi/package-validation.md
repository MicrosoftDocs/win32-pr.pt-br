---
description: É altamente recomendável que você execute a validação em cada pacote de instalação novo ou recém modificado antes de tentar instalar o pacote pela primeira vez.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Validação do pacote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827870"
---
# <a name="package-validation"></a><span data-ttu-id="45825-103">Validação do pacote</span><span class="sxs-lookup"><span data-stu-id="45825-103">Package Validation</span></span>

<span data-ttu-id="45825-104">É altamente recomendável que você execute a validação em cada pacote de instalação novo ou recém modificado antes de tentar instalar o pacote pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="45825-104">It is strongly recommended that you run validation on every new or newly modified installation package before attempting to install the package for the first time.</span></span>

<span data-ttu-id="45825-105">A validação do pacote inclui os três processos a seguir:</span><span class="sxs-lookup"><span data-stu-id="45825-105">Package validation includes the following three processes:</span></span>

-   [<span data-ttu-id="45825-106">Validação interna</span><span class="sxs-lookup"><span data-stu-id="45825-106">Internal Validation</span></span>](internal-validation.md)
-   [<span data-ttu-id="45825-107">Validação do pool de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="45825-107">String-Pool Validation</span></span>](string-pool-validation.md)
-   [<span data-ttu-id="45825-108">Avaliadores de consistência internos-ICEs</span><span class="sxs-lookup"><span data-stu-id="45825-108">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

<span data-ttu-id="45825-109">Os módulos de mesclagem devem ser validados usando o método descrito em [Validando módulos de mesclagem](validating-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="45825-109">Merge modules should be validated by using the method described in [Validating Merge Modules](validating-merge-modules.md).</span></span>

<span data-ttu-id="45825-110">Evalcom2.dll fornece um objeto COM que implementa operações de validação para pacotes de instalação e módulos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="45825-110">Evalcom2.dll provides a COM object that implements validation operations for installation packages and merge modules.</span></span> <span data-ttu-id="45825-111">O objeto principal implementa interfaces para programas C/C++.</span><span class="sxs-lookup"><span data-stu-id="45825-111">The main object implements interfaces for C/C++ programs.</span></span> <span data-ttu-id="45825-112">Para obter mais informações, consulte [automação de validação](validation-automation.md).</span><span class="sxs-lookup"><span data-stu-id="45825-112">For more information, see [Validation Automation](validation-automation.md).</span></span>

 

 



