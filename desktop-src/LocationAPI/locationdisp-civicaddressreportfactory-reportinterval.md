---
description: O intervalo de eventos de relatório de endereços do cívico atual em milissegundos.
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: Propriedade LocationDisp. CivicAddressReportFactory. ReportInterval
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: 47f7840be20ac640b5a8e7014f8401bc2350d328
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782340"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a><span data-ttu-id="4e21b-103">Propriedade LocationDisp. CivicAddressReportFactory. ReportInterval</span><span class="sxs-lookup"><span data-stu-id="4e21b-103">LocationDisp.CivicAddressReportFactory.ReportInterval property</span></span>

<span data-ttu-id="4e21b-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4e21b-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4e21b-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="4e21b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="4e21b-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e21b-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="4e21b-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="4e21b-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="4e21b-108">O intervalo de eventos de relatório de endereços do cívico atual em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="4e21b-108">The current civic address report event interval in milliseconds.</span></span>

<span data-ttu-id="4e21b-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4e21b-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e21b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e21b-110">Syntax</span></span>


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a><span data-ttu-id="4e21b-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4e21b-111">Property value</span></span>

<span data-ttu-id="4e21b-112">Esta propriedade é um **ULONG** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4e21b-112">This property is a read/write **ULONG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e21b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e21b-113">Remarks</span></span>

<span data-ttu-id="4e21b-114">Esse valor é uma solicitação para o provedor de localização.</span><span class="sxs-lookup"><span data-stu-id="4e21b-114">This value is a request for the location provider.</span></span> <span data-ttu-id="4e21b-115">O provedor de localização não é necessário para fornecer relatórios no intervalo que você solicitou.</span><span class="sxs-lookup"><span data-stu-id="4e21b-115">The location provider is not required to provide reports at the interval that you requested.</span></span> <span data-ttu-id="4e21b-116">Leia o valor dessa propriedade para descobrir a configuração real do intervalo de relatório.</span><span class="sxs-lookup"><span data-stu-id="4e21b-116">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e21b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e21b-117">Requirements</span></span>



| <span data-ttu-id="4e21b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e21b-118">Requirement</span></span> | <span data-ttu-id="4e21b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4e21b-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="4e21b-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e21b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4e21b-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4e21b-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4e21b-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e21b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4e21b-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4e21b-123">None supported</span></span><br/>                  |



 

