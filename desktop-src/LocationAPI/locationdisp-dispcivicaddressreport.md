---
description: Representa um relatório de endereços cívicos.
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: Objeto LocationDisp. DispCivicAddressReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a2a96f3d0c2a1fe8e3ac78e5db67ded031a4aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757243"
---
# <a name="locationdispdispcivicaddressreport-object"></a><span data-ttu-id="7507e-103">Objeto LocationDisp. DispCivicAddressReport</span><span class="sxs-lookup"><span data-stu-id="7507e-103">LocationDisp.DispCivicAddressReport object</span></span>

<span data-ttu-id="7507e-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="7507e-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7507e-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="7507e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7507e-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7507e-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="7507e-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="7507e-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="7507e-108">Representa um relatório de endereços cívicos.</span><span class="sxs-lookup"><span data-stu-id="7507e-108">Represents a civic address report.</span></span>

## <a name="members"></a><span data-ttu-id="7507e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="7507e-109">Members</span></span>

<span data-ttu-id="7507e-110">O objeto **LocationDisp. DispCivicAddressReport** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7507e-110">The **LocationDisp.DispCivicAddressReport** object has these types of members:</span></span>

-   [<span data-ttu-id="7507e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7507e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7507e-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7507e-112">Properties</span></span>

<span data-ttu-id="7507e-113">O objeto **LocationDisp. DispCivicAddressReport** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7507e-113">The **LocationDisp.DispCivicAddressReport** object has these properties.</span></span>



| <span data-ttu-id="7507e-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7507e-114">Property</span></span>                                                                              | <span data-ttu-id="7507e-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="7507e-115">Access type</span></span>          | <span data-ttu-id="7507e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="7507e-116">Description</span></span>                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [<span data-ttu-id="7507e-117">**AddressLine1**</span><span class="sxs-lookup"><span data-stu-id="7507e-117">**AddressLine1**</span></span>](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | <span data-ttu-id="7507e-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7507e-118">Read-only</span></span><br/> | <span data-ttu-id="7507e-119">A primeira linha de um endereço.</span><span class="sxs-lookup"><span data-stu-id="7507e-119">The first line of a street address.</span></span><br/>              |
| [<span data-ttu-id="7507e-120">**AddressLine2**</span><span class="sxs-lookup"><span data-stu-id="7507e-120">**AddressLine2**</span></span>](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | <span data-ttu-id="7507e-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7507e-121">Read-only</span></span><br/> | <span data-ttu-id="7507e-122">A segunda linha de um endereço de rua.</span><span class="sxs-lookup"><span data-stu-id="7507e-122">The second line of a street address.</span></span><br/>             |
| [<span data-ttu-id="7507e-123">**City**</span><span class="sxs-lookup"><span data-stu-id="7507e-123">**City**</span></span>](locationdisp-dispcivicaddressreport-city.md)<br/>                   | <span data-ttu-id="7507e-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7507e-124">Read-only</span></span><br/> | <span data-ttu-id="7507e-125">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="7507e-125">The city name.</span></span><br/>                                   |
| [<span data-ttu-id="7507e-126">**CountryRegion**</span><span class="sxs-lookup"><span data-stu-id="7507e-126">**CountryRegion**</span></span>](locationdisp-civicaddressreport-countryregion.md)<br/>     | <span data-ttu-id="7507e-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7507e-127">Read-only</span></span><br/> | <span data-ttu-id="7507e-128">O nome do país ou da região.</span><span class="sxs-lookup"><span data-stu-id="7507e-128">The country or region name.</span></span><br/>                      |
| [<span data-ttu-id="7507e-129">**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="7507e-129">**DetailLevel**</span></span>](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | <span data-ttu-id="7507e-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7507e-130">Read-only</span></span><br/> | <span data-ttu-id="7507e-131">O nível de detalhe do relatório.</span><span class="sxs-lookup"><span data-stu-id="7507e-131">The detail level for the report.</span></span><br/>                 |
| [<span data-ttu-id="7507e-132">**PostalCode**</span><span class="sxs-lookup"><span data-stu-id="7507e-132">**PostalCode**</span></span>](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | <span data-ttu-id="7507e-133">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7507e-133">Read-only</span></span><br/> | <span data-ttu-id="7507e-134">O código postal.</span><span class="sxs-lookup"><span data-stu-id="7507e-134">The postal code.</span></span><br/>                                 |
| [<span data-ttu-id="7507e-135">**StateProvince**</span><span class="sxs-lookup"><span data-stu-id="7507e-135">**StateProvince**</span></span>](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | <span data-ttu-id="7507e-136">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7507e-136">Read-only</span></span><br/> | <span data-ttu-id="7507e-137">O nome do Estado ou da província.</span><span class="sxs-lookup"><span data-stu-id="7507e-137">The state or province name.</span></span><br/>                      |
| [<span data-ttu-id="7507e-138">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="7507e-138">**Timestamp**</span></span>](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | <span data-ttu-id="7507e-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7507e-139">Read-only</span></span><br/> | <span data-ttu-id="7507e-140">A data e a hora em que o relatório foi gerado.</span><span class="sxs-lookup"><span data-stu-id="7507e-140">The date and time when the report was generated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7507e-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="7507e-141">Remarks</span></span>

<span data-ttu-id="7507e-142">Você pode recuperar esse objeto por meio da propriedade [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) de um objeto [**CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="7507e-142">You can retrieve this object through the [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) property of a [**CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md) object.</span></span> <span data-ttu-id="7507e-143">Você pode receber esse objeto por meio do evento [**NewCivicAddressReport**](newcivicaddressreport.md) .</span><span class="sxs-lookup"><span data-stu-id="7507e-143">You can receive this object through the [**NewCivicAddressReport**](newcivicaddressreport.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="7507e-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7507e-144">Requirements</span></span>



| <span data-ttu-id="7507e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="7507e-145">Requirement</span></span> | <span data-ttu-id="7507e-146">Valor</span><span class="sxs-lookup"><span data-stu-id="7507e-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="7507e-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7507e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="7507e-148">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7507e-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7507e-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7507e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="7507e-150">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7507e-150">None supported</span></span><br/>                  |



 

