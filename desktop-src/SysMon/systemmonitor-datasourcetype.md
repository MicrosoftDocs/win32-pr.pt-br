---
title: Propriedade DataSourceType SystemMonitor
description: Recupera ou define a origem dos dados do contador de desempenho.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- Propriedade DataSourceType SysMon
- Propriedade DataSourceType SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, Propriedade DataSourceType
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009583"
---
# <a name="systemmonitordatasourcetype-property"></a><span data-ttu-id="8cc02-106">SystemMonitor: Propriedade ataSourceType de:D</span><span class="sxs-lookup"><span data-stu-id="8cc02-106">SystemMonitor::DataSourceType property</span></span>

<span data-ttu-id="8cc02-107">Recupera ou define a origem dos dados do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="8cc02-107">Retrieves or sets the source of the performance counter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc02-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cc02-108">Syntax</span></span>


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="8cc02-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8cc02-109">Property value</span></span>

<span data-ttu-id="8cc02-110">Origem dos dados do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="8cc02-110">Source of the performance counter data.</span></span> <span data-ttu-id="8cc02-111">Para obter os valores possíveis, consulte [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="8cc02-111">For possible values, see [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="8cc02-112">Exceções</span><span class="sxs-lookup"><span data-stu-id="8cc02-112">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8cc02-113">Tipo de exceção</span><span class="sxs-lookup"><span data-stu-id="8cc02-113">Exception type</span></span></th>
<th><span data-ttu-id="8cc02-114">Condição</span><span class="sxs-lookup"><span data-stu-id="8cc02-114">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8cc02-115"><strong>System. ArgumentException</strong></span><span class="sxs-lookup"><span data-stu-id="8cc02-115"><strong>System.ArgumentException</strong></span></span></td>
<td><span data-ttu-id="8cc02-116">Você pode receber essa exceção por um dos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="8cc02-116">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="8cc02-117">O valor da fonte de dados especificada não é válido.</span><span class="sxs-lookup"><span data-stu-id="8cc02-117">The specified data source value is not valid.</span></span></li>
<li><span data-ttu-id="8cc02-118">Se a fonte de dados for um arquivo de log, o SYSMON não poderá localizar um dos arquivos especificados.</span><span class="sxs-lookup"><span data-stu-id="8cc02-118">If the data source is a log file, SYSMON cannot find one of the specified files.</span></span> <span data-ttu-id="8cc02-119">O valor Err. Number é 0xC0000BD1.</span><span class="sxs-lookup"><span data-stu-id="8cc02-119">The Err.Number value is 0xC0000BD1.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="8cc02-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cc02-120">Remarks</span></span>

<span data-ttu-id="8cc02-121">**Antes do Windows Vista:** Você não poderá adicionar ou remover arquivos de log da [**coleção de arquivos de log**](systemmonitor-logfiles.md) se o valor dessa propriedade for definido como sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="8cc02-121">**Prior to Windows Vista:** You cannot add or remove a log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of this property is set to sysmonLogFiles.</span></span> <span data-ttu-id="8cc02-122">Defina o valor dessa propriedade como sysmonLogFiles depois de criar ou modificar a coleção de arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="8cc02-122">Only set the value of this property to sysmonLogFiles after creating or modifying the log file collection.</span></span>

<span data-ttu-id="8cc02-123">Além disso, você não pode modificar as propriedades [**SqlDsnName**](systemmonitor-sqldsnname.md) e [**SqlLogSetName**](systemmonitor-sqllogsetname.md) se o valor dessa propriedade não deve ser definido como sysmonSqlLog.</span><span class="sxs-lookup"><span data-stu-id="8cc02-123">Also, you cannot modify the [**SqlDsnName**](systemmonitor-sqldsnname.md) and [**SqlLogSetName**](systemmonitor-sqllogsetname.md) properties if the value of this property must not be set to sysmonSqlLog.</span></span> <span data-ttu-id="8cc02-124">Defina o valor dessa propriedade como sysmonSqlLog depois de modificar os nomes do servidor e do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8cc02-124">Only set the value of this property to sysmonSqlLog after modifying the server and database names.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc02-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cc02-125">Requirements</span></span>



| <span data-ttu-id="8cc02-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cc02-126">Requirement</span></span> | <span data-ttu-id="8cc02-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc02-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc02-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cc02-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8cc02-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8cc02-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8cc02-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cc02-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8cc02-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8cc02-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cc02-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8cc02-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cc02-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8cc02-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cc02-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cc02-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc02-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="8cc02-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





