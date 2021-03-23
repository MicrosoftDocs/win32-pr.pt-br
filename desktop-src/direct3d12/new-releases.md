---
title: O que há de novo no Direct3D 12
description: Este tópico descreve a nova documentação mais significativa do Direct3D 12 disponível para várias versões.
ms.assetid: 38F41E05-FECB-41DE-8D30-09733FBEAC48
ms.localizationpriority: high
ms.topic: article
ms.date: 12/05/2019
ms.openlocfilehash: ec3ecc9e68fc4711def2c364793eca32804d8d04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548197"
---
# <a name="whats-new-in-direct3d-12"></a>O que há de novo no Direct3D 12

Este tópico descreve a nova documentação mais significativa do Direct3D 12 disponível para várias versões.

Para obter informações sobre como obter e instalar o Direct3D, consulte [configuração do ambiente de programação do Direct3D 12](./directx-12-programming-environment-set-up.md).

## <a name="direct3d-12-on-windows-7"></a>Direct3D 12 no Windows 7

- O [Direct3D 12 no Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/) já está disponível para os desenvolvedores usarem.

## <a name="windows-10-may-2019-update"></a>Atualização de maio de 2019 para Windows 10

Esses recursos e APIs foram adicionados ou atualizados para o Windows 10, versão 1903 (10,0; Build 18362) &mdash; também conhecido como Windows 10 pode 2019 atualização.

- [Sombreamento de taxa variável (VRS)](./vrs.md). Permite alocar desempenho de renderização/energia em taxas que variam em sua imagem renderizada.
- [HLSL Shader model 6,4](../direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12.md). Descreve os intrínsecos do Machine Learning adicionados ao modelo de sombreador HLSL 6,4.
- Enumeração de [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version) . Define constantes que especificam uma versão do dispositivo removeu dados estendidos (DRED com).
- Estrutura de [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) . Indica o nível de suporte que o adaptador fornece para metacomandos.
- Estrutura de [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command) . Indica o nível de suporte que o adaptador fornece para metacomandos.
- Enumeração de [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) . Define constantes que especificam uma camada de taxa de sombreamento (para sombreamento de taxa variável ou VRS).
- Interface [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) e seus métodos. Usado para definir o modo para otimizações de processamento em segundo plano do driver. Consulte também [otimizações de sombreador em segundo plano](https://devblogs.microsoft.com/directx/background-shader-optimizations/).
- Interface [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) e seus métodos. Fornece acesso ao tempo de execução para dados de dados estendidos removidos do dispositivo (DRED com).
- Interface [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) e seus métodos. Controla o dispositivo removeu as configurações de dados estendidos (DRED com).
- Interface [**D3D12GraphicsCommandList5**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist5) e seus métodos. Suporte para sombreamento de taxa variável (VRS).

A enumeração de [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) foi atualizada com a adição da constante de **D3D_SHADER_MODEL_6_5** (um recurso de nível experimental).

A enumeração de [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) foi atualizada com a adição da constante de **D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE** .

A enumeração de [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) foi atualizada com a adição das constantes **D3D12_FEATURE_D3D12_OPTIONS6** e **D3D12_FEATURE_QUERY_META_COMMAND** .

A enumeração de [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) foi atualizada com a adição da constante de **D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE** .

## <a name="windows-10-version-1809"></a>Windows 10, versão 1809

Esses recursos e APIs foram adicionados ou atualizados para o Windows 10, versão 1809 (10,0; Build 17763) &mdash; também conhecido como atualização do Windows 10 de outubro de 2018.

- [Direct3D 12 raytracing](./direct3d-12-raytracing.md)
- [Passagens de renderização do Direct3D 12](./direct3d-12-render-passes.md)

## <a name="windows-10-version-1709"></a>Windows 10, versão 1709

Essas interfaces foram adicionadas à documentação do Direct3D para Windows 10, versão 1709.

-   [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) estende a funcionalidade de criação de limites ao dar suporte à recuperação de sinalizadores passados para criar a cerca.
-   [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) estende a lista de comandos gráficos disponíveis ao dar suporte à gravação de valores imediatos diretamente em um buffer.
-   [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) estende a funcionalidade do adaptador virtual criando heaps de diagnóstico de uso especial na memória do sistema que persistem mesmo no caso de um cenário de falha da GPU ou remoção do dispositivo.

A enumeração do [**\_ \_ modelo do sombreador D3D**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) tem um novo valor do **modelo de sombreador do D3D \_ \_ \_ 6 \_ 1** adicionado para descrever o modelo do sombreador 6,1.

A enumeração de [**\_ recursos D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) também tem o **novo \_ recurso D3D12 \_ D3D12 \_ OPTIONS3** e os valores de **\_ \_ \_ heaps existentes do recurso D3D12** . Como os nomes sugerem, esses valores permitem verificar opções de Direct3D12 adicionais, bem como verificar o suporte de heaps existentes.

## <a name="windows-10-version-1703"></a>Windows 10, versão 1703

Esses tópicos foram adicionados à documentação do Direct3D para Windows 10, versão 1703.

-   O método [**ID3D12Device2:: Createpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) e a estrutura Desc do fluxo de [**estado do \_ pipeline \_ \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) representam uma maneira nova e mais robusta de criar PSOs e unifica o interface para a criação de pipelines de computação e gráficos.
-   O método [**ID3D12Device1:: CreatePipelineLibrary1**](https://www.bing.com/search?q=**ID3D12Device1::CreatePipelineLibrary1**) expande a interface da biblioteca de pipeline para aceitar o PSOs criado com a estrutura Desc do novo e unificado fluxo de estado de [**\_ pipeline \_ \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) .
-   A função [**D3D12EnableExperimentalFeatures**](/windows/win32/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) permite que os desenvolvedores experimentem alguns recursos no desenvolvimento usando um computador no modo de desenvolvedor.
-   Há cinco novas interfaces (consulte a [hierarquia de interface](interface-hierarchy.md)):
    -   [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1)
    -   [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1)
    -   [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2)
    -   [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2)
    -   [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools)
-   Consulte a [visão geral do HLSL Shader Model 6,0](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md), que descreve as operações intrínsecas de ondas para pixel e sombreadores de computação com vários threads.
-   O uso de [**ID3D12Device:: SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) foi alterado.
-   Alguns recursos novos para o Direct3D 11 são descritos nos [recursos do direct3d 11,4](../direct3d11/direct3d-11-4-features.md).
-   [**AtomicCopyBufferUINT**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint) e [**AtomicCopyBufferUINT64**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64) habilitam a **trava tardia** para reduzir a latência de pervieved.
-   [**ID3D12Device2:: Createpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) e [**OMSetDepthBounds**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-omsetdepthbounds) habilitam o **teste de limites de profundidade** em hardware com suporte.
-   O [**ResolveSubresourceRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion) permite a **resolução parcial** de subrecursos para ajudar a otimizar o desempenho.
-   O [**SetSamplePositions**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) permite **posições de exemplo programáveis** em hardware com suporte.

## <a name="november-2016-documentation-update"></a>Atualização de documentação de novembro de 2016

-   Revisão dos comentários para [**ID3D12GraphicsCommandList::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource).
-   Esclarecimento de "estado decaimento a comum" (consulte [usando barreiras de recursos para sincronizar Estados de recursos no Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)).
-   O arquivo de cabeçalho D3dx12. h, mencionado em [estruturas auxiliares e funções para D3D12](helper-structures-and-functions-for-d3d12.md), pode ser baixado diretamente da [biblioteca auxiliar do D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).

## <a name="august-2016-documentation-update-2"></a>Atualização da documentação de agosto de 2016 2

-   Uma nova seção de guia denominada [Understanding the D3D12 Debug Layer](understanding-the-d3d12-debug-layer.md).

    Três novas interfaces de camada de depuração (no modo de visualização) são descritas: [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1), [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1), [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1).

## <a name="august-2016-documentation-update-1"></a>Atualização 1 de agosto de 2016

-   Revisão do [uso de barreiras de recursos para sincronizar Estados de recursos no Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).
-   Revisão do [acesso a recursos de várias filas](./user-mode-heap-synchronization.md#multi-queue-resource-access).

## <a name="windows-10-version-1607"></a>Windows 10, versão 1607

Esses tópicos foram adicionados à documentação do Direct3D para Windows 10, versão 1607.

-   [Assinatura de raiz versão 1,1](root-signature-version-1-1.md) : uma visão geral das assinaturas raiz atualizadas, permitindo que os aplicativos especifiquem como os dados e os descritores estáticos ou voláteis são, o que pode auxiliar as otimizações de driver de gráficos.
-   O método [**ID3D12Device1:: CreatePipelineLibrary**](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary) descreve as vantagens de criar uma biblioteca de pipeline.
-   Há três novas interfaces (consulte a [hierarquia de interface](interface-hierarchy.md)):
    -   [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary)
    -   [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1)
    -   [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer)
-   Consulte a [visão geral do HLSL Shader Model 6,0](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md), que descreve as operações intrínsecas de ondas para pixel e sombreadores de computação com vários threads.
-   O uso de [**ID3D12Device:: SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) foi alterado.
-   Alguns recursos novos para o Direct3D 11 são descritos nos [recursos do direct3d 11,4](../direct3d11/direct3d-11-4-features.md).
-   O intervalo de bibliotecas com suporte para o Direct3D 12 foi atualizado, consulte a seção **ferramentas e bibliotecas com suporte** da [instalação do ambiente de programação do Direct3D 12](directx-12-programming-environment-set-up.md).
-   [Usar DirectX com exibições de alto alcance dinâmico e cor avançada](../direct3darticles/high-dynamic-range.md)
-   [Exibição da taxa de atualização da variável](../direct3ddxgi/variable-refresh-rate-displays.md)
-   [Aprimoramentos de DXGI 1,5](../direct3ddxgi/dxgi-1-5-improvements.md)

## <a name="related-topics"></a>Tópicos relacionados

* [Guia de programação do Direct3D 12](directx-12-programming-guide.md)