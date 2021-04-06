---
description: Você usa as funções de PDH para coletar dados de desempenho.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Usando as funções de PDH para consumir dados de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 431bf160ef6ca54b4a37363d7fe6ed48bb25d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828374"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a><span data-ttu-id="44ee3-103">Usando as funções de PDH para consumir dados de contador</span><span class="sxs-lookup"><span data-stu-id="44ee3-103">Using the PDH Functions to Consume Counter Data</span></span>

<span data-ttu-id="44ee3-104">Use as funções de PDH para coletar dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="44ee3-104">Use the PDH functions to collect performance data.</span></span> <span data-ttu-id="44ee3-105">As funções de PDH são mais fáceis de usar do que as [funções de registro](using-the-registry-functions-to-consume-counter-data.md) e podem ser usadas para acessar dados de contador de provedores v1 e v2.</span><span class="sxs-lookup"><span data-stu-id="44ee3-105">The PDH functions are easier to use than the [registry functions](using-the-registry-functions-to-consume-counter-data.md) and can be used to access counter data both V1 and V2 providers.</span></span> <span data-ttu-id="44ee3-106">A PDH tem APIs para coletar dados de desempenho atuais, salvar dados de desempenho em arquivos de log e ler dados de arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="44ee3-106">PDH has APIs for collecting current performance data, saving performance data to log files, and reading data from log files.</span></span>

> [!Note]
> <span data-ttu-id="44ee3-107">Você não poderá usar as funções de camada de abstração do auxiliar de dados de desempenho se estiver escrevendo aplicativos do Windows OneCore.</span><span class="sxs-lookup"><span data-stu-id="44ee3-107">You cannot use the Performance Data Helper abstraction-layer functions if you are writing Windows OneCore apps.</span></span> <span data-ttu-id="44ee3-108">Em vez disso, use as [funções de consumidor do PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="44ee3-108">Instead, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

<span data-ttu-id="44ee3-109">A PDH é uma API de alto nível que simplifica a coleta de dados do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="44ee3-109">PDH is a high-level API that simplifies collecting performance counter data.</span></span> <span data-ttu-id="44ee3-110">Ele ajuda na análise de consultas, no cache de metadados, na correspondência de instâncias entre amostras, na computação de valores formatados de valores brutos, na leitura de dados de arquivos de log e no salvamento de dados em arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="44ee3-110">It helps with query parsing, metadata caching, matching up instances between samples, computing formatted values from raw values, reading data from log files, and saving data to log files.</span></span> <span data-ttu-id="44ee3-111">A PDH usa automaticamente [as funções de registro](using-the-registry-functions-to-consume-counter-data.md) ao coletar dados de **provedores v1** e usa as [funções de consumidor v2](using-the-perflib-functions-to-consume-counter-data.md) ao coletar dados de **provedores v2**.</span><span class="sxs-lookup"><span data-stu-id="44ee3-111">PDH automatically uses the [registry functions](using-the-registry-functions-to-consume-counter-data.md) when collecting data from **V1 providers** and it uses the [V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md) when collecting data from **V2 providers**.</span></span>

<span data-ttu-id="44ee3-112">Para coletar dados de desempenho usando as funções de PDH, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="44ee3-112">To collect performance data using the PDH functions, perform the following steps.</span></span>

1. [<span data-ttu-id="44ee3-113">Criar uma consulta</span><span class="sxs-lookup"><span data-stu-id="44ee3-113">Create a query</span></span>](creating-a-query.md)
2. [<span data-ttu-id="44ee3-114">Adicionar contadores à consulta</span><span class="sxs-lookup"><span data-stu-id="44ee3-114">Add counters to the query</span></span>](creating-a-query.md)
3. [<span data-ttu-id="44ee3-115">Coletar os dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="44ee3-115">Collect the performance data</span></span>](collecting-performance-data.md)
4. [<span data-ttu-id="44ee3-116">Exibir os dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="44ee3-116">Display the performance data</span></span>](displaying-performance-data.md)
5. [<span data-ttu-id="44ee3-117">Fechar a consulta</span><span class="sxs-lookup"><span data-stu-id="44ee3-117">Close the query</span></span>](creating-a-query.md)

<span data-ttu-id="44ee3-118">Você pode coletar dados de desempenho de fontes em tempo real ou arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="44ee3-118">You can collect performance data from either real-time sources or log files.</span></span> <span data-ttu-id="44ee3-119">Para obter mais informações sobre como gravar dados de desempenho em arquivos de log, consulte [trabalhando com arquivos de log](working-with-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="44ee3-119">For more information on how to write performance data to log files, see [Working with Log Files](working-with-log-files.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="44ee3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="44ee3-120">See also</span></span>

- [<span data-ttu-id="44ee3-121">Coletando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="44ee3-121">Collecting Performance Data</span></span>](collecting-performance-data.md)
- [<span data-ttu-id="44ee3-122">Contadores de navegação</span><span class="sxs-lookup"><span data-stu-id="44ee3-122">Browsing Counters</span></span>](browsing-counters.md)
- [<span data-ttu-id="44ee3-123">Verificando valores de retorno da interface PDH</span><span class="sxs-lookup"><span data-stu-id="44ee3-123">Checking PDH Interface Return Values</span></span>](checking-pdh-interface-return-values.md)
- [<span data-ttu-id="44ee3-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="44ee3-124">Examples</span></span>](examples.md)
