---
description: Especifica a categoria PnP-X à qual o dispositivo pertence. Mais de uma categoria pode ser especificada.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Elemento PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08084d780c26d2f7fab902156939fd14a3e60c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996583"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="87693-104">Elemento PnPXDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="87693-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="87693-105">Especifica a categoria PnP-X à qual o dispositivo pertence.</span><span class="sxs-lookup"><span data-stu-id="87693-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="87693-106">Mais de uma categoria pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="87693-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="87693-107">Uso</span><span class="sxs-lookup"><span data-stu-id="87693-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="87693-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="87693-108">Attributes</span></span>

<span data-ttu-id="87693-109">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="87693-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="87693-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="87693-110">Child elements</span></span>

<span data-ttu-id="87693-111">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="87693-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="87693-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="87693-112">Parent elements</span></span>



| <span data-ttu-id="87693-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="87693-113">Element</span></span>                                                   | <span data-ttu-id="87693-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="87693-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87693-115">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="87693-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="87693-116">Define os metadados de modelo e fabricante para o dispositivo a ser implementado.</span><span class="sxs-lookup"><span data-stu-id="87693-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="87693-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="87693-117">Remarks</span></span>

<span data-ttu-id="87693-118">Os dispositivos também podem especificar uma subcategoria de dispositivo para uma categoria de dispositivo mais descritiva.</span><span class="sxs-lookup"><span data-stu-id="87693-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="87693-119">Por exemplo, "phones. WindowsMobile cameras. DigitalStillCamera MediaDevices. MusicPlayer" identifica um dispositivo que é um dispositivo Microsoft Windows Mobile com uma câmera e um player de música.</span><span class="sxs-lookup"><span data-stu-id="87693-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="87693-120">A categoria de dispositivo primário para este dispositivo seria "telefones".</span><span class="sxs-lookup"><span data-stu-id="87693-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="87693-121">Para especificar mais de uma categoria de dispositivo, separe as categorias com um espaço.</span><span class="sxs-lookup"><span data-stu-id="87693-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="87693-122">Por exemplo, "armazenamento de impressoras" identifica um dispositivo com uma categoria primária de "impressoras" e uma categoria secundária de "armazenamento".</span><span class="sxs-lookup"><span data-stu-id="87693-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="87693-123">Se um elemento **PnPXDeviceCategory** estiver presente, pelo menos um elemento [**hospedado**](hosted.md) deverá conter ambos os elementos [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="87693-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="87693-124">Da mesma forma, se os elementos **PnPXHardwareId** e **PnPXCompatibleId** estiverem presentes em um elemento **hospedado** , pelo menos um elemento **PnPXDeviceCategory** deverá estar presente dentro do elemento [**thisModelMetadata**](thismodelmetadata.md) .</span><span class="sxs-lookup"><span data-stu-id="87693-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="87693-125">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="87693-125">Element information</span></span>



| <span data-ttu-id="87693-126">Label</span><span class="sxs-lookup"><span data-stu-id="87693-126">Label</span></span> | <span data-ttu-id="87693-127">Valor</span><span class="sxs-lookup"><span data-stu-id="87693-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="87693-128">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87693-128">Minimum supported system</span></span><br/> | <span data-ttu-id="87693-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87693-129">Windows Vista</span></span> |
| <span data-ttu-id="87693-130">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="87693-130">Can be empty</span></span>                        | <span data-ttu-id="87693-131">Sim</span><span class="sxs-lookup"><span data-stu-id="87693-131">Yes</span></span>           |



 

 




