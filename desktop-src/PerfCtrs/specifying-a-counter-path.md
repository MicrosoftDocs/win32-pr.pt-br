---
description: O sistema usa contadores para coletar dados de desempenho.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Especificar um Caminho do Contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3a92f94b4bf3d2252903d92785f43bb0cac110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750772"
---
# <a name="specifying-a-counter-path"></a><span data-ttu-id="f56f9-103">Especificar um Caminho do Contador</span><span class="sxs-lookup"><span data-stu-id="f56f9-103">Specifying a Counter Path</span></span>

<span data-ttu-id="f56f9-104">O sistema usa contadores para coletar dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="f56f9-104">The system uses counters to collect performance data.</span></span> <span data-ttu-id="f56f9-105">Cada contador é identificado exclusivamente por meio de seu nome e seu caminho ou local.</span><span class="sxs-lookup"><span data-stu-id="f56f9-105">Each counter is uniquely identified through its name and its path, or location.</span></span> <span data-ttu-id="f56f9-106">A sintaxe de um caminho de contador é:</span><span class="sxs-lookup"><span data-stu-id="f56f9-106">The syntax of a counter path is:</span></span>

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

<span data-ttu-id="f56f9-107">O elemento Computer especifica o nome ou o endereço IP do computador do qual você deseja consultar dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="f56f9-107">The Computer element specifies the name or IP address of the computer from which you want to query performance data.</span></span> <span data-ttu-id="f56f9-108">O nome do computador será opcional se o contador estiver localizado no computador local.</span><span class="sxs-lookup"><span data-stu-id="f56f9-108">The computer name is optional if the counter is located on the local computer.</span></span>

<span data-ttu-id="f56f9-109">O elemento Perfobject especifica o objeto de desempenho a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="f56f9-109">The PerfObject element specifies the performance object to query.</span></span> <span data-ttu-id="f56f9-110">Um objeto de desempenho pode ser um componente físico, como processadores, discos e memória, ou um objeto do sistema, como processos e threads.</span><span class="sxs-lookup"><span data-stu-id="f56f9-110">A performance object can be a physical component, such as processors, disks, and memory, or a system object, such as processes and threads.</span></span> <span data-ttu-id="f56f9-111">Cada objeto do sistema está relacionado a um elemento funcional dentro do computador e tem um conjunto de contadores padrão atribuído a ele.</span><span class="sxs-lookup"><span data-stu-id="f56f9-111">Each system object is related to a functional element within the computer and has a set of standard counters assigned to it.</span></span> <span data-ttu-id="f56f9-112">Cada computador pode ter um conjunto diferente de objetos de desempenho e contadores instalados nele, pois os aplicativos podem instalar seus próprios objetos e contadores de desempenho.</span><span class="sxs-lookup"><span data-stu-id="f56f9-112">Each computer may have a different set of performance objects and counters installed on it because applications can install their own performance objects and counters.</span></span> <span data-ttu-id="f56f9-113">Para obter uma lista dos objetos de desempenho e dos contadores instalados no seu computador, consulte a caixa de diálogo **Adicionar contadores** na ferramenta de desempenho em seu computador.</span><span class="sxs-lookup"><span data-stu-id="f56f9-113">For a list of the performance objects and counters installed on your computer, see the **Add Counters** dialog box in the Performance tool on your computer.</span></span> <span data-ttu-id="f56f9-114">Esses objetos também são listados na caixa de diálogo Procurar PDH (consulte os [contadores de navegação](browsing-counters.md)).</span><span class="sxs-lookup"><span data-stu-id="f56f9-114">These objects are also listed in the PDH browse dialog box (see [Browsing Counters](browsing-counters.md)).</span></span> <span data-ttu-id="f56f9-115">Para obter uma lista de objetos e contadores de desempenho do sistema, consulte [contadores por objeto](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="f56f9-115">For a list of system performance objects and counters, see [Counters by Object](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span></span>

<span data-ttu-id="f56f9-116">O ParentInstance, ObjectInstance e InstanceIndex serão incluídos no caminho se várias instâncias do objeto puderem existir.</span><span class="sxs-lookup"><span data-stu-id="f56f9-116">The ParentInstance, ObjectInstance, and InstanceIndex are included in the path if multiple instances of the object can exist.</span></span> <span data-ttu-id="f56f9-117">Por exemplo, processos e threads são vários objetos de instância porque mais de um processo ou thread podem ser executados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="f56f9-117">For example, processes and threads are multiple instance objects because more than one process or thread can run at the same time.</span></span> <span data-ttu-id="f56f9-118">Se um objeto puder ter mais de uma instância, o caminho do contador deverá especificar uma instância de objeto.</span><span class="sxs-lookup"><span data-stu-id="f56f9-118">If an object can have more than one instance, the counter path must specify an object instance.</span></span>

<span data-ttu-id="f56f9-119">O formato dos elementos relacionados à instância depende do tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="f56f9-119">The format of the instance related elements depends on the object type.</span></span> <span data-ttu-id="f56f9-120">Se o objeto tiver instâncias simples, o formato será apenas o nome da instância entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="f56f9-120">If the object has simple instances, then the format is only the instance name enclosed in parentheses.</span></span> <span data-ttu-id="f56f9-121">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f56f9-121">For example:</span></span>

``` syntax
(Explorer)
```

<span data-ttu-id="f56f9-122">Se a instância desse objeto também exigir um nome de instância pai, o nome da instância pai deverá vir antes da instância do objeto e ser separado por um caractere de barra invertida.</span><span class="sxs-lookup"><span data-stu-id="f56f9-122">If the instance of this object also requires a parent instance name, the parent instance name must come before the object instance and be separated by a forward slash character.</span></span> <span data-ttu-id="f56f9-123">Por exemplo, os threads pertencem a processos.</span><span class="sxs-lookup"><span data-stu-id="f56f9-123">For example, threads belong to processes.</span></span> <span data-ttu-id="f56f9-124">Se você consultar um objeto de thread, também deverá especificar o processo ao qual ele pertence, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="f56f9-124">If you query a thread object, you must also specify the process to which it belongs as shown in the following example:</span></span>

``` syntax
(Explorer/0)
```

<span data-ttu-id="f56f9-125">Se o objeto tiver várias instâncias que têm a mesma cadeia de caracteres de nome, elas poderão ser indexadas sequencialmente especificando o índice de instância prefixado por um sinal de libra.</span><span class="sxs-lookup"><span data-stu-id="f56f9-125">If the object has multiple instances that have the same name string, they can be indexed sequentially by specifying the instance index prefixed by a pound sign.</span></span> <span data-ttu-id="f56f9-126">Os índices de instância são baseados em 0.</span><span class="sxs-lookup"><span data-stu-id="f56f9-126">Instance indexes are 0-based.</span></span> <span data-ttu-id="f56f9-127">Se você quiser consultar a primeira instância, não inclua \# 0 – basta especificar o nome da instância.</span><span class="sxs-lookup"><span data-stu-id="f56f9-127">If you want to query the first instance, do not include \#0—just specify the instance name.</span></span> <span data-ttu-id="f56f9-128">Para especificar a segunda instância, use \# 1; para especificar a terceira instância, use \# 2; e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="f56f9-128">To specify the second instance, use \#1; to specify the third instance, use \#2; and so on.</span></span> <span data-ttu-id="f56f9-129">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f56f9-129">For example:</span></span>

``` syntax
(Explorer/0#1)
```

<span data-ttu-id="f56f9-130">O elemento Counter Especifica o contador de desempenho que você deseja consultar para o objeto de desempenho fornecido.</span><span class="sxs-lookup"><span data-stu-id="f56f9-130">The Counter element specifies the performance counter that you want to query for the given the performance object.</span></span>

<span data-ttu-id="f56f9-131">A PDH usa os seguintes caracteres especiais em um caminho de contador.</span><span class="sxs-lookup"><span data-stu-id="f56f9-131">PDH uses the following special characters in a counter path.</span></span> <span data-ttu-id="f56f9-132">Os provedores não devem usar esses caracteres em seus nomes.</span><span class="sxs-lookup"><span data-stu-id="f56f9-132">Providers should not use these characters in their names.</span></span> <span data-ttu-id="f56f9-133">Se um provedor usar esses caracteres especiais, a PDH não poderá analisar o caminho completo do contador para obter os nomes do contador e das instâncias.</span><span class="sxs-lookup"><span data-stu-id="f56f9-133">If a provider uses these special characters, PDH cannot parse the full counter path to obtain the counter and instances names.</span></span>



| <span data-ttu-id="f56f9-134">Caractere</span><span class="sxs-lookup"><span data-stu-id="f56f9-134">Character</span></span> | <span data-ttu-id="f56f9-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="f56f9-135">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| \\        | <span data-ttu-id="f56f9-136">Separador genérico para computador, objeto e contador.</span><span class="sxs-lookup"><span data-stu-id="f56f9-136">Generic separator for computer, object, and counter.</span></span>       |
| <span data-ttu-id="f56f9-137">(</span><span class="sxs-lookup"><span data-stu-id="f56f9-137">(</span></span>         | <span data-ttu-id="f56f9-138">Início do nome da instância.</span><span class="sxs-lookup"><span data-stu-id="f56f9-138">Beginning of instance name.</span></span>                                |
| <span data-ttu-id="f56f9-139">)</span><span class="sxs-lookup"><span data-stu-id="f56f9-139">)</span></span>         | <span data-ttu-id="f56f9-140">Final do nome da instância.</span><span class="sxs-lookup"><span data-stu-id="f56f9-140">Ending of instance name.</span></span>                                   |
| /         | <span data-ttu-id="f56f9-141">Separa instância e instância pai.</span><span class="sxs-lookup"><span data-stu-id="f56f9-141">Separates instance and parent instance.</span></span>                    |
| <span data-ttu-id="f56f9-142">\#n</span><span class="sxs-lookup"><span data-stu-id="f56f9-142">\#n</span></span>       | <span data-ttu-id="f56f9-143">Identifica uma ocorrência específica de uma instância do mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="f56f9-143">Identifies a specific occurrence of a same-named instance.</span></span> |
| \*        | <span data-ttu-id="f56f9-144">Caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="f56f9-144">Wildcard character.</span></span>                                        |



 

<span data-ttu-id="f56f9-145">Os exemplos a seguir mostram os possíveis formatos para caminhos de contador:</span><span class="sxs-lookup"><span data-stu-id="f56f9-145">The following examples show the possible formats for counter paths:</span></span>

-   <span data-ttu-id="f56f9-146">\\\\\\contador de objeto de computador (índice pai/instância \# ) \\</span><span class="sxs-lookup"><span data-stu-id="f56f9-146">\\\\computer\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="f56f9-147">\\\\\\contador de objeto de computador (pai/instância) \\</span><span class="sxs-lookup"><span data-stu-id="f56f9-147">\\\\computer\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="f56f9-148">\\\\\\contador de objeto de computador (índice de instância \# ) \\</span><span class="sxs-lookup"><span data-stu-id="f56f9-148">\\\\computer\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="f56f9-149">\\\\\\contador de objeto (instância) de computador \\</span><span class="sxs-lookup"><span data-stu-id="f56f9-149">\\\\computer\\object(instance)\\counter</span></span>
-   <span data-ttu-id="f56f9-150">\\\\\\contador de objetos de computador \\</span><span class="sxs-lookup"><span data-stu-id="f56f9-150">\\\\computer\\object\\counter</span></span>
-   <span data-ttu-id="f56f9-151">\\contador de objeto (índice pai/instância \# ) \\</span><span class="sxs-lookup"><span data-stu-id="f56f9-151">\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="f56f9-152">\\contador de objeto (pai/instância) \\</span><span class="sxs-lookup"><span data-stu-id="f56f9-152">\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="f56f9-153">\\contador de objeto (índice de instância \# ) \\</span><span class="sxs-lookup"><span data-stu-id="f56f9-153">\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="f56f9-154">\\contador de objeto (instância) \\</span><span class="sxs-lookup"><span data-stu-id="f56f9-154">\\object(instance)\\counter</span></span>
-   <span data-ttu-id="f56f9-155">\\contador de objeto \\</span><span class="sxs-lookup"><span data-stu-id="f56f9-155">\\object\\counter</span></span>

## <a name="using-wildcard-characters"></a><span data-ttu-id="f56f9-156">Usando caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="f56f9-156">Using wildcard characters</span></span>

<span data-ttu-id="f56f9-157">Os caminhos de contador podem conter um caractere curinga somente para o nome da instância, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f56f9-157">Counter paths may contain a wildcard character only for the instance name as shown in the following example.</span></span>

``` syntax
\Process(*)\% Processor Time
```

<span data-ttu-id="f56f9-158">Para expandir o curinga em uma lista de caminhos de contadores que contêm instâncias encontradas no computador ou no arquivo de log, chame [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span><span class="sxs-lookup"><span data-stu-id="f56f9-158">To expand the wildcard into a list of counter paths that contain instances found on the computer or in the log file, call [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span></span>

 

 
