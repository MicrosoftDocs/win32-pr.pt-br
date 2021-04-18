---
title: Método SystemMonitor. SaveAs
description: Salva os valores do contador no modo de exibição de gráfico em um arquivo de log.
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- Método SaveAs SysMon
- Método SaveAs SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método SaveAs
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771791"
---
# <a name="systemmonitorsaveas-method"></a><span data-ttu-id="3946f-106">Método SystemMonitor. SaveAs</span><span class="sxs-lookup"><span data-stu-id="3946f-106">SystemMonitor.SaveAs method</span></span>

<span data-ttu-id="3946f-107">Salva os valores do contador no modo de exibição de gráfico em um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="3946f-107">Saves the counter values in the graph view to a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3946f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3946f-108">Syntax</span></span>


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a><span data-ttu-id="3946f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3946f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3946f-110">*nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3946f-110">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3946f-111">Caminho do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="3946f-111">File path of the log file.</span></span> <span data-ttu-id="3946f-112">Você pode especificar o caminho como um caminho absoluto, relativo ou UNC.</span><span class="sxs-lookup"><span data-stu-id="3946f-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="3946f-113">A extensão do nome do arquivo de log deve ser. tsv ou. htm.</span><span class="sxs-lookup"><span data-stu-id="3946f-113">The log file name extension must be either .tsv or .htm.</span></span> <span data-ttu-id="3946f-114">Se uma pasta no caminho não existir, o SYSMON a criará.</span><span class="sxs-lookup"><span data-stu-id="3946f-114">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="3946f-115">Se o arquivo existir, o arquivo será substituído.</span><span class="sxs-lookup"><span data-stu-id="3946f-115">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="3946f-116">O SYSMON aplica as ACLs padrão do diretório pai.</span><span class="sxs-lookup"><span data-stu-id="3946f-116">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="3946f-117">*filetype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3946f-117">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3946f-118">Formato dos dados do contador salvos no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="3946f-118">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="3946f-119">Você pode especificar [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) ou **SysmonFileType.sysmonFileTsv**.</span><span class="sxs-lookup"><span data-stu-id="3946f-119">You can specify either [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3946f-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3946f-120">Return value</span></span>

<span data-ttu-id="3946f-121">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3946f-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3946f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="3946f-122">Remarks</span></span>

<span data-ttu-id="3946f-123">Somente os dados do contador visíveis no modo de exibição de gráfico são salvos (para o número real de pontos de dados salvos, consulte [**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md)).</span><span class="sxs-lookup"><span data-stu-id="3946f-123">Only the counter data visible in the graph view is saved (for the actual number of data points saved, see [**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="3946f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3946f-124">Requirements</span></span>



| <span data-ttu-id="3946f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3946f-125">Requirement</span></span> | <span data-ttu-id="3946f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3946f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3946f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3946f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3946f-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3946f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3946f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3946f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3946f-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3946f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3946f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3946f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3946f-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="3946f-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3946f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="3946f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3946f-134">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="3946f-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="3946f-135">**SystemMonitor. relog**</span><span class="sxs-lookup"><span data-stu-id="3946f-135">**SystemMonitor.Relog**</span></span>](systemmonitor-relog.md)
</dt> </dl>

 

 





