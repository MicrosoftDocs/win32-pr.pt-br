---
description: O objeto WIA é o ponto de entrada para toda a funcionalidade de script da aquisição de imagem do Windows (WIA).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: Objeto WIA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090486"
---
# <a name="wia-object"></a><span data-ttu-id="fe8d1-103">Objeto WIA</span><span class="sxs-lookup"><span data-stu-id="fe8d1-103">Wia object</span></span>

<span data-ttu-id="fe8d1-104">O objeto **WIA** é o ponto de entrada para toda a funcionalidade de script da aquisição de imagem do Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="fe8d1-104">The **Wia** object is the entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="fe8d1-105">Qualquer aplicativo que usa o modelo de script WIA deve criar um objeto [**SafeWia**](-wia-safewia.md) ou **WIA** .</span><span class="sxs-lookup"><span data-stu-id="fe8d1-105">Any application that uses the WIA scripting model must create a [**SafeWia**](-wia-safewia.md) or **Wia** object.</span></span> <span data-ttu-id="fe8d1-106">Use esse objeto para enumerar e criar dispositivos e para receber notificações de eventos de hardware.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

> [!Note]  
> <span data-ttu-id="fe8d1-107">Este objeto não é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-107">This object is not safe for scripting.</span></span> <span data-ttu-id="fe8d1-108">Para obter uma versão desse objeto que seja segura para scripts, consulte [**SafeWia**](-wia-safewia.md).</span><span class="sxs-lookup"><span data-stu-id="fe8d1-108">For a version of this object that is safe for scripting, see [**SafeWia**](-wia-safewia.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="fe8d1-109">Membros</span><span class="sxs-lookup"><span data-stu-id="fe8d1-109">Members</span></span>

<span data-ttu-id="fe8d1-110">O objeto **WIA** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fe8d1-110">The **Wia** object has these types of members:</span></span>

-   [<span data-ttu-id="fe8d1-111">Eventos</span><span class="sxs-lookup"><span data-stu-id="fe8d1-111">Events</span></span>](#events)
-   [<span data-ttu-id="fe8d1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe8d1-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="fe8d1-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fe8d1-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="fe8d1-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="fe8d1-114">Events</span></span>

<span data-ttu-id="fe8d1-115">O objeto **WIA** tem esses eventos.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-115">The **Wia** object has these events.</span></span>



| <span data-ttu-id="fe8d1-116">Evento</span><span class="sxs-lookup"><span data-stu-id="fe8d1-116">Event</span></span>                                                                 | <span data-ttu-id="fe8d1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe8d1-117">Description</span></span>                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="fe8d1-118">**OnDeviceConnected**</span><span class="sxs-lookup"><span data-stu-id="fe8d1-118">**OnDeviceConnected**</span></span>](-wia--iwiaevents-ondeviceconnected.md)       | <span data-ttu-id="fe8d1-119">Evento que ocorre quando um novo dispositivo de hardware WIA é conectado.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-119">Event that occurs when a new WIA hardware device is connected.</span></span><br/>    |
| [<span data-ttu-id="fe8d1-120">**OnDeviceDisconnected**</span><span class="sxs-lookup"><span data-stu-id="fe8d1-120">**OnDeviceDisconnected**</span></span>](-wia--iwiaevents-ondevicedisconnected.md) | <span data-ttu-id="fe8d1-121">Evento que ocorre quando um novo dispositivo de hardware WIA é desconectado.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-121">Event that occurs when a new WIA hardware device is disconnected.</span></span><br/> |
| [<span data-ttu-id="fe8d1-122">**OnTransferComplete**</span><span class="sxs-lookup"><span data-stu-id="fe8d1-122">**OnTransferComplete**</span></span>](-wia--iwiaevents-ontransfercomplete.md)     | <span data-ttu-id="fe8d1-123">Evento que ocorre quando uma transferência de dados é concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-123">Event that occurs when a data transfer is completed successfully.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="fe8d1-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe8d1-124">Methods</span></span>

<span data-ttu-id="fe8d1-125">O objeto **WIA** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-125">The **Wia** object has these methods.</span></span>



| <span data-ttu-id="fe8d1-126">Método</span><span class="sxs-lookup"><span data-stu-id="fe8d1-126">Method</span></span>                             | <span data-ttu-id="fe8d1-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe8d1-127">Description</span></span>                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe8d1-128">**Criada**</span><span class="sxs-lookup"><span data-stu-id="fe8d1-128">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="fe8d1-129">O método [**Create**](-wia-iwia-create.md) do objeto **WIA** faz uma conexão com o dispositivo WIA especificado e retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-129">The [**Create**](-wia-iwia-create.md) method of the **Wia** object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fe8d1-130">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fe8d1-130">Properties</span></span>

<span data-ttu-id="fe8d1-131">O objeto **WIA** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-131">The **Wia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="fe8d1-132">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fe8d1-132">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="fe8d1-133">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="fe8d1-133">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="fe8d1-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe8d1-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="fe8d1-135"><a href="-wia-iwia-devices.md"><strong>Dispositivos</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe8d1-135"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="fe8d1-136">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe8d1-136">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="fe8d1-137">Coleção de objetos <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> que representa todos os dispositivos instalados no computador.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-137">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="fe8d1-138">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-138">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fe8d1-139">Esta coleção é baseada em 0.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-139">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="fe8d1-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe8d1-140">Requirements</span></span>



| <span data-ttu-id="fe8d1-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe8d1-141">Requirement</span></span> | <span data-ttu-id="fe8d1-142">Valor</span><span class="sxs-lookup"><span data-stu-id="fe8d1-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8d1-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe8d1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="fe8d1-144">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fe8d1-144">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe8d1-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe8d1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="fe8d1-146">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe8d1-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fe8d1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="fe8d1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe8d1-148"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="fe8d1-148"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="fe8d1-149">IID</span><span class="sxs-lookup"><span data-stu-id="fe8d1-149">IID</span></span><br/>                      | <span data-ttu-id="fe8d1-150">CLSID \_ WIA</span><span class="sxs-lookup"><span data-stu-id="fe8d1-150">CLSID\_Wia</span></span><br/>                                                                                         |



 

 




