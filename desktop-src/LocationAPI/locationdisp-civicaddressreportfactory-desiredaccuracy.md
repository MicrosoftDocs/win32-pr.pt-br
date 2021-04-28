---
description: Propriedade LocationDisp. CivicAddressReportFactory. DesiredAccuracy-o valor de precisão desejado atual.
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: Propriedade LocationDisp. CivicAddressReportFactory. DesiredAccuracy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a18a363c2f24e9b17e16064b7375a4f075a1a8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110914"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a><span data-ttu-id="b70a6-103">Propriedade LocationDisp. CivicAddressReportFactory. DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="b70a6-103">LocationDisp.CivicAddressReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="b70a6-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b70a6-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b70a6-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b70a6-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b70a6-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b70a6-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="b70a6-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="b70a6-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="b70a6-108">O valor de precisão desejado atual.</span><span class="sxs-lookup"><span data-stu-id="b70a6-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="b70a6-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b70a6-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b70a6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b70a6-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="b70a6-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b70a6-111">Property value</span></span>

<span data-ttu-id="b70a6-112">Esta propriedade é um **ULONG** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b70a6-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="b70a6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b70a6-113">Value</span></span>                                                                        | <span data-ttu-id="b70a6-114">Significado</span><span class="sxs-lookup"><span data-stu-id="b70a6-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b70a6-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b70a6-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="b70a6-116">Padrão.</span><span class="sxs-lookup"><span data-stu-id="b70a6-116">Default.</span></span> <span data-ttu-id="b70a6-117">O sensor deve usar a precisão para a qual ele pode otimizar o uso de energia e outras considerações de custo.</span><span class="sxs-lookup"><span data-stu-id="b70a6-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="b70a6-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b70a6-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b70a6-119">O sensor deve fornecer o relatório mais preciso possível.</span><span class="sxs-lookup"><span data-stu-id="b70a6-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="b70a6-120">Isso inclui usar serviços que podem cobrar dinheiro ou consumir níveis mais altos de energia da bateria ou largura de banda da conexão.</span><span class="sxs-lookup"><span data-stu-id="b70a6-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b70a6-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b70a6-121">Remarks</span></span>

<span data-ttu-id="b70a6-122">Esse valor é uma solicitação para o provedor de localização.</span><span class="sxs-lookup"><span data-stu-id="b70a6-122">This value is a request to the location provider.</span></span> <span data-ttu-id="b70a6-123">O provedor de localização não é necessário para fornecer a precisão solicitada.</span><span class="sxs-lookup"><span data-stu-id="b70a6-123">The location provider is not required to provide the accuracy that you request.</span></span> <span data-ttu-id="b70a6-124">Leia o valor dessa propriedade para descobrir a configuração de precisão real.</span><span class="sxs-lookup"><span data-stu-id="b70a6-124">Read the value of this property to discover the true accuracy setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="b70a6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b70a6-125">Requirements</span></span>



| <span data-ttu-id="b70a6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b70a6-126">Requirement</span></span> | <span data-ttu-id="b70a6-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b70a6-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="b70a6-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b70a6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b70a6-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b70a6-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b70a6-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b70a6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b70a6-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b70a6-131">None supported</span></span><br/>                  |



 

