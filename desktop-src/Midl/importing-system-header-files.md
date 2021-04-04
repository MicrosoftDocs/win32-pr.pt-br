---
title: Importar arquivos de cabeçalho do sistema
description: Embora geralmente seja possível usar a diretiva \ include para incluir arquivos de cabeçalho em seu arquivo IDL, isso não é recomendado.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- importando MIDL, arquivos de cabeçalho do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663852"
---
# <a name="importing-system-header-files"></a><span data-ttu-id="32fb6-104">Importar arquivos de cabeçalho do sistema</span><span class="sxs-lookup"><span data-stu-id="32fb6-104">Importing System Header Files</span></span>

<span data-ttu-id="32fb6-105">Embora muitas vezes seja possível usar a diretiva **\# include** para incluir arquivos de cabeçalho em seu arquivo IDL, isso não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="32fb6-105">While it is often possible to use the **\#include** directive to include header files in your IDL file, it is not recommended.</span></span> <span data-ttu-id="32fb6-106">O compilador MIDL irá gerar stubs para todas as funções definidas no arquivo IDL que está sendo compilado.</span><span class="sxs-lookup"><span data-stu-id="32fb6-106">The MIDL compiler will generate stubs for all functions defined in the IDL file being compiled.</span></span> <span data-ttu-id="32fb6-107">Normalmente, um arquivo de cabeçalho contém um número de protótipos que você não precisa nem deseja incluir nos arquivos de stub, e um **\# inclui** efetivamente coloca todas essas definições em seu arquivo IDL principal.</span><span class="sxs-lookup"><span data-stu-id="32fb6-107">Usually a header file contains a number of prototypes that you neither need nor want to include in your stub files, and a **\#include** effectively puts all those definitions into your main IDL file.</span></span> <span data-ttu-id="32fb6-108">Além disso, se houver tipos não-Remotable definidos no arquivo de cabeçalho, o arquivo IDL não poderá ser compilado.</span><span class="sxs-lookup"><span data-stu-id="32fb6-108">Furthermore, if there are nonremotable types defined in the header file, the IDL file may not compile.</span></span>

<span data-ttu-id="32fb6-109">Há duas maneiras de incluir definições de tipo de arquivos de cabeçalho em um arquivo IDL:</span><span class="sxs-lookup"><span data-stu-id="32fb6-109">There are two ways to include type definitions from header files in an IDL file:</span></span>

-   <span data-ttu-id="32fb6-110">Use a diretiva de [**importação**](import.md) para incluir tipos de dados definidos em um arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="32fb6-110">Use the [**import**](import.md) directive to include data types defined in a header file.</span></span> <span data-ttu-id="32fb6-111">Ao contrário da diretiva de **\# inclusão** de linguagem C, a diretiva de **importação** só seleciona o tipo e as definições constantes e ignora os protótipos de procedimento.</span><span class="sxs-lookup"><span data-stu-id="32fb6-111">Unlike the C-language **\#include** directive, the **import** directive only picks up type and constant definitions and ignores procedure prototypes.</span></span> <span data-ttu-id="32fb6-112">Essa abordagem funcionará contanto que seu arquivo IDL principal não referencie nenhum tipo de não-Remotable definido no arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="32fb6-112">This approach will work as long as your main IDL file does not reference any nonremotable types defined in the header file.</span></span>
-   <span data-ttu-id="32fb6-113">Crie um arquivo IDL auxiliar com uma interface fictícia que inclua os arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="32fb6-113">Create a helper IDL file with a dummy interface that includes the header files.</span></span> <span data-ttu-id="32fb6-114">Em seguida, use a diretiva de [**importação**](import.md) para incluir o arquivo auxiliar.</span><span class="sxs-lookup"><span data-stu-id="32fb6-114">Then, use the [**import**](import.md) directive to include the helper file.</span></span> <span data-ttu-id="32fb6-115">Dessa forma, somente os s de [**typedef**](typedef.md)serão exibidos nos stubs compilados.</span><span class="sxs-lookup"><span data-stu-id="32fb6-115">In this way, only the [**typedef**](typedef.md)s will appear in the compiled stubs.</span></span> <span data-ttu-id="32fb6-116">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="32fb6-116">For example:</span></span>

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
