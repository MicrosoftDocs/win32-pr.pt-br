---
description: As funções a seguir são os pontos de entrada para DLLs de especialistas e chamadas do sistema operacional e Monitor de Rede.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Funções de exportação de DLL de especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923611521b98619b357eb2de93ee2269caf9c838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920711"
---
# <a name="expert-dll-export-functions"></a><span data-ttu-id="7a7b9-103">Funções de exportação de DLL de especialista</span><span class="sxs-lookup"><span data-stu-id="7a7b9-103">Expert DLL Export Functions</span></span>

<span data-ttu-id="7a7b9-104">As funções a seguir são os pontos de entrada para DLLs de especialistas e chamadas do sistema operacional e Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-104">The following functions are the entry points for expert DLLs and for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="7a7b9-105">Função</span><span class="sxs-lookup"><span data-stu-id="7a7b9-105">Function</span></span>                                   | <span data-ttu-id="7a7b9-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a7b9-106">Description</span></span>                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a7b9-107">**Especialista em DllMain**</span><span class="sxs-lookup"><span data-stu-id="7a7b9-107">**DllMain Expert**</span></span>](dllmain-expert.md)   | <span data-ttu-id="7a7b9-108">Indica que a DLL de especialista foi carregada ou descarregada.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-108">Indicates that the expert DLL has been loaded or unloaded.</span></span> <span data-ttu-id="7a7b9-109">Quando um processo carrega ou descarrega a DLL, o sistema operacional chama a função [**DllMain**](/windows/desktop/Dlls/dllmain) .</span><span class="sxs-lookup"><span data-stu-id="7a7b9-109">When a process loads or unloads the DLL, the operating system calls the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> |
| [<span data-ttu-id="7a7b9-110">**Registrar especialista**</span><span class="sxs-lookup"><span data-stu-id="7a7b9-110">**Register Expert**</span></span>](register-expert.md) | <span data-ttu-id="7a7b9-111">Determina as informações básicas sobre o especialista dentro da DLL.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-111">Determines basic information about the expert within the DLL.</span></span> <span data-ttu-id="7a7b9-112">Monitor de Rede chama a função de **registro** .</span><span class="sxs-lookup"><span data-stu-id="7a7b9-112">Network Monitor calls the **Register** function.</span></span>                                                           |
| [<span data-ttu-id="7a7b9-113">**Configurar**</span><span class="sxs-lookup"><span data-stu-id="7a7b9-113">**Configure**</span></span>](configure.md)             | <span data-ttu-id="7a7b9-114">Configura o especialista dentro da DLL.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-114">Configures the expert within the DLL.</span></span> <span data-ttu-id="7a7b9-115">Monitor de Rede chama a função [**Configurar**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="7a7b9-115">Network Monitor calls the [**Configure**](configure.md) function.</span></span>                                                                 |
| [<span data-ttu-id="7a7b9-116">**Executar**</span><span class="sxs-lookup"><span data-stu-id="7a7b9-116">**Run**</span></span>](run.md)                         | <span data-ttu-id="7a7b9-117">Inicia o especialista na DLL.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-117">Starts the expert within the DLL.</span></span> <span data-ttu-id="7a7b9-118">Monitor de Rede chama a função [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="7a7b9-118">Network Monitor calls the [**Run**](run.md) function.</span></span>                                                                                 |



 

<span data-ttu-id="7a7b9-119">O Monitor de Rede também fornece estruturas, enumerações e funções auxiliares que o especialista pode chamar.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-119">Network Monitor also provides structures, enumerations, and helper functions that the expert can call.</span></span>



| <span data-ttu-id="7a7b9-120">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="7a7b9-120">For information about</span></span>                                      | <span data-ttu-id="7a7b9-121">Consulte</span><span class="sxs-lookup"><span data-stu-id="7a7b9-121">See</span></span>                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7a7b9-122">Funções auxiliares que podem ser chamadas por especialistas e analisadores</span><span class="sxs-lookup"><span data-stu-id="7a7b9-122">Helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="7a7b9-123">Funções comuns de expert e parser</span><span class="sxs-lookup"><span data-stu-id="7a7b9-123">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="7a7b9-124">Funções auxiliares que são chamadas apenas por especialistas</span><span class="sxs-lookup"><span data-stu-id="7a7b9-124">Helper functions that are called only by experts</span></span>           | [<span data-ttu-id="7a7b9-125">Funções de especialista</span><span class="sxs-lookup"><span data-stu-id="7a7b9-125">Expert Functions</span></span>](expert-functions.md)                                     |
| <span data-ttu-id="7a7b9-126">Estruturas que são usadas por funções de especialista</span><span class="sxs-lookup"><span data-stu-id="7a7b9-126">Structures that are used by expert functions</span></span>               | [<span data-ttu-id="7a7b9-127">Estruturas de especialistas</span><span class="sxs-lookup"><span data-stu-id="7a7b9-127">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="7a7b9-128">Enumerações usadas por estruturas e funções de especialistas</span><span class="sxs-lookup"><span data-stu-id="7a7b9-128">Enumerations used by expert structures and functions</span></span>       | [<span data-ttu-id="7a7b9-129">Enumerações de especialistas</span><span class="sxs-lookup"><span data-stu-id="7a7b9-129">Expert Enumerations</span></span>](expert-enumerations.md)                               |



 

 

 
