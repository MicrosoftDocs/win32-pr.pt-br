---
description: Solicita eventos de relatório de endereços cívicos.
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: Método LocationDisp. CivicAddressReportFactory. ListenForReports (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 02315f8b2f7fced76c3d0d1330df246af6bad4b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922820"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a><span data-ttu-id="a8f0d-103">Método LocationDisp. CivicAddressReportFactory. ListenForReports</span><span class="sxs-lookup"><span data-stu-id="a8f0d-103">LocationDisp.CivicAddressReportFactory.ListenForReports method</span></span>

<span data-ttu-id="a8f0d-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a8f0d-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a8f0d-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a8f0d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a8f0d-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a8f0d-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="a8f0d-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="a8f0d-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="a8f0d-108">Solicita eventos de relatório de endereços cívicos.</span><span class="sxs-lookup"><span data-stu-id="a8f0d-108">Requests civic address report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f0d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8f0d-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a><span data-ttu-id="a8f0d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8f0d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f0d-111">*requestedReportInterval*</span><span class="sxs-lookup"><span data-stu-id="a8f0d-111">*requestedReportInterval*</span></span> 
</dt> <dd> <span data-ttu-id="a8f0d-112">Número (**palavra dupla**) que representa o tempo solicitado entre eventos de relatório de endereço cívico, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="a8f0d-112">Number (**double word**) representing the requested time between civic address report events, in milliseconds.</span></span> <span data-ttu-id="a8f0d-113">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="a8f0d-113">See Remarks.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f0d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8f0d-114">Return value</span></span>

<span data-ttu-id="a8f0d-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a8f0d-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f0d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8f0d-116">Remarks</span></span>

<span data-ttu-id="a8f0d-117">O provedor de localização não é necessário para fornecer a precisão solicitada.</span><span class="sxs-lookup"><span data-stu-id="a8f0d-117">The location provider is not required to provide the accuracy that you request.</span></span> <span data-ttu-id="a8f0d-118">Leia o valor da propriedade [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) para descobrir a configuração real do intervalo de relatório.</span><span class="sxs-lookup"><span data-stu-id="a8f0d-118">Read the value of the [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) property to discover the true report interval setting.</span></span>

## <a name="examples"></a><span data-ttu-id="a8f0d-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a8f0d-119">Examples</span></span>

<span data-ttu-id="a8f0d-120">Para obter um exemplo de como usar esse método, consulte [escutando eventos de relatório de endereço cívico](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="a8f0d-120">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f0d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8f0d-121">Requirements</span></span>



| <span data-ttu-id="a8f0d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8f0d-122">Requirement</span></span> | <span data-ttu-id="a8f0d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a8f0d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f0d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8f0d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f0d-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a8f0d-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a8f0d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8f0d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f0d-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a8f0d-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a8f0d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8f0d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8f0d-129"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8f0d-129"><dt>Locationapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8f0d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8f0d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f0d-131">**Evento NewCivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="a8f0d-131">**NewCivicAddressReport Event**</span></span>](newcivicaddressreport.md)
</dt> </dl>

 

