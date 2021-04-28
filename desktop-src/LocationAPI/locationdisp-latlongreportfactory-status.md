---
description: Propriedade LocationDisp. LatLongReportFactory. status-o status atual do relatório.
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: Propriedade LocationDisp. LatLongReportFactory. status
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 37e66c3f289f5376b31ffe516f45d79f2fef51e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088894"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a><span data-ttu-id="c2b02-103">Propriedade LocationDisp. LatLongReportFactory. status</span><span class="sxs-lookup"><span data-stu-id="c2b02-103">LocationDisp.LatLongReportFactory.Status property</span></span>

<span data-ttu-id="c2b02-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c2b02-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c2b02-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c2b02-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c2b02-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c2b02-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="c2b02-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="c2b02-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="c2b02-108">O status atual do relatório.</span><span class="sxs-lookup"><span data-stu-id="c2b02-108">The current report status.</span></span>

<span data-ttu-id="c2b02-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="c2b02-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b02-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2b02-110">Syntax</span></span>


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="c2b02-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c2b02-111">Property value</span></span>

<span data-ttu-id="c2b02-112">Esta propriedade é um **número** somente leitura (sem sinal).</span><span class="sxs-lookup"><span data-stu-id="c2b02-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="c2b02-113">Status</span><span class="sxs-lookup"><span data-stu-id="c2b02-113">Status</span></span>                                                                                               | <span data-ttu-id="c2b02-114">Significado</span><span class="sxs-lookup"><span data-stu-id="c2b02-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="c2b02-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b02-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="c2b02-116">Relatório sem suporte.</span><span class="sxs-lookup"><span data-stu-id="c2b02-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="c2b02-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b02-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c2b02-118">Erro.</span><span class="sxs-lookup"><span data-stu-id="c2b02-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="c2b02-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b02-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c2b02-120">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="c2b02-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="c2b02-121"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b02-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c2b02-122">Inicializando.</span><span class="sxs-lookup"><span data-stu-id="c2b02-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="c2b02-123"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b02-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c2b02-124">Running.</span><span class="sxs-lookup"><span data-stu-id="c2b02-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="c2b02-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c2b02-125">Examples</span></span>

<span data-ttu-id="c2b02-126">Para obter um exemplo de como usar essa propriedade, consulte [escutando eventos de relatório LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="c2b02-126">For an example of how to use this property, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2b02-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2b02-127">Requirements</span></span>



| <span data-ttu-id="c2b02-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2b02-128">Requirement</span></span> | <span data-ttu-id="c2b02-129">Valor</span><span class="sxs-lookup"><span data-stu-id="c2b02-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="c2b02-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2b02-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c2b02-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c2b02-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c2b02-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2b02-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c2b02-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c2b02-133">None supported</span></span><br/>                  |



 

