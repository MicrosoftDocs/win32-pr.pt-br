---
description: O status atual do relatório.
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
ms.openlocfilehash: c32f1e58c5c519bdbdf797f81f11a449bfb3dc1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296855"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a><span data-ttu-id="9ce7e-103">Propriedade LocationDisp. LatLongReportFactory. status</span><span class="sxs-lookup"><span data-stu-id="9ce7e-103">LocationDisp.LatLongReportFactory.Status property</span></span>

<span data-ttu-id="9ce7e-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9ce7e-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9ce7e-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9ce7e-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="9ce7e-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="9ce7e-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="9ce7e-108">O status atual do relatório.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-108">The current report status.</span></span>

<span data-ttu-id="9ce7e-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce7e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ce7e-110">Syntax</span></span>


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="9ce7e-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9ce7e-111">Property value</span></span>

<span data-ttu-id="9ce7e-112">Esta propriedade é um **número** somente leitura (sem sinal).</span><span class="sxs-lookup"><span data-stu-id="9ce7e-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="9ce7e-113">Status</span><span class="sxs-lookup"><span data-stu-id="9ce7e-113">Status</span></span>                                                                                               | <span data-ttu-id="9ce7e-114">Significado</span><span class="sxs-lookup"><span data-stu-id="9ce7e-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="9ce7e-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce7e-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="9ce7e-116">Relatório sem suporte.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="9ce7e-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce7e-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9ce7e-118">Erro.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="9ce7e-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce7e-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9ce7e-120">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="9ce7e-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce7e-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="9ce7e-122">Inicializando.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="9ce7e-123"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="9ce7e-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="9ce7e-124">Running.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="9ce7e-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9ce7e-125">Examples</span></span>

<span data-ttu-id="9ce7e-126">Para obter um exemplo de como usar essa propriedade, consulte [escutando eventos de relatório LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="9ce7e-126">For an example of how to use this property, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce7e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ce7e-127">Requirements</span></span>



| <span data-ttu-id="9ce7e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ce7e-128">Requirement</span></span> | <span data-ttu-id="9ce7e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="9ce7e-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="9ce7e-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ce7e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9ce7e-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9ce7e-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9ce7e-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ce7e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9ce7e-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9ce7e-133">None supported</span></span><br/>                  |



 

