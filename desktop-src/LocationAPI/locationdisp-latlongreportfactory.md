---
description: Gerencia relatórios de latitude/longitude.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: Objeto LocationDisp. LatLongReportFactory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837326"
---
# <a name="locationdisplatlongreportfactory-object"></a><span data-ttu-id="b9d0d-103">Objeto LocationDisp. LatLongReportFactory</span><span class="sxs-lookup"><span data-stu-id="b9d0d-103">LocationDisp.LatLongReportFactory object</span></span>

<span data-ttu-id="b9d0d-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b9d0d-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b9d0d-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b9d0d-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="b9d0d-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="b9d0d-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="b9d0d-108">Gerencia relatórios de latitude/longitude.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-108">Manages latitude/longitude reports.</span></span>

## <a name="members"></a><span data-ttu-id="b9d0d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b9d0d-109">Members</span></span>

<span data-ttu-id="b9d0d-110">O objeto **LocationDisp. LatLongReportFactory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b9d0d-110">The **LocationDisp.LatLongReportFactory** object has these types of members:</span></span>

-   [<span data-ttu-id="b9d0d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9d0d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b9d0d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b9d0d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b9d0d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9d0d-113">Methods</span></span>

<span data-ttu-id="b9d0d-114">O objeto **LocationDisp. LatLongReportFactory** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-114">The **LocationDisp.LatLongReportFactory** object has these methods.</span></span>



| <span data-ttu-id="b9d0d-115">Método</span><span class="sxs-lookup"><span data-stu-id="b9d0d-115">Method</span></span>                                                                                       | <span data-ttu-id="b9d0d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9d0d-116">Description</span></span>                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9d0d-117">**ListenForReports**</span><span class="sxs-lookup"><span data-stu-id="b9d0d-117">**ListenForReports**</span></span>](locationdisp-latlongreportfactory-listenforreports.md)               | <span data-ttu-id="b9d0d-118">Solicita eventos de relatório de latitude/longitude.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-118">Requests latitude/longitude report events.</span></span><br/>                                         |
| [<span data-ttu-id="b9d0d-119">**RequestPermissions**</span><span class="sxs-lookup"><span data-stu-id="b9d0d-119">**RequestPermissions**</span></span>](locationdisp-latlongreportfactory-requestpermissions.md)           | <span data-ttu-id="b9d0d-120">Abre uma caixa de diálogo do sistema para solicitar permissão de usuário para dispositivos habilitados para localização.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-120">Opens a system dialog box to request user permission for location-enabled devices.</span></span><br/> |
| <span data-ttu-id="b9d0d-121">[**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b9d0d-121">[**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span></span> | <span data-ttu-id="b9d0d-122">Cancela solicitações de eventos de relatório de latitude/longitude.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-122">Cancels requests for latitude/longitude report events.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="b9d0d-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b9d0d-123">Properties</span></span>

<span data-ttu-id="b9d0d-124">O objeto **LocationDisp. LatLongReportFactory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-124">The **LocationDisp.LatLongReportFactory** object has these properties.</span></span>



| <span data-ttu-id="b9d0d-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b9d0d-125">Property</span></span>                                                                                | <span data-ttu-id="b9d0d-126">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="b9d0d-126">Access type</span></span>           | <span data-ttu-id="b9d0d-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9d0d-127">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9d0d-128">**DesiredAccuracy**</span><span class="sxs-lookup"><span data-stu-id="b9d0d-128">**DesiredAccuracy**</span></span>](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | <span data-ttu-id="b9d0d-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b9d0d-129">Read/write</span></span><br/> | <span data-ttu-id="b9d0d-130">O valor de precisão desejado atual.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-130">The current desired-accuracy value.</span></span><br/>                                                   |
| [<span data-ttu-id="b9d0d-131">**LatLongReport**</span><span class="sxs-lookup"><span data-stu-id="b9d0d-131">**LatLongReport**</span></span>](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | <span data-ttu-id="b9d0d-132">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9d0d-132">Read-only</span></span><br/>  | <span data-ttu-id="b9d0d-133">O [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md)atual.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-133">The current [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span><br/> |
| [<span data-ttu-id="b9d0d-134">**ReportInterval**</span><span class="sxs-lookup"><span data-stu-id="b9d0d-134">**ReportInterval**</span></span>](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | <span data-ttu-id="b9d0d-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b9d0d-135">Read/write</span></span><br/> | <span data-ttu-id="b9d0d-136">O intervalo de eventos de relatório de latitude/longitude atual em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-136">The current latitude/longitude report event interval in milliseconds.</span></span><br/>                 |
| [<span data-ttu-id="b9d0d-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="b9d0d-137">**Status**</span></span>](locationdisp-latlongreportfactory-status.md)<br/>                   | <span data-ttu-id="b9d0d-138">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9d0d-138">Read-only</span></span><br/>  | <span data-ttu-id="b9d0d-139">O status atual do relatório.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-139">The current report status.</span></span><br/>                                                            |



 

## <a name="examples"></a><span data-ttu-id="b9d0d-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b9d0d-140">Examples</span></span>

<span data-ttu-id="b9d0d-141">O código de exemplo a seguir mostra como criar esse objeto em código HTML.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-141">The following example code shows how to create this object in HTML code.</span></span>


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



<span data-ttu-id="b9d0d-142">O código de exemplo a seguir mostra como criar esse objeto em JScript usando o Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-142">The following example code shows how to create this object in JScript using Windows Script Host.</span></span>


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



<span data-ttu-id="b9d0d-143">O código de exemplo a seguir mostra como criar esse objeto em VBScript usando o Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="b9d0d-143">The following example code shows how to create this object in VBScript using Windows Script Host.</span></span>


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a><span data-ttu-id="b9d0d-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9d0d-144">Requirements</span></span>



| <span data-ttu-id="b9d0d-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9d0d-145">Requirement</span></span> | <span data-ttu-id="b9d0d-146">Valor</span><span class="sxs-lookup"><span data-stu-id="b9d0d-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="b9d0d-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9d0d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="b9d0d-148">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b9d0d-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b9d0d-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9d0d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="b9d0d-150">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b9d0d-150">None supported</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="b9d0d-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9d0d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d0d-152">**LocationDisp.DispLatLongReport**</span><span class="sxs-lookup"><span data-stu-id="b9d0d-152">**LocationDisp.DispLatLongReport**</span></span>](locationdisp-displatlongreport.md)
</dt> </dl>

 

