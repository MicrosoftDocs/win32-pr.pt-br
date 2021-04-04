---
title: Método SystemMonitor. relog
description: Registra novamente os dados do contador em um novo arquivo. Você também pode usar esse método para especificar um novo tipo de arquivo e reduzir o número de amostras contidas no arquivo de log.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Método relog. SysMon
- Método relog SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método relog
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d0a6e44ef73652bd563099929ce601670610b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085432"
---
# <a name="systemmonitorrelog-method"></a><span data-ttu-id="7f2ad-107">Método SystemMonitor. relog</span><span class="sxs-lookup"><span data-stu-id="7f2ad-107">SystemMonitor.Relog method</span></span>

<span data-ttu-id="7f2ad-108">Registra novamente os dados do contador em um novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-108">Relogs the counter data to a new file.</span></span> <span data-ttu-id="7f2ad-109">Você também pode usar esse método para especificar um novo tipo de arquivo e reduzir o número de amostras contidas no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-109">You can also use this method to specify a new file type and to reduce the number of samples contained in the log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f2ad-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f2ad-110">Syntax</span></span>


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="7f2ad-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f2ad-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f2ad-112">*nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f2ad-112">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2ad-113">Caminho do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-113">File path of the log file.</span></span> <span data-ttu-id="7f2ad-114">Você pode especificar o caminho como um caminho absoluto, relativo ou UNC.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-114">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="7f2ad-115">A extensão do nome do arquivo de log deve ser. blg,. tsv ou. csv.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-115">The log file name extension must be either .blg, .tsv, or .csv.</span></span> <span data-ttu-id="7f2ad-116">Se uma pasta no caminho não existir, o SYSMON a criará.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-116">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="7f2ad-117">Se o arquivo existir, o arquivo será substituído.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-117">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="7f2ad-118">O SYSMON aplica as ACLs padrão do diretório pai.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-118">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="7f2ad-119">*filetype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f2ad-119">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2ad-120">Formato dos dados do contador salvos no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-120">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="7f2ad-121">Você pode especificar [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysMonFileCsv** ou **SysmonFileType.sysmonFileTsv**.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-121">You can specify either [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysmonFileCsv**, or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> <dt>

<span data-ttu-id="7f2ad-122">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f2ad-122">*filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2ad-123">Número de amostras dos arquivos de log antigos a serem salvos no novo arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-123">Number of samples from the old log files to save in the new log file.</span></span> <span data-ttu-id="7f2ad-124">Especifique 1 para salvar todas as amostras dos arquivos antigos nos novos arquivos.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-124">Specify 1 to save every sample from the old files to the new files.</span></span> <span data-ttu-id="7f2ad-125">Especifique 2 para salvar um de cada dois exemplos do arquivo antigo.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-125">Specify 2 to save one out of every two samples from the old file.</span></span> <span data-ttu-id="7f2ad-126">Especifique 3 para salvar um de cada três amostras do arquivo antigo.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-126">Specify 3 to save one out of every three samples from the old file.</span></span> <span data-ttu-id="7f2ad-127">E assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-127">And so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f2ad-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f2ad-128">Return value</span></span>

<span data-ttu-id="7f2ad-129">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f2ad-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f2ad-130">Remarks</span></span>

<span data-ttu-id="7f2ad-131">Esse método usa os arquivos de log contidos na coleção [**SystemMonitor. LogFiles**](systemmonitor-logfiles.md) para repetir os dados do contador.</span><span class="sxs-lookup"><span data-stu-id="7f2ad-131">This method uses the log files contained in the [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md) collection to relog the counter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f2ad-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f2ad-132">Requirements</span></span>



| <span data-ttu-id="7f2ad-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f2ad-133">Requirement</span></span> | <span data-ttu-id="7f2ad-134">Valor</span><span class="sxs-lookup"><span data-stu-id="7f2ad-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f2ad-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f2ad-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7f2ad-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f2ad-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f2ad-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f2ad-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7f2ad-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f2ad-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f2ad-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7f2ad-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f2ad-140"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="7f2ad-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f2ad-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f2ad-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f2ad-142">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="7f2ad-142">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="7f2ad-143">**SystemMonitor. SaveAs**</span><span class="sxs-lookup"><span data-stu-id="7f2ad-143">**SystemMonitor.SaveAs**</span></span>](systemmonitor-saveas.md)
</dt> </dl>

 

 





