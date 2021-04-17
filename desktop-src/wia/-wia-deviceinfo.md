---
description: O objeto DeviceInfo fornece acesso às propriedades de um dispositivo de hardware de aquisição de imagem do Windows (WIA).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Objeto DeviceInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748303"
---
# <a name="deviceinfo-object"></a><span data-ttu-id="b54de-103">Objeto DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="b54de-103">DeviceInfo object</span></span>

<span data-ttu-id="b54de-104">O objeto **DeviceInfo** fornece acesso às propriedades de um dispositivo de hardware de aquisição de imagem do Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="b54de-104">The **DeviceInfo** object provides access to the properties of a Windows Image Acquisition (WIA) hardware device.</span></span> <span data-ttu-id="b54de-105">Ele também, por meio de seu método [**Create**](-wia-iwiadeviceinfo-create.md) , fornece uma maneira para o aplicativo ou script se conectar ao dispositivo e obter um objeto [**Item**](-wia-item.md) que representa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b54de-105">It also, through its [**Create**](-wia-iwiadeviceinfo-create.md) method, provides a way for the application or script to connect to the device and obtain an [**Item**](-wia-item.md) object that represents the device.</span></span> <span data-ttu-id="b54de-106">Use o método [**Devices**](-wia-iwia-devices.md) para obter uma coleção de objetos **DeviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="b54de-106">Use the [**Devices**](-wia-iwia-devices.md) method to obtain a collection of **DeviceInfo** objects.</span></span>

## <a name="members"></a><span data-ttu-id="b54de-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b54de-107">Members</span></span>

<span data-ttu-id="b54de-108">O objeto **DeviceInfo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b54de-108">The **DeviceInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="b54de-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="b54de-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="b54de-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b54de-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b54de-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b54de-111">Methods</span></span>

<span data-ttu-id="b54de-112">O objeto **DeviceInfo** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b54de-112">The **DeviceInfo** object has these methods.</span></span>



| <span data-ttu-id="b54de-113">Método</span><span class="sxs-lookup"><span data-stu-id="b54de-113">Method</span></span>                                                 | <span data-ttu-id="b54de-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b54de-114">Description</span></span>                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b54de-115">**Criada**</span><span class="sxs-lookup"><span data-stu-id="b54de-115">**Create**</span></span>](-wia-iwiadeviceinfo-create.md)           | <span data-ttu-id="b54de-116">O método [**Create**](-wia-iwiadeviceinfo-create.md) do objeto **DeviceInfo** faz uma conexão com o dispositivo WIA especificado pelo objeto **DeviceInfo** e retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b54de-116">The [**Create**](-wia-iwiadeviceinfo-create.md) method of the **DeviceInfo** object makes a connection to the WIA device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |
| [<span data-ttu-id="b54de-117">**GetPropById**</span><span class="sxs-lookup"><span data-stu-id="b54de-117">**GetPropById**</span></span>](-wia-iwiadeviceinfo-getpropbyid.md) | <span data-ttu-id="b54de-118">O método [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) do objeto **DEVICEINFO** usa a ID de uma propriedade de dispositivo para retornar seu valor.</span><span class="sxs-lookup"><span data-stu-id="b54de-118">The [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) method of the **DeviceInfo** object uses a device property's ID to return its value.</span></span><br/>                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="b54de-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b54de-119">Properties</span></span>

<span data-ttu-id="b54de-120">O objeto **DeviceInfo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b54de-120">The **DeviceInfo** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b54de-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b54de-121">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b54de-122">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="b54de-122">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b54de-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="b54de-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b54de-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Sessão</strong></a></span><span class="sxs-lookup"><span data-stu-id="b54de-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b54de-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b54de-125">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b54de-126">Recupera a ID do dispositivo de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="b54de-126">Retrieves the ID of the WIA hardware device.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b54de-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Manufacturer</strong></a></span><span class="sxs-lookup"><span data-stu-id="b54de-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Manufacturer</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b54de-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b54de-128">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b54de-129">Recupera o nome do fabricante deste dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="b54de-129">Retrieves the name of the manufacturer of this hardware device.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b54de-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Nome</strong></a></span><span class="sxs-lookup"><span data-stu-id="b54de-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b54de-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b54de-131">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b54de-132">O nome do dispositivo de hardware WIA como ele aparece na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b54de-132">The name of the WIA hardware device as it appears in the UI.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b54de-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Porta</strong></a></span><span class="sxs-lookup"><span data-stu-id="b54de-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b54de-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b54de-134">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b54de-135">Recupera a porta à qual o dispositivo de hardware WIA está conectado.</span><span class="sxs-lookup"><span data-stu-id="b54de-135">Retrieves the port to which the WIA hardware device is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b54de-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>Tipo</strong></a></span><span class="sxs-lookup"><span data-stu-id="b54de-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>Type</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b54de-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b54de-137">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b54de-138">Recupera o tipo de dispositivo de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="b54de-138">Retrieves the type of WIA hardware device.</span></span> <span data-ttu-id="b54de-139">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="b54de-139">Possible values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="b54de-140">DigitalCamera</span><span class="sxs-lookup"><span data-stu-id="b54de-140">DigitalCamera</span></span></li>
<li><span data-ttu-id="b54de-141">Scanner</span><span class="sxs-lookup"><span data-stu-id="b54de-141">Scanner</span></span></li>
<li><span data-ttu-id="b54de-142">StreamingVideo</span><span class="sxs-lookup"><span data-stu-id="b54de-142">StreamingVideo</span></span></li>
<li><span data-ttu-id="b54de-143">Padrão</span><span class="sxs-lookup"><span data-stu-id="b54de-143">Default</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b54de-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a></span><span class="sxs-lookup"><span data-stu-id="b54de-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b54de-145">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b54de-145">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b54de-146">Recupera a ID de classe da interface do usuário fornecida pelo fabricante para este dispositivo de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="b54de-146">Retrieves the class id of the manufacturer-provided user interface for this WIA hardware device.</span></span> <span data-ttu-id="b54de-147">O valor é uma representação de cadeia de caracteres de um GUID.</span><span class="sxs-lookup"><span data-stu-id="b54de-147">The value is a string representation of a GUID.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b54de-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b54de-148">Requirements</span></span>



| <span data-ttu-id="b54de-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="b54de-149">Requirement</span></span> | <span data-ttu-id="b54de-150">Valor</span><span class="sxs-lookup"><span data-stu-id="b54de-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b54de-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b54de-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b54de-152">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b54de-152">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b54de-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b54de-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b54de-154">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b54de-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b54de-155">DLL</span><span class="sxs-lookup"><span data-stu-id="b54de-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b54de-156"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b54de-156"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




