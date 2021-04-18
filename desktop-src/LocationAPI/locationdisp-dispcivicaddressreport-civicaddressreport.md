---
description: O relatório de endereços do cívico atual.
ms.assetid: a58dd612-bc54-42d1-9960-8c3de1c4fa83
title: Propriedade LocationDisp. CivicAddressReportFactory. CivicAddressReport (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.CivicAddressReport
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: c8be6e03861f1c5b2abffcb4b23d4845defa494e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810476"
---
# <a name="locationdispcivicaddressreportfactorycivicaddressreport-property"></a><span data-ttu-id="e6d1c-103">Propriedade LocationDisp. CivicAddressReportFactory. CivicAddressReport</span><span class="sxs-lookup"><span data-stu-id="e6d1c-103">LocationDisp.CivicAddressReportFactory.CivicAddressReport property</span></span>

<span data-ttu-id="e6d1c-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e6d1c-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e6d1c-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6d1c-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="e6d1c-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="e6d1c-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="e6d1c-108">O relatório de endereços do cívico atual.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-108">The current civic address report.</span></span>

<span data-ttu-id="e6d1c-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d1c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6d1c-110">Syntax</span></span>


```JScript
objCivicAddressReport = LocationDisp.CivicAddressReportFactory.CivicAddressReport
```



## <a name="property-value"></a><span data-ttu-id="e6d1c-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e6d1c-111">Property value</span></span>

<span data-ttu-id="e6d1c-112">Esta propriedade é somente leitura [**LocationDisp. CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md).</span><span class="sxs-lookup"><span data-stu-id="e6d1c-112">This property is a read-only [**LocationDisp.CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e6d1c-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e6d1c-113">Examples</span></span>

<span data-ttu-id="e6d1c-114">Para obter um exemplo de como usar essa propriedade, consulte [um exemplo de relatório de endereço cívico simples](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="e6d1c-114">For an example of how to use this property, see [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d1c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6d1c-115">Requirements</span></span>



| <span data-ttu-id="e6d1c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6d1c-116">Requirement</span></span> | <span data-ttu-id="e6d1c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e6d1c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d1c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6d1c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e6d1c-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e6d1c-119">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e6d1c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6d1c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e6d1c-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e6d1c-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e6d1c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6d1c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6d1c-123"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6d1c-123"><dt>Locationapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6d1c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6d1c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d1c-125">**LocationDisp.CivicAddressReportFactory**</span><span class="sxs-lookup"><span data-stu-id="e6d1c-125">**LocationDisp.CivicAddressReportFactory**</span></span>](locationdisp-civicaddressreportfactory.md)
</dt> </dl>

 

