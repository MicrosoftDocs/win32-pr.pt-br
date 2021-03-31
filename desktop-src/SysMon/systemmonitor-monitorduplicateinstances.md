---
title: Propriedade SystemMonitor. MonitorDuplicateInstances
description: Recupera ou define um valor que determina se várias instâncias de um contador podem ser monitoradas.
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- Propriedade MonitorDuplicateInstances SysMon
- Propriedade MonitorDuplicateInstances SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade MonitorDuplicateInstances
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6ae53d0a1dcf3f67a43dab7959bb42619ace6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369514"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a><span data-ttu-id="564b7-106">Propriedade SystemMonitor. MonitorDuplicateInstances</span><span class="sxs-lookup"><span data-stu-id="564b7-106">SystemMonitor.MonitorDuplicateInstances property</span></span>

<span data-ttu-id="564b7-107">Recupera ou define um valor que determina se várias instâncias de um contador podem ser monitoradas.</span><span class="sxs-lookup"><span data-stu-id="564b7-107">Retrieves or sets a value that determines whether multiple instances of a counter can be monitored.</span></span>

<span data-ttu-id="564b7-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="564b7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="564b7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="564b7-109">Syntax</span></span>


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a><span data-ttu-id="564b7-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="564b7-110">Property value</span></span>

<span data-ttu-id="564b7-111">Verdadeiro indica que várias instâncias de um contador podem ser monitoradas (true é o padrão).</span><span class="sxs-lookup"><span data-stu-id="564b7-111">True indicates that multiple instances of a counter can be monitored (True is the default).</span></span> <span data-ttu-id="564b7-112">False indica que apenas uma instância de um contador pode ser monitorada.</span><span class="sxs-lookup"><span data-stu-id="564b7-112">False indicates that only one instance of a counter can be monitored.</span></span>

## <a name="remarks"></a><span data-ttu-id="564b7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="564b7-113">Remarks</span></span>

<span data-ttu-id="564b7-114">O monitor do sistema acrescenta \# n a cada nome de instância, exceto o primeiro, se houver várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="564b7-114">System Monitor appends \#n to every instance name, except the first, if multiple instances exist.</span></span> <span data-ttu-id="564b7-115">O número de série, n, começa com um e é incrementado em um para cada nova instância.</span><span class="sxs-lookup"><span data-stu-id="564b7-115">The serial number, n, begins with one and is incremented by one for each new instance.</span></span> <span data-ttu-id="564b7-116">Por exemplo, se você especificar " \\ processo ( \* ) \\ % tempo do processador", a coleção do contador deverá conter várias instâncias de svchost.</span><span class="sxs-lookup"><span data-stu-id="564b7-116">For example, if you specify "\\Process(\*)\\% Processor Time", the counter collection should contain multiple instances of svchost.</span></span> <span data-ttu-id="564b7-117">A primeira ocorrência será svchost, a próxima ocorrência será svchost \# 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="564b7-117">The first occurrence will be svchost, the next occurrence will be svchost\#1, and so on.</span></span>

<span data-ttu-id="564b7-118">As instâncias duplicadas serão monitoradas apenas se você usar o caractere curinga ( \* ) para o nome da instância.</span><span class="sxs-lookup"><span data-stu-id="564b7-118">Duplicate instances are monitored only if you use the wildcard character (\*) for the instance name.</span></span> <span data-ttu-id="564b7-119">Se você especificou " \\ processo (svchost) \\ % tempo do processador", somente a primeira instância encontrada de svchost será monitorada, nem todas as instâncias do svchost.</span><span class="sxs-lookup"><span data-stu-id="564b7-119">If you specified "\\Process(svchost)\\% Processor Time" only the first instance found of svchost is monitored, not all instances of svchost.</span></span>

## <a name="requirements"></a><span data-ttu-id="564b7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="564b7-120">Requirements</span></span>



| <span data-ttu-id="564b7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="564b7-121">Requirement</span></span> | <span data-ttu-id="564b7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="564b7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="564b7-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="564b7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="564b7-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="564b7-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="564b7-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="564b7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="564b7-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="564b7-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="564b7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="564b7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="564b7-128"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="564b7-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="564b7-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="564b7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="564b7-130">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="564b7-130">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





