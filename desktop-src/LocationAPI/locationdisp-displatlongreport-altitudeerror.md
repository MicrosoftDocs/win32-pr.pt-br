---
description: Erro de altitude, em metros.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: Propriedade LocationDisp. DispLatLongReport. AltitudeError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.AltitudeError
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92fd71b133912a57e6ed4ef034dda6fe92ef9b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829016"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a><span data-ttu-id="e19f4-103">Propriedade LocationDisp. DispLatLongReport. AltitudeError</span><span class="sxs-lookup"><span data-stu-id="e19f4-103">LocationDisp.DispLatLongReport.AltitudeError property</span></span>

<span data-ttu-id="e19f4-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e19f4-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e19f4-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e19f4-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e19f4-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e19f4-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="e19f4-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="e19f4-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="e19f4-108">Erro de altitude, em metros.</span><span class="sxs-lookup"><span data-stu-id="e19f4-108">Altitude error, in meters.</span></span>

<span data-ttu-id="e19f4-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e19f4-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e19f4-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e19f4-110">Syntax</span></span>


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a><span data-ttu-id="e19f4-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e19f4-111">Property value</span></span>

<span data-ttu-id="e19f4-112">Essa propriedade é um **número** somente leitura (ponto flutuante de precisão dupla).</span><span class="sxs-lookup"><span data-stu-id="e19f4-112">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="e19f4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e19f4-113">Remarks</span></span>

<span data-ttu-id="e19f4-114">Os sensores de localização não são necessários para fornecer essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e19f4-114">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="e19f4-115">Você deve tratar exceções ao tentar acessar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e19f4-115">You should handle exceptions when attempting to access this property.</span></span>

## <a name="examples"></a><span data-ttu-id="e19f4-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e19f4-116">Examples</span></span>

<span data-ttu-id="e19f4-117">Para obter um exemplo de como usar essa propriedade, consulte [um exemplo de relatório simples de LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="e19f4-117">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="e19f4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e19f4-118">Requirements</span></span>



| <span data-ttu-id="e19f4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e19f4-119">Requirement</span></span> | <span data-ttu-id="e19f4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e19f4-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="e19f4-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e19f4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e19f4-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e19f4-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e19f4-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e19f4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e19f4-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e19f4-124">None supported</span></span><br/>                  |



 

