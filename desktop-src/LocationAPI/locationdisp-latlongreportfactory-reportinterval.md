---
description: O intervalo de eventos de relatório de latitude/longitude atual em milissegundos.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: Propriedade LocationDisp. LatLongReportFactory. ReportInterval
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: b456f69a70655b22b1eca30e02d9d5369d19f38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170060"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a><span data-ttu-id="62fcb-103">Propriedade LocationDisp. LatLongReportFactory. ReportInterval</span><span class="sxs-lookup"><span data-stu-id="62fcb-103">LocationDisp.LatLongReportFactory.ReportInterval property</span></span>

<span data-ttu-id="62fcb-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="62fcb-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="62fcb-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="62fcb-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="62fcb-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62fcb-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="62fcb-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="62fcb-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="62fcb-108">O intervalo de eventos de relatório de latitude/longitude atual em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="62fcb-108">The current latitude/longitude report event interval in milliseconds.</span></span>

<span data-ttu-id="62fcb-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="62fcb-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="62fcb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="62fcb-110">Syntax</span></span>


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a><span data-ttu-id="62fcb-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="62fcb-111">Property value</span></span>

<span data-ttu-id="62fcb-112">Esta propriedade é um **ULONG** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="62fcb-112">This property is a read/write **ULONG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="62fcb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="62fcb-113">Remarks</span></span>

<span data-ttu-id="62fcb-114">Esse valor é uma solicitação para o provedor de localização.</span><span class="sxs-lookup"><span data-stu-id="62fcb-114">This value is a request to the location provider.</span></span> <span data-ttu-id="62fcb-115">O provedor de localização não é necessário para fornecer relatórios no intervalo solicitado.</span><span class="sxs-lookup"><span data-stu-id="62fcb-115">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="62fcb-116">Leia o valor dessa propriedade para descobrir a configuração real do intervalo de relatório.</span><span class="sxs-lookup"><span data-stu-id="62fcb-116">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="62fcb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62fcb-117">Requirements</span></span>



| <span data-ttu-id="62fcb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="62fcb-118">Requirement</span></span> | <span data-ttu-id="62fcb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="62fcb-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="62fcb-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62fcb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62fcb-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="62fcb-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="62fcb-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62fcb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62fcb-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="62fcb-123">None supported</span></span><br/>                  |



 

