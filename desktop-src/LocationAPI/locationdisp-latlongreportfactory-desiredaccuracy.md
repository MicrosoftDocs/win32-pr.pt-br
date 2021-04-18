---
description: O valor de precisão desejado atual.
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: Propriedade LocationDisp. LatLongReportFactory. DesiredAccuracy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: e17e415d9503660d873ae4df67d2469c646dd80e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810160"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a><span data-ttu-id="c2a9d-103">Propriedade LocationDisp. LatLongReportFactory. DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="c2a9d-103">LocationDisp.LatLongReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="c2a9d-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c2a9d-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c2a9d-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c2a9d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c2a9d-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c2a9d-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="c2a9d-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="c2a9d-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="c2a9d-108">O valor de precisão desejado atual.</span><span class="sxs-lookup"><span data-stu-id="c2a9d-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="c2a9d-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c2a9d-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a9d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2a9d-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="c2a9d-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c2a9d-111">Property value</span></span>

<span data-ttu-id="c2a9d-112">Esta propriedade é um **ULONG** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c2a9d-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="c2a9d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c2a9d-113">Value</span></span>                                                                        | <span data-ttu-id="c2a9d-114">Significado</span><span class="sxs-lookup"><span data-stu-id="c2a9d-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2a9d-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c2a9d-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="c2a9d-116">Padrão.</span><span class="sxs-lookup"><span data-stu-id="c2a9d-116">Default.</span></span> <span data-ttu-id="c2a9d-117">O sensor deve usar a precisão para a qual ele pode otimizar o uso de energia e outras considerações de custo.</span><span class="sxs-lookup"><span data-stu-id="c2a9d-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="c2a9d-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c2a9d-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c2a9d-119">O sensor deve fornecer o relatório mais preciso possível.</span><span class="sxs-lookup"><span data-stu-id="c2a9d-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="c2a9d-120">Isso inclui usar serviços que podem cobrar dinheiro ou consumir níveis mais altos de energia da bateria ou largura de banda da conexão.</span><span class="sxs-lookup"><span data-stu-id="c2a9d-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2a9d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2a9d-121">Remarks</span></span>

<span data-ttu-id="c2a9d-122">Esse valor é uma solicitação para o provedor de localização.</span><span class="sxs-lookup"><span data-stu-id="c2a9d-122">This value is a request to the location provider.</span></span> <span data-ttu-id="c2a9d-123">O provedor de localização não é necessário para fornecer relatórios no intervalo solicitado.</span><span class="sxs-lookup"><span data-stu-id="c2a9d-123">The location provider is not required to provide reports at the interval you requested.</span></span> <span data-ttu-id="c2a9d-124">Leia o valor dessa propriedade para descobrir a configuração real do intervalo de relatório.</span><span class="sxs-lookup"><span data-stu-id="c2a9d-124">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a9d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2a9d-125">Requirements</span></span>



| <span data-ttu-id="c2a9d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2a9d-126">Requirement</span></span> | <span data-ttu-id="c2a9d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c2a9d-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="c2a9d-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2a9d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a9d-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c2a9d-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c2a9d-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2a9d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a9d-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c2a9d-131">None supported</span></span><br/>                  |



 

