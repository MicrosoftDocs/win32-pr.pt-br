---
description: A data e a hora em que o relatório foi gerado.
ms.assetid: 3b8036aa-499c-4baf-bcc4-5b6c3f54eb7b
title: Propriedade LocationDisp. DispLatLongReport. Timestamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5ec179c5958b1be73a5fd5f74e48d0063edb6696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789887"
---
# <a name="locationdispdisplatlongreporttimestamp-property"></a><span data-ttu-id="51e34-103">Propriedade LocationDisp. DispLatLongReport. Timestamp</span><span class="sxs-lookup"><span data-stu-id="51e34-103">LocationDisp.DispLatLongReport.Timestamp property</span></span>

<span data-ttu-id="51e34-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="51e34-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="51e34-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="51e34-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="51e34-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="51e34-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="51e34-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="51e34-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="51e34-108">A data e a hora em que o relatório foi gerado.</span><span class="sxs-lookup"><span data-stu-id="51e34-108">The date and time when the report was generated.</span></span>

<span data-ttu-id="51e34-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="51e34-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e34-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51e34-110">Syntax</span></span>


```JScript
Timestamp = LocationDisp.DispLatLongReport.Timestamp
```



## <a name="property-value"></a><span data-ttu-id="51e34-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="51e34-111">Property value</span></span>

<span data-ttu-id="51e34-112">Esta propriedade é uma **Data** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="51e34-112">This property is a read-only **Date**.</span></span> <span data-ttu-id="51e34-113">Os carimbos de data/hora são fornecidos como UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="51e34-113">Time stamps are provided as Coordinated Universal Time (UTC).</span></span>

## <a name="remarks"></a><span data-ttu-id="51e34-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="51e34-114">Remarks</span></span>

<span data-ttu-id="51e34-115">Observe que as linguagens de script, como o Microsoft JScript, podem exigir que você execute conversões para outros formatos de tempo ao exibir carimbos de data/hora como cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="51e34-115">Note that scripting languages, such as Microsoft JScript, might require you to perform conversions to other time formats when you display time stamps as strings.</span></span>

## <a name="examples"></a><span data-ttu-id="51e34-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="51e34-116">Examples</span></span>

<span data-ttu-id="51e34-117">Para obter um exemplo de como usar essa propriedade, consulte [um exemplo de relatório simples de LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="51e34-117">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="51e34-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51e34-118">Requirements</span></span>



| <span data-ttu-id="51e34-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="51e34-119">Requirement</span></span> | <span data-ttu-id="51e34-120">Valor</span><span class="sxs-lookup"><span data-stu-id="51e34-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="51e34-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51e34-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51e34-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="51e34-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="51e34-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51e34-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51e34-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="51e34-124">None supported</span></span><br/>                  |



 

