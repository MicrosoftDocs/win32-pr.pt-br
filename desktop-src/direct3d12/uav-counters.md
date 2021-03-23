---
title: Contadores de UAV
description: Você pode usar os contadores UAV (unordened-Access-View) para associar um contador atômico de 32 bits a um UAV (não ordenado-Access-View).
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104548241"
---
# <a name="uav-counters"></a><span data-ttu-id="197fd-103">Contadores de UAV</span><span class="sxs-lookup"><span data-stu-id="197fd-103">UAV Counters</span></span>
<span data-ttu-id="197fd-104">Você pode usar os contadores UAV (unordened-Access-View) para associar um contador atômico de 32 bits a um UAV (não ordenado-Access-View).</span><span class="sxs-lookup"><span data-stu-id="197fd-104">You can use unordered-access-view (UAV) counters to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span>

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="197fd-105">Diferenças nos contadores de UAV do Direct3D 11 para o Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="197fd-105">Differences in UAV counters from Direct3D 11 to Direct3D 12</span></span>
<span data-ttu-id="197fd-106">Aplicativos Direct3D 12 e Direct3D 11 usam as mesmas funções de sombreador HLSL (linguagem de sombreamento de alto nível) para acessar os contadores UAV.</span><span class="sxs-lookup"><span data-stu-id="197fd-106">Direct3D 12 apps and Direct3D 11 apps both use the same high-level shader language (HLSL) shader functions to access the UAV counters.</span></span>

-   <span data-ttu-id="197fd-107">**IncrementCounter**</span><span class="sxs-lookup"><span data-stu-id="197fd-107">**IncrementCounter**</span></span>
-   <span data-ttu-id="197fd-108">**DecrementCounter**</span><span class="sxs-lookup"><span data-stu-id="197fd-108">**DecrementCounter**</span></span>
-   <span data-ttu-id="197fd-109">**Append**</span><span class="sxs-lookup"><span data-stu-id="197fd-109">**Append**</span></span>
-   <span data-ttu-id="197fd-110">**Consumir**</span><span class="sxs-lookup"><span data-stu-id="197fd-110">**Consume**</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="197fd-111">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="197fd-111">Direct3D 12</span></span>
<span data-ttu-id="197fd-112">No Direct3D 12, os valores de 32 bits são alocados pelo aplicativo, de modo que os valores de 32 bits podem ser lidos e gravados pela CPU ou pela GPU, assim como qualquer outro recurso do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="197fd-112">In Direct3D 12, the 32-bit values are allocated by the application, so the 32-bit values can be read and written by either the CPU or the GPU, just like any other Direct3D 12 resource.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="197fd-113">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="197fd-113">Direct3D 11</span></span>
<span data-ttu-id="197fd-114">Fora dos sombreadores, com o Direct3D 11, você precisa chamar métodos de API para acessar os contadores (por exemplo, [ID3D11DeviceContext:: CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span><span class="sxs-lookup"><span data-stu-id="197fd-114">Outside of the shaders, with Direct3D 11 you need to call API methods in order to access the counters (for example, [ID3D11DeviceContext::CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span></span>

## <a name="using-uav-counters"></a><span data-ttu-id="197fd-115">Usando contadores do UAV</span><span class="sxs-lookup"><span data-stu-id="197fd-115">Using UAV counters</span></span>
<span data-ttu-id="197fd-116">Seu aplicativo é responsável por alocar 32 bits de armazenamento para contadores de UAV.</span><span class="sxs-lookup"><span data-stu-id="197fd-116">Your app is responsible for allocating 32-bits of storage for UAV counters.</span></span> <span data-ttu-id="197fd-117">Esse armazenamento pode ser alocado em um recurso diferente como aquele que contém os dados acessíveis por meio do UAV.</span><span class="sxs-lookup"><span data-stu-id="197fd-117">This storage can be allocated in a different resource as the one that contains data accessible via the UAV.</span></span>

<span data-ttu-id="197fd-118">Consulte [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12 \_ buffer \_ UAV \_ flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) e [**D3D12 \_ buffer \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span><span class="sxs-lookup"><span data-stu-id="197fd-118">Refer to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12\_BUFFER\_UAV\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) and [**D3D12\_BUFFER\_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span></span>

<span data-ttu-id="197fd-119">Se *pCounterResource* for especificado na chamada para [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), haverá um contador associado ao UAV.</span><span class="sxs-lookup"><span data-stu-id="197fd-119">If *pCounterResource* is specified in the call to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), then there is a counter associated with the UAV.</span></span> <span data-ttu-id="197fd-120">Nesse caso:</span><span class="sxs-lookup"><span data-stu-id="197fd-120">In this case:</span></span>

-   <span data-ttu-id="197fd-121">*StructureByteStride* deve ser maior que zero</span><span class="sxs-lookup"><span data-stu-id="197fd-121">*StructureByteStride* must be greater than zero</span></span>
-   <span data-ttu-id="197fd-122">O formato deve ser um \_ formato dxgi \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="197fd-122">Format must be DXGI\_FORMAT\_UNKNOWN</span></span>
-   <span data-ttu-id="197fd-123">O sinalizador bruto não deve ser definido</span><span class="sxs-lookup"><span data-stu-id="197fd-123">The RAW flag must not be set</span></span>
-   <span data-ttu-id="197fd-124">Ambos os recursos devem ser buffers</span><span class="sxs-lookup"><span data-stu-id="197fd-124">Both of the resources must be buffers</span></span>
-   <span data-ttu-id="197fd-125">*CounterOffsetInBytes* deve ser um múltiplo de 4 bytes</span><span class="sxs-lookup"><span data-stu-id="197fd-125">*CounterOffsetInBytes* must be a multiple of 4 bytes</span></span>
-   <span data-ttu-id="197fd-126">*CounterOffsetInBytes* deve estar dentro do intervalo do recurso do contador</span><span class="sxs-lookup"><span data-stu-id="197fd-126">*CounterOffsetInBytes* must be within the range of the counter resource</span></span>
-   <span data-ttu-id="197fd-127">*pDesc* não pode ser nulo</span><span class="sxs-lookup"><span data-stu-id="197fd-127">*pDesc* cannot be NULL</span></span>
-   <span data-ttu-id="197fd-128">a *origem* não pode ser nula</span><span class="sxs-lookup"><span data-stu-id="197fd-128">*pResource* cannot be NULL</span></span>

<span data-ttu-id="197fd-129">E observe os seguintes casos de uso:</span><span class="sxs-lookup"><span data-stu-id="197fd-129">And note the following use cases:</span></span>

-   <span data-ttu-id="197fd-130">Se *pCounterResource* não for especificado, *CounterOffsetInBytes* deverá ser 0.</span><span class="sxs-lookup"><span data-stu-id="197fd-130">If *pCounterResource* is not specified, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="197fd-131">Se o sinalizador bruto estiver definido, o formato deverá ser sem \_ tipo de formato dxgi \_ R32 \_ e o recurso UAV deverá ser um buffer.</span><span class="sxs-lookup"><span data-stu-id="197fd-131">If the RAW flag is set then the format must be DXGI\_FORMAT\_R32\_TYPELESS and the UAV resource must be a buffer.</span></span>
-   <span data-ttu-id="197fd-132">Se *pCounterResource* não for definido, *CounterOffsetInBytes* deverá ser 0.</span><span class="sxs-lookup"><span data-stu-id="197fd-132">If *pCounterResource* is not set, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="197fd-133">Se o sinalizador bruto não for definido e *StructureByteStride* = 0, o formato deverá ser um formato UAV válido.</span><span class="sxs-lookup"><span data-stu-id="197fd-133">If the RAW flag is not set and *StructureByteStride* = 0, then the format must be a valid UAV format.</span></span>

<span data-ttu-id="197fd-134">O Direct3D 12 remove a distinção entre Append e Counter UAVs (embora a distinção ainda exista no código de bytes HLSL).</span><span class="sxs-lookup"><span data-stu-id="197fd-134">Direct3D 12 removes the distinction between append and counter UAVs (although the distinction still exists in HLSL bytecode).</span></span>

<span data-ttu-id="197fd-135">O tempo de execução principal validará essas restrições dentro de [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span><span class="sxs-lookup"><span data-stu-id="197fd-135">The core runtime will validate these restrictions inside of [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span></span>

<span data-ttu-id="197fd-136">Durante o empate/expedição, o recurso de contador deve estar no estado D3D12 recurso de estado de [**\_ \_ \_ \_ acesso não ordenado**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).</span><span class="sxs-lookup"><span data-stu-id="197fd-136">During Draw/Dispatch, the counter resource must be in the state [**D3D12\_RESOURCE\_STATE\_UNORDERED\_ACCESS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).</span></span> <span data-ttu-id="197fd-137">Além disso, em uma única chamada de emissão/expedição, é inválido para um aplicativo acessar o mesmo local de memória de 32 bits por meio de dois contadores de UAV separados.</span><span class="sxs-lookup"><span data-stu-id="197fd-137">Also, within a single Draw/Dispatch call, it is invalid for an application to access the same 32-bit memory location via two separate UAV counters.</span></span> <span data-ttu-id="197fd-138">A camada de depuração emitirá erros se um deles for detectado.</span><span class="sxs-lookup"><span data-stu-id="197fd-138">The debug layer will issue errors if either of these is detected.</span></span>

<span data-ttu-id="197fd-139">Não há nenhum método "SetUnorderedAccessViewCounterValue" ou "CopyStructureCount" porque os aplicativos podem simplesmente copiar dados de e para o valor do contador diretamente.</span><span class="sxs-lookup"><span data-stu-id="197fd-139">There are no "SetUnorderedAccessViewCounterValue" or "CopyStructureCount" methods because apps can simply copy data to and from the counter value directly.</span></span>

<span data-ttu-id="197fd-140">Há suporte para a indexação dinâmica de UAVs com contadores.</span><span class="sxs-lookup"><span data-stu-id="197fd-140">Dynamic indexing of UAVs with counters is supported.</span></span>

<span data-ttu-id="197fd-141">Se um sombreador tentar acessar o contador de um UAV que não tem um contador associado, a camada de depuração emitirá um aviso e uma falha de página de GPU ocorrerá, fazendo com que o dispositivo do aplicativo seja removido.</span><span class="sxs-lookup"><span data-stu-id="197fd-141">If a shader attempts to access the counter of a UAV that does not have an associated counter, then the debug layer will issue a warning, and a GPU page fault will occur causing the apps’s device to be removed.</span></span>

<span data-ttu-id="197fd-142">Os contadores UAV têm suporte em todos os tipos de heap (padrão, upload, readback).</span><span class="sxs-lookup"><span data-stu-id="197fd-142">UAV counters are supported in all heap types (default, upload, readback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="197fd-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="197fd-143">Related topics</span></span>

* [<span data-ttu-id="197fd-144">Contadores e consultas</span><span class="sxs-lookup"><span data-stu-id="197fd-144">Counters and queries</span></span>](counters-and-queries.md)