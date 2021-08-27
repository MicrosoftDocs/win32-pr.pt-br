---
title: Indexação dinâmica usando HLSL 5.1
description: O exemplo D3D12DynamicIndexing demonstra alguns dos novos recursos do HLSL disponíveis no Shader Model 5,1 – especialmente a indexação dinâmica e matrizes não associadas – para renderizar a mesma malha várias vezes, sempre processando-a com um material selecionado dinamicamente. Com a indexação dinâmica, os sombreadores agora podem ser indexados em uma matriz sem saber o valor do índice no momento da compilação. Quando combinado com matrizes não associadas, isso adiciona outro nível de indireção e flexibilidade para autores de sombreador e pipelines de arte.
ms.assetid: 9821AEDF-E83D-4034-863A-2B820D9B7455
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc560a71ac602f7c78d41e4805d90cb404c2210790b462fb5353b9e5b3ad48f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529279"
---
# <a name="dynamic-indexing-using-hlsl-51"></a>Indexação dinâmica usando HLSL 5.1

O exemplo **D3D12DynamicIndexing** demonstra alguns dos novos recursos do HLSL disponíveis no Shader Model 5,1 – especialmente a indexação dinâmica e matrizes não associadas – para renderizar a mesma malha várias vezes, sempre processando-a com um material selecionado dinamicamente. Com a indexação dinâmica, os sombreadores agora podem ser indexados em uma matriz sem saber o valor do índice no momento da compilação. Quando combinado com matrizes não associadas, isso adiciona outro nível de indireção e flexibilidade para autores de sombreador e pipelines de arte.

-   [Configurar o sombreador de pixel](#set-up-the-pixel-shader)
-   [Configurar a assinatura raiz](#set-up-the-root-signature)
-   [Criar as texturas](#create-the-textures)
-   [Upload os dados de textura](#upload-the-texture-data)
-   [Carregar a textura difusa](#load-the-diffuse-texture)
-   [Criar uma amostra](#create-a-sampler)
-   [Alterar dinamicamente o índice do parâmetro raiz](#dynamically-change-the-root-parameter-index)
-   [Executar o exemplo](#run-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="set-up-the-pixel-shader"></a>Configurar o sombreador de pixel

Vamos primeiro examinar o próprio sombreador, que neste exemplo é um sombreador de pixel.

``` syntax
Texture2D        g_txDiffuse : register(t0);
Texture2D        g_txMats[]  : register(t1);
SamplerState     g_sampler   : register(s0);

struct PSSceneIn
{
    float4 pos : SV_Position;
    float2 tex : TEXCOORD0;
};

struct MaterialConstants
{
    uint matIndex;  // Dynamically set index for looking up from g_txMats[].
};
ConstantBuffer<MaterialConstants> materialConstants : register(b0, space0);

float4 PSSceneMain(PSSceneIn input) : SV_Target
{
    float3 diffuse = g_txDiffuse.Sample(g_sampler, input.tex).rgb;
    float3 mat = g_txMats[materialConstants.matIndex].Sample(g_sampler, input.tex).rgb;
    return float4(diffuse * mat, 1.0f);
}
```

O recurso de matriz não vinculada é ilustrado pela `g_txMats[]` matriz, pois não especifica um tamanho de matriz. A indexação dinâmica é usada para indexar `g_txMats[]` com `matIndex` , que é definido como uma constante raiz. O sombreador não tem conhecimento do tamanho ou da matriz ou do valor do índice em tempo de compilação. Ambos os atributos são definidos na assinatura raiz do objeto de estado do pipeline usado com o sombreador.

Para aproveitar os recursos de indexação dinâmica no HLSL, é necessário que o sombreador seja compilado com o SM 5,1. Além disso, para fazer uso de matrizes não associadas, o sinalizador de **\_ \_ \_ tabelas de descritor/Enable não associado** também deve ser usado. As opções de linha de comando a seguir são usadas para compilar esse sombreador com a [ferramenta de compilador de efeito](/windows/desktop/direct3dtools/fxc) (FXC):

``` syntax
fxc /Zi /E"PSSceneMain" /Od /Fo"dynamic_indexing_pixel.cso" /ps"_5_1" /nologo /enable_unbounded_descriptor_tables
```

## <a name="set-up-the-root-signature"></a>Configurar a assinatura raiz

Agora, vamos examinar a definição de assinatura raiz, particularmente, como definimos o tamanho da matriz não associada e vinculo uma constante raiz a `matIndex` . Para o sombreador de pixel, definimos três coisas: uma tabela de descritores para SRVs (nossa Texture2Ds), uma tabela de descritores para amostras e uma única constante raiz. A tabela de descritores de nosso SRVs contém `CityMaterialCount + 1` entradas. `CityMaterialCount` é uma constante que define o comprimento de `g_txMats[]` e + 1 é para `g_txDiffuse` . A tabela de descritores de nossos exemplos contém apenas uma entrada e só definimos o valor da constante raiz de 1 32 bits por meio de **InitAsConstants**(...). no método **loadassets** .

``` syntax
 // Create the root signature.
    {
        CD3DX12_DESCRIPTOR_RANGE ranges[3];
        ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1 + CityMaterialCount, 0);  // Diffuse texture + array of materials.
        ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER, 1, 0);
        ranges[2].Init(D3D12_DESCRIPTOR_RANGE_TYPE_CBV, 1, 0);

        CD3DX12_ROOT_PARAMETER rootParameters[4];
        rootParameters[0].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_PIXEL);
        rootParameters[1].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_PIXEL);
        rootParameters[2].InitAsDescriptorTable(1, &ranges[2], D3D12_SHADER_VISIBILITY_VERTEX);
        rootParameters[3].InitAsConstants(1, 0, 0, D3D12_SHADER_VISIBILITY_PIXEL);

        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(_countof(rootParameters), rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }
```



| Fluxo de chamadas                                                             | Parâmetros                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**\_Intervalo do descritor de CD3DX12 \_**](cd3dx12-descriptor-range.md)        | [**\_Tipo de intervalo do descritor D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [**\_Parâmetro raiz \_ CD3DX12**](cd3dx12-root-parameter.md)            | [**\_Visibilidade do sombreador D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [**Desc. de \_ assinatura raiz CD3DX12 \_ \_**](cd3dx12-root-signature-desc.md) | [**\_Sinalizadores de \_ assinatura \_ raiz D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))                                   |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**\_Versão da \_ assinatura \_ raiz do D3D**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-textures"></a>Criar as texturas

O conteúdo de `g_txMats[]` são texturas geradas por procedimentos criados em **loadassets**. Cada cidade renderizada na cena compartilha a mesma textura difusa, mas cada uma também tem sua própria textura gerada de procedimento. A matriz de texturas engloba o espectro arco-íris para visualizar facilmente a técnica de indexação.

``` syntax
 // Create the textures and sampler.
    {
        // Procedurally generate an array of textures to use as city materials.
        {
            // All of these materials use the same texture desc.
            D3D12_RESOURCE_DESC textureDesc = {};
            textureDesc.MipLevels = 1;
            textureDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
            textureDesc.Width = CityMaterialTextureWidth;
            textureDesc.Height = CityMaterialTextureHeight;
            textureDesc.Flags = D3D12_RESOURCE_FLAG_NONE;
            textureDesc.DepthOrArraySize = 1;
            textureDesc.SampleDesc.Count = 1;
            textureDesc.SampleDesc.Quality = 0;
            textureDesc.Dimension = D3D12_RESOURCE_DIMENSION_TEXTURE2D;

            // The textures evenly span the color rainbow so that each city gets
            // a different material.
            float materialGradStep = (1.0f / static_cast<float>(CityMaterialCount));

            // Generate texture data.
            vector<vector<unsigned char>> cityTextureData;
            cityTextureData.resize(CityMaterialCount);
            for (int i = 0; i < CityMaterialCount; ++i)
            {
                CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
                ThrowIfFailed(m_device->CreateCommittedResource(
                    &heapProps,
                    D3D12_HEAP_FLAG_NONE,
                    &textureDesc,
                    D3D12_RESOURCE_STATE_COPY_DEST,
                    nullptr,
                    IID_PPV_ARGS(&m_cityMaterialTextures[i])));

                // Fill the texture.
                float t = i * materialGradStep;
                cityTextureData[i].resize(CityMaterialTextureWidth * CityMaterialTextureHeight * CityMaterialTextureChannelCount);
                for (int x = 0; x < CityMaterialTextureWidth; ++x)
                {
                    for (int y = 0; y < CityMaterialTextureHeight; ++y)
                    {
                        // Compute the appropriate index into the buffer based on the x/y coordinates.
                        int pixelIndex = (y * CityMaterialTextureChannelCount * CityMaterialTextureWidth) + (x * CityMaterialTextureChannelCount);

                        // Determine this row's position along the rainbow gradient.
                        float tPrime = t + ((static_cast<float>(y) / static_cast<float>(CityMaterialTextureHeight)) * materialGradStep);

                        // Compute the RGB value for this position along the rainbow
                        // and pack the pixel value.
                        XMVECTOR hsl = XMVectorSet(tPrime, 0.5f, 0.5f, 1.0f);
                        XMVECTOR rgb = XMColorHSLToRGB(hsl);
                        cityTextureData[i][pixelIndex + 0] = static_cast<unsigned char>((255 * XMVectorGetX(rgb)));
                        cityTextureData[i][pixelIndex + 1] = static_cast<unsigned char>((255 * XMVectorGetY(rgb)));
                        cityTextureData[i][pixelIndex + 2] = static_cast<unsigned char>((255 * XMVectorGetZ(rgb)));
                        cityTextureData[i][pixelIndex + 3] = 255;
                    }
                }
            }
        }
```



<table>
<thead>
<tr class="header">
<th>Fluxo de chamadas</th>
<th>Parâmetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a><br />
<a href=""></a>[<strong>D3D12_RESOURCE_DIMENSION</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_dimension)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a><br />
<a href=""></a>[<strong>D3D12_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_flags)<br />
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a><br />
<a href=""></a>[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/dxmath/xmvector-data-type"><strong>XMVECTOR</strong></a></td>
<td><dl><a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorset"><strong>XMVectorSet</strong></a><br />
<a href=""></a>[<strong>XMColorHSLToRGB</strong>] (/windows/desktop/api/directxmath/nf-directxmath-xmcolorhsltorgb)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="upload-the-texture-data"></a>Upload os dados de textura

Os dados de textura são carregados na GPU por meio de um heap de carregamento e SRVs são criados para cada e armazenados em um heap de descritor SRV.

``` syntax
         // Upload texture data to the default heap resources.
            {
                const UINT subresourceCount = textureDesc.DepthOrArraySize * textureDesc.MipLevels;
                const UINT64 uploadBufferStep = GetRequiredIntermediateSize(m_cityMaterialTextures[0].Get(), 0, subresourceCount); // All of our textures are the same size in this case.
                const UINT64 uploadBufferSize = uploadBufferStep * CityMaterialCount;
                CD3DX12_HEAP_PROPERTIES uploadHeap(D3D12_HEAP_TYPE_UPLOAD);
                auto uploadDesc = CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize);
                ThrowIfFailed(m_device->CreateCommittedResource(
                    &uploadHeap,
                    D3D12_HEAP_FLAG_NONE,
                    &uploadDesc,
                    D3D12_RESOURCE_STATE_GENERIC_READ,
                    nullptr,
                    IID_PPV_ARGS(&materialsUploadHeap)));

                for (int i = 0; i < CityMaterialCount; ++i)
                {
                    // Copy data to the intermediate upload heap and then schedule 
                    // a copy from the upload heap to the appropriate texture.
                    D3D12_SUBRESOURCE_DATA textureData = {};
                    textureData.pData = &cityTextureData[i][0];
                    textureData.RowPitch = static_cast<LONG_PTR>((CityMaterialTextureChannelCount * textureDesc.Width));
                    textureData.SlicePitch = textureData.RowPitch * textureDesc.Height;

                    UpdateSubresources(m_commandList.Get(), m_cityMaterialTextures[i].Get(), materialsUploadHeap.Get(), i * uploadBufferStep, 0, subresourceCount, &textureData);
                    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_cityMaterialTextures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE);
                    m_commandList->ResourceBarrier(1, &barrier);
                }
            }
```



<table>
<thead>
<tr class="header">
<th>Fluxo de chamadas</th>
<th>Parâmetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a><br />
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></td>

</tr>
<tr class="even">
<td><a href="updatesubresources1.md"><strong>UpdateSubresources</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>
<td><dl><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="load-the-diffuse-texture"></a>Carregar a textura difusa

A textura difusa, g \_ `txDiffuse` , é carregada de maneira semelhante e também obtém seu próprio SRV, mas os dados de textura já estão definidos em occcity. bin.

``` syntax
// Load the occcity diffuse texture with baked-in ambient lighting.
        // This texture will be blended with a texture from the materials
        // array in the pixel shader.
        {
            D3D12_RESOURCE_DESC textureDesc = {};
            textureDesc.MipLevels = SampleAssets::Textures[0].MipLevels;
            textureDesc.Format = SampleAssets::Textures[0].Format;
            textureDesc.Width = SampleAssets::Textures[0].Width;
            textureDesc.Height = SampleAssets::Textures[0].Height;
            textureDesc.Flags = D3D12_RESOURCE_FLAG_NONE;
            textureDesc.DepthOrArraySize = 1;
            textureDesc.SampleDesc.Count = 1;
            textureDesc.SampleDesc.Quality = 0;
            textureDesc.Dimension = D3D12_RESOURCE_DIMENSION_TEXTURE2D;

            CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &heapProps,
                D3D12_HEAP_FLAG_NONE,
                &textureDesc,
                D3D12_RESOURCE_STATE_COPY_DEST,
                nullptr,
                IID_PPV_ARGS(&m_cityDiffuseTexture)));

            const UINT subresourceCount = textureDesc.DepthOrArraySize * textureDesc.MipLevels;
            const UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_cityDiffuseTexture.Get(), 0, subresourceCount);
            CD3DX12_HEAP_PROPERTIES uploadHeap(D3D12_HEAP_TYPE_UPLOAD);
            auto uploadDesc = CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &uploadHeap,
                D3D12_HEAP_FLAG_NONE,
                &uploadDesc,
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&textureUploadHeap)));

            // Copy data to the intermediate upload heap and then schedule 
            // a copy from the upload heap to the diffuse texture.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pMeshData + SampleAssets::Textures[0].Data[0].Offset;
            textureData.RowPitch = SampleAssets::Textures[0].Data[0].Pitch;
            textureData.SlicePitch = SampleAssets::Textures[0].Data[0].Size;

            UpdateSubresources(m_commandList.Get(), m_cityDiffuseTexture.Get(), textureUploadHeap.Get(), 0, 0, subresourceCount, &textureData);
            auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_cityDiffuseTexture.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE);
            m_commandList->ResourceBarrier(1, &barrier);
        }
```



<table>
<thead>
<tr class="header">
<th>Fluxo de chamadas</th>
<th>Parâmetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension"><strong>D3D12_RESOURCE_DIMENSION</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a><br />
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a><br />
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>
<td><dl><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="create-a-sampler"></a>Criar uma amostra

Por fim, para **Loadassets**, uma única amostra é criada para amostragem da textura difusa ou da matriz de textura.

``` syntax
 // Describe and create a sampler.
        D3D12_SAMPLER_DESC samplerDesc = {};
        samplerDesc.Filter = D3D12_FILTER_MIN_MAG_MIP_LINEAR;
        samplerDesc.AddressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.AddressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.AddressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.MinLOD = 0;
        samplerDesc.MaxLOD = D3D12_FLOAT32_MAX;
        samplerDesc.MipLODBias = 0.0f;
        samplerDesc.MaxAnisotropy = 1;
        samplerDesc.ComparisonFunc = D3D12_COMPARISON_FUNC_ALWAYS;
        m_device->CreateSampler(&samplerDesc, m_samplerHeap->GetCPUDescriptorHandleForHeapStart());

        // Create SRV for the city's diffuse texture.
        CD3DX12_CPU_DESCRIPTOR_HANDLE srvHandle(m_cbvSrvHeap->GetCPUDescriptorHandleForHeapStart(), 0, m_cbvSrvDescriptorSize);
        D3D12_SHADER_RESOURCE_VIEW_DESC diffuseSrvDesc = {};
        diffuseSrvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        diffuseSrvDesc.Format = SampleAssets::Textures->Format;
        diffuseSrvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        diffuseSrvDesc.Texture2D.MipLevels = 1;
        m_device->CreateShaderResourceView(m_cityDiffuseTexture.Get(), &diffuseSrvDesc, srvHandle);
        srvHandle.Offset(m_cbvSrvDescriptorSize);

        // Create SRVs for each city material.
        for (int i = 0; i < CityMaterialCount; ++i)
        {
            D3D12_SHADER_RESOURCE_VIEW_DESC materialSrvDesc = {};
            materialSrvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
            materialSrvDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
            materialSrvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
            materialSrvDesc.Texture2D.MipLevels = 1;
            m_device->CreateShaderResourceView(m_cityMaterialTextures[i].Get(), &materialSrvDesc, srvHandle);

            srvHandle.Offset(m_cbvSrvDescriptorSize);
        }   
```



<table>
<thead>
<tr class="header">
<th>Fluxo de chamadas</th>
<th>Parâmetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc"><strong>D3D12_SAMPLER_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter"><strong>D3D12_FILTER</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode"></a><br />
D3D12_FLOAT32_MAX (<a href="constants.md"><strong>constantes</strong></a>)<br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func"><strong>D3D12_COMPARISON_FUNC</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler"><strong>CreateSampler</strong></a></td>

</tr>
<tr class="odd">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></td>
<td><dl><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></td>
<td><dl><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a><br />
<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></td>

</tr>
</tbody>
</table>



 

## <a name="dynamically-change-the-root-parameter-index"></a>Alterar dinamicamente o índice do parâmetro raiz

Se tivéssemos de renderizar a cena agora, todas as cidades apareceriam as mesmas, porque não definimos o valor da nossa constante raiz, `matIndex` . Cada sombreador de pixel seria indexado no slot 0º de `g_txMats` e a cena ficaria assim:

![todas as cidades aparecem na mesma cor](images/dynamicindexing-image1.png)

O valor da constante raiz é definido em **FrameResource::P opulatecommandlists**. No loop **for** duplo em que um comando Draw é registrado para cada cidade, registramos uma chamada para [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants) especificando nosso índice de parâmetro raiz em relação à assinatura raiz – neste caso, 3 – o valor do índice dinâmico e um deslocamento – nesse caso, 0. Como o comprimento de `g_txMats` é igual ao número de cidades que renderizamos, o valor do índice é definido incrementalmente para cada cidade.

``` syntax
 for (UINT i = 0; i < m_cityRowCount; i++)
    {
        for (UINT j = 0; j < m_cityColumnCount; j++)
        {
            pCommandList->SetPipelineState(pPso);

            // Set the city's root constant for dynamically indexing into the material array.
            pCommandList->SetGraphicsRoot32BitConstant(3, (i * m_cityColumnCount) + j, 0);

            // Set this city's CBV table and move to the next descriptor.
            pCommandList->SetGraphicsRootDescriptorTable(2, cbvSrvHandle);
            cbvSrvHandle.Offset(cbvSrvDescriptorSize);

            pCommandList->DrawIndexedInstanced(numIndices, 1, 0, 0, 0);
        }
    }
```



| Fluxo de chamadas                                                                                          | Parâmetros |
|----------------------------------------------------------------------------------------------------|------------|
| [**SetPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)                             |            |
| [**SetGraphicsRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)     |            |
| [**SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) |            |
| [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)                     |            |

## <a name="run-the-sample"></a>Execute o exemplo

Agora, quando renderizamos a cena, cada cidade terá um valor diferente `matIndex` e, portanto, procurará uma textura diferente de `g_txMats[]` fazer com que a cena se pareça com esta:

![todas as cidades aparecem em cores diferentes](images/dynamicindexing-image2.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia detalhado do código D3D12](d3d12-code-walk-throughs.md)
</dt> <dt>

[Efeito-ferramenta do compilador](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[Recursos do HLSL Shader Model 5,1 para Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Associação de recursos no HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Modelo do sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Como especificar assinaturas raiz no HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>
