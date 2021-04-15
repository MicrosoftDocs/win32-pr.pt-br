---
title: Propriedade SystemMonitor. LogFilename
description: Recupera ou define o nome de um arquivo de log a ser usado como a origem dos valores do contador exibidos no monitor do sistema.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- Propriedade LogFilename SysMon
- Propriedade LogFilename SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade LogFilename
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369639"
---
# <a name="systemmonitorlogfilename-property"></a><span data-ttu-id="a8d02-106">Propriedade SystemMonitor. LogFilename</span><span class="sxs-lookup"><span data-stu-id="a8d02-106">SystemMonitor.LogFileName property</span></span>

<span data-ttu-id="a8d02-107">Recupera ou define o nome de um arquivo de log a ser usado como a origem dos valores do contador exibidos no monitor do sistema.</span><span class="sxs-lookup"><span data-stu-id="a8d02-107">Retrieves or sets the name of a log file to use as the source of counter values displayed in the System Monitor.</span></span>

> [!Note]  
> <span data-ttu-id="a8d02-108">Essa propriedade tornou-se obsoleta pela propriedade [**LogFiles**](systemmonitor-logfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="a8d02-108">This property has been made obsolete by the [**LogFiles**](systemmonitor-logfiles.md) property.</span></span>

 

<span data-ttu-id="a8d02-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a8d02-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d02-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8d02-110">Syntax</span></span>


```VB
Property LogFileName As String
```



## <a name="property-value"></a><span data-ttu-id="a8d02-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a8d02-111">Property value</span></span>

<span data-ttu-id="a8d02-112">Caminho para o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="a8d02-112">Path to the log file.</span></span> <span data-ttu-id="a8d02-113">Você pode especificar um caminho absoluto, relativo ou UNC.</span><span class="sxs-lookup"><span data-stu-id="a8d02-113">You can specify an absolute, relative, or UNC path.</span></span> <span data-ttu-id="a8d02-114">A extensão do nome do arquivo de log deve ser. csv,. tsv ou. blg.</span><span class="sxs-lookup"><span data-stu-id="a8d02-114">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

## <a name="exceptions"></a><span data-ttu-id="a8d02-115">Exceções</span><span class="sxs-lookup"><span data-stu-id="a8d02-115">Exceptions</span></span>



| <span data-ttu-id="a8d02-116">Tipo de exceção</span><span class="sxs-lookup"><span data-stu-id="a8d02-116">Exception type</span></span>                                  | <span data-ttu-id="a8d02-117">Condição</span><span class="sxs-lookup"><span data-stu-id="a8d02-117">Condition</span></span>                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="a8d02-118">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="a8d02-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="a8d02-119">Não é possível localizar o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a8d02-119">Unable to find the specified file.</span></span> <span data-ttu-id="a8d02-120">O valor Err. Number é 0xC0000BD1.</span><span class="sxs-lookup"><span data-stu-id="a8d02-120">The Err.Number value is 0xC0000BD1.</span></span> |
| <span data-ttu-id="a8d02-121">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="a8d02-121">**System.ArgumentException**</span></span>                    | <span data-ttu-id="a8d02-122">Você não pode especificar uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="a8d02-122">You cannot specify an empty string.</span></span>                                    |



 

## <a name="remarks"></a><span data-ttu-id="a8d02-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8d02-123">Remarks</span></span>

<span data-ttu-id="a8d02-124">Essa propriedade retorna o nome do arquivo de log do primeiro membro da coleção [**LogFiles**](systemmonitor-logfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="a8d02-124">This property returns the log file name from the first member of the [**LogFiles**](systemmonitor-logfiles.md) collection.</span></span>

<span data-ttu-id="a8d02-125">A definição dessa propriedade falhará se a coleção [**LogFiles**](systemmonitor-logfiles.md) contiver um ou mais membros.</span><span class="sxs-lookup"><span data-stu-id="a8d02-125">Setting this property will fail if the [**LogFiles**](systemmonitor-logfiles.md) collection contains one or more members.</span></span>

<span data-ttu-id="a8d02-126">Você deve usar a ferramenta Logman.exe ou o snap-in do MMC Perfmon. msc para gerar os arquivos de log que você adiciona a essa coleção.</span><span class="sxs-lookup"><span data-stu-id="a8d02-126">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="a8d02-127">Para Perfmon. msc, os logs de contador estão localizados em **logs e alertas de desempenho**.</span><span class="sxs-lookup"><span data-stu-id="a8d02-127">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="a8d02-128">Para obter detalhes sobre como usar Logman.exe ou Perfmon. msc, pesquise logman ou usando o desempenho, respectivamente, no **centro de ajuda e suporte**.</span><span class="sxs-lookup"><span data-stu-id="a8d02-128">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8d02-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8d02-129">Requirements</span></span>



| <span data-ttu-id="a8d02-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8d02-130">Requirement</span></span> | <span data-ttu-id="a8d02-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a8d02-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d02-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8d02-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a8d02-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a8d02-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a8d02-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8d02-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a8d02-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a8d02-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8d02-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a8d02-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8d02-137"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a8d02-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8d02-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8d02-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8d02-139">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="a8d02-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="a8d02-140">**SystemMonitor. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="a8d02-140">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





