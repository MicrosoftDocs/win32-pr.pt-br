---
description: Define os metadados de modelo e fabricante para o dispositivo a ser implementado. Este elemento é usado apenas para implementações de dispositivo (hosts).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: elemento thisModelMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a35d6449d4e8bba0ecf79e7dc87b00dee894b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829630"
---
# <a name="thismodelmetadata-element"></a><span data-ttu-id="f94f1-104">elemento thisModelMetadata</span><span class="sxs-lookup"><span data-stu-id="f94f1-104">thisModelMetadata element</span></span>

<span data-ttu-id="f94f1-105">Define os metadados de modelo e fabricante para o dispositivo a ser implementado.</span><span class="sxs-lookup"><span data-stu-id="f94f1-105">Defines the manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="f94f1-106">Este elemento é usado apenas para implementações de dispositivo (hosts).</span><span class="sxs-lookup"><span data-stu-id="f94f1-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="f94f1-107">Uso</span><span class="sxs-lookup"><span data-stu-id="f94f1-107">Usage</span></span>

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a><span data-ttu-id="f94f1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f94f1-108">Attributes</span></span>

<span data-ttu-id="f94f1-109">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="f94f1-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f94f1-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f94f1-110">Child elements</span></span>



| <span data-ttu-id="f94f1-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="f94f1-111">Element</span></span>                                                     | <span data-ttu-id="f94f1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f94f1-112">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f94f1-113">**fabricante**</span><span class="sxs-lookup"><span data-stu-id="f94f1-113">**manufacturer**</span></span>](manufacturer.md)<br/>             | <span data-ttu-id="f94f1-114">Nome do fabricante.</span><span class="sxs-lookup"><span data-stu-id="f94f1-114">Name of the manufacturer.</span></span> <span data-ttu-id="f94f1-115">Pelo menos um dos [**fabricantes**](manufacturer.md) ou [**manufacturerLS**](manufacturerls.md) deve estar presente nos metadados.</span><span class="sxs-lookup"><span data-stu-id="f94f1-115">At least one of [**manufacturer**](manufacturer.md) or [**manufacturerLS**](manufacturerls.md) must be present in the metadata.</span></span><br/> <br/> |
| [<span data-ttu-id="f94f1-116">**manufacturerLS**</span><span class="sxs-lookup"><span data-stu-id="f94f1-116">**manufacturerLS**</span></span>](manufacturerls.md)<br/>         | <span data-ttu-id="f94f1-117">Versão localizada do nome do fabricante.</span><span class="sxs-lookup"><span data-stu-id="f94f1-117">Localized version of the manufacturer name.</span></span><br/> <br/>                                                                                                                 |
| [<span data-ttu-id="f94f1-118">**manufacturerURL**</span><span class="sxs-lookup"><span data-stu-id="f94f1-118">**manufacturerURL**</span></span>](manufacturerurl.md)<br/>       | <span data-ttu-id="f94f1-119">Endereço URL do fabricante.</span><span class="sxs-lookup"><span data-stu-id="f94f1-119">Manufacturer URL address.</span></span><br/> <br/>                                                                                                                                   |
| [<span data-ttu-id="f94f1-120">**modelName**</span><span class="sxs-lookup"><span data-stu-id="f94f1-120">**modelName**</span></span>](modelname.md)<br/>                   | <span data-ttu-id="f94f1-121">Nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f94f1-121">Name of the device.</span></span> <span data-ttu-id="f94f1-122">Pelo menos um de [**ModelName**](modelname.md) ou [**modelNameLS**](modelnamels.md) deve estar presente nos metadados.</span><span class="sxs-lookup"><span data-stu-id="f94f1-122">At least one of [**modelName**](modelname.md) or [**modelNameLS**](modelnamels.md) must be present in the metadata.</span></span><br/> <br/>                   |
| [<span data-ttu-id="f94f1-123">**modelNameLS**</span><span class="sxs-lookup"><span data-stu-id="f94f1-123">**modelNameLS**</span></span>](modelnamels.md)<br/>               | <span data-ttu-id="f94f1-124">Versão localizada do nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f94f1-124">Localized version of the device name.</span></span><br/> <br/>                                                                                                                       |
| [<span data-ttu-id="f94f1-125">**modelNumber**</span><span class="sxs-lookup"><span data-stu-id="f94f1-125">**modelNumber**</span></span>](modelnumber.md)<br/>               | <span data-ttu-id="f94f1-126">O número do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f94f1-126">Model number of the device.</span></span><br/> <br/>                                                                                                                                 |
| [<span data-ttu-id="f94f1-127">**modelURL**</span><span class="sxs-lookup"><span data-stu-id="f94f1-127">**modelURL**</span></span>](modelurl.md)<br/>                     | <span data-ttu-id="f94f1-128">Endereço de URL para o modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f94f1-128">URL address for the device model.</span></span><br/> <br/>                                                                                                                           |
| [<span data-ttu-id="f94f1-129">**PnPXDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="f94f1-129">**PnPXDeviceCategory**</span></span>](pnpxdevicecategory.md)<br/> | <span data-ttu-id="f94f1-130">Categoria PnP-X à qual o dispositivo pertence.</span><span class="sxs-lookup"><span data-stu-id="f94f1-130">PnP-X category to which the device belongs.</span></span> <br/> <br/>                                                                                                                |
| [<span data-ttu-id="f94f1-131">**presentationURL**</span><span class="sxs-lookup"><span data-stu-id="f94f1-131">**presentationURL**</span></span>](presentationurl.md)<br/>       | <span data-ttu-id="f94f1-132">Endereço URL dos dados de apresentação do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f94f1-132">URL address of the device model's presentation data.</span></span><br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a><span data-ttu-id="f94f1-133">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="f94f1-133">Child element sequence</span></span>

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a><span data-ttu-id="f94f1-134">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f94f1-134">Parent elements</span></span>



| <span data-ttu-id="f94f1-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="f94f1-135">Element</span></span>                                     | <span data-ttu-id="f94f1-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="f94f1-136">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="f94f1-137">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="f94f1-137">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="f94f1-138">O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="f94f1-138">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f94f1-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="f94f1-139">Remarks</span></span>

<span data-ttu-id="f94f1-140">Os metadados do fabricante correspondem à seção de metadados do fabricante descrita no perfil do dispositivo (consulte o perfil do dispositivo para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="f94f1-140">The manufacturer metadata matches the manufacturer metadata section described in the device profile (consult the device profile for details).</span></span> <span data-ttu-id="f94f1-141">O nome do fabricante ou pelo menos uma versão localizada do nome do fabricante deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="f94f1-141">The manufacturer name or at least one localized version of the manufacturer name must be provided.</span></span> <span data-ttu-id="f94f1-142">O nome do modelo ou pelo menos uma versão localizada do nome do modelo deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="f94f1-142">The model name or at least one localized version of the model name must be provided.</span></span>

<span data-ttu-id="f94f1-143">O elemento [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) é usado subsequentemente para gerar uma constante C que contém essas informações.</span><span class="sxs-lookup"><span data-stu-id="f94f1-143">The [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) element is subsequently used to generate a C constant containing this information.</span></span>

<span data-ttu-id="f94f1-144">Se um elemento [**PnPXDeviceCategory**](pnpxdevicecategory.md) estiver presente, pelo menos um elemento [**hospedado**](hosted.md) deverá conter ambos os elementos [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="f94f1-144">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one [**hosted**](hosted.md) element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="f94f1-145">Da mesma forma, se os elementos **PnPXHardwareId** e **PnPXCompatibleId** estiverem presentes em um elemento **hospedado** , um elemento **PnPXDeviceCategory** deverá estar presente dentro do elemento **thisModelMetadata** .</span><span class="sxs-lookup"><span data-stu-id="f94f1-145">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, a **PnPXDeviceCategory** element must be present inside the **thisModelMetadata** element.</span></span>

## <a name="element-information"></a><span data-ttu-id="f94f1-146">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f94f1-146">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f94f1-147">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f94f1-147">Minimum supported system</span></span><br/> | <span data-ttu-id="f94f1-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f94f1-148">Windows Vista</span></span> |
| <span data-ttu-id="f94f1-149">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="f94f1-149">Can be empty</span></span>                        | <span data-ttu-id="f94f1-150">Não</span><span class="sxs-lookup"><span data-stu-id="f94f1-150">No</span></span>            |



 

 




