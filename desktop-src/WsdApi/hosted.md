---
description: Define os elementos ServiceId, Types, PnPXHardwareId e PnPXCompatibleId para os serviços definidos pelo host de serviço.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: elemento hospedado
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46549898f0a95de362467c759c3d95eb806a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771480"
---
# <a name="hosted-element"></a><span data-ttu-id="2a570-103">elemento hospedado</span><span class="sxs-lookup"><span data-stu-id="2a570-103">hosted element</span></span>

<span data-ttu-id="2a570-104">Define os elementos [**ServiceId**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md)e [**PnPXCompatibleId**](pnpxcompatibleid.md) para os serviços definidos pelo host de serviço.</span><span class="sxs-lookup"><span data-stu-id="2a570-104">Defines the [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md), and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements for the services defined by the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="2a570-105">Uso</span><span class="sxs-lookup"><span data-stu-id="2a570-105">Usage</span></span>

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a><span data-ttu-id="2a570-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="2a570-106">Attributes</span></span>

<span data-ttu-id="2a570-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="2a570-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2a570-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2a570-108">Child elements</span></span>



| <span data-ttu-id="2a570-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="2a570-109">Element</span></span>                                                 | <span data-ttu-id="2a570-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a570-110">Description</span></span>                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="2a570-111">**PnPXCompatibleId**</span><span class="sxs-lookup"><span data-stu-id="2a570-111">**PnPXCompatibleId**</span></span>](pnpxcompatibleid.md)<br/> | <span data-ttu-id="2a570-112">Especifica o identificador compatível com PnP-X do serviço.</span><span class="sxs-lookup"><span data-stu-id="2a570-112">Specifies the PnP-X Compatible Identifier of the service.</span></span><br/> <br/> |
| [<span data-ttu-id="2a570-113">**PnPXHardwareId**</span><span class="sxs-lookup"><span data-stu-id="2a570-113">**PnPXHardwareId**</span></span>](pnpxhardwareid.md)<br/>     | <span data-ttu-id="2a570-114">Especifica o identificador de hardware PnP-X do serviço.</span><span class="sxs-lookup"><span data-stu-id="2a570-114">Specifies the PnP-X Hardware Identifier of the service.</span></span><br/> <br/>   |
| [<span data-ttu-id="2a570-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="2a570-115">**ServiceID**</span></span>](serviceid.md)<br/>               | <span data-ttu-id="2a570-116">Define um identificador de serviço para o host de serviço.</span><span class="sxs-lookup"><span data-stu-id="2a570-116">Defines a service identifier for the service host.</span></span><br/> <br/>        |
| [<span data-ttu-id="2a570-117">**Tipos**</span><span class="sxs-lookup"><span data-stu-id="2a570-117">**Types**</span></span>](types.md)<br/>                       | <span data-ttu-id="2a570-118">Define uma lista de nomes qualificados XSD.</span><span class="sxs-lookup"><span data-stu-id="2a570-118">Defines a list of XSD qualified names.</span></span><br/> <br/>                    |



### <a name="child-element-sequence"></a><span data-ttu-id="2a570-119">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="2a570-119">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a><span data-ttu-id="2a570-120">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2a570-120">Parent elements</span></span>



| <span data-ttu-id="2a570-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="2a570-121">Element</span></span>                                         | <span data-ttu-id="2a570-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a570-122">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="2a570-123">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="2a570-123">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="2a570-124">Os metadados de hospedagem para o dispositivo a ser implementado.</span><span class="sxs-lookup"><span data-stu-id="2a570-124">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2a570-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a570-125">Remarks</span></span>

<span data-ttu-id="2a570-126">Cada serviço fornecido por um host de serviço deve ter suas próprias informações de elemento **hospedado** para garantir que o serviço seja publicado corretamente em respostas a solicitações de metadados.</span><span class="sxs-lookup"><span data-stu-id="2a570-126">Each service provided by a service host should have its own **hosted** element information to ensure that the service is published properly in responses to metadata requests.</span></span>

<span data-ttu-id="2a570-127">Os elementos [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) são opcionais, mas quando usados, eles devem ser usados juntos.</span><span class="sxs-lookup"><span data-stu-id="2a570-127">The [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements are optional, but when used, they must be used together.</span></span> <span data-ttu-id="2a570-128">Se um estiver presente, o outro também deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="2a570-128">If one is present, the other must be present as well.</span></span>

<span data-ttu-id="2a570-129">Se um elemento [**PnPXDeviceCategory**](pnpxdevicecategory.md) estiver presente, pelo menos um elemento **hospedado** deverá conter ambos os elementos [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="2a570-129">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one **hosted** element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="2a570-130">Da mesma forma, se os elementos **PnPXHardwareId** e **PnPXCompatibleId** estiverem presentes em um elemento **hospedado** , pelo menos um elemento **PnPXDeviceCategory** deverá estar presente dentro do elemento [**thisModelMetadata**](thismodelmetadata.md) .</span><span class="sxs-lookup"><span data-stu-id="2a570-130">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element must be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="2a570-131">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2a570-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="2a570-132">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a570-132">Minimum supported system</span></span><br/> | <span data-ttu-id="2a570-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a570-133">Windows Vista</span></span> |
| <span data-ttu-id="2a570-134">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="2a570-134">Can be empty</span></span>                        | <span data-ttu-id="2a570-135">Não</span><span class="sxs-lookup"><span data-stu-id="2a570-135">No</span></span>            |



 

 




