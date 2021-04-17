---
description: A data e a hora em que o relatório foi gerado.
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: Propriedade LocationDisp. DispCivicAddressReport. Timestamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b805454a6c2d62a58ba5a2a3de8f5b5095e1db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761828"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a><span data-ttu-id="1bc83-103">Propriedade LocationDisp. DispCivicAddressReport. Timestamp</span><span class="sxs-lookup"><span data-stu-id="1bc83-103">LocationDisp.DispCivicAddressReport.Timestamp property</span></span>

<span data-ttu-id="1bc83-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1bc83-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1bc83-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1bc83-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1bc83-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1bc83-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="1bc83-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="1bc83-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="1bc83-108">A data e a hora em que o relatório foi gerado.</span><span class="sxs-lookup"><span data-stu-id="1bc83-108">The date and time when the report was generated.</span></span>

<span data-ttu-id="1bc83-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1bc83-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bc83-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bc83-110">Syntax</span></span>


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a><span data-ttu-id="1bc83-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1bc83-111">Property value</span></span>

<span data-ttu-id="1bc83-112">Esta propriedade é uma **Data** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="1bc83-112">This property is a read-only **Date**.</span></span> <span data-ttu-id="1bc83-113">Os carimbos de data/hora são fornecidos como UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="1bc83-113">Time stamps are provided as Coordinated Universal Time (UTC).</span></span>

## <a name="remarks"></a><span data-ttu-id="1bc83-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bc83-114">Remarks</span></span>

<span data-ttu-id="1bc83-115">Observe que as linguagens de script, como o Microsoft JScript, podem exigir que você execute conversões para outros formatos de tempo ao exibir carimbos de data/hora como cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1bc83-115">Note that scripting languages, such as Microsoft JScript, might require you to perform conversions to other time formats when you display time stamps as strings.</span></span>

## <a name="examples"></a><span data-ttu-id="1bc83-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1bc83-116">Examples</span></span>

<span data-ttu-id="1bc83-117">Para obter um exemplo de como usar essa propriedade, consulte [um exemplo de relatório de endereço cívico simples](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="1bc83-117">For an example of how to use this property, see [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc83-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bc83-118">Requirements</span></span>



| <span data-ttu-id="1bc83-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bc83-119">Requirement</span></span> | <span data-ttu-id="1bc83-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1bc83-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="1bc83-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bc83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1bc83-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1bc83-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1bc83-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bc83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1bc83-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1bc83-124">None supported</span></span><br/>                  |



 

