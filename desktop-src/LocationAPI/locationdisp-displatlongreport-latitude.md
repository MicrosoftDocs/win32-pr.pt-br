---
description: Latitude atual, em graus.
ms.assetid: 24a4e75c-5162-406a-bf34-471387bff5d9
title: Propriedade LocationDisp. DispLatLongReport. latitude
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Latitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7f1bb6e7441b4e007c972f43bb45f59236ebe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766987"
---
# <a name="locationdispdisplatlongreportlatitude-property"></a><span data-ttu-id="f9961-103">Propriedade LocationDisp. DispLatLongReport. latitude</span><span class="sxs-lookup"><span data-stu-id="f9961-103">LocationDisp.DispLatLongReport.Latitude property</span></span>

<span data-ttu-id="f9961-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="f9961-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f9961-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f9961-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f9961-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f9961-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="f9961-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="f9961-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="f9961-108">Latitude atual, em graus.</span><span class="sxs-lookup"><span data-stu-id="f9961-108">Current latitude, in degrees.</span></span> <span data-ttu-id="f9961-109">A latitude está entre-90 e 90, em que o norte é positivo.</span><span class="sxs-lookup"><span data-stu-id="f9961-109">The latitude is between -90 and 90, where north is positive.</span></span>

<span data-ttu-id="f9961-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f9961-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9961-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9961-111">Syntax</span></span>


```JScript
Latitude = LocationDisp.DispLatLongReport.Latitude
```



## <a name="property-value"></a><span data-ttu-id="f9961-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f9961-112">Property value</span></span>

<span data-ttu-id="f9961-113">Essa propriedade é um **número** somente leitura (ponto flutuante de precisão dupla).</span><span class="sxs-lookup"><span data-stu-id="f9961-113">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="f9961-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9961-114">Examples</span></span>

<span data-ttu-id="f9961-115">Para obter um exemplo de como usar essa propriedade, consulte [um exemplo de relatório simples de LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="f9961-115">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9961-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9961-116">Requirements</span></span>



| <span data-ttu-id="f9961-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9961-117">Requirement</span></span> | <span data-ttu-id="f9961-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f9961-118">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="f9961-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9961-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f9961-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f9961-120">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f9961-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9961-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f9961-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f9961-122">None supported</span></span><br/>                  |



 

