---
title: Método LogFiles. Add
description: Adiciona um arquivo de log à coleção.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Adicionar método SysMon
- Adicionar método SysMon, classe LogFiles
- Classe LogFiles SysMon, método Add
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f690670606cd7ee307ba945fc2daabe92953e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085605"
---
# <a name="logfilesadd-method"></a><span data-ttu-id="cce72-106">Método LogFiles. Add</span><span class="sxs-lookup"><span data-stu-id="cce72-106">LogFiles.Add method</span></span>

<span data-ttu-id="cce72-107">Adiciona um arquivo de log à coleção.</span><span class="sxs-lookup"><span data-stu-id="cce72-107">Adds a log file to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cce72-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cce72-108">Syntax</span></span>


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a><span data-ttu-id="cce72-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cce72-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cce72-110">*nome do caminho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cce72-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cce72-111">Caminho para o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="cce72-111">Path to the log file.</span></span> <span data-ttu-id="cce72-112">Você pode especificar o caminho como um caminho absoluto, relativo ou UNC.</span><span class="sxs-lookup"><span data-stu-id="cce72-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="cce72-113">A extensão do nome do arquivo de log deve ser. csv,. tsv ou. blg.</span><span class="sxs-lookup"><span data-stu-id="cce72-113">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cce72-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cce72-114">Remarks</span></span>

<span data-ttu-id="cce72-115">Você deve usar a ferramenta Logman.exe ou o snap-in do MMC Perfmon. msc para gerar os arquivos de log que você adiciona a essa coleção.</span><span class="sxs-lookup"><span data-stu-id="cce72-115">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="cce72-116">Para Perfmon. msc, os logs de contador estão localizados em **logs e alertas de desempenho**.</span><span class="sxs-lookup"><span data-stu-id="cce72-116">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="cce72-117">Para obter detalhes sobre como usar Logman.exe ou Perfmon. msc, pesquise logman ou usando o desempenho, respectivamente, no **centro de ajuda e suporte**.</span><span class="sxs-lookup"><span data-stu-id="cce72-117">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

<span data-ttu-id="cce72-118">**Antes do Windows Vista:** Você não poderá adicionar arquivos de log à [**coleção de arquivos de log**](systemmonitor-logfiles.md) se o valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) for definido como [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="cce72-118">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="cce72-119">Primeiro, defina **SystemMonitor. DataSourceType** como **DataSourceTypeConstants.sysmonNullDataSource**, adicione os arquivos de log e contadores e, em seguida, defina **SystemMonitor. DataSourceType** como **DataSourceTypeConstants.sysmonLogFiles**.</span><span class="sxs-lookup"><span data-stu-id="cce72-119">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cce72-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cce72-120">Requirements</span></span>



| <span data-ttu-id="cce72-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cce72-121">Requirement</span></span> | <span data-ttu-id="cce72-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cce72-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cce72-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cce72-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cce72-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cce72-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cce72-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cce72-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cce72-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cce72-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cce72-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cce72-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cce72-128"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="cce72-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cce72-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cce72-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce72-130">arquivos de log</span><span class="sxs-lookup"><span data-stu-id="cce72-130">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="cce72-131">**LogFileItem**</span><span class="sxs-lookup"><span data-stu-id="cce72-131">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="cce72-132">**arquivos de log**</span><span class="sxs-lookup"><span data-stu-id="cce72-132">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





