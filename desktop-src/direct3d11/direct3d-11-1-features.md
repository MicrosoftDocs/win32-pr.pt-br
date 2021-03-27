---
title: Recursos do Direct3D 11,1
description: A funcionalidade a seguir foi adicionada no Direct3D 11,1, que está incluído no Windows 8, Windows RT e Windows Server 2012.
ms.assetid: 2203D2D2-ECF6-4753-90FA-12A52678DFBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dece9ed6e0a40ade28857277c344be0e9f2e7ce1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641148"
---
# <a name="direct3d-111-features"></a>Recursos do Direct3D 11,1

A funcionalidade a seguir foi adicionada no Direct3D 11,1, que está incluído no Windows 8, Windows RT e Windows Server 2012. O suporte parcial para o [Direct3D 11,1](direct3d-11-features.md) está disponível no Windows 7 e no windows Server 2008 R2 por meio da [atualização de plataforma para o Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), que está disponível por meio da [atualização de plataforma para o Windows 7](https://support.microsoft.com/kb/2670838).

-   [Rastreamento de sombreador e aprimoramentos do compilador](#shader-tracing-and-compiler-enhancements)
-   [Compartilhamento de dispositivo Direct3D](#direct3d-device-sharing)
-   [Verificar o suporte dos novos recursos e formatos do Direct3D 11,1](#check-support-of-new-direct3d-111-features-and-formats)
-   [Usar precisão mínima de HLSL](#use-hlsl-minimum-precision)
-   [Especifique os planos de corte do usuário no HLSL no nível de recurso 9 e superior](#specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Criar buffers de constante maiores do que um sombreador pode acessar](#create-larger-constant-buffers-than-a-shader-can-access)
-   [Usar operações lógicas em um destino de renderização](#use-logical-operations-in-a-render-target)
-   [Forçar a contagem de amostras para criar um estado de rasterizador](#force-the-sample-count-to-create-a-rasterizer-state)
-   [Processar recursos de vídeo com sombreadores](#process-video-resources-with-shaders)
-   [Suporte estendido para recursos de Texture2D compartilhados](#extended-support-for-shared-texture2d-resources)
-   [Alterar os subrecursos com novas opções de cópia](#change-subresources-with-new-copy-options)
-   [Descartar recursos e exibições de recursos](#discard-resources-and-resource-views)
-   [Suporte a um número maior de UAVs](#support-a-larger-number-of-uavs)
-   [Associar um subintervalo de um buffer constante a um sombreador](#bind-a-subrange-of-a-constant-buffer-to-a-shader)
-   [Recuperar o subintervalo de um buffer constante que está associado a um sombreador](#retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader)
-   [Limpar todo ou parte de um modo de exibição de recurso](#clear-all-or-part-of-a-resource-view)
-   [Mapear SRVs de buffers dinâmicos sem \_ substituição](/windows)
-   [Usar UAVs em cada estágio do pipeline](#use-uavs-at-every-pipeline-stage)
-   [Suporte estendido para dispositivos WARP](#extended-support-for-warp-devices)
-   [Usar Direct3D nos processos da sessão 0](#use-direct3d-in-session-0-processes)
-   [Suporte para buffer de sombra no nível de recurso 9](#support-for-shadow-buffer-on-feature-level-9)
-   [Tópicos relacionados](#related-topics)

## <a name="shader-tracing-and-compiler-enhancements"></a>Rastreamento de sombreador e aprimoramentos do compilador

O Direct3D 11,1 permite usar o rastreamento de sombreador para garantir que seu código esteja funcionando conforme o esperado e, se não for, você poderá descobrir e corrigir o problema. O SDK (Software Development Kit) do Windows para Windows 8 contém aprimoramentos do compilador HLSL. O rastreamento de sombreador e o compilador HLSL são implementados no D3dcompiler \_nn.dll.

A API de rastreamento de sombreador e os aprimoramentos do compilador HLSL consistem nos métodos e funções a seguir.

-   [**ID3D11RefDefaultTrackingOptions:: settrackingoptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions)
-   [**ID3D11RefTrackingOptions:: settrackingoptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11reftrackingoptions-settrackingoptions)
-   [**ID3D11TracingDevice::SetShaderTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11TracingDevice::SetShaderTrackingOptionsByType**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11ShaderTraceFactory::CreateShaderTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace)
-   [**ID3D11ShaderTrace::TraceReady**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-traceready)
-   [**ID3D11ShaderTrace::ResetTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-resettrace)
-   [**ID3D11ShaderTrace::GetTraceStats**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-gettracestats)
-   [**ID3D11ShaderTrace::P SSelectStamp**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-psselectstamp)
-   [**ID3D11ShaderTrace::GetInitialRegisterContents**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents)
-   [**ID3D11ShaderTrace:: getstep**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getstep)
-   [**ID3D11ShaderTrace::GetWrittenRegister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getwrittenregister)
-   [**ID3D11ShaderTrace::GetReadRegister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getreadregister)
-   [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2)
-   [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)
-   [**D3DDisassemble11Trace**](/windows/desktop/direct3dhlsl/d3ddisassemble11trace)
-   [**D3DDisassembleRegion**](/windows/desktop/direct3dhlsl/d3ddisassembleregion)
-   [**D3DGetTraceInstructionOffsets**](/windows/desktop/direct3dhlsl/d3dgettraceinstructionoffsets)
-   [**D3DReadFileToBlob**](/windows/desktop/direct3dhlsl/d3dreadfiletoblob)
-   [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart)
-   [**D3DWriteBlobToFile**](/windows/desktop/direct3dhlsl/d3dwriteblobtofile)

A biblioteca D3dcompiler. lib requer D3dcompiler \_nn.dll. Essa DLL não faz parte do Windows 8; Ele está na \\ pasta bin do SDK do Windows para Windows 8, juntamente com a versão de linha de comando Fxc.exe do compilador HLSL.

> [!Note]  
> Embora você possa usar essa biblioteca e a combinação de DLL para desenvolvimento, não é possível implantar aplicativos da Windows Store que usam essa combinação. Portanto, você deve compilar sombreadores HLSL antes de enviar seu aplicativo da Windows Store. Você pode gravar binários de compilação HLSL em disco ou o compilador pode gerar cabeçalhos com matrizes de bytes estáticos que contêm os dados de blob de sombreador. Você usa a interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) para acessar os dados de BLOB. Para desenvolver seu aplicativo da Windows Store, chame [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2) ou [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) para COMPILAR a fonte de HLSL bruta e, em seguida, alimentar os dados de blob resultantes para o Direct3D.

 

## <a name="direct3d-device-sharing"></a>Compartilhamento de dispositivo Direct3D

O Direct3D 11,1 permite que as APIs do Direct3D 10 e as APIs do Direct3D 11 usem um dispositivo de renderização subjacente.

Esse recurso do Direct3D 11,1 consiste nos seguintes métodos e interface.

-   [**ID3D11Device1::CreateDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate)
-   [**ID3D11DeviceContext1::SwapDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate)
-   [**ID3DDeviceContextState**](/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate)

## <a name="check-support-of-new-direct3d-111-features-and-formats"></a>Verificar o suporte dos novos recursos e formatos do Direct3D 11,1

O Direct3D 11,1 permite que você verifique se há novos recursos aos quais o driver de gráficos pode dar suporte e novas maneiras em que um formato tem suporte em um dispositivo. O Microsoft DirectX Graphics Infrastructure (DXGI) 1,2 também especifica novos valores de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

Esse recurso do Direct3D 11,1 consiste na API a seguir.

-   [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) com [**D3D11 \_ recurso \_ Data \_ D3D11 \_ Opções**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), [**D3D11 \_ recurso recursos de \_ arquitetura de dados \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info), [**D3D11 \_ recurso \_ dados \_ d3d9 \_ Opções**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options), [**D3D11 \_ recursos recurso \_ \_ \_ \_ \_ suporte mínimo de precisão**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)e D3D11 de dados de recursos d3d9 estruturas de [**\_ \_ \_ \_ \_ suporte de sombra**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support)
-   [**ID3D11Device:: CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) com [**\_ formato D3D11 \_ dá suporte à \_ \_ saída do decodificador**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), o [**\_ formato D3D11 \_ dá suporte à \_ \_ \_ saída do processador de vídeo**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), o [**formato D3D11 \_ \_ dá suporte à \_ \_ \_ entrada do processador de vídeo**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), o [**\_ formato D3D11 suporta o \_ \_ \_ codificador de vídeo**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)e o [**formato D3D11 SUPPORT2 de \_ \_ \_ \_ \_ lógica \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)

## <a name="use-hlsl-minimum-precision"></a>Usar precisão mínima de HLSL

A partir do Windows 8, os drivers gráficos podem implementar os [tipos de dados escalares HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) mínimos de precisão usando qualquer precisão maior ou igual à precisão de bit especificada. Quando o código do sombreador de precisão mínima do HLSL é usado em hardware que implementa a precisão mínima do HLSL, você usa menos largura de banda de memória e, como resultado, você também usa menos energia do sistema.

Você pode consultar o suporte mínimo de precisão que o driver de gráficos fornece chamando [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) com o valor de [**\_ \_ \_ \_ \_ suporte mínimo de precisão do recurso do D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) . Nesta chamada **ID3D11Device:: CheckFeatureSupport** , passe um ponteiro para uma estrutura [**de \_ \_ \_ \_ \_ \_ suporte mínimo de precisão de dados de recurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support) , que **ID3D11Device:: CheckFeatureSupport** preenche os níveis mínimos de precisão que o driver dá suporte para o estágio Pixel Shader e para outros estágios de sombreador. As informações retornadas apenas indicam que o hardware de gráficos pode executar operações de HLSL em uma precisão menor do que a precisão padrão de float de 32 bits, mas não garante que o hardware de gráficos seja realmente executado com uma precisão mais baixa.

Você não precisa criar vários sombreadores que não usam a precisão mínima. Em vez disso, crie sombreadores com precisão mínima, e as variáveis de precisão mínimas se comportarão na precisão de 32 bits completa se o driver de gráficos relatar que ele não dá suporte a precisão mínima. Para obter mais informações sobre a precisão mínima do HLSL, consulte [usando a precisão mínima do HLSL](/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision).

Os sombreadores de precisão mínima do HLSL não funcionam em sistemas operacionais anteriores ao Windows 8.

## <a name="specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Especifique os planos de corte do usuário no HLSL no nível de recurso 9 e superior

A partir do Windows 8, você pode usar o atributo de função **clipplanes** em uma [declaração de função](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-syntax) HLSL em vez de [VA \_ ClipDistance](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) para fazer com que o sombreador funcione no [nível de recurso](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, bem como no nível de recurso 10 e superior. Para obter mais informações, consulte os [planos de corte do usuário no hardware nível 9 do recurso](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).

## <a name="create-larger-constant-buffers-than-a-shader-can-access"></a>Criar buffers de constante maiores do que um sombreador pode acessar

O Direct3D 11,1 permite que você crie buffers constantes maiores que o tamanho máximo de buffer de constante que um sombreador pode acessar (constantes de 4096 32 bits \* 4 – 64 KB). Posteriormente, ao associar os buffers ao pipeline, por exemplo, por meio de [**PSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers) ou [**PSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1), você pode especificar um intervalo de buffers que o sombreador pode acessar e que se ajusta dentro do limite de 4096.

O Direct3D 11,1 atualiza o método [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) para esse recurso.

## <a name="use-logical-operations-in-a-render-target"></a>Usar operações lógicas em um destino de renderização

O Direct3D 11,1 permite que você use operações lógicas em vez de Mesclar em um destino de renderização. No entanto, você não pode misturar operações lógicas com mesclagem em vários destinos de renderização.

Esse recurso do Direct3D 11,1 consiste na API a seguir.

-   [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1) com [ **\_ \_ op lógico D3D11**](/windows/desktop/api/D3D11_1/ne-d3d11_1-d3d11_logic_op)

## <a name="force-the-sample-count-to-create-a-rasterizer-state"></a>Forçar a contagem de amostras para criar um estado de rasterizador

O Direct3D 11,1 permite especificar uma contagem de amostras forçada quando você cria um estado de rasterizador.

Esse recurso do Direct3D 11,1 consiste na API a seguir.

-   [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)

> [!Note]  
>
> Se você quiser renderizar com a contagem de amostras forçada para 1 ou maior, deverá seguir estas diretrizes:
>
> -   Não associe exibições de estêncil de profundidade.
> -   Desabilite o teste de profundidade.
> -   Certifique-se de que o sombreador não gere profundidade.
> -   Se você tiver quaisquer exibições de destino de renderização vinculadas ([**\_ destino de \_ renderização \_ de associação D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)) e tiver forçado a contagem de amostras para maior que 1, verifique se cada destino de renderização tem apenas um único exemplo.
> -   Não opere o sombreador na frequência de exemplo. Portanto, [**ID3D11ShaderReflection:: IsSampleFrequencyShader**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader) retorna **false**.
>
> Caso contrário, o comportamento de renderização será indefinido. Para obter informações sobre como configurar o estêncil de profundidade, consulte [Configurando Depth-Stencil funcionalidade](d3d10-graphics-programming-guide-depth-stencil.md).

 

## <a name="process-video-resources-with-shaders"></a>Processar recursos de vídeo com sombreadores

O Direct3D 11,1 permite criar modos de exibição (SRV/RTV/UAV) para recursos de vídeo para que os sombreadores de Direct3D possam processar esses recursos de vídeo. O formato de um recurso de vídeo subjacente restringe os formatos que o modo de exibição pode usar. A enumeração de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) contém novos valores de formato de recurso de vídeo. Esses valores de **\_ formato dxgi** especificam os formatos de exibição válidos que você pode criar e como o tempo de execução do Direct3D 11,1 mapeia a exibição. Você pode criar várias exibições de partes diferentes da mesma superfície e, dependendo do formato, os tamanhos das exibições podem diferir uns dos outros.

O Direct3D 11,1 atualiza os seguintes métodos para esse recurso.

-   [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)
-   [**ID3D11Device::CreateRenderTargetView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview)
-   [**ID3D11Device::CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview)

## <a name="extended-support-for-shared-texture2d-resources"></a>Suporte estendido para recursos de Texture2D compartilhados

O Direct3D 11,1 garante que você possa compartilhar recursos Texture2D criados com tipos e formatos de recursos específicos. Para compartilhar recursos do Texture2D, use [**o \_ recurso \_ D3D11 \_ misc**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)compartilhado, o [**D3D11 \_ \_ misc \_ compartilhado \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)do recurso, ou uma combinação do recurso **D3D11 \_ \_ \_ multishared \_ KEYEDMUTEX** e do recurso D3D11 [**\_ \_ \_ multishared \_ NTHANDLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) (novo para o Windows 8) sinalizadores ao criar esses recursos.

O Direct3D 11,1 garante que você possa compartilhar recursos de Texture2D que você criou com esses valores de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) :

-   \_Formato dxgi \_ R8G8B8A8 \_ UNORM
-   \_Formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB
-   \_Formato dxgi \_ B8G8R8A8 \_ UNORM
-   \_Formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB
-   \_Formato dxgi \_ B8G8R8X8 \_ UNORM
-   \_Formato dxgi \_ B8G8R8X8 \_ UNORM \_ sRGB
-   \_Formato dxgi \_ R10G10B10A2 \_ UNORM
-   \_ \_ Float R16G16B16A16 de formato dxgi \_

Além disso, o Direct3D 11,1 garante que você possa compartilhar recursos de Texture2D que você criou com um nível de mipmap de 1, tamanho da matriz de 1, associar sinalizadores do [**\_ \_ \_ recurso do sombreador de ligação do D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) e o [**\_ \_ \_ destino de renderização do D3D11 associado**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) , padrão de uso ([**\_ \_ padrão de uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) e somente esses valores de [**\_ \_ \_ sinalizador diverso de recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) :

-   [**\_Recurso \_ diverso \_ compartilhado do D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ \_ \_ dishared \_ KEYEDMUTEX de recursos**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ \_ \_ dishared \_ NTHANDLE de recursos**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_ \_ \_ Compatível com GDI variado do recurso D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

O Direct3D 11,1 permite que você compartilhe uma maior variedade de formatos e tipos de recursos Texture2D. Você pode consultar se o driver de gráficos e o hardware dão suporte ao compartilhamento de recursos Texture2D estendido chamando [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) com o valor de [**\_ \_ \_ Opções D3D11 de recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) . Nesta chamada **ID3D11Device:: CheckFeatureSupport** , passe um ponteiro para uma estrutura [**de \_ \_ Opções de \_ D3D11 \_ de dados do recurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) . **ID3D11Device:: CheckFeatureSupport** define o membro **ExtendedResourceSharing** de **D3D11 \_ recurso \_ Data \_ D3D11 \_ Opções** como **true** se o hardware e o driver dão suporte ao compartilhamento estendido de recursos de Texture2D.

Se [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) retornar **true** em **ExtendedResourceSharing**, você poderá compartilhar os recursos que criou com esses valores de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) :

-   \_Tipo de \_ R32G32B32A32 de formato dxgi \_
-   \_ \_ Float R32G32B32A32 de formato dxgi \_
-   \_Formato dxgi \_ R32G32B32A32 \_ uint
-   \_Formato dxgi \_ R32G32B32A32 \_ Santo
-   \_Tipo de \_ R16G16B16A16 de formato dxgi \_
-   \_ \_ Float R16G16B16A16 de formato dxgi \_
-   \_Formato dxgi \_ R16G16B16A16 \_ UNORM
-   \_Formato dxgi \_ R16G16B16A16 \_ uint
-   \_Formato dxgi \_ R16G16B16A16 \_ SNORM
-   \_Formato dxgi \_ R16G16B16A16 \_ Santo
-   \_Formato dxgi \_ R10G10B10A2 \_ UNORM
-   \_Formato dxgi \_ R10G10B10A2 \_ uint
-   \_Tipo de \_ R8G8B8A8 de formato dxgi \_
-   \_Formato dxgi \_ R8G8B8A8 \_ UNORM
-   \_Formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB
-   \_Formato dxgi \_ R8G8B8A8 \_ uint
-   \_Formato dxgi \_ R8G8B8A8 \_ SNORM
-   \_Formato dxgi \_ R8G8B8A8 \_ Santo
-   \_Tipo de \_ B8G8R8A8 de formato dxgi \_
-   \_Formato dxgi \_ B8G8R8A8 \_ UNORM
-   \_Formato dxgi \_ B8G8R8X8 \_ UNORM
-   \_Formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB
-   \_Tipo de \_ B8G8R8X8 de formato dxgi \_
-   \_Formato dxgi \_ B8G8R8X8 \_ UNORM \_ sRGB
-   \_Tipo de \_ R32 de formato dxgi \_
-   \_ \_ Float R32 de formato dxgi \_
-   \_Formato dxgi \_ R32 \_ uint
-   \_Formato dxgi \_ R32 \_ Santo
-   \_Tipo de \_ R16 de formato dxgi \_
-   \_ \_ Float R16 de formato dxgi \_
-   \_Formato dxgi \_ R16 \_ UNORM
-   \_Formato dxgi \_ R16 \_ uint
-   \_Formato dxgi \_ R16 \_ SNORM
-   \_Formato dxgi \_ R16 \_ Santo
-   \_Tipo de \_ R8 de formato dxgi \_
-   \_UNORM de \_ R8 de formato dxgi \_
-   \_R8 de formato dxgi \_ \_ uint
-   \_SNORM de \_ R8 de formato dxgi \_
-   \_R8 de formato dxgi \_ \_ Santo
-   \_Formato dxgi \_ a8 \_ UNORM
-   \_AYUV de formato dxgi \_
-   \_YUY2 de formato dxgi \_
-   \_NV12 de formato dxgi \_
-   \_NV11 de formato dxgi \_
-   \_P016 de formato dxgi \_
-   \_P010 de formato dxgi \_
-   \_Y216 de formato dxgi \_
-   \_Y210 de formato dxgi \_
-   \_Y416 de formato dxgi \_
-   \_Y410 de formato dxgi \_

Se [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) retornar **true** em **ExtendedResourceSharing**, você poderá compartilhar recursos que você criou com estes recursos e sinalizadores:

-   [**\_Padrão de uso de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)
-   [**\_Recurso do \_ sombreador do D3D11 BIND \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**\_Destino de \_ renderização de associação D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ de \_ regeração de recursos diversos de recurso \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ associar \_ acesso não ordenado \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   Níveis de mipmap (um ou mais níveis) nos recursos de textura 2D (especificados no membro **MipLevels** de [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   Matrizes de recursos de textura 2D (uma ou mais texturas) (especificado no membro de **matrizes** de [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   [**\_Decodificador de associação D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**\_ \_ \_ Conteúdo multirestricted do recurso D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_ \_ Recurso compartilhado D3D11 misc \_ restrict \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_Driver de \_ \_ \_ recurso compartilhado D3D11 misc restrict \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

> [!Note]  
> Quando **ExtendedResourceSharing** for **true**, você terá mais flexibilidade quando especificar sinalizadores de associação para compartilhar recursos de Texture2D. Não apenas o driver de gráficos e o hardware dão suporte a mais sinalizadores de ligação, mas também a combinações mais possíveis de sinalizadores de associação. Por exemplo, você pode especificar apenas [**D3D11 \_ de \_ \_ destino de processamento de associação**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) ou nenhum sinalizador de associação, e assim por diante.

 

Mesmo se [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) retornar **true** em **ExtendedResourceSharing**, você ainda não poderá compartilhar recursos criados com estes recursos e sinalizadores:

-   [**\_Estêncil de \_ profundidade de associação do D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   recursos de textura 2D no modo de anti-aliasing multiamostra (MSAA) (especificado com o [**\_ exemplo \_ desc de dxgi**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc))
-   [**D3D11 \_ de \_ recursos diversos do recurso \_ \_ fixe**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ USO \_ imutável**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), [**D3D11 \_ uso \_ dinâmico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)ou uso de [**D3D11 \_ de \_ preparo**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) (ou seja, mapeável)
-   [**D3D11 \_ diversos recursos de \_ \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="change-subresources-with-new-copy-options"></a>Alterar os subrecursos com novas opções de cópia

O Direct3D 11,1 permite que você use novos sinalizadores de cópia para copiar e atualizar os subrecursos. Quando você copia um subrecurso, os recursos de origem e de destino podem ser idênticos e as regiões de origem e de destino podem se sobrepor.

Esse recurso do Direct3D 11,1 consiste na API a seguir.

-   [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)
-   [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)

## <a name="discard-resources-and-resource-views"></a>Descartar recursos e exibições de recursos

O Direct3D 11,1 permite descartar recursos e exibições de recursos do contexto do dispositivo. Essa nova funcionalidade informa à GPU que o conteúdo existente em recursos ou exibições de recursos não é mais necessário.

Esse recurso do Direct3D 11,1 consiste na API a seguir.

-   [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource)
-   [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview)
-   [**ID3D11DeviceContext1::D iscardView1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview1)

## <a name="support-a-larger-number-of-uavs"></a>Suporte a um número maior de UAVs

O Direct3D 11,1 permite que você use um número maior de UAVs ao associar recursos ao [estágio de mesclagem de saída](d3d10-graphics-programming-guide-output-merger-stage.md) e ao definir uma matriz de exibições para um recurso não ordenado.

O Direct3D 11,1 atualiza os seguintes métodos para esse recurso.

-   [**ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews)
-   [**ID3D11DeviceContext::CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)

## <a name="bind-a-subrange-of-a-constant-buffer-to-a-shader"></a>Associar um subintervalo de um buffer constante a um sombreador

O Direct3D 11,1 permite associar um subintervalo de um buffer constante a acesso de um sombreador. Você pode fornecer um buffer de constante maior e especificar o subintervalo que o sombreador pode usar.

Esse recurso do Direct3D 11,1 consiste na API a seguir.

-   [**ID3D11DeviceContext1::CSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gssetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hssetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vssetconstantbuffers1)

## <a name="retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader"></a>Recuperar o subintervalo de um buffer constante que está associado a um sombreador

O Direct3D 11,1 permite recuperar o subintervalo de um buffer constante associado a um sombreador.

Esse recurso do Direct3D 11,1 consiste na API a seguir.

-   [**ID3D11DeviceContext1::CSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-csgetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-psgetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vsgetconstantbuffers1)

## <a name="clear-all-or-part-of-a-resource-view"></a>Limpar todo ou parte de um modo de exibição de recurso

O Direct3D 11,1 permite que você desmarque uma exibição de recurso (RTV, UAV ou qualquer exibição de vídeo de uma superfície de Texture2D). Você aplica o mesmo valor de cor a todas as partes da exibição.

Esse recurso do Direct3D 11,1 consiste na API a seguir.

-   [**ID3D11DeviceContext1::ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview)

## <a name="map-srvs-of-dynamic-buffers-with-no_overwrite"></a>Mapear SRVs de buffers dinâmicos sem \_ substituição

O Direct3D 11,1 permite mapear os modos de exibição de recurso do sombreador (SRV) de buffers dinâmicos com D3D11 \_ map \_ Write \_ sem \_ substituição. Os tempos de execução do Direct3D 11 e anteriores limitam o mapeamento para os buffers de vértice ou de índice.

O Direct3D 11,1 atualiza o método [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) para esse recurso.

## <a name="use-uavs-at-every-pipeline-stage"></a>Usar UAVs em cada estágio do pipeline

O Direct3D 11,1 permite que você use as seguintes instruções do modelo de sombreador 5,0 em todos os estágios do sombreador que foram usados anteriormente em sombreadores apenas de pixel e sombreadores de computação.

-   [\_UAV DCL \_ digitado](/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-)
-   [DCL \_ UAV \_ bruto](/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-)
-   [UAV de DCL \_ \_ estruturado](/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-)
-   [LD \_ bruto](/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-)
-   [LD \_ estruturada](/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-)
-   [LD \_ UAV de \_ tipos](/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-)
-   [armazenamento \_ bruto](/windows/desktop/direct3dhlsl/store-raw--sm5---asm-)
-   [armazenamento \_ estruturado](/windows/desktop/direct3dhlsl/store-structured--sm5---asm-)
-   [armazenar \_ UAV \_ tipado](/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-)
-   [sincronizar \_ uglobal](/windows/desktop/direct3dhlsl/sync--sm5---asm-)
-   Todos os Atomics e Atomics imediatos (por exemplo, [Atomic \_ e](/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-) and [IMM \_ Atomic \_ e](/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-))

O Direct3D 11,1 atualiza os seguintes métodos para esse recurso.

-   [**ID3D11DeviceContext::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**ID3D11DeviceContext::CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**ID3D11DeviceContext::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**ID3D11DeviceContext::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**ID3D11DeviceContext::CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Essas instruções existiam no Direct3D 11,0 no PS \_ 5 \_ 0 e cs \_ 5 \_ 0. Como o Direct3D 11,1 torna o UAVs disponível em todos os estágios do sombreador, essas instruções estão disponíveis em todos os estágios do sombreador.

Se você passar sombreadores compilados (VS/HS/DS/HS) que usam qualquer uma dessas instruções para uma função CREATE-Shader, como [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader), em dispositivos que não dão suporte a UAVs em todos os estágios (incluindo drivers existentes que não são implementados com esse recurso), a função CREATE-Shader falhará. A função CREATE-Shader também falhará se o sombreador tentar usar um slot UAV além do conjunto de Slots UAV aos quais o hardware dá suporte.

Os UAVs que são referenciados por essas instruções são compartilhados entre todos os estágios de pipeline. Por exemplo, um UAV que está associado ao slot 0 no [estágio output-merger](d3d10-graphics-programming-guide-output-merger-stage.md) está disponível no slot 0 para vs/HS/DS/GS/PS.

Os acessos UAV que você emite de dentro ou entre os estágios de sombreador que são executados em um determinado empate \* () ou que você emite do sombreador de computação dentro de um despacho \* () não são garantidos para serem concluídos na ordem em que você os emitiu. Mas todos os acessos do UAV são concluídos no final do draw \* () ou expedição \* ().

## <a name="extended-support-for-warp-devices"></a>Suporte estendido para dispositivos WARP

O Direct3D 11,1 estende o suporte para dispositivos [Warp](overviews-direct3d-11-devices-create-warp.md) , que você cria passando o [**tipo de driver do D3D \_ \_ \_ Warp**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) no parâmetro *driverType* de [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice).

Começando com suporte a dispositivos Direct3D 11,1 WARP:

-   Todos os [níveis de recurso](overviews-direct3d-11-devices-downlevel-intro.md) do Direct3D de 9,1 até 11,1
-   [Sombreadores de computação](direct3d-11-advanced-stages-compute-shader.md) e [mosaico](direct3d-11-advanced-stages-tessellation.md)
-   Superfícies compartilhadas. Ou seja, você pode compartilhar totalmente as superfícies entre os dispositivos Warp, bem como entre os dispositivos distorcedores em processos diferentes.

Os dispositivos dewarp não oferecem suporte a estes recursos opcionais:

-   [dobra](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)
-   [codificação ou decodificação de vídeo](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)
-   [suporte mínimo para sombreador de precisão](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)

Quando você executa uma VM (máquina virtual), o Hyper-V, com sua GPU (unidade de processamento gráfico) desabilitada ou sem um driver de vídeo, você obtém um dispositivo de detorção cujo nome amigável é "adaptador de vídeo básico da Microsoft". Esse dispositivo WARP pode executar a experiência completa do Windows, que inclui DWM, Internet Explorer e aplicativos da Windows Store. Esse dispositivo WARP também dá suporte à execução de aplicativos herdados que usam o [DirectDraw](/windows/desktop/directdraw/directdraw) ou aplicativos em execução que usam o Direct3D 3 por meio do Direct3D 11,1.

## <a name="use-direct3d-in-session-0-processes"></a>Usar Direct3D nos processos da sessão 0

A partir do Windows 8 e do Windows Server 2012, você pode usar a maioria das APIs do Direct3D nos processos da sessão 0.

> [!Note]  
> Essas APIs de saída, janela, Cadeia de permuta e de apresentação não estão disponíveis nos processos da sessão 0 porque não se aplicam ao ambiente da sessão 0:
>
> -   [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)
> -   [**IDXGIFactory::GetWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-getwindowassociation)
> -   [**IDXGIFactory::MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation)
> -   [**IDXGIAdapter::EnumOutputs**](/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs)
> -   [**ID3D11Debug::SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)
> -   [**ID3D11Debug::SetPresentPerRenderOpDelay**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setpresentperrenderopdelay)
> -   [**ID3D11Debug::SetSwapChain**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setswapchain)
> -   [**ID3D10Debug::SetFeatureMask**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setfeaturemask)
> -   [**ID3D10Debug::SetPresentPerRenderOpDelay**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setpresentperrenderopdelay)
> -   [**ID3D10Debug::SetSwapChain**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setswapchain)
> -   [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdeviceandswapchain)
> -   [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)
> -   [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)
>
> Se você chamar uma das APIs anteriores em um processo da sessão 0, ela retornará [**o \_ erro \_ dxgi \_ não \_ disponível no momento**](/windows/desktop/direct3ddxgi/dxgi-error).

 

## <a name="support-for-shadow-buffer-on-feature-level-9"></a>Suporte para buffer de sombra no nível de recurso 9

Use um subconjunto de recursos do Direct3D 10 \_ 0 + Shadow buffer para implementar efeitos de sombra no [nível de recurso](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x. Para obter informações sobre o que você precisa fazer para implementar efeitos de sombra no nível de recurso 9 \_ x, consulte [implementando buffers de sombra para o nível de recurso do Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O que há de novo no Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 