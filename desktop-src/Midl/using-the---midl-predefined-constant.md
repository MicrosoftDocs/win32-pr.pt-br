---
title: Usando o __midl constante predefinida
description: Quando o compilador MIDL processa os arquivos IDL e ACF de entrada, \_ \_ MIDL é definido por padrão e é usado para compilação condicional para atingir a consistência em todo o Build.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL do compilador MIDL, usando a _midl constante predefinida
- _midl MIDL de constante predefinida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae49675b38dcc3cab2d3d41e4f48cd0637d78523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005595"
---
# <a name="using-the-__midl-predefined-constant"></a><span data-ttu-id="fa903-105">Usando a \_ \_ constante predefinida MIDL</span><span class="sxs-lookup"><span data-stu-id="fa903-105">Using the \_\_midl Predefined Constant</span></span>

<span data-ttu-id="fa903-106">Quando o compilador MIDL processa os arquivos IDL e ACF de entrada, \_ \_ MIDL é definido por padrão e é usado para compilação condicional para atingir a consistência em todo o Build.</span><span class="sxs-lookup"><span data-stu-id="fa903-106">When the MIDL compiler processes the input IDL and ACF files, \_\_midl is defined by default and is used for conditional compilation to attain consistency throughout the build.</span></span> <span data-ttu-id="fa903-107">Isso reduz o uso de instruções de definição nos arquivos de cabeçalho, como o **\_ passo de MIDL**, e os substitui por um sinalizador consistente.</span><span class="sxs-lookup"><span data-stu-id="fa903-107">This phases out the use of define statements in the header files, such as **MIDL\_PASS**, and replaces them with a consistent flag.</span></span> <span data-ttu-id="fa903-108">O valor da \_ \_ constante MIDL indica a versão do compilador *Major. Minor* de acordo com a fórmula *Major* \* 100 + *Minor*; por exemplo, MIDL ver.</span><span class="sxs-lookup"><span data-stu-id="fa903-108">The value of the \_\_midl constant indicates the compiler version *major.minor* according to the formula *major* \* 100 + *minor*; for example MIDL ver.</span></span> <span data-ttu-id="fa903-109">6.0. x tem o \_ \_ MIDL definido como 600.</span><span class="sxs-lookup"><span data-stu-id="fa903-109">6.0.x has the \_\_midl defined as 600.</span></span>

<span data-ttu-id="fa903-110">Se você escolher, poderá substituir esse padrão especificando o seguinte na linha de comando: **/u \_ \_ MIDL**.</span><span class="sxs-lookup"><span data-stu-id="fa903-110">If you choose, you can override this default by specifying the following on the command line: **/U\_\_midl**.</span></span> <span data-ttu-id="fa903-111">Para obter mais informações, consulte [**/u**](-u.md).</span><span class="sxs-lookup"><span data-stu-id="fa903-111">For more information, see [**/U**](-u.md).</span></span>

 

 




