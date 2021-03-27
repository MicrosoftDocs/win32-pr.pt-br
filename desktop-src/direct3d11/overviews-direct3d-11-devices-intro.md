---
title: Introdução a um dispositivo no Direct3D 11
description: O modelo de objeto do Direct3D 11 separa a funcionalidade de criação e renderização de recursos em um dispositivo e em um ou mais contextos; Essa separação foi projetada para facilitar o multithreading.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b03333c6594f17d85fee28880e46928241e06c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104967025"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a><span data-ttu-id="8ff5b-103">Introdução a um dispositivo no Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="8ff5b-103">Introduction to a Device in Direct3D 11</span></span>

<span data-ttu-id="8ff5b-104">O modelo de objeto do Direct3D 11 separa a funcionalidade de criação e renderização de recursos em um dispositivo e em um ou mais contextos; Essa separação foi projetada para facilitar o multithreading.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-104">The Direct3D 11 object model separates resource creation and rendering functionality into a device and one or more contexts; this separation is designed to facilitate multithreading.</span></span>

-   [<span data-ttu-id="8ff5b-105">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="8ff5b-105">Device</span></span>](#introduction-to-a-device-in-direct3d-11)
-   [<span data-ttu-id="8ff5b-106">Contexto do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8ff5b-106">Device Context</span></span>](#device-context)
    -   [<span data-ttu-id="8ff5b-107">Contexto imediato</span><span class="sxs-lookup"><span data-stu-id="8ff5b-107">Immediate Context</span></span>](#immediate-context)
    -   [<span data-ttu-id="8ff5b-108">Contexto adiado</span><span class="sxs-lookup"><span data-stu-id="8ff5b-108">Deferred Context</span></span>](#deferred-context)
-   [<span data-ttu-id="8ff5b-109">Considerações de thread</span><span class="sxs-lookup"><span data-stu-id="8ff5b-109">Threading Considerations</span></span>](#threading-considerations)
-   [<span data-ttu-id="8ff5b-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ff5b-110">Related topics</span></span>](#related-topics)

## <a name="device"></a><span data-ttu-id="8ff5b-111">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="8ff5b-111">Device</span></span>

<span data-ttu-id="8ff5b-112">Um dispositivo é usado para criar recursos e para enumerar os recursos de um adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-112">A device is used to create resources and to enumerate the capabilities of a display adapter.</span></span> <span data-ttu-id="8ff5b-113">No Direct3D 11, um dispositivo é representado por uma interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="8ff5b-113">In Direct3D 11, a device is represented with an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface.</span></span>

<span data-ttu-id="8ff5b-114">Cada aplicativo deve ter pelo menos um dispositivo; a maioria dos aplicativos só cria um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-114">Each application must have at least one device, most applications only create one device.</span></span> <span data-ttu-id="8ff5b-115">Crie um dispositivo para um dos drivers de hardware instalados em seu computador chamando [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) e especifique o tipo de driver com o sinalizador de [**\_ \_ tipo de driver do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="8ff5b-115">Create a device for one of the hardware drivers installed on your machine by calling [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and specify the driver type with the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) flag.</span></span> <span data-ttu-id="8ff5b-116">Cada dispositivo pode usar um ou mais contextos de dispositivo, dependendo da funcionalidade desejada.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-116">Each device can use one or more device contexts, depending on the functionality desired.</span></span>

## <a name="device-context"></a><span data-ttu-id="8ff5b-117">Contexto do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8ff5b-117">Device Context</span></span>

<span data-ttu-id="8ff5b-118">Um contexto de dispositivo contém a circunstância ou a configuração em que um dispositivo é usado.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-118">A device context contains the circumstance or setting in which a device is used.</span></span> <span data-ttu-id="8ff5b-119">Mais especificamente, um contexto de dispositivo é usado para definir o estado do pipeline e gerar comandos de renderização usando os recursos de propriedade de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-119">More specifically, a device context is used to set pipeline state and generate rendering commands using the resources owned by a device.</span></span> <span data-ttu-id="8ff5b-120">O Direct3D 11 implementa dois tipos de contextos de dispositivo, um para renderização imediata e outro para renderização adiada; ambos os contextos são representados com uma interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="8ff5b-120">Direct3D 11 implements two types of device contexts, one for immediate rendering and the other for deferred rendering; both contexts are represented with an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span>

### <a name="immediate-context"></a><span data-ttu-id="8ff5b-121">Contexto imediato</span><span class="sxs-lookup"><span data-stu-id="8ff5b-121">Immediate Context</span></span>

<span data-ttu-id="8ff5b-122">Um contexto imediato é renderizado diretamente para o driver.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-122">An immediate context renders directly to the driver.</span></span> <span data-ttu-id="8ff5b-123">Cada dispositivo tem um e apenas um contexto imediato que pode recuperar dados da GPU.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-123">Each device has one and only one immediate context which can retrieve data from the GPU.</span></span> <span data-ttu-id="8ff5b-124">Um contexto imediato pode ser usado para renderizar imediatamente (ou reproduzir) uma [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="8ff5b-124">An immediate context can be used to immediately render (or play back) a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span>

<span data-ttu-id="8ff5b-125">Há duas maneiras de obter um contexto imediato:</span><span class="sxs-lookup"><span data-stu-id="8ff5b-125">There are two ways to get an immediate context:</span></span>

-   <span data-ttu-id="8ff5b-126">Chamando [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="8ff5b-126">By calling either [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>
-   <span data-ttu-id="8ff5b-127">Chamando [**ID3D11Device:: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span><span class="sxs-lookup"><span data-stu-id="8ff5b-127">By calling [**ID3D11Device::GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span></span>

### <a name="deferred-context"></a><span data-ttu-id="8ff5b-128">Contexto adiado</span><span class="sxs-lookup"><span data-stu-id="8ff5b-128">Deferred Context</span></span>

<span data-ttu-id="8ff5b-129">Um contexto adiado registra comandos de GPU em uma [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="8ff5b-129">A deferred context records GPU commands into a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="8ff5b-130">Um contexto adiado é usado principalmente para multithreading e não é necessário para um aplicativo de thread único.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-130">A deferred context is primarily used for multithreading and is not necessary for a single-threaded application.</span></span> <span data-ttu-id="8ff5b-131">Um contexto adiado geralmente é usado por um thread de trabalho em vez do thread de renderização principal.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-131">A deferred context is generally used by a worker thread instead of the main rendering thread.</span></span> <span data-ttu-id="8ff5b-132">Quando você cria um contexto adiado, ele não herda nenhum estado do contexto imediato.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-132">When you create a deferred context, it does not inherit any state from the immediate context.</span></span>

<span data-ttu-id="8ff5b-133">Para obter um contexto adiado, chame [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span><span class="sxs-lookup"><span data-stu-id="8ff5b-133">To get a deferred context, call [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

<span data-ttu-id="8ff5b-134">Qualquer contexto--immediate ou adiado--pode ser usado em qualquer thread, desde que o contexto seja usado apenas em um thread por vez.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-134">Any context -- immediate or deferred -- can be used on any thread as long as the context is only used in one thread at a time.</span></span>

## <a name="threading-considerations"></a><span data-ttu-id="8ff5b-135">Considerações de thread</span><span class="sxs-lookup"><span data-stu-id="8ff5b-135">Threading Considerations</span></span>

<span data-ttu-id="8ff5b-136">Esta tabela destaca as diferenças no modelo de threading no Direct3D 11 de versões anteriores do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-136">This table highlights the differences in the threading model in Direct3D 11 from prior versions of Direct3D.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ff5b-137">Diferenças entre o Direct3D 11 e versões anteriores do Direct3D:</span><span class="sxs-lookup"><span data-stu-id="8ff5b-137">Differences between Direct3D 11 and previous versions of Direct3D:</span></span><br/> <span data-ttu-id="8ff5b-138">Todos os métodos de interface <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> são de thread livre, o que significa que é seguro ter vários threads chamando as funções ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-138">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> interface methods are free-threaded, which means it is safe to have multiple threads call the functions at the same time.</span></span><br/>
<ul>
<li><span data-ttu-id="8ff5b-139">Todas as interfaces derivadas de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>(<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) são de thread livre.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-139">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>-derived interfaces (<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) are free-threaded.</span></span></li>
<li><span data-ttu-id="8ff5b-140">O Direct3D 11 divide a criação e a renderização de recursos em duas interfaces.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-140">Direct3D 11 splits resource creating and rendering into two interfaces.</span></span> <span data-ttu-id="8ff5b-141">MAP, remapear, Begin, end e GetData são implementados em <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> porque <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> define fortemente a ordem das operações.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-141">Map, Unmap, Begin, End, and GetData are implemented on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> because <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> strongly defines the order of operations.</span></span> <span data-ttu-id="8ff5b-142">As interfaces <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> e <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> também implementam métodos para operações de thread livre.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-142"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> and <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> interfaces also implement methods for free-threaded operations.</span></span></li>
<li><span data-ttu-id="8ff5b-143">Os métodos <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> (exceto aqueles que existem em <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) não são de thread livre, ou seja, eles exigem um único Threading.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-143">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> methods (except for those that exist on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) are not free-threaded, that is, they require single threading.</span></span> <span data-ttu-id="8ff5b-144">Somente um thread pode chamar com segurança qualquer um de seus métodos (Draw, copiar, mapear, etc.) de cada vez.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-144">Only one thread may safely be calling any of its methods (Draw, Copy, Map, etc.) at a time.</span></span></li>
<li><span data-ttu-id="8ff5b-145">Em geral, o Threading livre minimiza o número de primitivos de sincronização usados, bem como sua duração.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-145">In general, free-threading minimizes the number of synchronization primitives used as well as their duration.</span></span> <span data-ttu-id="8ff5b-146">No entanto, um aplicativo que usa a sincronização mantida por um longo tempo pode impactar diretamente a quantidade de simultaneidade que um aplicativo pode esperar alcançar.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-146">However, an application that uses synchronization held for a long time can directly impact how much concurrency an application can expect to achieve.</span></span></li>
</ul>
<span data-ttu-id="8ff5b-147">Os métodos de interface ID3D10Device não são projetados para serem de thread livre.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-147">ID3D10Device interface methods are not designed to be free-threaded.</span></span> <span data-ttu-id="8ff5b-148">ID3D10Device implementa toda a funcionalidade de criação e renderização (como o ID3D9Device no Direct3D 9).</span><span class="sxs-lookup"><span data-stu-id="8ff5b-148">ID3D10Device implements all create and rendering functionality (as does ID3D9Device in Direct3D 9).</span></span> <span data-ttu-id="8ff5b-149">Mapear e desmapear são implementados em interfaces derivadas de ID3D10Resource, Begin, end e GetData são implementados em interfaces derivadas de ID3D10Asynchronous.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-149">Map and Unmap are implemented on ID3D10Resource-derived interfaces, Begin, End, and GetData are implemented on ID3D10Asynchronous-derived interfaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8ff5b-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ff5b-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ff5b-151">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="8ff5b-151">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





