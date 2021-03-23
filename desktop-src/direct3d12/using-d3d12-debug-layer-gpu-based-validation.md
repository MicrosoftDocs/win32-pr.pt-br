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
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a>Validação baseada em GPU e a camada de depuração do Direct3D 12

Este tópico descreve como fazer o melhor uso da camada de depuração do Direct3D 12. A validação baseada em GPU (GBV) permite cenários de validação na linha do tempo GPU que não são possíveis durante chamadas de API na CPU. O GBV está disponível a partir da atualização de aniversário das ferramentas de gráficos para Windows 10.

## <a name="purpose-of-gpu-based-validation"></a>Finalidade da validação baseada em GPU

A validação baseada em GPU ajuda a identificar os seguintes erros:

- Uso de descritores não inicializados ou incompatíveis em um sombreador.
- Uso de descritores que fazem referência a recursos excluídos em um sombreador.
- Validação de Estados de recursos promovidos e decaimento do estado do recurso.
- Indexação além do fim do heap do descritor em um sombreador.
- Acesso ao sombreador de recursos em estado incompatível.
- Uso de amostras não inicializadas ou incompatíveis em um sombreador.

O GBV funciona criando sombreadores com patches que têm validação adicionada diretamente ao sombreador. Os sombreadores com patch inspecionam os argumentos raiz e os recursos acessados durante a execução do sombreador e relatam erros para um buffer de log. O GBV também injeta operações adicionais e despacha chamadas para as listas de comandos do aplicativo para validar e controlar as alterações no estado do recurso imposto pela lista de comandos na linha do tempo da GPU.

Como o GBV requer a capacidade de executar sombreadores, as listas de comandos de cópia são emuladas por uma lista de comandos de computação. Isso pode potencialmente alterar o modo como o hardware realiza cópias, embora o resultado final não deva ser alterado. O aplicativo ainda perceberá que essas são listas de comandos de cópia e a camada de depuração as validará como tal.

## <a name="turning-on-gpu-based-validation"></a>Ativando a validação baseada em GPU

O GBV pode ser forçado a usar o DXCPL (painel de controle do DirectX) forçando a camada de depuração do Direct3D 12 e, adicionalmente, forçando a validação baseada em GPU (nova guia no painel de controle). Uma vez habilitado, o GBV permanecerá habilitado até que o dispositivo Direct3D 12 seja liberado. Como alternativa, o GBV pode ser habilitado programaticamente antes de criar o dispositivo Direct3D 12:

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

## <a name="recommended-usage"></a>Uso recomendado

Em geral, você deve executar o código com a camada de depuração habilitada na maioria das vezes. No entanto, o GBV pode reduzir muito as coisas. Os desenvolvedores podem considerar a possibilidade de habilitar GBV com conjuntos de dados menores (por exemplo, demonstrações de mecanismos ou pequenos níveis de jogos com menos PSOs e recursos) ou durante o início do aplicativo inicial para reduzir problemas de desempenho. Com conteúdo maior, considere a ativação de GBV em um ou dois computadores de teste em um passo de teste noturno.

## <a name="debug-output"></a>Saída de depuração

GBV produz a saída de depuração depois que uma chamada para [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) conclui a execução na GPU. Como isso está na GPU, a saída de depuração pode ser assíncrona com outra validação de linha do tempo da CPU. Os desenvolvedores de aplicativos podem querer injetar sua própria espera após executar para sincronizar a saída de depuração.

A saída de GBV identifica onde ocorreu um erro, juntamente com a contagem de empate/expedição atual e identidades de objetos relacionados (por exemplo, lista de comandos, fila, PSO, etc.).

## <a name="example-debug-message"></a>Exemplo de mensagem de depuração

A mensagem de erro a seguir indica que um recurso denominado "buffer de cores principal" foi acessado em um sombreador como um recurso de sombreador, mas estava no estado de acesso não ordenado quando o sombreador foi executado na GPU. Informações adicionais, como o local na origem do sombreador, o nome da lista de comandos e a contagem de empates (índice de desenho) e os nomes dos objetos de interface D3D relacionados também são fornecidos.

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

## <a name="debug-layer-apis"></a>APIs de camada de depuração

Para habilitar a camada de depuração, chame [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).

Para habilitar a validação baseada em GPU, chame [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)e consulte os métodos das seguintes interfaces:

- [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

Consulte as seguintes enumerações e estruturas:

- [**\_Tipo de \_ parâmetro de lista de comandos de depuração D3D12 \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [**\_Tipo de \_ parâmetro de dispositivo de depuração D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [**\_Sinalizadores de \_ \_ criação de \_ estado do pipeline de validação baseada \_ \_ em \_ GPU D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [**\_Modo de \_ \_ patch do \_ sombreador de validação baseado \_ em GPU D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [**\_Configurações de \_ \_ \_ \_ validação baseadas em GPU \_ da \_ lista de comandos de depuração do D3D12**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [**\_Configurações de \_ \_ \_ validação baseadas em \_ GPU \_ do dispositivo de depuração D3D12**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a>Tópicos relacionados

* [Noções básicas sobre a camada de depuração do Direct3D 12](understanding-the-d3d12-debug-layer.md)
