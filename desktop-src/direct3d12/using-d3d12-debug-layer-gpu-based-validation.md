---
title: Validação baseada em GPU e a camada de depuração do Direct3D 12
description: Este tópico descreve como fazer o melhor uso da camada de depuração do Direct3D 12. A validação baseada em GPU (GBV) permite cenários de validação na linha do tempo GPU que não são possíveis durante chamadas de API na CPU.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 3160df3faf994df2abf9cf878088e84564bb5fe1
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548299"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a><span data-ttu-id="a1152-104">Validação baseada em GPU e a camada de depuração do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a1152-104">GPU-based validation and the Direct3D 12 Debug Layer</span></span>

<span data-ttu-id="a1152-105">Este tópico descreve como fazer o melhor uso da camada de depuração do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="a1152-105">This topic describes how to make best use of the Direct3D 12 Debug Layer.</span></span> <span data-ttu-id="a1152-106">A validação baseada em GPU (GBV) permite cenários de validação na linha do tempo GPU que não são possíveis durante chamadas de API na CPU.</span><span class="sxs-lookup"><span data-stu-id="a1152-106">GPU-based validation (GBV) enables validation scenarios on the GPU timeline that are not possible during API calls on the CPU.</span></span> <span data-ttu-id="a1152-107">O GBV está disponível a partir da atualização de aniversário das ferramentas de gráficos para Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a1152-107">GBV is available starting with the Graphics Tools for Windows 10 Anniversary Update.</span></span>

## <a name="purpose-of-gpu-based-validation"></a><span data-ttu-id="a1152-108">Finalidade da validação baseada em GPU</span><span class="sxs-lookup"><span data-stu-id="a1152-108">Purpose of GPU-based validation</span></span>

<span data-ttu-id="a1152-109">A validação baseada em GPU ajuda a identificar os seguintes erros:</span><span class="sxs-lookup"><span data-stu-id="a1152-109">GPU-based validation helps to identify the following errors:</span></span>

- <span data-ttu-id="a1152-110">Uso de descritores não inicializados ou incompatíveis em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="a1152-110">Use of uninitialized or incompatible descriptors in a shader.</span></span>
- <span data-ttu-id="a1152-111">Uso de descritores que fazem referência a recursos excluídos em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="a1152-111">Use of descriptors referencing deleted Resources in a shader.</span></span>
- <span data-ttu-id="a1152-112">Validação de Estados de recursos promovidos e decaimento do estado do recurso.</span><span class="sxs-lookup"><span data-stu-id="a1152-112">Validation of promoted resource states and resource state decay.</span></span>
- <span data-ttu-id="a1152-113">Indexação além do fim do heap do descritor em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="a1152-113">Indexing beyond the end of the descriptor heap in a shader.</span></span>
- <span data-ttu-id="a1152-114">Acesso ao sombreador de recursos em estado incompatível.</span><span class="sxs-lookup"><span data-stu-id="a1152-114">Shader accesses of resources in incompatible state.</span></span>
- <span data-ttu-id="a1152-115">Uso de amostras não inicializadas ou incompatíveis em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="a1152-115">Use of uninitialized or incompatible Samplers in a shader.</span></span>

<span data-ttu-id="a1152-116">O GBV funciona criando sombreadores com patches que têm validação adicionada diretamente ao sombreador.</span><span class="sxs-lookup"><span data-stu-id="a1152-116">GBV works by creating patched shaders that have validation added directly to the shader.</span></span> <span data-ttu-id="a1152-117">Os sombreadores com patch inspecionam os argumentos raiz e os recursos acessados durante a execução do sombreador e relatam erros para um buffer de log.</span><span class="sxs-lookup"><span data-stu-id="a1152-117">The patched shaders inspect root arguments and resources accessed during shader execution and report errors to a log buffer.</span></span> <span data-ttu-id="a1152-118">O GBV também injeta operações adicionais e despacha chamadas para as listas de comandos do aplicativo para validar e controlar as alterações no estado do recurso imposto pela lista de comandos na linha do tempo da GPU.</span><span class="sxs-lookup"><span data-stu-id="a1152-118">GBV also injects extra operations and Dispatch calls into the application command lists to validate and track changes to resource state imposed by the command list on the GPU-timeline.</span></span>

<span data-ttu-id="a1152-119">Como o GBV requer a capacidade de executar sombreadores, as listas de comandos de cópia são emuladas por uma lista de comandos de computação.</span><span class="sxs-lookup"><span data-stu-id="a1152-119">Because GBV requires the ability to execute shaders, COPY command lists are emulated by a COMPUTE command list.</span></span> <span data-ttu-id="a1152-120">Isso pode potencialmente alterar o modo como o hardware realiza cópias, embora o resultado final não deva ser alterado.</span><span class="sxs-lookup"><span data-stu-id="a1152-120">This may potentially change how hardware performs copies though the end result should not be changed.</span></span> <span data-ttu-id="a1152-121">O aplicativo ainda perceberá que essas são listas de comandos de cópia e a camada de depuração as validará como tal.</span><span class="sxs-lookup"><span data-stu-id="a1152-121">The application will still perceive these are COPY command lists and the debug layer will validate them as such.</span></span>

## <a name="turning-on-gpu-based-validation"></a><span data-ttu-id="a1152-122">Ativando a validação baseada em GPU</span><span class="sxs-lookup"><span data-stu-id="a1152-122">Turning on GPU-based validation</span></span>

<span data-ttu-id="a1152-123">O GBV pode ser forçado a usar o DXCPL (painel de controle do DirectX) forçando a camada de depuração do Direct3D 12 e, adicionalmente, forçando a validação baseada em GPU (nova guia no painel de controle).</span><span class="sxs-lookup"><span data-stu-id="a1152-123">GBV can be forced on using the DirectX Control Panel (DXCPL) by forcing on the Direct3D 12 Debug Layer and additionally forcing on GPU-based validation (new tab in the control panel).</span></span> <span data-ttu-id="a1152-124">Uma vez habilitado, o GBV permanecerá habilitado até que o dispositivo Direct3D 12 seja liberado.</span><span class="sxs-lookup"><span data-stu-id="a1152-124">Once enabled, GBV will remain enabled until the Direct3D 12 device is released.</span></span> <span data-ttu-id="a1152-125">Como alternativa, o GBV pode ser habilitado programaticamente antes de criar o dispositivo Direct3D 12:</span><span class="sxs-lookup"><span data-stu-id="a1152-125">Alternatively, GBV can be enabled programmatically prior to creating the Direct3D 12 Device:</span></span>

```cpp
void EnableShaderBasedValidation()
{
    CComPtr<ID3D12Debug> spDebugController0;
    CComPtr<ID3D12Debug1> spDebugController1;
    VERIFY(D3D12GetDebugInterface(IID_PPV_ARGS(&spDebugController0)));
    VERIFY(spDebugController0->QueryInterface(IID_PPV_ARGS(&spDebugController1)));
    spDebugController1->SetEnableGPUBasedValidation(true);
}
```

## <a name="recommended-usage"></a><span data-ttu-id="a1152-126">Uso recomendado</span><span class="sxs-lookup"><span data-stu-id="a1152-126">Recommended usage</span></span>

<span data-ttu-id="a1152-127">Em geral, você deve executar o código com a camada de depuração habilitada na maioria das vezes.</span><span class="sxs-lookup"><span data-stu-id="a1152-127">Generally, you should run your code with the debug layer enabled most of the time.</span></span> <span data-ttu-id="a1152-128">No entanto, o GBV pode reduzir muito as coisas.</span><span class="sxs-lookup"><span data-stu-id="a1152-128">However, GBV can slow things down a lot.</span></span> <span data-ttu-id="a1152-129">Os desenvolvedores podem considerar a possibilidade de habilitar GBV com conjuntos de dados menores (por exemplo, demonstrações de mecanismos ou pequenos níveis de jogos com menos PSOs e recursos) ou durante o início do aplicativo inicial para reduzir problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a1152-129">Developers may consider enabling GBV with smaller data sets (for example, engine demos or small game levels with fewer PSO’s and resources) or during early application bring-up to reduce performance problems.</span></span> <span data-ttu-id="a1152-130">Com conteúdo maior, considere a ativação de GBV em um ou dois computadores de teste em um passo de teste noturno.</span><span class="sxs-lookup"><span data-stu-id="a1152-130">With larger content consider turning on GBV on one or two test machines in a nightly test pass.</span></span>

## <a name="debug-output"></a><span data-ttu-id="a1152-131">Saída de depuração</span><span class="sxs-lookup"><span data-stu-id="a1152-131">Debug output</span></span>

<span data-ttu-id="a1152-132">GBV produz a saída de depuração depois que uma chamada para [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) conclui a execução na GPU.</span><span class="sxs-lookup"><span data-stu-id="a1152-132">GBV produces debug output after a call to [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) completes execution on the GPU.</span></span> <span data-ttu-id="a1152-133">Como isso está na GPU, a saída de depuração pode ser assíncrona com outra validação de linha do tempo da CPU.</span><span class="sxs-lookup"><span data-stu-id="a1152-133">Since this is on the GPU-timeline the debug output may be asynchronous with other CPU-timeline validation.</span></span> <span data-ttu-id="a1152-134">Os desenvolvedores de aplicativos podem querer injetar sua própria espera após executar para sincronizar a saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="a1152-134">Application developers may want to inject their own wait-after-execute to synchronize debug output.</span></span>

<span data-ttu-id="a1152-135">A saída de GBV identifica onde ocorreu um erro, juntamente com a contagem de empate/expedição atual e identidades de objetos relacionados (por exemplo, lista de comandos, fila, PSO, etc.).</span><span class="sxs-lookup"><span data-stu-id="a1152-135">GBV output identifies where in a shader an error occurred, along with the current draw/dispatch count and identities of related objects (e.g. command list, queue, PSO, etc).</span></span>

## <a name="example-debug-message"></a><span data-ttu-id="a1152-136">Exemplo de mensagem de depuração</span><span class="sxs-lookup"><span data-stu-id="a1152-136">Example debug message</span></span>

<span data-ttu-id="a1152-137">A mensagem de erro a seguir indica que um recurso denominado "buffer de cores principal" foi acessado em um sombreador como um recurso de sombreador, mas estava no estado de acesso não ordenado quando o sombreador foi executado na GPU.</span><span class="sxs-lookup"><span data-stu-id="a1152-137">The following error message indicates that a resource named “Main Color Buffer” was accessed in a shader as a shader resource but was in the unordered access state when the shader ran on the GPU.</span></span> <span data-ttu-id="a1152-138">Informações adicionais, como o local na origem do sombreador, o nome da lista de comandos e a contagem de empates (índice de desenho) e os nomes dos objetos de interface D3D relacionados também são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="a1152-138">Additional information, such as the location in the shader source, the name of the command list and the Draw count (Draw Index), and the names of related D3D interface objects are also provided.</span></span>

```cmd
D3D12 ERROR: Incompatible resource state: Resource: 0x0000016F61A6EA80:'Main Color Buffer', 
Subresource Index: [0], 
Descriptor heap index: [0], 
Binding Type In Descriptor: SRV, 
Resource State: D3D12_RESOURCE_STATE_UNORDERED_ACCESS(0x8), 
Shader Stage: PIXEL, 
Root Parameter Index: [0], 
Draw Index: [0], 
Shader Code: E:\FileShare\MiniEngine_GitHub_160128\MiniEngine_GitHub\Core\Shaders\SharpeningUpsamplePS.hlsl(37,2-59), 
Asm Instruction Range: [0x138-0x16b], 
Asm Operand Index: [3], 
Command List: 0x0000016F6F75F740:'CommandList', SRV/UAV/CBV Descriptor Heap: 0x0000016F6F76F280:'Unnamed ID3D12DescriptorHeap Object', 
Sampler Descriptor Heap: <not set>, 
Pipeline State: 0x0000016F572C89F0:'Unnamed ID3D12PipelineState Object',  
[ EXECUTION ERROR #942: GPU_BASED_VALIDATION_INCOMPATIBLE_RESOURCE_STATE]
```

## <a name="debug-layer-apis"></a><span data-ttu-id="a1152-139">APIs de camada de depuração</span><span class="sxs-lookup"><span data-stu-id="a1152-139">Debug Layer APIs</span></span>

<span data-ttu-id="a1152-140">Para habilitar a camada de depuração, chame [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).</span><span class="sxs-lookup"><span data-stu-id="a1152-140">To enable the debug layer, call [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).</span></span>

<span data-ttu-id="a1152-141">Para habilitar a validação baseada em GPU, chame [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)e consulte os métodos das seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="a1152-141">To enable GPU-based validation, call [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation), and refer to the methods of the following interfaces:</span></span>

- [<span data-ttu-id="a1152-142">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="a1152-142">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [<span data-ttu-id="a1152-143">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="a1152-143">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [<span data-ttu-id="a1152-144">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="a1152-144">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

<span data-ttu-id="a1152-145">Consulte as seguintes enumerações e estruturas:</span><span class="sxs-lookup"><span data-stu-id="a1152-145">Refer to the following enumerations and structures:</span></span>

- [<span data-ttu-id="a1152-146">**\_Tipo de \_ parâmetro de lista de comandos de depuração D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a1152-146">**D3D12\_DEBUG\_COMMAND\_LIST\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [<span data-ttu-id="a1152-147">**\_Tipo de \_ parâmetro de dispositivo de depuração D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a1152-147">**D3D12\_DEBUG\_DEVICE\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [<span data-ttu-id="a1152-148">**\_Sinalizadores de \_ \_ criação de \_ estado do pipeline de validação baseada \_ \_ em \_ GPU D3D12**</span><span class="sxs-lookup"><span data-stu-id="a1152-148">**D3D12\_GPU\_BASED\_VALIDATION\_PIPELINE\_STATE\_CREATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [<span data-ttu-id="a1152-149">**\_Modo de \_ \_ patch do \_ sombreador de validação baseado \_ em GPU D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="a1152-149">**D3D12\_GPU\_BASED\_VALIDATION\_SHADER\_PATCH\_MODE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [<span data-ttu-id="a1152-150">**\_Configurações de \_ \_ \_ \_ validação baseadas em GPU \_ da \_ lista de comandos de depuração do D3D12**</span><span class="sxs-lookup"><span data-stu-id="a1152-150">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [<span data-ttu-id="a1152-151">**\_Configurações de \_ \_ \_ validação baseadas em \_ GPU \_ do dispositivo de depuração D3D12**</span><span class="sxs-lookup"><span data-stu-id="a1152-151">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a><span data-ttu-id="a1152-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1152-152">Related topics</span></span>

* [<span data-ttu-id="a1152-153">Noções básicas sobre a camada de depuração do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a1152-153">Understanding the Direct3D 12 Debug Layer</span></span>](understanding-the-d3d12-debug-layer.md)
