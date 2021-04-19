---
description: Esta seção descreve os novos recursos que foram adicionados aos contadores de desempenho para cada versão.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: O que há de novo (contadores de desempenho)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0c1189a185351eabae438a01c6f111952f164e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753418"
---
# <a name="whats-new-with-performance-counters"></a><span data-ttu-id="3e262-103">O que há de novo nos contadores de desempenho</span><span class="sxs-lookup"><span data-stu-id="3e262-103">What's New with Performance Counters</span></span>

<span data-ttu-id="3e262-104">Esta seção descreve os novos recursos que foram adicionados aos contadores de desempenho para cada versão.</span><span class="sxs-lookup"><span data-stu-id="3e262-104">This section describes the new features that were added to Performance Counters for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="3e262-105">Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3e262-105">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="3e262-106">A ferramenta [ctrpp](ctrpp.md) foi alterada para melhorar e simplificar a geração de código.</span><span class="sxs-lookup"><span data-stu-id="3e262-106">The [CTRPP](ctrpp.md) tool was changed to improve and simplify code generation.</span></span> <span data-ttu-id="3e262-107">A ferramenta agora gera apenas um arquivo de cabeçalho e de recurso.</span><span class="sxs-lookup"><span data-stu-id="3e262-107">The tool now generates only a header and resource file.</span></span> <span data-ttu-id="3e262-108">Se você quiser o comportamento de geração de código antigo (não recomendado), poderá usar o novo `-legacy` argumento.</span><span class="sxs-lookup"><span data-stu-id="3e262-108">If you want to old code generation behavior (not recommended), you can use the new `-legacy` argument.</span></span>

- <span data-ttu-id="3e262-109">Agora você deve especificar os novos `-o` `-rc` argumentos e que especificam o nome e o local do arquivo de cabeçalho e de recurso, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3e262-109">You must now specify the new `-o` and `-rc` arguments that specify the name and location of the header and resource file, respectively.</span></span>
- <span data-ttu-id="3e262-110">Você pode usar o argumento New opcional `-prefix` para especificar uma cadeia de caracteres a ser adicionada ao início das variáveis globais e funções definidas no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="3e262-110">You can use the optional new `-prefix` argument to specify a string to add to the beginning of global variables and functions defined in the generated header file.</span></span>
- <span data-ttu-id="3e262-111">Se você precisar atualizar seu manifesto de contadores, o uso da nova geração de código elimina a necessidade de Mesclar sua implementação de retorno de chamada anterior com o novo código gerado, já que os retornos de chamada não são mais incluídos no código gerado.</span><span class="sxs-lookup"><span data-stu-id="3e262-111">If you have to update your counters manifest, using the new code generation eliminates the need to merge your previous callback implementation with the new generated code since the callbacks are no longer included in the generated code.</span></span>

<span data-ttu-id="3e262-112">Um novo `symbol` atributo está disponível para os seguintes elementos de manifesto:</span><span class="sxs-lookup"><span data-stu-id="3e262-112">A new `symbol` attribute is available for the following manifest elements:</span></span>

- [<span data-ttu-id="3e262-113">operador</span><span class="sxs-lookup"><span data-stu-id="3e262-113">provider</span></span>](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [<span data-ttu-id="3e262-114">counterSet</span><span class="sxs-lookup"><span data-stu-id="3e262-114">counterSet</span></span>](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [<span data-ttu-id="3e262-115">neutraliza</span><span class="sxs-lookup"><span data-stu-id="3e262-115">counter</span></span>](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

<span data-ttu-id="3e262-116">O `symbol` atributo é necessário para o [provedor](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) e [CounterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)e é opcional para o [contador](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element).</span><span class="sxs-lookup"><span data-stu-id="3e262-116">The `symbol` attribute is required for [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) and [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element), and is optional for [counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element).</span></span> <span data-ttu-id="3e262-117">O atributo permite que você forneça um nome simbólico que pode ser usado para fazer referência a cada elemento ao chamar as funções do provedor (por exemplo, você pode usar o nome simbólico do conjunto de contadores ao chamar [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).</span><span class="sxs-lookup"><span data-stu-id="3e262-117">The attribute lets you provide a symbolic name that you can use to reference each element when calling the provider functions (for example, you can use the counter set symbolic name when calling [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="3e262-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e262-118">Windows Vista</span></span>

<span data-ttu-id="3e262-119">A arquitetura de contadores de desempenho para fornecer dados do contador foi completamente alterada para esta versão.</span><span class="sxs-lookup"><span data-stu-id="3e262-119">The Performance Counters architecture for providing counter data was completely changed for this release.</span></span>

<span data-ttu-id="3e262-120">Anteriormente, você usou um arquivo INI para definir os dados do contador e implementou uma DLL de desempenho que foi executada no processo do consumidor para fornecer os dados quando um consumidor o solicitou.</span><span class="sxs-lookup"><span data-stu-id="3e262-120">Previously, you used an INI file to define your counter data and you implemented a performance DLL which ran in the consumer's process to provide the data when a consumer requested it.</span></span> <span data-ttu-id="3e262-121">Essa arquitetura é preterida e não é recomendada para um novo código devido a problemas significativos de desempenho e confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="3e262-121">This architecture is deprecated and is not recommended for new code due to significant performance and reliability issues.</span></span>

<span data-ttu-id="3e262-122">A nova arquitetura usa um manifesto para definir os dados do contador e executa o código no processo do provedor para fornecer os dados quando um consumidor o solicita.</span><span class="sxs-lookup"><span data-stu-id="3e262-122">The new architecture uses a manifest to define the counter data and runs code in the provider's process to provide the data when a consumer requests it.</span></span> <span data-ttu-id="3e262-123">Para obter detalhes adicionais, consulte [fornecendo dados do contador usando a versão 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="3e262-123">For additional details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="3e262-124">As seguintes funções foram adicionadas para esta versão:</span><span class="sxs-lookup"><span data-stu-id="3e262-124">The following functions were added for this release:</span></span>

- [<span data-ttu-id="3e262-125">ControlCallback</span><span class="sxs-lookup"><span data-stu-id="3e262-125">ControlCallback</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="3e262-126">PerfCreateInstance</span><span class="sxs-lookup"><span data-stu-id="3e262-126">PerfCreateInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="3e262-127">PerfDeleteInstance</span><span class="sxs-lookup"><span data-stu-id="3e262-127">PerfDeleteInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="3e262-128">PerfQueryInstance</span><span class="sxs-lookup"><span data-stu-id="3e262-128">PerfQueryInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="3e262-129">PerfSetCounterSetInfo</span><span class="sxs-lookup"><span data-stu-id="3e262-129">PerfSetCounterSetInfo</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="3e262-130">PerfSetULongCounterValue</span><span class="sxs-lookup"><span data-stu-id="3e262-130">PerfSetULongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="3e262-131">PerfSetULongLongCounterValue</span><span class="sxs-lookup"><span data-stu-id="3e262-131">PerfSetULongLongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="3e262-132">PerfSetCounterRefValue</span><span class="sxs-lookup"><span data-stu-id="3e262-132">PerfSetCounterRefValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="3e262-133">PerfStartProvider</span><span class="sxs-lookup"><span data-stu-id="3e262-133">PerfStartProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="3e262-134">PerfStopProvider</span><span class="sxs-lookup"><span data-stu-id="3e262-134">PerfStopProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

<span data-ttu-id="3e262-135">As seguintes estruturas foram adicionadas para esta versão:</span><span class="sxs-lookup"><span data-stu-id="3e262-135">The following structures were added for this release:</span></span>

- [<span data-ttu-id="3e262-136">\_identidade do contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="3e262-136">PERF\_COUNTER\_IDENTITY</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="3e262-137">\_informações do contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="3e262-137">PERF\_COUNTER\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="3e262-138">informações do contador de desempenho \_ \_</span><span class="sxs-lookup"><span data-stu-id="3e262-138">PERF\_COUNTERSET\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="3e262-139">instância do contador de desempenho \_ \_</span><span class="sxs-lookup"><span data-stu-id="3e262-139">PERF\_COUNTERSET\_INSTANCE</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

<span data-ttu-id="3e262-140">Para obter uma lista dos elementos XML que você usa em seu manifesto para definir seus contadores, consulte [esquema de contadores de desempenho](performance-counters-schema.md).</span><span class="sxs-lookup"><span data-stu-id="3e262-140">For a list of the XML elements that you use in your manifest to define your counters, see [Performance Counters Schema](performance-counters-schema.md).</span></span>

<span data-ttu-id="3e262-141">Para obter informações sobre a ferramenta de pré-processador CTRPP que analisa seu manifesto e gera o código que você usa como ponto de partida para seu provedor, consulte [ctrpp](ctrpp.md).</span><span class="sxs-lookup"><span data-stu-id="3e262-141">For information on the CTRPP pre-processor tool that parses your manifest and generates the code that you use as the starting point for your provider, see [CTRPP](ctrpp.md).</span></span>
