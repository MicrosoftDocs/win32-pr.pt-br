---
title: Propriedade SystemMonitor SqlLogSetName
description: Recupera ou define o nome amigável do conjunto de logs.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Propriedade SqlLogSetName SysMon
- Propriedade SqlLogSetName SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, Propriedade SqlLogSetName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008823"
---
# <a name="systemmonitorsqllogsetname-property"></a><span data-ttu-id="e157f-106">Propriedade SystemMonitor:: SqlLogSetName</span><span class="sxs-lookup"><span data-stu-id="e157f-106">SystemMonitor::SqlLogSetName property</span></span>

<span data-ttu-id="e157f-107">Recupera ou define o nome amigável do conjunto de logs.</span><span class="sxs-lookup"><span data-stu-id="e157f-107">Retrieves or sets the friendly name of the log set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e157f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e157f-108">Syntax</span></span>


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a><span data-ttu-id="e157f-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e157f-109">Property value</span></span>

<span data-ttu-id="e157f-110">Nome amigável do conjunto de logs, que corresponde a um único arquivo de log que contém dados binários ou de texto no SQL Database.</span><span class="sxs-lookup"><span data-stu-id="e157f-110">Friendly name of the log set, which corresponds to a single log file containing binary or text data in the SQL database.</span></span>

## <a name="remarks"></a><span data-ttu-id="e157f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e157f-111">Remarks</span></span>

<span data-ttu-id="e157f-112">**Antes do Windows Vista:** Você não poderá modificar essa propriedade se o valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) estiver definido como sysmonSqlLog.</span><span class="sxs-lookup"><span data-stu-id="e157f-112">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonSqlLog.</span></span>

## <a name="requirements"></a><span data-ttu-id="e157f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e157f-113">Requirements</span></span>



| <span data-ttu-id="e157f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e157f-114">Requirement</span></span> | <span data-ttu-id="e157f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e157f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e157f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e157f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e157f-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e157f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e157f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e157f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e157f-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e157f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e157f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e157f-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e157f-121"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e157f-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e157f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e157f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e157f-123">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="e157f-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="e157f-124">**SystemMonitor.SqlDsnName**</span><span class="sxs-lookup"><span data-stu-id="e157f-124">**SystemMonitor.SqlDsnName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





