---
description: Especifica a categoria PnP-X à qual o dispositivo pertence. Mais de uma categoria pode ser especificada.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Elemento PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731dd78fbe366fc9c7923686d3d9ac90b772c23d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781577"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="5d47c-104">Elemento PnPXDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="5d47c-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="5d47c-105">Especifica a categoria PnP-X à qual o dispositivo pertence.</span><span class="sxs-lookup"><span data-stu-id="5d47c-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="5d47c-106">Mais de uma categoria pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="5d47c-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="5d47c-107">Uso</span><span class="sxs-lookup"><span data-stu-id="5d47c-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="5d47c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5d47c-108">Attributes</span></span>

<span data-ttu-id="5d47c-109">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="5d47c-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5d47c-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5d47c-110">Child elements</span></span>

<span data-ttu-id="5d47c-111">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="5d47c-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="5d47c-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5d47c-112">Parent elements</span></span>



| <span data-ttu-id="5d47c-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="5d47c-113">Element</span></span>                                                   | <span data-ttu-id="5d47c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d47c-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d47c-115">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="5d47c-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="5d47c-116">Define os metadados de modelo e fabricante para o dispositivo a ser implementado.</span><span class="sxs-lookup"><span data-stu-id="5d47c-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5d47c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d47c-117">Remarks</span></span>

<span data-ttu-id="5d47c-118">Os dispositivos também podem especificar uma subcategoria de dispositivo para uma categoria de dispositivo mais descritiva.</span><span class="sxs-lookup"><span data-stu-id="5d47c-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="5d47c-119">Por exemplo, "phones. WindowsMobile cameras. DigitalStillCamera MediaDevices. MusicPlayer" identifica um dispositivo que é um dispositivo Microsoft Windows Mobile com uma câmera e um player de música.</span><span class="sxs-lookup"><span data-stu-id="5d47c-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="5d47c-120">A categoria de dispositivo primário para este dispositivo seria "telefones".</span><span class="sxs-lookup"><span data-stu-id="5d47c-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="5d47c-121">Para especificar mais de uma categoria de dispositivo, separe as categorias com um espaço.</span><span class="sxs-lookup"><span data-stu-id="5d47c-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="5d47c-122">Por exemplo, "armazenamento de impressoras" identifica um dispositivo com uma categoria primária de "impressoras" e uma categoria secundária de "armazenamento".</span><span class="sxs-lookup"><span data-stu-id="5d47c-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="5d47c-123">Se um elemento **PnPXDeviceCategory** estiver presente, pelo menos um elemento [**hospedado**](hosted.md) deverá conter ambos os elementos [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="5d47c-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="5d47c-124">Da mesma forma, se os elementos **PnPXHardwareId** e **PnPXCompatibleId** estiverem presentes em um elemento **hospedado** , pelo menos um elemento **PnPXDeviceCategory** deverá estar presente dentro do elemento [**thisModelMetadata**](thismodelmetadata.md) .</span><span class="sxs-lookup"><span data-stu-id="5d47c-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="5d47c-125">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5d47c-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="5d47c-126">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d47c-126">Minimum supported system</span></span><br/> | <span data-ttu-id="5d47c-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d47c-127">Windows Vista</span></span> |
| <span data-ttu-id="5d47c-128">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="5d47c-128">Can be empty</span></span>                        | <span data-ttu-id="5d47c-129">Sim</span><span class="sxs-lookup"><span data-stu-id="5d47c-129">Yes</span></span>           |



 

 




