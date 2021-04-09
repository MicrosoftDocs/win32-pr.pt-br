---
description: O relatório de latitude/longitude atual.
ms.assetid: d2bb305f-911e-46f7-abde-56e9fba9182b
title: Propriedade LocationDisp. LatLongReportFactory. LatLongReport (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.LatLongReport
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: c44582c01685431e9b5dfa4820735728dd2a9cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169870"
---
# <a name="locationdisplatlongreportfactorylatlongreport-property"></a><span data-ttu-id="a4952-103">Propriedade LocationDisp. LatLongReportFactory. LatLongReport</span><span class="sxs-lookup"><span data-stu-id="a4952-103">LocationDisp.LatLongReportFactory.LatLongReport property</span></span>

<span data-ttu-id="a4952-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a4952-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a4952-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a4952-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a4952-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a4952-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="a4952-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="a4952-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="a4952-108">O relatório de latitude/longitude atual.</span><span class="sxs-lookup"><span data-stu-id="a4952-108">The current latitude/longitude report.</span></span>

<span data-ttu-id="a4952-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a4952-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4952-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4952-110">Syntax</span></span>


```JScript
objLatLongReport = LocationDisp.LatLongReportFactory.LatLongReport
```



## <a name="property-value"></a><span data-ttu-id="a4952-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a4952-111">Property value</span></span>

<span data-ttu-id="a4952-112">Esta propriedade é somente leitura [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md).</span><span class="sxs-lookup"><span data-stu-id="a4952-112">This property is a read-only [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a4952-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4952-113">Examples</span></span>

<span data-ttu-id="a4952-114">Para obter um exemplo de como usar essa propriedade, consulte [um exemplo de relatório simples de LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="a4952-114">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4952-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4952-115">Requirements</span></span>



| <span data-ttu-id="a4952-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4952-116">Requirement</span></span> | <span data-ttu-id="a4952-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a4952-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4952-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4952-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a4952-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a4952-119">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a4952-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4952-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a4952-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a4952-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a4952-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4952-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4952-123"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4952-123"><dt>Locationapi.h</dt></span></span> </dl> |



 

