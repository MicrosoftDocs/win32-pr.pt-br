---
title: Recursos do Direct3D 11.1
description: A funcionalidade a seguir foi adicionada ao Direct3D 11.1, que está incluído no Windows 8, Windows RT e Windows Server 2012.
ms.assetid: 2203D2D2-ECF6-4753-90FA-12A52678DFBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee5f4721a9f7ef7727539387603e839f36690ed5d4b6762121ceddefa0672ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535961"
---
# <a name="direct3d-111-features"></a>Recursos do Direct3D 11.1

A funcionalidade a seguir foi adicionada ao Direct3D 11.1, que está incluído no Windows 8, Windows RT e Windows Server 2012. O suporte parcial para [o Direct3D 11.1](direct3d-11-features.md) está disponível no Windows 7 e no Windows Server 2008 R2 por meio da Atualização da Plataforma [para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), que está disponível por meio da Atualização da Plataforma [para Windows 7](https://support.microsoft.com/kb/2670838).

-   [Aprimoramentos do compilador e rastreamento do sombreador](#shader-tracing-and-compiler-enhancements)
-   [Compartilhamento de dispositivo Direct3D](#direct3d-device-sharing)
-   [Verificar o suporte de novos recursos e formatos do Direct3D 11.1](#check-support-of-new-direct3d-111-features-and-formats)
-   [Usar precisão mínima de HLSL](#use-hlsl-minimum-precision)
-   [Especificar planos de clipe de usuário em HLSL no nível de recurso 9 e superior](#specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Criar buffers constantes maiores do que um sombreador pode acessar](#create-larger-constant-buffers-than-a-shader-can-access)
-   [Usar operações lógicas em um destino de renderização](#use-logical-operations-in-a-render-target)
-   [Forçar a contagem de exemplos para criar um estado de rasterizador](#force-the-sample-count-to-create-a-rasterizer-state)
-   [Processar recursos de vídeo com sombreadores](#process-video-resources-with-shaders)
-   [Suporte estendido para recursos texture2D compartilhados](#extended-support-for-shared-texture2d-resources)
-   [Alterar sub-recursos com novas opções de cópia](#change-subresources-with-new-copy-options)
-   [Descartar recursos e exibições de recursos](#discard-resources-and-resource-views)
-   [Dar suporte a um número maior de UAVs](#support-a-larger-number-of-uavs)
-   [Vincular um subrange de um buffer constante a um sombreador](#bind-a-subrange-of-a-constant-buffer-to-a-shader)
-   [Recuperar o subrange de um buffer constante que está vinculado a um sombreador](#retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader)
-   [Limpar todo ou parte de uma exibição de recurso](#clear-all-or-part-of-a-resource-view)
-   [Mapear SRVs de buffers dinâmicos sem \_ OVERWRITE](/windows)
-   [Usar UAVs em cada estágio de pipeline](#use-uavs-at-every-pipeline-stage)
-   [Suporte estendido para dispositivos WARP](#extended-support-for-warp-devices)
-   [Usar o Direct3D em processos da Sessão 0](#use-direct3d-in-session-0-processes)
-   [Suporte para buffer de sombra no nível de recurso 9](#support-for-shadow-buffer-on-feature-level-9)
-   [Tópicos relacionados](#related-topics)

## <a name="shader-tracing-and-compiler-enhancements"></a>Aprimoramentos do compilador e rastreamento do sombreador

O Direct3D 11.1 permite que você use o rastreamento de sombreador para garantir que seu código está executando conforme o esperado e, se não for, você poderá descobrir e corrigir o problema. O Windows SDK (Software Development Kit) para Windows 8 contém aprimoramentos do compilador HLSL. O rastreamento de sombreador e o compilador HLSL são implementados em D3dcompiler \_nn.dll.

A API de rastreamento de sombreador e os aprimoramentos para o compilador HLSL consistem nos métodos e funções a seguir.

-   [**ID3D11RefDefaultTrackingOptions::SetTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions)
-   [**ID3D11RefTrackingOptions::SetTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11reftrackingoptions-settrackingoptions)
-   [**ID3D11TracingDevice::SetShaderTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11TracingDevice::SetShaderTrackingOptionsByType**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11ShaderTraceFactory::CreateShaderTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace)
-   [**ID3D11ShaderTrace::TraceReady**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-traceready)
-   [**ID3D11ShaderTrace::ResetTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-resettrace)
-   [**ID3D11ShaderTrace::GetTraceStats**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-gettracestats)
-   [**ID3D11ShaderTrace::P SSelectStamp**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-psselectstamp)
-   [**ID3D11ShaderTrace::GetInitialRegisterContents**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents)
-   [**ID3D11ShaderTrace::GetStep**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getstep)
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

A biblioteca D3dcompiler.lib requer D3dcompiler \_nn.dll. Essa DLL não faz parte do Windows 8; ele está na pasta bin do SDK do Windows para Windows 8 juntamente com a Fxc.exe de linha de comando do \\ compilador HLSL.

> [!Note]  
> Embora você possa usar essa biblioteca e a combinação de DLL para desenvolvimento, não é possível implantar aplicativos Windows Store que usam essa combinação. Portanto, você deve compilar sombreadores HLSL antes de enviar seu aplicativo Windows Store. Você pode gravar binários de compilação HLSL no disco ou o compilador pode gerar os headers com matrizes de byte estáticos que contêm os dados do blob do sombreador. Use a interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) para acessar os dados do blob. Para desenvolver seu aplicativo Windows Store, chame [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2) ou [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) para compilar a origem HLSL bruta e, em seguida, alimente os dados de blob resultantes para o Direct3D.

 

## <a name="direct3d-device-sharing"></a>Compartilhamento de dispositivo Direct3D

O Direct3D 11.1 permite que as APIs do Direct3D 10 e as APIs do Direct3D 11 usem um dispositivo de renderização subjacente.

Esse recurso direct3D 11.1 consiste nos métodos e interface a seguir.

-   [**ID3D11Device1::CreateDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate)
-   [**ID3D11DeviceContext1::SwapDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate)
-   [**ID3DDeviceContextState**](/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate)

## <a name="check-support-of-new-direct3d-111-features-and-formats"></a>Verificar o suporte de novos recursos e formatos do Direct3D 11.1

O Direct3D 11.1 permite verificar se há novos recursos aos quais o driver gráfico pode dar suporte e novas maneiras de dar suporte a um formato em um dispositivo. O Microsoft DirectX Graphic Infrastructure (DXGI) 1.2 também especifica novos [**valores DXGI \_ FORMAT.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Esse recurso do Direct3D 11.1 consiste na API a seguir.

-   [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) com [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPÇÕES**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), [**D3D11 \_ FEATURE DATA ARCHITECTURE \_ \_ \_ INFO**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info), [**D3D11 \_ FEATURE DATA \_ \_ D3D9 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options), [**D3D11 \_ FEATURE DATA \_ \_ SHADER MIN PRECISION \_ \_ \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)e [**D3D11 \_ FEATURE DATA \_ \_ D3D9 \_ SHADOW \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support) SUPPORT STRUCTURES
-   [**ID3D11Device::CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) com SAÍDA DO [**\_ \_ \_ \_ DECODIFICADOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)DE SUPORTE AO FORMATO D3D11 , SAÍDA DO PROCESSADOR DE VÍDEO DE SUPORTE AO FORMATO [**D3D11 \_ \_ \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), SUPORTE AO FORMATO [**D3D11 ENTRADA DO PROCESSADOR DE VÍDEO \_ \_ \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**D3D11 \_ FORMAT SUPPORT2 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support) [**OUTPUT MERGER LOGIC \_ \_ \_ \_ \_ \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)

## <a name="use-hlsl-minimum-precision"></a>Usar precisão mínima de HLSL

Começando com Windows 8, os drivers gráficos podem implementar tipos de dados escalares [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) de precisão mínima usando qualquer precisão maior ou igual à precisão de bit especificada. Quando o código do sombreador de precisão mínima HLSL é usado em hardware que implementa a precisão mínima de HLSL, você usa menos largura de banda de memória e, como resultado, você também usa menos energia do sistema.

Você pode consultar o suporte mínimo de precisão que o driver gráfico fornece chamando [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) com o valor [**D3D11 \_ FEATURE \_ SHADER \_ MIN PRECISION \_ \_ SUPPORT.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) Nesta chamada **ID3D11Device::CheckFeatureSupport,** passe um ponteiro para uma estrutura [**D3D11 \_ FEATURE DATA \_ \_ \_ SHADER MIN \_ PRECISION \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support) que **ID3D11Device::CheckFeatureSupport** preenche com os níveis mínimos de precisão aos quais o driver dá suporte para o estágio do sombreador de pixel e para outros estágios do sombreador. As informações retornadas apenas indicam que o hardware gráfico pode executar operações HLSL com uma precisão menor do que a precisão float de 32 bits padrão, mas não garante que o hardware gráfico realmente será executado com uma precisão mais baixa.

Você não precisa autor de vários sombreadores que usam e não usam precisão mínima. Em vez disso, crie sombreadores com precisão mínima e as variáveis de precisão mínima se comportarão com precisão total de 32 bits se o driver de gráficos relata que ele não dá suporte a nenhuma precisão mínima. Para obter mais informações sobre a precisão mínima de HLSL, consulte [Usando precisão mínima HLSL.](/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision)

Sombreadores de precisão mínima HLSL não funcionam em sistemas operacionais anteriores ao Windows 8.

## <a name="specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Especificar planos de clipe de usuário em HLSL no nível de recurso 9 e superior

A partir do Windows 8, você pode usar o atributo de função [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-syntax) **clipplanes** em uma declaração de função HLSL em vez de [SV \_ ClipDistance](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) para fazer com que o sombreador funcione no nível [do](overviews-direct3d-11-devices-downlevel-intro.md) recurso 9 x, bem como no nível de \_ recurso 10 e superior. Para obter mais informações, consulte [Planos de clipe de usuário no hardware de nível de recurso 9.](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)

## <a name="create-larger-constant-buffers-than-a-shader-can-access"></a>Criar buffers constantes maiores do que um sombreador pode acessar

O Direct3D 11.1 permite que você crie buffers constantes maiores que o tamanho máximo do buffer constante que um sombreador pode acessar (constantes de 4 componentes de 32 bits de 4 bits – \* 64KB). Posteriormente, ao vincular os buffers ao pipeline, por exemplo, por meio de [**PSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers) ou [**PSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1), você pode especificar um intervalo de buffers que o sombreador pode acessar que se ajuste ao limite 4096.

O Direct3D 11.1 atualiza o [**método ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) para esse recurso.

## <a name="use-logical-operations-in-a-render-target"></a>Usar operações lógicas em um destino de renderização

O Direct3D 11.1 permite usar operações lógicas em vez de mesclar em um destino de renderização. No entanto, você não pode misturar operações lógicas com a combinação entre vários destinos de renderização.

Esse recurso do Direct3D 11.1 consiste na API a seguir.

-   [**ID3D11Device1::CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1) com [ **D3D11 \_ LOGIC \_ OP**](/windows/desktop/api/D3D11_1/ne-d3d11_1-d3d11_logic_op)

## <a name="force-the-sample-count-to-create-a-rasterizer-state"></a>Forçar a contagem de exemplos para criar um estado de rasterizador

O Direct3D 11.1 permite especificar uma contagem de amostras de força ao criar um estado de rasterizador.

Esse recurso do Direct3D 11.1 consiste na API a seguir.

-   [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)

> [!Note]  
>
> Se você quiser renderizar com a contagem de exemplo forçada para 1 ou superior, siga estas diretrizes:
>
> -   Não a bind depth-stencil views.
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

O Direct3D 11,1 garante que você possa compartilhar recursos Texture2D criados com tipos e formatos de recursos específicos. para compartilhar recursos do Texture2D, use o recurso [**D3D11 \_ \_ misc \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)compartilhado, o [**D3D11 \_ \_ misc \_ \_ compartilhado**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)do recurso, ou uma combinação dos sinalizadores D3D11 do **\_ recurso \_ \_ \_** KEYEDMUTEX dishare e D3D11 [**\_ \_ \_ multishared \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) NTHANDLE (novo para Windows 8) ao criar esses recursos.

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
-   [**D3D11 \_ RESOURCE \_ MISC \_ RESTRICT \_ SHARED \_ RESOURCE \_ DRIVER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

> [!Note]  
> Quando **ExtendedResourceSharing** é **TRUE,** você tem mais flexibilidade ao especificar sinalizadores de vinculação para compartilhar recursos Texture2D. O driver de gráfico e o hardware não só suportam mais sinalizadores de associação, mas também mais combinações possíveis de sinalizadores de associação. Por exemplo, você pode especificar apenas [**D3D11 \_ BIND RENDER TARGET \_ \_ ou**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) nenhum sinalizador de vinculação e assim por diante.

 

Mesmo que [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) retorne **TRUE** em **ExtendedResourceSharing,** você ainda não poderá compartilhar recursos criados com esses recursos e sinalizadores:

-   [**ESTÊNCIL DE PROFUNDIDADE \_ \_ DE \_ VINCULAÇÃO D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   Recursos de textura 2D no modo MSAA (multisample antialiasing) (especificado com [**\_ DXGI SAMPLE \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc))
-   [**D3D11 \_ RESOURCE \_ MISC RESOURCE \_ \_ FIX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ USAGE \_ IMMUTABLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)ou [**D3D11 \_ USAGE \_ STAGING**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) (ou seja, mappable)
-   [**TEXTURA MISC DO RECURSO D3D11CUBE \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="change-subresources-with-new-copy-options"></a>Alterar sub-recursos com novas opções de cópia

O Direct3D 11.1 permite que você use novos sinalizadores de cópia para copiar e atualizar sub-recursos. Quando você copia uma sub-fonte, os recursos de origem e destino podem ser idênticos e as regiões de origem e destino podem se sobrepor.

Esse recurso do Direct3D 11.1 consiste na API a seguir.

-   [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)
-   [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)

## <a name="discard-resources-and-resource-views"></a>Descartar recursos e exibições de recursos

O Direct3D 11.1 permite descartar recursos e exibições de recursos do contexto do dispositivo. Essa nova funcionalidade informa à GPU que o conteúdo existente em recursos ou exibições de recursos não são mais necessários.

Esse recurso do Direct3D 11.1 consiste na API a seguir.

-   [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource)
-   [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview)
-   [**ID3D11DeviceContext1::D iscardView1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview1)

## <a name="support-a-larger-number-of-uavs"></a>Dar suporte a um número maior de UAVs

O Direct3D 11.1 permite que você use um número maior [](d3d10-graphics-programming-guide-output-merger-stage.md) de UAVs ao vincular recursos ao estágio de fusão de saída e ao definir uma matriz de exibições para um recurso não organizado.

O Direct3D 11.1 atualiza os métodos a seguir para esse recurso.

-   [**ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews)
-   [**ID3D11DeviceContext::CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)

## <a name="bind-a-subrange-of-a-constant-buffer-to-a-shader"></a>Vincular um subrange de um buffer constante a um sombreador

O Direct3D 11.1 permite que você a bind um subrange de um buffer constante para um sombreador acessar. Você pode fornecer um buffer constante maior e especificar o subconjunto que o sombreador pode usar.

Esse recurso do Direct3D 11.1 consiste na API a seguir.

-   [**ID3D11DeviceContext1::CSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gssetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hssetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vssetconstantbuffers1)

## <a name="retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader"></a>Recuperar o subrange de um buffer constante que está vinculado a um sombreador

O Direct3D 11.1 permite recuperar o subconjunto de um buffer constante que está vinculado a um sombreador.

Esse recurso do Direct3D 11.1 consiste na API a seguir.

-   [**ID3D11DeviceContext1::CSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-csgetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-psgetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vsgetconstantbuffers1)

## <a name="clear-all-or-part-of-a-resource-view"></a>Limpar todo ou parte de uma exibição de recurso

O Direct3D 11.1 permite limpar uma exibição de recurso (RTV, UAV ou qualquer exibição de vídeo de uma superfície Texture2D). Você aplica o mesmo valor de cor a todas as partes da exibição.

Esse recurso do Direct3D 11.1 consiste na API a seguir.

-   [**ID3D11DeviceContext1::ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview)

## <a name="map-srvs-of-dynamic-buffers-with-no_overwrite"></a>Mapear SRVs de buffers dinâmicos sem \_ OVERWRITE

O Direct3D 11.1 permite mapear exibições de recursos do sombreador (SRV) de buffers dinâmicos com D3D11 \_ MAP \_ WRITE NO \_ \_ OVERWRITE. O direct3D 11 e runtimes anteriores limitam o mapeamento para buffers de vértice ou índice.

O Direct3D 11.1 atualiza o [**método ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) para esse recurso.

## <a name="use-uavs-at-every-pipeline-stage"></a>Usar UAVs em cada estágio de pipeline

O Direct3D 11.1 permite que você use as seguintes instruções do modelo de sombreador 5.0 em todos os estágios do sombreador que foram usados anteriormente apenas em sombreadores de pixel e sombreadores de computação.

-   [dcl \_ uav \_ digitado](/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-)
-   [dcl \_ uav \_ bruto](/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-)
-   [dcl \_ uav \_ estruturado](/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-)
-   [ld \_ raw](/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-)
-   [ld \_ estruturado](/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-)
-   [ld \_ uav \_ digitado](/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-)
-   [armazenar \_ bruto](/windows/desktop/direct3dhlsl/store-raw--sm5---asm-)
-   [estruturada \_ pelo armazenamento](/windows/desktop/direct3dhlsl/store-structured--sm5---asm-)
-   [store \_ uav \_ digitado](/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-)
-   [sync \_ uglobal](/windows/desktop/direct3dhlsl/sync--sm5---asm-)
-   Todos os atômicos e atômicos imediatos (por exemplo, [ \_ atômico e](/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-) [e imm \_ \_ atômico e](/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-))

O Direct3D 11.1 atualiza os métodos a seguir para esse recurso.

-   [**ID3D11DeviceContext::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**ID3D11DeviceContext::CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**ID3D11DeviceContext::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**ID3D11DeviceContext::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**ID3D11DeviceContext::CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Essas instruções existiam no Direct3D 11.0 em ps \_ 5 \_ 0 e cs \_ 5 \_ 0. Como o Direct3D 11.1 disponibiliza os UAVs em todos os estágios do sombreador, essas instruções estão disponíveis em todos os estágios do sombreador.

Se você passar sombreadores compilados (VS/HS/DS/HS) que usam qualquer uma dessas instruções para uma função create-shader, como [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader), em dispositivos que não são compatíveis com UAVs em cada estágio (incluindo drivers existentes que não são implementados com esse recurso), a função create-shader falhará. A função create-shader também falhará se o sombreador tentar usar um slot UAV além do conjunto de slots UAV compatíveis com o hardware.

Os UAVs referenciados por essas instruções são compartilhados em todos os estágios de pipeline. Por exemplo, um UAV que está vinculado [](d3d10-graphics-programming-guide-output-merger-stage.md) ao slot 0 no estágio de fusão de saída está disponível no slot 0 para VS/HS/DS/GS/PS.

Os acessos UAV emitidos de dentro ou entre os estágios do sombreador que são executados dentro de um determinado Draw () ou que você em questão no sombreador de computação dentro de um Dispatch () não têm garantia de que serão finalados na ordem em que você os \* \* emitiu. Mas todos os acessos UAV terminam no final do Draw \* () ou dispatch \* ().

## <a name="extended-support-for-warp-devices"></a>Suporte estendido para dispositivos WARP

O Direct3D 11.1 estende o suporte para dispositivos [WARP,](overviews-direct3d-11-devices-create-warp.md) que você cria passando [**D3D \_ DRIVER TYPE \_ \_ WARP**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) no parâmetro *DriverType* [**de D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice).

A partir do Direct3D 11.1, há suporte para dispositivos WARP:

-   Todos os níveis de [recursos do](overviews-direct3d-11-devices-downlevel-intro.md) Direct3D de 9.1 a 11.1
-   [Sombreadores de computação](direct3d-11-advanced-stages-compute-shader.md) e [mosaico](direct3d-11-advanced-stages-tessellation.md)
-   Superfícies compartilhadas. Ou seja, você pode compartilhar totalmente superfícies entre dispositivos WARP, bem como entre dispositivos WARP em processos diferentes.

Os dispositivos WARP não são compatíveis com estes recursos opcionais:

-   [Duplas](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)
-   [codificar ou decodificar vídeo](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)
-   [suporte ao sombreador de precisão mínima](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)

Quando você executar uma VM (máquina virtual), o Hyper-V, com sua GPU (unidade de processamento gráfico) desabilitada ou sem um driver de exibição, você obterá um dispositivo WARP cujo nome amigável é "Adaptador de Exibição Básico da Microsoft". Esse dispositivo WARP pode executar a experiência Windows completa, que inclui aplicativos DWM, Internet Explorer e Windows Store. Esse dispositivo WARP também dá suporte à execução de aplicativos herdados que usam [o DirectDraw](/windows/desktop/directdraw/directdraw) ou aplicativos em execução que usam o Direct3D 3 a Direct3D 11.1.

## <a name="use-direct3d-in-session-0-processes"></a>Usar o Direct3D em processos da Sessão 0

Começando com Windows 8 e Windows Server 2012, você pode usar a maioria das APIs direct3D nos processos da Sessão 0.

> [!Note]  
> Essas APIs relacionadas à saída, à janela, à cadeia de permuta e à apresentação não estão disponíveis nos processos da Sessão 0 porque não se aplicam ao ambiente da Sessão 0:
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

 

 