---
description: Uma distância do local relatado, em metros. Combinado com o local relatado como a origem, esse raio descreve o círculo no qual o local real é provavelmente localizado.
ms.assetid: a9565bd5-d1e0-45f8-abeb-3191b16480fa
title: Propriedade LocationDisp. DispLatLongReport. ErrorRadius
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.ErrorRadius
api_type:
- COM
api_location: ''
ms.openlocfilehash: f99ff9b03451738158a98541bfae0e67a8827717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811023"
---
# <a name="locationdispdisplatlongreporterrorradius-property"></a><span data-ttu-id="8f162-104">Propriedade LocationDisp. DispLatLongReport. ErrorRadius</span><span class="sxs-lookup"><span data-stu-id="8f162-104">LocationDisp.DispLatLongReport.ErrorRadius property</span></span>

<span data-ttu-id="8f162-105">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="8f162-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8f162-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="8f162-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8f162-107">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8f162-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="8f162-108">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="8f162-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="8f162-109">Uma distância do local relatado, em metros.</span><span class="sxs-lookup"><span data-stu-id="8f162-109">A distance from the reported location, in meters.</span></span> <span data-ttu-id="8f162-110">Combinado com o local relatado como a origem, esse raio descreve o círculo no qual o local real é provavelmente localizado.</span><span class="sxs-lookup"><span data-stu-id="8f162-110">Combined with the reported location as the origin, this radius describes the circle in which the actual location is probably located.</span></span>

<span data-ttu-id="8f162-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="8f162-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f162-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f162-112">Syntax</span></span>


```JScript
ErrorRadius = LocationDisp.DispLatLongReport.ErrorRadius
```



## <a name="property-value"></a><span data-ttu-id="8f162-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8f162-113">Property value</span></span>

<span data-ttu-id="8f162-114">Essa propriedade é um **número** somente leitura (ponto flutuante de precisão dupla).</span><span class="sxs-lookup"><span data-stu-id="8f162-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="8f162-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f162-115">Examples</span></span>

<span data-ttu-id="8f162-116">Para obter um exemplo de como usar essa propriedade, consulte [um exemplo de relatório simples de LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="8f162-116">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f162-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f162-117">Requirements</span></span>



| <span data-ttu-id="8f162-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f162-118">Requirement</span></span> | <span data-ttu-id="8f162-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8f162-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="8f162-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f162-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8f162-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8f162-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8f162-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f162-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8f162-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8f162-123">None supported</span></span><br/>                  |



 

