---
description: Por padrão, o sistema tem todas as exceções de FP desativadas.
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: Exceções de ponto flutuante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a4db92a13a0215bb372db12d30bb11a749a0fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749658"
---
# <a name="floating-point-exceptions"></a><span data-ttu-id="d7169-103">Exceções de ponto flutuante</span><span class="sxs-lookup"><span data-stu-id="d7169-103">Floating-Point Exceptions</span></span>

<span data-ttu-id="d7169-104">Por padrão, o sistema tem todas as exceções de FP desativadas.</span><span class="sxs-lookup"><span data-stu-id="d7169-104">By default, the system has all FP exceptions turned off.</span></span> <span data-ttu-id="d7169-105">Portanto, as computações resultam em NAN ou infinito, em vez de uma exceção.</span><span class="sxs-lookup"><span data-stu-id="d7169-105">Therefore, computations result in NAN or INFINITY, rather than an exception.</span></span> <span data-ttu-id="d7169-106">Antes de poder interceptar exceções de ponto flutuante (FP) usando manipulação de exceção estruturada, você deve chamar a função de biblioteca de tempo de execução [ \_ controlfp \_ s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) C para ativar todas as possíveis exceções de FP.</span><span class="sxs-lookup"><span data-stu-id="d7169-106">Before you can trap floating-point (FP) exceptions using structured exception handling, you must call the [\_controlfp\_s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) C run-time library function to turn on all possible FP exceptions.</span></span> <span data-ttu-id="d7169-107">Para interceptar apenas exceções específicas, use apenas os sinalizadores que correspondem às exceções a serem interceptadas.</span><span class="sxs-lookup"><span data-stu-id="d7169-107">To trap only particular exceptions, use only the flags that correspond to the exceptions to be trapped.</span></span> <span data-ttu-id="d7169-108">Observe que qualquer manipulador de erros FP deve chamar [ \_ clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) como sua primeira instrução FP.</span><span class="sxs-lookup"><span data-stu-id="d7169-108">Note that any handler for FP errors should call [\_clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) as its first FP instruction.</span></span> <span data-ttu-id="d7169-109">Essa função limpa as exceções de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="d7169-109">This function clears floating-point exceptions.</span></span>

 

 
