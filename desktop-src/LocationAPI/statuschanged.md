---
description: Ocorre quando o status operacional de um relatório é alterado.
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: Evento StatusChanged
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1bda6645002f586eda0e2dad99a134450329d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172341"
---
# <a name="statuschanged-event"></a><span data-ttu-id="3971a-103">Evento StatusChanged</span><span class="sxs-lookup"><span data-stu-id="3971a-103">StatusChanged event</span></span>

<span data-ttu-id="3971a-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="3971a-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3971a-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="3971a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="3971a-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3971a-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="3971a-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="3971a-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="3971a-108">Ocorre quando o status operacional de um relatório é alterado.</span><span class="sxs-lookup"><span data-stu-id="3971a-108">Occurs when the operational status of a report changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3971a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3971a-109">Syntax</span></span>


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a><span data-ttu-id="3971a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3971a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3971a-111">*status*</span><span class="sxs-lookup"><span data-stu-id="3971a-111">*status*</span></span> 
</dt> <dd>

<span data-ttu-id="3971a-112">O novo status.</span><span class="sxs-lookup"><span data-stu-id="3971a-112">The new status.</span></span>



| <span data-ttu-id="3971a-113">Status</span><span class="sxs-lookup"><span data-stu-id="3971a-113">Status</span></span>                                                                                               | <span data-ttu-id="3971a-114">Significado</span><span class="sxs-lookup"><span data-stu-id="3971a-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="3971a-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="3971a-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="3971a-116">Relatório sem suporte.</span><span class="sxs-lookup"><span data-stu-id="3971a-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="3971a-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="3971a-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="3971a-118">Erro.</span><span class="sxs-lookup"><span data-stu-id="3971a-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="3971a-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="3971a-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="3971a-120">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="3971a-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="3971a-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="3971a-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="3971a-122">Inicializando.</span><span class="sxs-lookup"><span data-stu-id="3971a-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="3971a-123"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="3971a-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="3971a-124">Running.</span><span class="sxs-lookup"><span data-stu-id="3971a-124">Running.</span></span><br/>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3971a-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3971a-125">Return value</span></span>

<span data-ttu-id="3971a-126">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3971a-126">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3971a-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="3971a-127">Remarks</span></span>

<span data-ttu-id="3971a-128">Você deve implementar manipuladores de relatório de alteração de status separados para relatórios de endereço cívico e relatórios de latitude/longitude.</span><span class="sxs-lookup"><span data-stu-id="3971a-128">You should implement separate status change report handlers for civic address reports and latitude/longitude reports.</span></span>

## <a name="examples"></a><span data-ttu-id="3971a-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3971a-129">Examples</span></span>

<span data-ttu-id="3971a-130">Para obter um exemplo de como usar esse evento, consulte [escutando eventos de relatório do LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="3971a-130">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="3971a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3971a-131">Requirements</span></span>



| <span data-ttu-id="3971a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3971a-132">Requirement</span></span> | <span data-ttu-id="3971a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="3971a-133">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="3971a-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3971a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3971a-135">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3971a-135">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3971a-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3971a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3971a-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3971a-137">None supported</span></span><br/>                  |



 

