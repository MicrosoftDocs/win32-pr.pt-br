---
description: O status atual do relatório.
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: Propriedade LocationDisp. CivicAddressReportFactory. status
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: ff937b11fbb64e0ec1596f9b3b9d85b33528eb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812923"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a><span data-ttu-id="f1a36-103">Propriedade LocationDisp. CivicAddressReportFactory. status</span><span class="sxs-lookup"><span data-stu-id="f1a36-103">LocationDisp.CivicAddressReportFactory.Status property</span></span>

<span data-ttu-id="f1a36-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="f1a36-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f1a36-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f1a36-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f1a36-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1a36-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="f1a36-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="f1a36-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="f1a36-108">O status atual do relatório.</span><span class="sxs-lookup"><span data-stu-id="f1a36-108">The current report status.</span></span>

<span data-ttu-id="f1a36-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f1a36-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1a36-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1a36-110">Syntax</span></span>


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="f1a36-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f1a36-111">Property value</span></span>

<span data-ttu-id="f1a36-112">Esta propriedade é um **número** somente leitura (sem sinal).</span><span class="sxs-lookup"><span data-stu-id="f1a36-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="f1a36-113">Status</span><span class="sxs-lookup"><span data-stu-id="f1a36-113">Status</span></span>                                                                                               | <span data-ttu-id="f1a36-114">Significado</span><span class="sxs-lookup"><span data-stu-id="f1a36-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="f1a36-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="f1a36-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="f1a36-116">Relatório sem suporte.</span><span class="sxs-lookup"><span data-stu-id="f1a36-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="f1a36-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f1a36-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f1a36-118">Erro.</span><span class="sxs-lookup"><span data-stu-id="f1a36-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="f1a36-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f1a36-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f1a36-120">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="f1a36-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="f1a36-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="f1a36-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f1a36-122">Inicializando.</span><span class="sxs-lookup"><span data-stu-id="f1a36-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="f1a36-123"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="f1a36-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f1a36-124">Running.</span><span class="sxs-lookup"><span data-stu-id="f1a36-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="f1a36-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f1a36-125">Examples</span></span>

<span data-ttu-id="f1a36-126">Para obter um exemplo de como usar essa propriedade, consulte [escutando eventos de relatório de endereço cívico](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="f1a36-126">For an example of how to use this property, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1a36-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1a36-127">Requirements</span></span>



| <span data-ttu-id="f1a36-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1a36-128">Requirement</span></span> | <span data-ttu-id="f1a36-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f1a36-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="f1a36-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1a36-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f1a36-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f1a36-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f1a36-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1a36-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f1a36-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f1a36-133">None supported</span></span><br/>                  |



 

