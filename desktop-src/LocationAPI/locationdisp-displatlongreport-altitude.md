---
description: Altitude atual, em metros. Altitude é relativa ao elipsoide de referência.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: Propriedade LocationDisp. DispLatLongReport. altitude
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2004c8df6c61fb890bf8f71fb3c2b5446d71d79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828569"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a><span data-ttu-id="9694e-104">Propriedade LocationDisp. DispLatLongReport. altitude</span><span class="sxs-lookup"><span data-stu-id="9694e-104">LocationDisp.DispLatLongReport.Altitude property</span></span>

<span data-ttu-id="9694e-105">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="9694e-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9694e-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="9694e-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9694e-107">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9694e-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="9694e-108">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="9694e-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="9694e-109">Altitude atual, em metros.</span><span class="sxs-lookup"><span data-stu-id="9694e-109">Current altitude, in meters.</span></span> <span data-ttu-id="9694e-110">Altitude é relativa ao elipsoide de referência.</span><span class="sxs-lookup"><span data-stu-id="9694e-110">Altitude is relative to the reference ellipsoid.</span></span>

<span data-ttu-id="9694e-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9694e-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9694e-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9694e-112">Syntax</span></span>


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a><span data-ttu-id="9694e-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9694e-113">Property value</span></span>

<span data-ttu-id="9694e-114">Essa propriedade é um **número** somente leitura (ponto flutuante de precisão dupla).</span><span class="sxs-lookup"><span data-stu-id="9694e-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="9694e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9694e-115">Remarks</span></span>

<span data-ttu-id="9694e-116">Os sensores de localização não são necessários para fornecer essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="9694e-116">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="9694e-117">Você deve tratar exceções ao tentar acessar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="9694e-117">You should handle exceptions when attempting to access this property.</span></span>

<span data-ttu-id="9694e-118">O método **altitude** recupera a altitude relativa ao elipsoide de referência que é definido pela revisão mais recente do sistema geodésico (WGS 84), em vez da altitude em relação ao nível do Sea.</span><span class="sxs-lookup"><span data-stu-id="9694e-118">The **Altitude** method retrieves the altitude relative to the reference ellipsoid that is defined by the latest revision of the World Geodetic System (WGS 84), rather than the altitude relative to sea level.</span></span>

## <a name="examples"></a><span data-ttu-id="9694e-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9694e-119">Examples</span></span>

<span data-ttu-id="9694e-120">Para obter um exemplo de como usar essa propriedade, consulte [um exemplo de relatório simples de LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="9694e-120">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="9694e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9694e-121">Requirements</span></span>



| <span data-ttu-id="9694e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9694e-122">Requirement</span></span> | <span data-ttu-id="9694e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9694e-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="9694e-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9694e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9694e-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9694e-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9694e-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9694e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9694e-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9694e-127">None supported</span></span><br/>                  |



 

