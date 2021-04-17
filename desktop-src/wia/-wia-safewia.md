---
description: O objeto SafeWia é um &\# 0034; seguro para scripts&\# 0034; ponto de entrada para a funcionalidade de script da aquisição de imagem do Windows (WIA).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Objeto SafeWia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812013"
---
# <a name="safewia-object"></a><span data-ttu-id="619c1-103">Objeto SafeWia</span><span class="sxs-lookup"><span data-stu-id="619c1-103">SafeWia object</span></span>

<span data-ttu-id="619c1-104">O objeto **SafeWia** é um ponto de entrada "seguro para scripts" para toda a funcionalidade de script da aquisição de imagem do Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="619c1-104">The **SafeWia** object is a "safe for scripting" entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="619c1-105">Qualquer aplicativo que usa o modelo de script WIA deve criar um objeto **SafeWia** ou [**WIA**](-wia-wia.md) .</span><span class="sxs-lookup"><span data-stu-id="619c1-105">Any application that uses the WIA scripting model must create a **SafeWia** or [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="619c1-106">Use esse objeto para enumerar e criar dispositivos e para receber notificações de eventos de hardware.</span><span class="sxs-lookup"><span data-stu-id="619c1-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

## <a name="members"></a><span data-ttu-id="619c1-107">Membros</span><span class="sxs-lookup"><span data-stu-id="619c1-107">Members</span></span>

<span data-ttu-id="619c1-108">O objeto **SafeWia** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="619c1-108">The **SafeWia** object has these types of members:</span></span>

-   [<span data-ttu-id="619c1-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="619c1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="619c1-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="619c1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="619c1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="619c1-111">Methods</span></span>

<span data-ttu-id="619c1-112">O objeto **SafeWia** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="619c1-112">The **SafeWia** object has these methods.</span></span>



| <span data-ttu-id="619c1-113">Método</span><span class="sxs-lookup"><span data-stu-id="619c1-113">Method</span></span>                             | <span data-ttu-id="619c1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="619c1-114">Description</span></span>                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="619c1-115">**Criada**</span><span class="sxs-lookup"><span data-stu-id="619c1-115">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="619c1-116">O método [**Create**](-wia-iwia-create.md) do objeto [**WIA**](-wia-wia.md) faz uma conexão com o dispositivo WIA especificado e retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="619c1-116">The [**Create**](-wia-iwia-create.md) method of the [**Wia**](-wia-wia.md) object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="619c1-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="619c1-117">Properties</span></span>

<span data-ttu-id="619c1-118">O objeto **SafeWia** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="619c1-118">The **SafeWia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="619c1-119">Propriedade</span><span class="sxs-lookup"><span data-stu-id="619c1-119">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="619c1-120">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="619c1-120">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="619c1-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="619c1-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="619c1-122"><a href="-wia-iwia-devices.md"><strong>Dispositivos</strong></a></span><span class="sxs-lookup"><span data-stu-id="619c1-122"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="619c1-123">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="619c1-123">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="619c1-124">Coleção de objetos <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> que representa todos os dispositivos instalados no computador.</span><span class="sxs-lookup"><span data-stu-id="619c1-124">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="619c1-125">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="619c1-125">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="619c1-126">Esta coleção é baseada em 0.</span><span class="sxs-lookup"><span data-stu-id="619c1-126">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="619c1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="619c1-127">Requirements</span></span>



| <span data-ttu-id="619c1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="619c1-128">Requirement</span></span> | <span data-ttu-id="619c1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="619c1-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="619c1-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="619c1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="619c1-131">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="619c1-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="619c1-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="619c1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="619c1-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="619c1-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="619c1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="619c1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="619c1-135"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="619c1-135"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="619c1-136">IID</span><span class="sxs-lookup"><span data-stu-id="619c1-136">IID</span></span><br/>                      | <span data-ttu-id="619c1-137">\_SAFEWIA CLSID</span><span class="sxs-lookup"><span data-stu-id="619c1-137">CLSID\_SafeWia</span></span><br/>                                                                                     |



## <a name="see-also"></a><span data-ttu-id="619c1-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="619c1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="619c1-139">**WIA**</span><span class="sxs-lookup"><span data-stu-id="619c1-139">**Wia**</span></span>](-wia-wia.md)
</dt> </dl>

 

 




