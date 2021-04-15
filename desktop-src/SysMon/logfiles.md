---
title: Objeto LogFiles (Isysmon.h)
description: Use essa classe para gerenciar uma coleção de um ou mais arquivos de log que contêm dados do contador de desempenho. Para recuperar esse objeto, chame SystemMonitor. LogFiles.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- Objeto LogFiles SysMon
- Objeto LogFiles SysMon, descrito
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab30de5c371c012e1320950e4a491021bb0b15c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454591"
---
# <a name="logfiles-object"></a><span data-ttu-id="91a8c-105">Objeto LogFiles</span><span class="sxs-lookup"><span data-stu-id="91a8c-105">LogFiles object</span></span>

<span data-ttu-id="91a8c-106">Use essa classe para gerenciar uma coleção de um ou mais arquivos de log que contêm dados do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="91a8c-106">Use this class to manage a collection of one or more log files that contain performance counter data.</span></span>

<span data-ttu-id="91a8c-107">Para recuperar esse objeto, chame [**SystemMonitor. LogFiles**](systemmonitor-logfiles.md).</span><span class="sxs-lookup"><span data-stu-id="91a8c-107">To retrieve this object, call [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md).</span></span>

## <a name="members"></a><span data-ttu-id="91a8c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="91a8c-108">Members</span></span>

<span data-ttu-id="91a8c-109">O objeto **LogFiles** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="91a8c-109">The **LogFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="91a8c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="91a8c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="91a8c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="91a8c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="91a8c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="91a8c-112">Methods</span></span>

<span data-ttu-id="91a8c-113">O objeto **LogFiles** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="91a8c-113">The **LogFiles** object has these methods.</span></span>



| <span data-ttu-id="91a8c-114">Método</span><span class="sxs-lookup"><span data-stu-id="91a8c-114">Method</span></span>                                          | <span data-ttu-id="91a8c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="91a8c-115">Description</span></span>                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="91a8c-116">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="91a8c-116">**Add**</span></span>](systemmonitor-logfiles-add.md)       | <span data-ttu-id="91a8c-117">Adiciona uma instância de [**LogFileItem**](logfileitem.md) à coleção.</span><span class="sxs-lookup"><span data-stu-id="91a8c-117">Adds a [**LogFileItem**](logfileitem.md) instance to the collection.</span></span><br/>      |
| [<span data-ttu-id="91a8c-118">**Remover**</span><span class="sxs-lookup"><span data-stu-id="91a8c-118">**Remove**</span></span>](systemmonitor-logfiles-remove.md) | <span data-ttu-id="91a8c-119">Remove uma instância de [**LogFileItem**](logfileitem.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="91a8c-119">Removes a [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="91a8c-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="91a8c-120">Properties</span></span>

<span data-ttu-id="91a8c-121">O objeto **LogFiles** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="91a8c-121">The **LogFiles** object has these properties.</span></span>



| <span data-ttu-id="91a8c-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="91a8c-122">Property</span></span>                                                 | <span data-ttu-id="91a8c-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="91a8c-123">Description</span></span>                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91a8c-124">**Contar**</span><span class="sxs-lookup"><span data-stu-id="91a8c-124">**Count**</span></span>](systemmonitor-logfiles-count.md)<br/> | <span data-ttu-id="91a8c-125">Recupera o número de instâncias [**LogFileItem**](logfileitem.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="91a8c-125">Retrieves the number of [**LogFileItem**](logfileitem.md) instances in the collection.</span></span><br/>  |
| [<span data-ttu-id="91a8c-126">**Item**</span><span class="sxs-lookup"><span data-stu-id="91a8c-126">**Item**</span></span>](systemmonitor-logfiles-item.md)<br/>   | <span data-ttu-id="91a8c-127">Recupera a instância [**LogFileItem**](logfileitem.md) especificada da coleção.</span><span class="sxs-lookup"><span data-stu-id="91a8c-127">Retrieves the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91a8c-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="91a8c-128">Remarks</span></span>

<span data-ttu-id="91a8c-129">Para ter os contadores de desempenho de exibição SYSMON de um arquivo de log, defina [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) como [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="91a8c-129">To have SYSMON display performance counters from a log file, set [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="91a8c-130">Depois de adicionar os arquivos de log à coleção, use a coleção de [**contadores**](counters.md) para especificar os dados de contadores que você deseja ler dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="91a8c-130">After adding the log files to the collection, use the [**Counters**](counters.md) collection to specify the counters data that you want to read from the log files.</span></span> <span data-ttu-id="91a8c-131">Observe que, se **SystemMonitor. DataSourceType** for definido como **DataSourceTypeConstants.sysmonLogFiles**, o SYSMON recriará os arquivos de log sempre que você adicionar um arquivo de log ou contador às respectivas coleções.</span><span class="sxs-lookup"><span data-stu-id="91a8c-131">Note that if **SystemMonitor.DataSourceType** is set to **DataSourceTypeConstants.sysmonLogFiles**, SYSMON will resample the log files each time you add a log file or counter to their respective collections.</span></span>

<span data-ttu-id="91a8c-132">**Antes do Windows Vista:** Você não poderá adicionar arquivos de log à [**coleção de arquivos de log**](systemmonitor-logfiles.md) se o valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) for definido como [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="91a8c-132">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="91a8c-133">Primeiro, defina **SystemMonitor. DataSourceType** como **DataSourceTypeConstants.sysmonNullDataSource**, adicione os arquivos de log e contadores e, em seguida, defina **SystemMonitor. DataSourceType** como **DataSourceTypeConstants.sysmonLogFiles**.</span><span class="sxs-lookup"><span data-stu-id="91a8c-133">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

<span data-ttu-id="91a8c-134">As propriedades [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) e [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) especificam o intervalo de valores de amostra dos arquivos de log para o grafo.</span><span class="sxs-lookup"><span data-stu-id="91a8c-134">The [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties specify the range of sampled values from the log files to graph.</span></span> <span data-ttu-id="91a8c-135">Os grafos do SYSMON apenas uma exibição de dados do arquivo de log (a exibição de gráfico não rola como faz ao grafar a atividade atual do computador).</span><span class="sxs-lookup"><span data-stu-id="91a8c-135">SYSMON graphs only one view worth of data from the log file (the graph view does not scroll as it does when graphing the current activity of the computer).</span></span> <span data-ttu-id="91a8c-136">Se os dados de amostra excederem o que pode ser mostrado em uma exibição de gráfico único, o SYSMON compacta os dados de amostra (cada ponto grafado representa a média de vários valores de amostra) para ajustar todos os dados de amostra dos arquivos de log no grafo.</span><span class="sxs-lookup"><span data-stu-id="91a8c-136">If the sampled data exceeds what can be shown on a single graph view, SYSMON compresses the sampled data (each graphed point represents the average of multiple sampled values) to fit all the sampled data from the log files on the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="91a8c-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91a8c-137">Requirements</span></span>



| <span data-ttu-id="91a8c-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="91a8c-138">Requirement</span></span> | <span data-ttu-id="91a8c-139">Valor</span><span class="sxs-lookup"><span data-stu-id="91a8c-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91a8c-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91a8c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="91a8c-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="91a8c-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="91a8c-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91a8c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="91a8c-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="91a8c-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91a8c-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="91a8c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="91a8c-145"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="91a8c-145"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="91a8c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="91a8c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91a8c-147"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="91a8c-147"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





