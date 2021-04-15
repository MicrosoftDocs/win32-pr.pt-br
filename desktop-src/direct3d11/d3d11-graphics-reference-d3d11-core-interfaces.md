---
title: Interfaces principais do Direct3D 11
description: Esta seção contém informações sobre as interfaces principais.
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- interfaces, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c578d84a7a9f223cb81285b69f5b5d1baed4e6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104454417"
---
# <a name="direct3d-11-core-interfaces"></a><span data-ttu-id="e2ea8-104">Interfaces principais do Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e2ea8-104">Direct3D 11 core interfaces</span></span>

<span data-ttu-id="e2ea8-105">Esta seção contém informações sobre as interfaces principais.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-105">This section contains information about the core interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e2ea8-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e2ea8-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e2ea8-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="e2ea8-107">Topic</span></span></th>
<th><span data-ttu-id="e2ea8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2ea8-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e2ea8-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-110">Essa interface encapsula métodos para recuperar dados da GPU de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-110">This interface encapsulates methods for retrieving data from the GPU asynchronously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-112">A interface de estado de mesclagem contém uma descrição para o estado de mesclagem que você pode associar ao <a href="d3d10-graphics-programming-guide-output-merger-stage.md">estágio de mesclagem de saída</a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-112">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-114">A interface de estado de mesclagem contém uma descrição para o estado de mesclagem que você pode associar ao <a href="d3d10-graphics-programming-guide-output-merger-stage.md">estágio de mesclagem de saída</a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-114">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span> <span data-ttu-id="e2ea8-115">Essa interface de estado de mesclagem dá suporte a operações lógicas, bem como operações de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-115">This blend-state interface supports logical operations as well as blending operations.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-117">A interface <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> encapsula uma lista de comandos gráficos para reproduzir.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-117">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> interface encapsulates a list of graphics commands for play back.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-119">Essa interface encapsula métodos para medir o desempenho da GPU.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-119">This interface encapsulates methods for measuring GPU performance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-121">A interface de estado de estêncil de profundidade contém uma descrição para o estado de estêncil de profundidade que você pode associar ao <a href="d3d10-graphics-programming-guide-output-merger-stage.md">estágio de mesclagem de saída</a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-121">The depth-stencil-state interface holds a description for depth-stencil state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-123">A interface do dispositivo representa um adaptador virtual; Ele é usado para criar recursos.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-123">The device interface represents a virtual adapter; it is used to create resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-125">A interface do dispositivo representa um adaptador virtual; Ele é usado para criar recursos.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-125">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="e2ea8-126">O <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-128">A interface do dispositivo representa um adaptador virtual; Ele é usado para criar recursos.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-128">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="e2ea8-129">O <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-131">A interface do dispositivo representa um adaptador virtual; Ele é usado para criar recursos.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-131">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="e2ea8-132">O <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-134">A interface do dispositivo representa um adaptador virtual; Ele é usado para criar recursos.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-134">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="e2ea8-135">O <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, como <strong>RegisterDeviceRemovedEvent</strong> e <strong>UnregisterDeviceRemoved</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, such as <strong>RegisterDeviceRemovedEvent</strong> and <strong>UnregisterDeviceRemoved</strong>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-137">A interface do dispositivo representa um adaptador virtual; Ele é usado para criar recursos.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-137">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="e2ea8-138">O <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-140">Uma interface de dispositivo-filho acessa dados usados por um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-140">A device-child interface accesses data used by a device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-142">A interface <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> representa um contexto de dispositivo que gera comandos de renderização.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-142">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> interface represents a device context which generates rendering commands.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e2ea8-143">A versão mais recente dessa interface é <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introduzida na atualização do Windows 10 para criadores.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-143">The latest version of this interface is <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introduced in the Windows 10 Creators Update.</span></span> <span data-ttu-id="e2ea8-144">Aplicativos voltados atualização do Windows 10 para criadores deve usar a interface <strong>ID3D11DeviceContext4</strong> em vez de <strong>ID3D11Device</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-144">Applications targetting Windows 10 Creators Update should use the <strong>ID3D11DeviceContext4</strong> interface instead of <strong>ID3D11Device</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-146">A interface de contexto do dispositivo representa um contexto de dispositivo; Ele é usado para renderizar comandos.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-146">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="e2ea8-147">O <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-149">A interface de contexto do dispositivo representa um contexto de dispositivo; Ele é usado para renderizar comandos.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-149">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="e2ea8-150">O <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-152">A interface de contexto do dispositivo representa um contexto de dispositivo; Ele é usado para renderizar comandos.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-152">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="e2ea8-153">O <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-155">A interface de contexto do dispositivo representa um contexto de dispositivo; Ele é usado para renderizar comandos.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-155">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="e2ea8-156">O <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-158">A interface <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> representa um objeto de estado de contexto, que contém informações de estado e comportamento sobre um dispositivo Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-158">The <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> interface represents a context state object, which holds state and behavior information about a Microsoft Direct3D device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-160">Representa um limite, um objeto usado para sincronização da CPU e uma ou mais GPUs.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-160">Represents a fence, an object used for synchronization of the CPU and one or more GPUs.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-162">Uma interface de layout de entrada contém uma definição de como alimentar dados de vértice que são dispostos na memória no <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">estágio de Assembler de entrada</a> do <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline de gráficos</a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-162">An input-layout interface holds a definition of how to feed vertex data that is laid out in memory into the <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">input-assembler stage</a> of the <a href="overviews-direct3d-11-graphics-pipeline.md">graphics pipeline</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-164">Fornece proteção de threading para seções críticas de um aplicativo multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-164">Provides threading protection for critical sections of a multi-threaded application.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-166">Uma interface de predicado determina se a geometria deve ser processada dependendo dos resultados de uma chamada de desenho anterior.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-166">A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-168">Uma interface de consulta consulta informações da GPU.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-168">A query interface queries information from the GPU.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-170">Representa um objeto de consulta para consultar informações da GPU (unidade de processamento gráfico).</span><span class="sxs-lookup"><span data-stu-id="e2ea8-170">Represents a query object for querying information from the graphics processing unit (GPU).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-172">A interface de estado do rasterizador contém uma descrição para o estado do rasterizador que você pode associar ao <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">estágio do rasterizador</a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-172">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-174">A interface de estado do rasterizador contém uma descrição para o estado do rasterizador que você pode associar ao <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">estágio do rasterizador</a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-174">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="e2ea8-175">Essa interface de estado do rasterizador dá suporte à contagem de amostra forçada.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-175">This rasterizer-state interface supports forced sample count.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ea8-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-177">A interface de estado do rasterizador contém uma descrição para o estado do rasterizador que você pode associar ao <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">estágio do rasterizador</a>.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-177">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="e2ea8-178">Essa interface de estado do rasterizador dá suporte à contagem de amostras forçada e ao modo de rasterização conservador.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-178">This rasterizer-state interface supports forced sample count and conservative rasterization mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2ea8-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2ea8-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2ea8-180">A interface de estado de amostra contém uma descrição para o estado de amostra que você pode associar a qualquer estágio de sombreador do <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> para referência por operações de exemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="e2ea8-180">The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> for reference by texture sample operations.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e2ea8-181">O Direct3D 11 implementa interfaces para:</span><span class="sxs-lookup"><span data-stu-id="e2ea8-181">Direct3D 11 implements interfaces for:</span></span>

-   [<span data-ttu-id="e2ea8-182">Recursos</span><span class="sxs-lookup"><span data-stu-id="e2ea8-182">Resources</span></span>](d3d11-graphics-reference-resource-interfaces.md)
-   [<span data-ttu-id="e2ea8-183">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="e2ea8-183">Shaders</span></span>](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="e2ea8-184">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2ea8-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2ea8-185">Referência principal</span><span class="sxs-lookup"><span data-stu-id="e2ea8-185">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>

