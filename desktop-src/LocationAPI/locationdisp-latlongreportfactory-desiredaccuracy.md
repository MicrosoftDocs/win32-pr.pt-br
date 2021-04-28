---
description: Propriedade LocationDisp. LatLongReportFactory. DesiredAccuracy-o valor de precisão desejado atual.
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
ms.openlocfilehash: afc5ec235df6c9e07a665410cb09e00f24305304
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088964"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a><span data-ttu-id="866fa-103">Propriedade LocationDisp. LatLongReportFactory. DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="866fa-103">LocationDisp.LatLongReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="866fa-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="866fa-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="866fa-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="866fa-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="866fa-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="866fa-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="866fa-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="866fa-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="866fa-108">O valor de precisão desejado atual.</span><span class="sxs-lookup"><span data-stu-id="866fa-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="866fa-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="866fa-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="866fa-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="866fa-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="866fa-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="866fa-111">Property value</span></span>

<span data-ttu-id="866fa-112">Esta propriedade é um **ULONG** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="866fa-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="866fa-113">Valor</span><span class="sxs-lookup"><span data-stu-id="866fa-113">Value</span></span>                                                                        | <span data-ttu-id="866fa-114">Significado</span><span class="sxs-lookup"><span data-stu-id="866fa-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="866fa-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="866fa-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="866fa-116">Padrão.</span><span class="sxs-lookup"><span data-stu-id="866fa-116">Default.</span></span> <span data-ttu-id="866fa-117">O sensor deve usar a precisão para a qual ele pode otimizar o uso de energia e outras considerações de custo.</span><span class="sxs-lookup"><span data-stu-id="866fa-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="866fa-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="866fa-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="866fa-119">O sensor deve fornecer o relatório mais preciso possível.</span><span class="sxs-lookup"><span data-stu-id="866fa-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="866fa-120">Isso inclui usar serviços que podem cobrar dinheiro ou consumir níveis mais altos de energia da bateria ou largura de banda da conexão.</span><span class="sxs-lookup"><span data-stu-id="866fa-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="866fa-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="866fa-121">Remarks</span></span>

<span data-ttu-id="866fa-122">Esse valor é uma solicitação para o provedor de localização.</span><span class="sxs-lookup"><span data-stu-id="866fa-122">This value is a request to the location provider.</span></span> <span data-ttu-id="866fa-123">O provedor de localização não é necessário para fornecer relatórios no intervalo solicitado.</span><span class="sxs-lookup"><span data-stu-id="866fa-123">The location provider is not required to provide reports at the interval you requested.</span></span> <span data-ttu-id="866fa-124">Leia o valor dessa propriedade para descobrir a configuração real do intervalo de relatório.</span><span class="sxs-lookup"><span data-stu-id="866fa-124">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="866fa-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="866fa-125">Requirements</span></span>



| <span data-ttu-id="866fa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="866fa-126">Requirement</span></span> | <span data-ttu-id="866fa-127">Valor</span><span class="sxs-lookup"><span data-stu-id="866fa-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="866fa-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="866fa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="866fa-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="866fa-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="866fa-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="866fa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="866fa-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="866fa-131">None supported</span></span><br/>                  |



 

