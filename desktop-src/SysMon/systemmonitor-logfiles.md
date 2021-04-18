---
title: Propriedade SystemMonitor. LogFiles
description: Coleção de um ou mais arquivos de log a serem usados como a origem dos valores do contador exibidos no monitor do sistema.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Propriedade LogFiles SysMon
- Propriedade LogFiles SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade LogFiles
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755290"
---
# <a name="systemmonitorlogfiles-property"></a><span data-ttu-id="bab76-106">Propriedade SystemMonitor. LogFiles</span><span class="sxs-lookup"><span data-stu-id="bab76-106">SystemMonitor.LogFiles property</span></span>

<span data-ttu-id="bab76-107">Coleção de um ou mais arquivos de log a serem usados como a origem dos valores do contador exibidos no monitor do sistema.</span><span class="sxs-lookup"><span data-stu-id="bab76-107">Collection of one or more log files to use as the source of counter values displayed in the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab76-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bab76-108">Syntax</span></span>


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a><span data-ttu-id="bab76-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bab76-109">Property value</span></span>

<span data-ttu-id="bab76-110">Coleção de objetos [**LogFileItem**](logfileitem.md) que especificam os arquivos de log usados como a fonte de dados para o grafo.</span><span class="sxs-lookup"><span data-stu-id="bab76-110">Collection of [**LogFileItem**](logfileitem.md) objects that specify the log files used as the data source for the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="bab76-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bab76-111">Remarks</span></span>

<span data-ttu-id="bab76-112">Para adicionar ou remover um arquivo de log da coleção de arquivos de log, o valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) não deve ser definido como sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="bab76-112">To add or remove a log file from the log file collection, the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) must not be set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="bab76-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bab76-113">Requirements</span></span>



| <span data-ttu-id="bab76-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bab76-114">Requirement</span></span> | <span data-ttu-id="bab76-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bab76-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bab76-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bab76-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bab76-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bab76-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bab76-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bab76-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bab76-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bab76-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bab76-120">DLL</span><span class="sxs-lookup"><span data-stu-id="bab76-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bab76-121"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="bab76-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bab76-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="bab76-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab76-123">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="bab76-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="bab76-124">**SystemMonitor. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="bab76-124">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> <dt>

[<span data-ttu-id="bab76-125">**SystemMonitor.LogViewStart**</span><span class="sxs-lookup"><span data-stu-id="bab76-125">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="bab76-126">**SystemMonitor.LogViewStop**</span><span class="sxs-lookup"><span data-stu-id="bab76-126">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="bab76-127">**SystemMonitor.SqlLogSetName**</span><span class="sxs-lookup"><span data-stu-id="bab76-127">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





