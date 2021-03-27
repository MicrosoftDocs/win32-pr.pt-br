---
title: Desempacotando e empacotando DXGI_FORMAT para edição de imagem In-Place
description: O \_ arquivo D3DX DXGIFormatConvert. inl contém funções de conversão de formato embutido que você pode usar no sombreador de computação ou sombreador de pixel no hardware do Direct3D 11.
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c613a3f0068537733961b58a8a4c2b4528d21f25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291957"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a>Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place

O \_ arquivo D3DX DXGIFormatConvert. inl contém funções de conversão de formato embutido que você pode usar no sombreador de computação ou sombreador de pixel no hardware do Direct3D 11. Você pode usar essas funções em seu aplicativo para, simultaneamente, ler e gravar em uma textura. Ou seja, você pode executar a edição de imagem in-loco. Para usar essas funções de conversão de formato embutido, inclua o \_ arquivo D3DX DXGIFormatConvert. inl em seu aplicativo.

O UAV (modo de exibição de acesso não ordenado) do Direct3D 11 de um recurso Texture1D, Texture2D ou Texture3D dá suporte a leituras de acesso aleatório e gravações na memória de um sombreador de computação ou sombreador de pixel. No entanto, o Direct3D 11 dá suporte a leitura e gravação simultâneas somente no \_ formato de textura R32 do formato dxgi \_ \_ . Por exemplo, o Direct3D 11 não oferece suporte simultaneamente à leitura e gravação em outros formatos mais úteis, como o formato DXGI \_ \_ R8G8B8A8 \_ UNORM. Você pode usar apenas um UAV para a gravação de acesso aleatório em outros formatos, ou você pode usar apenas um Modo de Exibição de Recursos de sombreador (SRV) para acesso aleatório a leitura de outros formatos. O hardware de conversão de formato não está disponível para ler simultaneamente e gravar em outros formatos.

No entanto, você ainda pode, simultaneamente, ler e gravar em outros formatos, convertendo a textura no formato de \_ textura R32 do formato dxgi \_ \_ ao criar um UAV, desde que o formato original do recurso dê suporte à conversão em \_ formato dxgi \_ R32 \_ uint. A maioria dos formatos de 32 bits por elemento dá suporte à conversão para o \_ formato dxgi \_ R32 \_ uint. Ao converter a textura no formato de \_ textura R32 do formato dxgi \_ \_ quando você cria um UAV, você pode executar, simultaneamente, leituras e gravações na textura, desde que o sombreador execute o desempacotamento de formato manual na leitura e no empacotamento na gravação.

O benefício de converter a textura para o \_ formato de \_ textura R32 uint do formato dxgi \_ é que, posteriormente, você pode usar o formato apropriado (por exemplo, o \_ formato dxgi \_ R16G16 \_ float) com outras exibições na mesma textura, como exibições de destino de renderização (RTVs) ou SRVs. Portanto, o hardware pode executar o desempacotamento e o pacote típicos de formato automático, pode executar a filtragem de textura e assim por diante, em que não há limitações de hardware.

O cenário a seguir requer que um aplicativo execute a seguinte sequência de ações para executar a edição de imagem in-loco.

Suponha que você queira criar uma textura na qual pode usar um sombreador de pixel ou sombreador de computação para executar a edição in-loco e deseja que os dados de textura sejam armazenados em um formato que seja um descendente de um dos seguintes formatos de tipo:

-   \_Tipo de \_ R10G10B10A2 de formato dxgi \_
-   \_Tipo de \_ R8G8B8A8 de formato dxgi \_
-   \_Tipo de \_ B8G8R8A8 de formato dxgi \_
-   \_Tipo de \_ B8G8R8X8 de formato dxgi \_
-   \_Tipo de \_ R16G16 de formato dxgi \_

Por exemplo, o formato \_ dxgi \_ R10G10B10A2 \_ UNORM é um descendente do formato dxgi \_ \_ R10G10B10A2 formato não \_ tipado. Portanto, \_ o formato dxgi \_ R10G10B10A2 \_ UNORM dá suporte ao padrão de uso que é descrito na sequência a seguir. Os formatos que descendem do \_ formato dxgi \_ R32 \_ sem tipo, como \_ o formato dxgi \_ R32 \_ float, são trivialmente compatíveis com a necessidade de qualquer uma das ajuda de conversão de formato descritas na sequência a seguir.

**Para executar a edição de imagem in-loco**

1.  Crie uma textura com o formato dependente sem tipo, especificado no cenário anterior, junto com os sinalizadores de ligação necessários, como D3D11 \_ BIND \_ unordeneted \_ Access \| D3D11 \_ BIND \_ Shader \_ Resource.
2.  Para a edição de imagem in-loco, crie um UAV com o formato \_ do \_ R32 uint de formato dxgi \_ . A API do Direct3D 11 normalmente não permite a conversão entre "famílias" de formato diferente. No entanto, a API do Direct3D 11 faz uma exceção com o formato do \_ R32 uint do formato dxgi \_ \_ .
3.  No sombreador de computação ou sombreador de pixel, use as funções de pacote de formato embutido e desempacotamento apropriadas que são fornecidas no \_ arquivo D3DX DXGIFormatConvert. inl. Por exemplo, suponha que o \_ formato dxgi \_ R32 \_ uint UAV da textura realmente contém o \_ formato dxgi \_ R10G10B10A2 \_ dados formatados UNORM. Depois que o aplicativo lê um UINT do UAV para o sombreador, ele deve chamar a seguinte função para desempacotar o formato de textura:

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    Em seguida, para gravar em UAV no mesmo sombreador, o aplicativo chama a seguinte função para empacotar dados do sombreador em um UINT que o aplicativo pode gravar no UAV:

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  O aplicativo pode, então, criar outros modos de exibição, como SRVs, com o formato necessário. Por exemplo, o aplicativo pode criar um SRV com o formato \_ dxgi \_ R10G10B10A2 \_ UNORM Format se o recurso foi criado como \_ formato dxgi \_ R10G10B10A2 sem \_ tipo. Quando um sombreador acessa esse SRV, o hardware pode executar a conversão automática de tipo como de costume.

> [!Note]  
> Se o sombreador precisar gravar somente em um UAV, ou ler como um SRV, nenhum desses trabalhos de conversão será necessário porque você pode usar o UAVs totalmente tipado ou o SRVs. As funções de conversão de formato fornecidas em D3DX \_ DXGIFormatConvert. inl são potencialmente úteis apenas se você deseja executar a leitura simultânea e gravação em um UAV de uma textura.

 

A seguir está a lista de funções de conversão de formato que estão incluídas no \_ arquivo D3DX DXGIFormatConvert. inl. Essas funções são categorizadas pelo formato DXGI \_ que são descompactadas e empacotadas. Cada um dos formatos com suporte descende de um dos formatos sem tipo listados no cenário anterior e dá suporte à conversão para \_ o formato dxgi \_ R32 \_ uint como um UAV.

<dl> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>\_Formato dxgi \_ R10G10B10A2 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>\_Formato dxgi \_ R10G10B10A2 \_ uint
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>\_Formato dxgi \_ R8G8B8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>\_Formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> A \_ função inexata tipo usa as instruções do sombreador que não têm precisão alta o suficiente para fornecer a resposta exata. A função alternativa usa uma tabela de pesquisa armazenada no sombreador para fornecer uma conversão exata de >flutuante de SRGB.

 

</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>\_Formato dxgi \_ R8G8B8A8 \_ uint
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>\_Formato dxgi \_ R8G8B8A8 \_ SNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>\_Formato dxgi \_ R8G8B8A8 \_ Santo
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>\_Formato dxgi \_ B8G8R8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>\_Formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> A \_ função inexata tipo usa as instruções do sombreador que não têm precisão alta o suficiente para fornecer a resposta exata. A função alternativa usa uma tabela de pesquisa armazenada no sombreador para fornecer uma conversão exata de >flutuante de SRGB.

 

</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>\_Formato dxgi \_ B8G8R8X8 \_ UNORM
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>\_Formato dxgi \_ B8G8R8X8 \_ UNORM \_ sRGB
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> A \_ função inexata tipo usa as instruções do sombreador que não têm precisão alta o suficiente para fornecer a resposta exata. A função alternativa usa uma tabela de pesquisa armazenada no sombreador para fornecer uma conversão exata de >flutuante de SRGB.

 

</dd> <dt>

<span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>\_ \_ Float R16G16 de formato dxgi \_
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>\_Formato dxgi \_ R16G16 \_ UNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>\_Formato dxgi \_ R16G16 \_ uint
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>\_Formato dxgi \_ R16G16 \_ SNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>\_Formato dxgi \_ R16G16 \_ Santo
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




