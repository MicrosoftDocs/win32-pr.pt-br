---
title: Método MyItem. GetDataAt
description: Recupera o valor do contador especificado de um ponto específico no grafo.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Método GetDataAt SysMon
- Método GetDataAt SysMon, objeto monoitem
- Objeto monoitem SysMon, método GetDataAt
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499422"
---
# <a name="counteritemgetdataat-method"></a><span data-ttu-id="f68cf-106">Método MyItem. GetDataAt</span><span class="sxs-lookup"><span data-stu-id="f68cf-106">CounterItem.GetDataAt method</span></span>

<span data-ttu-id="f68cf-107">Recupera o valor do contador especificado de um ponto específico no grafo.</span><span class="sxs-lookup"><span data-stu-id="f68cf-107">Retrieves the specified counter value from a specific point in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="f68cf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f68cf-108">Syntax</span></span>


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="f68cf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f68cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f68cf-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f68cf-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f68cf-111">Índice de base zero do ponto do grafo cujo valor você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="f68cf-111">Zero-based index of the graph point whose value you want to retrieve.</span></span> <span data-ttu-id="f68cf-112">Os valores válidos variam de 0 a ([**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md) -1).</span><span class="sxs-lookup"><span data-stu-id="f68cf-112">Valid values range from 0 to ([**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md) - 1).</span></span>

</dd> <dt>

<span data-ttu-id="f68cf-113">*que* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f68cf-113">*which* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f68cf-114">Tipo de valor do contador a recuperar, por exemplo, o valor médio do contador, conforme exibido na janela do grafo.</span><span class="sxs-lookup"><span data-stu-id="f68cf-114">Type of counter value to retrieve, for example, the average value of the counter as displayed in the graph window.</span></span> <span data-ttu-id="f68cf-115">Para obter os valores possíveis, consulte [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span><span class="sxs-lookup"><span data-stu-id="f68cf-115">For possible values, see [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span></span>

</dd> <dt>

<span data-ttu-id="f68cf-116">*variante* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f68cf-116">*variant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f68cf-117">Valor do contador que foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="f68cf-117">Counter value that was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f68cf-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f68cf-118">Return value</span></span>

<span data-ttu-id="f68cf-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f68cf-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f68cf-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f68cf-120">Remarks</span></span>

<span data-ttu-id="f68cf-121">Use este método somente se</span><span class="sxs-lookup"><span data-stu-id="f68cf-121">Use this method only if</span></span>

-   <span data-ttu-id="f68cf-122">[**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) está definido como sysmonLineGraph</span><span class="sxs-lookup"><span data-stu-id="f68cf-122">[**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is set to sysmonLineGraph</span></span>
-   <span data-ttu-id="f68cf-123">[**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) é definido como SysmonLogFiles ou sysmonSqlLog</span><span class="sxs-lookup"><span data-stu-id="f68cf-123">[**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles or sysmonSqlLog</span></span>

## <a name="requirements"></a><span data-ttu-id="f68cf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f68cf-124">Requirements</span></span>



| <span data-ttu-id="f68cf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f68cf-125">Requirement</span></span> | <span data-ttu-id="f68cf-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f68cf-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f68cf-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f68cf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f68cf-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f68cf-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f68cf-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f68cf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f68cf-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f68cf-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f68cf-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f68cf-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f68cf-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f68cf-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f68cf-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f68cf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f68cf-134">**Item**</span><span class="sxs-lookup"><span data-stu-id="f68cf-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="f68cf-135">**MYITEM. getstatistics**</span><span class="sxs-lookup"><span data-stu-id="f68cf-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="f68cf-136">**MYITEM. GetValue**</span><span class="sxs-lookup"><span data-stu-id="f68cf-136">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





