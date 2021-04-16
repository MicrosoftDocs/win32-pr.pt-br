---
title: Método Counters. Add
description: Adiciona uma instância de monoitem à coleção.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Adicionar método SysMon
- Adicionar método SysMon, classe de contadores
- Classe Counters SysMon, método Add
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c974c5df6f531cd75292290c61534a923e5be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454850"
---
# <a name="countersadd-method"></a><span data-ttu-id="aec6c-106">Método Counters. Add</span><span class="sxs-lookup"><span data-stu-id="aec6c-106">Counters.Add method</span></span>

<span data-ttu-id="aec6c-107">Adiciona uma instância de [**monoitem**](counteritem.md) à coleção.</span><span class="sxs-lookup"><span data-stu-id="aec6c-107">Adds a [**CounterItem**](counteritem.md) instance to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="aec6c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aec6c-108">Syntax</span></span>


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a><span data-ttu-id="aec6c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aec6c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aec6c-110">*nome do caminho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aec6c-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec6c-111">Caminho para o contador.</span><span class="sxs-lookup"><span data-stu-id="aec6c-111">Path to the counter.</span></span> <span data-ttu-id="aec6c-112">O caminho pode incluir um nome de computador e deve incluir um nome de objeto de desempenho, um nome de instância de objeto se o objeto de desempenho especificado der suporte a várias instâncias e um nome de contador.</span><span class="sxs-lookup"><span data-stu-id="aec6c-112">The path can include a machine name, and must include a performance object name, an object instance name if the specified performance object supports multiple instances, and a counter name.</span></span> <span data-ttu-id="aec6c-113">Esta especificação de caminho não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="aec6c-113">This path specification is not case-sensitive.</span></span>

<span data-ttu-id="aec6c-114">Para obter detalhes sobre como especificar um caminho de contador, consulte [especificando um caminho de contador](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span><span class="sxs-lookup"><span data-stu-id="aec6c-114">For details on specifying a counter path, see [Specifying a Counter Path](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span></span>

</dd> </dl>

## <a name="exceptions"></a><span data-ttu-id="aec6c-115">Exceções</span><span class="sxs-lookup"><span data-stu-id="aec6c-115">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aec6c-116">Tipo de exceção</span><span class="sxs-lookup"><span data-stu-id="aec6c-116">Exception type</span></span></th>
<th><span data-ttu-id="aec6c-117">Condição</span><span class="sxs-lookup"><span data-stu-id="aec6c-117">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aec6c-118"><strong>System. Runtime. InteropServices. COMException</strong></span><span class="sxs-lookup"><span data-stu-id="aec6c-118"><strong>System.Runtime.InteropServices.COMException</strong></span></span></td>
<td><span data-ttu-id="aec6c-119">Você pode receber essa exceção por um dos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="aec6c-119">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="aec6c-120">O objeto de desempenho especificado não foi encontrado no computador.</span><span class="sxs-lookup"><span data-stu-id="aec6c-120">The specified performance object was not found on the computer.</span></span> <span data-ttu-id="aec6c-121">O valor Err. Number é 0xC0000BB8.</span><span class="sxs-lookup"><span data-stu-id="aec6c-121">The Err.Number value is 0xC0000BB8.</span></span></li>
<li><span data-ttu-id="aec6c-122">O contador especificado não pôde ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="aec6c-122">The specified counter could not be found.</span></span> <span data-ttu-id="aec6c-123">O valor Err. Number é 0xC0000BB9.</span><span class="sxs-lookup"><span data-stu-id="aec6c-123">The Err.Number value is 0xC0000BB9.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="aec6c-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="aec6c-124">Remarks</span></span>

<span data-ttu-id="aec6c-125">Se você especificar um contador curinga no parâmetro *PathName* , o método **Add** criará um objeto de Counter [**Item**](counteritem.md) para cada caminho expandido.</span><span class="sxs-lookup"><span data-stu-id="aec6c-125">If you specify a wildcard counter in the *pathname* parameter, the **Add** method creates one [**CounterItem**](counteritem.md) object for each expanded path.</span></span> <span data-ttu-id="aec6c-126">Em seguida, o método **Add** retorna um ponteiro para o primeiro **Item** a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="aec6c-126">The **Add** method then returns a pointer to the first added **CounterItem**.</span></span>

<span data-ttu-id="aec6c-127">Se o caractere curinga resultar em um contador duplicado, o erro não será relatado e nenhuma duplicata será criada.</span><span class="sxs-lookup"><span data-stu-id="aec6c-127">If the wildcard would result in a duplicate counter, the error is not reported and no duplicate is created.</span></span> <span data-ttu-id="aec6c-128">Se ocorrer uma condição de erro antes que todos os contadores sejam criados, o erro será relatado e os contadores restantes não serão criados.</span><span class="sxs-lookup"><span data-stu-id="aec6c-128">If an error condition occurs before all counters are created, the error is reported and the remaining counters are not created.</span></span>

<span data-ttu-id="aec6c-129">Não há nenhum limite para o número de contadores que você pode adicionar; no entanto, o SYSMON irá grafar apenas os primeiros 1.024 contadores na coleção.</span><span class="sxs-lookup"><span data-stu-id="aec6c-129">There is no limit to the number of counters that you can add; however, SYSMON will graph only the first 1,024 counters in the collection.</span></span> <span data-ttu-id="aec6c-130">Não há nenhum limite para o número de contadores que o SYSMON exibirá em um relatório.</span><span class="sxs-lookup"><span data-stu-id="aec6c-130">There is no limit on the number of counters that SYSMON will display in a report.</span></span>

<span data-ttu-id="aec6c-131">Para receber uma notificação quando um contador é adicionado, implemente o evento [OnCounterAdded](systemmonitor-oncounteradded.md) .</span><span class="sxs-lookup"><span data-stu-id="aec6c-131">To receive notification when a counter is added, implement the [OnCounterAdded](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="aec6c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aec6c-132">Requirements</span></span>



| <span data-ttu-id="aec6c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="aec6c-133">Requirement</span></span> | <span data-ttu-id="aec6c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="aec6c-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aec6c-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aec6c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="aec6c-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aec6c-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="aec6c-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aec6c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="aec6c-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aec6c-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aec6c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="aec6c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aec6c-140"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="aec6c-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aec6c-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="aec6c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aec6c-142">**Item**</span><span class="sxs-lookup"><span data-stu-id="aec6c-142">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="aec6c-143">**Contadores**</span><span class="sxs-lookup"><span data-stu-id="aec6c-143">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="aec6c-144">**SystemMonitor.BrowseCounters**</span><span class="sxs-lookup"><span data-stu-id="aec6c-144">**SystemMonitor.BrowseCounters**</span></span>](systemmonitor-browsecounters.md)
</dt> </dl>

 

