---
description: Os mecanismos de manipulação de exceção estruturada e manipulação de encerramento são partes integrantes do sistema; Eles permitem que o sistema seja robusto. Você pode usar esses mecanismos para criar aplicativos consistentemente robustos e confiáveis.
ms.assetid: ab5bc1bd-107f-4ed2-b471-a229a76637fe
title: Sobre manipulação de exceção estruturada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161e60725f137f379b7d734485fae7cad39ae1be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163950"
---
# <a name="about-structured-exception-handling"></a><span data-ttu-id="9e437-104">Sobre manipulação de exceção estruturada</span><span class="sxs-lookup"><span data-stu-id="9e437-104">About Structured Exception Handling</span></span>

<span data-ttu-id="9e437-105">Os mecanismos de manipulação de exceção estruturada e manipulação de encerramento são partes integrantes do sistema; Eles permitem que o sistema seja robusto.</span><span class="sxs-lookup"><span data-stu-id="9e437-105">The structured exception handling and termination handling mechanisms are integral parts of the system; they enable the system to be robust.</span></span> <span data-ttu-id="9e437-106">Você pode usar esses mecanismos para criar aplicativos consistentemente robustos e confiáveis.</span><span class="sxs-lookup"><span data-stu-id="9e437-106">You can use these mechanisms to create consistently robust and reliable applications.</span></span>

<span data-ttu-id="9e437-107">A manipulação de exceção estruturada é disponibilizada principalmente por meio do suporte do compilador.</span><span class="sxs-lookup"><span data-stu-id="9e437-107">Structured exception handling is made available primarily through compiler support.</span></span> <span data-ttu-id="9e437-108">Por exemplo, o compilador de otimização do Microsoft C/C++ dá suporte à palavra-chave **\_ \_ try** que identifica um corpo de código protegido, a palavra-chave **\_ \_ Except** que identifica um manipulador de exceção e a palavra-chave **\_ \_ finally** que identifica um manipulador de encerramento.</span><span class="sxs-lookup"><span data-stu-id="9e437-108">For example, the Microsoft C/C++ Optimizing Compiler supports the **\_\_try** keyword that identifies a guarded body of code, the **\_\_except** keyword that identifies an exception handler, and the **\_\_finally** keyword that identifies a termination handler.</span></span> <span data-ttu-id="9e437-109">Embora essa visão geral use exemplos específicos para o compilador do Microsoft C/C++, outros compiladores também fornecem esse suporte.</span><span class="sxs-lookup"><span data-stu-id="9e437-109">Although this overview uses examples specific to the Microsoft C/C++ compiler, other compilers provide this support as well.</span></span>

-   [<span data-ttu-id="9e437-110">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="9e437-110">Exception Handling</span></span>](exception-handling.md)
-   [<span data-ttu-id="9e437-111">Manipulação de exceção baseada em quadros</span><span class="sxs-lookup"><span data-stu-id="9e437-111">Frame-based Exception Handling</span></span>](frame-based-exception-handling.md)
-   [<span data-ttu-id="9e437-112">Manipulação de exceção em vetor</span><span class="sxs-lookup"><span data-stu-id="9e437-112">Vectored Exception Handling</span></span>](vectored-exception-handling.md)
-   [<span data-ttu-id="9e437-113">Tratamento de encerramento</span><span class="sxs-lookup"><span data-stu-id="9e437-113">Termination Handling</span></span>](termination-handling.md)
-   [<span data-ttu-id="9e437-114">Sintaxe do manipulador</span><span class="sxs-lookup"><span data-stu-id="9e437-114">Handler Syntax</span></span>](handler-syntax.md)

 

 



