---
description: Ocorre quando um novo relatório de latitude/longitude é gerado.
ms.assetid: 2b1a25a1-ccd6-43f8-979b-c2d414d666a2
title: Evento NewLatLongReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: ea305d17169b71d183a8d453e9885d8de878b026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789636"
---
# <a name="newlatlongreport-event"></a><span data-ttu-id="d72e2-103">Evento NewLatLongReport</span><span class="sxs-lookup"><span data-stu-id="d72e2-103">NewLatLongReport event</span></span>

<span data-ttu-id="d72e2-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="d72e2-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d72e2-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d72e2-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d72e2-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d72e2-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="d72e2-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="d72e2-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="d72e2-108">Ocorre quando um novo relatório de latitude/longitude é gerado.</span><span class="sxs-lookup"><span data-stu-id="d72e2-108">Occurs when a new latitude/longitude report is generated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d72e2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d72e2-109">Syntax</span></span>


```JScript
.NewLatLongReport(
  newReport
)
```



## <a name="parameters"></a><span data-ttu-id="d72e2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d72e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d72e2-111">*newReport*</span><span class="sxs-lookup"><span data-stu-id="d72e2-111">*newReport*</span></span> 
</dt> <dd>

<span data-ttu-id="d72e2-112">O novo objeto [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md) .</span><span class="sxs-lookup"><span data-stu-id="d72e2-112">The new [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d72e2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d72e2-113">Return value</span></span>

<span data-ttu-id="d72e2-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d72e2-114">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="d72e2-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d72e2-115">Examples</span></span>

<span data-ttu-id="d72e2-116">Para obter um exemplo de como usar esse evento, consulte [escutando eventos de relatório do LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="d72e2-116">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="d72e2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d72e2-117">Requirements</span></span>



| <span data-ttu-id="d72e2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d72e2-118">Requirement</span></span> | <span data-ttu-id="d72e2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d72e2-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="d72e2-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d72e2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d72e2-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d72e2-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d72e2-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d72e2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d72e2-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d72e2-123">None supported</span></span><br/>                  |



 

