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
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a><span data-ttu-id="f89f2-103">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="f89f2-103">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>

<span data-ttu-id="f89f2-104">O \_ arquivo D3DX DXGIFormatConvert. inl contém funções de conversão de formato embutido que você pode usar no sombreador de computação ou sombreador de pixel no hardware do Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="f89f2-104">The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="f89f2-105">Você pode usar essas funções em seu aplicativo para, simultaneamente, ler e gravar em uma textura.</span><span class="sxs-lookup"><span data-stu-id="f89f2-105">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="f89f2-106">Ou seja, você pode executar a edição de imagem in-loco.</span><span class="sxs-lookup"><span data-stu-id="f89f2-106">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="f89f2-107">Para usar essas funções de conversão de formato embutido, inclua o \_ arquivo D3DX DXGIFormatConvert. inl em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f89f2-107">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>

<span data-ttu-id="f89f2-108">O UAV (modo de exibição de acesso não ordenado) do Direct3D 11 de um recurso Texture1D, Texture2D ou Texture3D dá suporte a leituras de acesso aleatório e gravações na memória de um sombreador de computação ou sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="f89f2-108">Direct3D 11's Unordered Access View (UAV) of a Texture1D, Texture2D, or Texture3D resource supports random access reads and writes to memory from a compute shader or pixel shader.</span></span> <span data-ttu-id="f89f2-109">No entanto, o Direct3D 11 dá suporte a leitura e gravação simultâneas somente no \_ formato de textura R32 do formato dxgi \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f89f2-109">However, Direct3D 11 supports simultaneously both reading from and writing to only the DXGI\_FORMAT\_R32\_UINT texture format.</span></span> <span data-ttu-id="f89f2-110">Por exemplo, o Direct3D 11 não oferece suporte simultaneamente à leitura e gravação em outros formatos mais úteis, como o formato DXGI \_ \_ R8G8B8A8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="f89f2-110">For example, Direct3D 11 does not support simultaneously both reading from and writing to other, more useful formats, such as DXGI\_FORMAT\_R8G8B8A8\_UNORM.</span></span> <span data-ttu-id="f89f2-111">Você pode usar apenas um UAV para a gravação de acesso aleatório em outros formatos, ou você pode usar apenas um Modo de Exibição de Recursos de sombreador (SRV) para acesso aleatório a leitura de outros formatos.</span><span class="sxs-lookup"><span data-stu-id="f89f2-111">You can use only a UAV to random access write to such other formats, or you can use only a Shader Resource View (SRV) to random access read from such other formats.</span></span> <span data-ttu-id="f89f2-112">O hardware de conversão de formato não está disponível para ler simultaneamente e gravar em outros formatos.</span><span class="sxs-lookup"><span data-stu-id="f89f2-112">Format conversion hardware is not available to simultaneously both read from and write to such other formats.</span></span>

<span data-ttu-id="f89f2-113">No entanto, você ainda pode, simultaneamente, ler e gravar em outros formatos, convertendo a textura no formato de \_ textura R32 do formato dxgi \_ \_ ao criar um UAV, desde que o formato original do recurso dê suporte à conversão em \_ formato dxgi \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="f89f2-113">However, you can still simultaneously both read from and write to such other formats by casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, as long as the original format of the resource supports casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="f89f2-114">A maioria dos formatos de 32 bits por elemento dá suporte à conversão para o \_ formato dxgi \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="f89f2-114">Most 32 bit per element formats support casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="f89f2-115">Ao converter a textura no formato de \_ textura R32 do formato dxgi \_ \_ quando você cria um UAV, você pode executar, simultaneamente, leituras e gravações na textura, desde que o sombreador execute o desempacotamento de formato manual na leitura e no empacotamento na gravação.</span><span class="sxs-lookup"><span data-stu-id="f89f2-115">By casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, you can then simultaneous perform reads and writes to the texture as long as the shader performs manual format unpacking on read and packing on write.</span></span>

<span data-ttu-id="f89f2-116">O benefício de converter a textura para o \_ formato de \_ textura R32 uint do formato dxgi \_ é que, posteriormente, você pode usar o formato apropriado (por exemplo, o \_ formato dxgi \_ R16G16 \_ float) com outras exibições na mesma textura, como exibições de destino de renderização (RTVs) ou SRVs.</span><span class="sxs-lookup"><span data-stu-id="f89f2-116">The benefit of casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format is that later on you can use the appropriate format (for example, DXGI\_FORMAT\_R16G16\_FLOAT) with other views on the same texture, such as Render Target Views (RTVs) or SRVs.</span></span> <span data-ttu-id="f89f2-117">Portanto, o hardware pode executar o desempacotamento e o pacote típicos de formato automático, pode executar a filtragem de textura e assim por diante, em que não há limitações de hardware.</span><span class="sxs-lookup"><span data-stu-id="f89f2-117">Therefore, the hardware can perform the typical automatic format unpack and pack, can perform texture filtering, and so on where there are no hardware limitations.</span></span>

<span data-ttu-id="f89f2-118">O cenário a seguir requer que um aplicativo execute a seguinte sequência de ações para executar a edição de imagem in-loco.</span><span class="sxs-lookup"><span data-stu-id="f89f2-118">The following scenario requires that an application take the following sequence of actions to perform in-place image editing.</span></span>

<span data-ttu-id="f89f2-119">Suponha que você queira criar uma textura na qual pode usar um sombreador de pixel ou sombreador de computação para executar a edição in-loco e deseja que os dados de textura sejam armazenados em um formato que seja um descendente de um dos seguintes formatos de tipo:</span><span class="sxs-lookup"><span data-stu-id="f89f2-119">Suppose you want to make a texture on which you can use a pixel shader or compute shader to perform in-place editing, and you want the texture data to be stored in a format that is a descendant of one of the following TYPELESS formats:</span></span>

-   <span data-ttu-id="f89f2-120">\_Tipo de \_ R10G10B10A2 de formato dxgi \_</span><span class="sxs-lookup"><span data-stu-id="f89f2-120">DXGI\_FORMAT\_R10G10B10A2\_TYPELESS</span></span>
-   <span data-ttu-id="f89f2-121">\_Tipo de \_ R8G8B8A8 de formato dxgi \_</span><span class="sxs-lookup"><span data-stu-id="f89f2-121">DXGI\_FORMAT\_R8G8B8A8\_TYPELESS</span></span>
-   <span data-ttu-id="f89f2-122">\_Tipo de \_ B8G8R8A8 de formato dxgi \_</span><span class="sxs-lookup"><span data-stu-id="f89f2-122">DXGI\_FORMAT\_B8G8R8A8\_TYPELESS</span></span>
-   <span data-ttu-id="f89f2-123">\_Tipo de \_ B8G8R8X8 de formato dxgi \_</span><span class="sxs-lookup"><span data-stu-id="f89f2-123">DXGI\_FORMAT\_B8G8R8X8\_TYPELESS</span></span>
-   <span data-ttu-id="f89f2-124">\_Tipo de \_ R16G16 de formato dxgi \_</span><span class="sxs-lookup"><span data-stu-id="f89f2-124">DXGI\_FORMAT\_R16G16\_TYPELESS</span></span>

<span data-ttu-id="f89f2-125">Por exemplo, o formato \_ dxgi \_ R10G10B10A2 \_ UNORM é um descendente do formato dxgi \_ \_ R10G10B10A2 formato não \_ tipado.</span><span class="sxs-lookup"><span data-stu-id="f89f2-125">For example, the DXGI\_FORMAT\_R10G10B10A2\_UNORM format is a descendant of the DXGI\_FORMAT\_R10G10B10A2\_TYPELESS format.</span></span> <span data-ttu-id="f89f2-126">Portanto, \_ o formato dxgi \_ R10G10B10A2 \_ UNORM dá suporte ao padrão de uso que é descrito na sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="f89f2-126">Therefore, DXGI\_FORMAT\_R10G10B10A2\_UNORM supports the usage pattern that is described in the following sequence.</span></span> <span data-ttu-id="f89f2-127">Os formatos que descendem do \_ formato dxgi \_ R32 \_ sem tipo, como \_ o formato dxgi \_ R32 \_ float, são trivialmente compatíveis com a necessidade de qualquer uma das ajuda de conversão de formato descritas na sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="f89f2-127">Formats that descend from DXGI\_FORMAT\_R32\_TYPELESS, such as DXGI\_FORMAT\_R32\_FLOAT, are trivially supported without requiring any of the format conversion help that is described in the following sequence.</span></span>

<span data-ttu-id="f89f2-128">**Para executar a edição de imagem in-loco**</span><span class="sxs-lookup"><span data-stu-id="f89f2-128">**To perform in-place image editing**</span></span>

1.  <span data-ttu-id="f89f2-129">Crie uma textura com o formato dependente sem tipo, especificado no cenário anterior, junto com os sinalizadores de ligação necessários, como D3D11 \_ BIND \_ unordeneted \_ Access \| D3D11 \_ BIND \_ Shader \_ Resource.</span><span class="sxs-lookup"><span data-stu-id="f89f2-129">Create a texture with the appropriate TYPELESS-dependent format that is specified in the previous scenario together with the required bind flags, such as D3D11\_BIND\_UNORDERED\_ACCESS \| D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
2.  <span data-ttu-id="f89f2-130">Para a edição de imagem in-loco, crie um UAV com o formato \_ do \_ R32 uint de formato dxgi \_ .</span><span class="sxs-lookup"><span data-stu-id="f89f2-130">For in-place image editing, create a UAV with the DXGI\_FORMAT\_R32\_UINT format.</span></span> <span data-ttu-id="f89f2-131">A API do Direct3D 11 normalmente não permite a conversão entre "famílias" de formato diferente.</span><span class="sxs-lookup"><span data-stu-id="f89f2-131">The Direct3D 11 API typically does not allow casting between different format "families."</span></span> <span data-ttu-id="f89f2-132">No entanto, a API do Direct3D 11 faz uma exceção com o formato do \_ R32 uint do formato dxgi \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f89f2-132">However, the Direct3D 11 API makes an exception with the DXGI\_FORMAT\_R32\_UINT format.</span></span>
3.  <span data-ttu-id="f89f2-133">No sombreador de computação ou sombreador de pixel, use as funções de pacote de formato embutido e desempacotamento apropriadas que são fornecidas no \_ arquivo D3DX DXGIFormatConvert. inl.</span><span class="sxs-lookup"><span data-stu-id="f89f2-133">In the compute shader or pixel shader, use the appropriate inline format pack and unpack functions that are provided in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="f89f2-134">Por exemplo, suponha que o \_ formato dxgi \_ R32 \_ uint UAV da textura realmente contém o \_ formato dxgi \_ R10G10B10A2 \_ dados formatados UNORM.</span><span class="sxs-lookup"><span data-stu-id="f89f2-134">For example, suppose the DXGI\_FORMAT\_R32\_UINT UAV of the texture really holds DXGI\_FORMAT\_R10G10B10A2\_UNORM-formatted data.</span></span> <span data-ttu-id="f89f2-135">Depois que o aplicativo lê um UINT do UAV para o sombreador, ele deve chamar a seguinte função para desempacotar o formato de textura:</span><span class="sxs-lookup"><span data-stu-id="f89f2-135">After the application reads a uint from the UAV into the shader, it must call the following function to unpack the texture format:</span></span>

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    <span data-ttu-id="f89f2-136">Em seguida, para gravar em UAV no mesmo sombreador, o aplicativo chama a seguinte função para empacotar dados do sombreador em um UINT que o aplicativo pode gravar no UAV:</span><span class="sxs-lookup"><span data-stu-id="f89f2-136">Then, to write to the UAV in the same shader, the application calls the following function to pack shader data into a uint that the application can write to the UAV:</span></span>

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  <span data-ttu-id="f89f2-137">O aplicativo pode, então, criar outros modos de exibição, como SRVs, com o formato necessário.</span><span class="sxs-lookup"><span data-stu-id="f89f2-137">The application can then create other views, such as SRVs, with the required format.</span></span> <span data-ttu-id="f89f2-138">Por exemplo, o aplicativo pode criar um SRV com o formato \_ dxgi \_ R10G10B10A2 \_ UNORM Format se o recurso foi criado como \_ formato dxgi \_ R10G10B10A2 sem \_ tipo.</span><span class="sxs-lookup"><span data-stu-id="f89f2-138">For example, the application can create a SRV with the DXGI\_FORMAT\_R10G10B10A2\_UNORM format if the resource was created as DXGI\_FORMAT\_R10G10B10A2\_TYPELESS.</span></span> <span data-ttu-id="f89f2-139">Quando um sombreador acessa esse SRV, o hardware pode executar a conversão automática de tipo como de costume.</span><span class="sxs-lookup"><span data-stu-id="f89f2-139">When a shader accesses that SRV, the hardware can perform automatic type conversion as usual.</span></span>

> [!Note]  
> <span data-ttu-id="f89f2-140">Se o sombreador precisar gravar somente em um UAV, ou ler como um SRV, nenhum desses trabalhos de conversão será necessário porque você pode usar o UAVs totalmente tipado ou o SRVs.</span><span class="sxs-lookup"><span data-stu-id="f89f2-140">If the shader must write only to a UAV, or read as an SRV, none of this conversion work is needed because you can use fully typed UAVs or SRVs.</span></span> <span data-ttu-id="f89f2-141">As funções de conversão de formato fornecidas em D3DX \_ DXGIFormatConvert. inl são potencialmente úteis apenas se você deseja executar a leitura simultânea e gravação em um UAV de uma textura.</span><span class="sxs-lookup"><span data-stu-id="f89f2-141">The format conversion functions provided in D3DX\_DXGIFormatConvert.inl are potentially useful only if you want to perform simultaneous reading from and writing to a UAV of a texture.</span></span>

 

<span data-ttu-id="f89f2-142">A seguir está a lista de funções de conversão de formato que estão incluídas no \_ arquivo D3DX DXGIFormatConvert. inl.</span><span class="sxs-lookup"><span data-stu-id="f89f2-142">The following is the list of format conversion functions that are included in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="f89f2-143">Essas funções são categorizadas pelo formato DXGI \_ que são descompactadas e empacotadas.</span><span class="sxs-lookup"><span data-stu-id="f89f2-143">These functions are categorized by the DXGI\_FORMAT that they unpack and pack.</span></span> <span data-ttu-id="f89f2-144">Cada um dos formatos com suporte descende de um dos formatos sem tipo listados no cenário anterior e dá suporte à conversão para \_ o formato dxgi \_ R32 \_ uint como um UAV.</span><span class="sxs-lookup"><span data-stu-id="f89f2-144">Each of the supported formats descends from one of the TYPELESS formats listed in the preceding scenario and supports casting to DXGI\_FORMAT\_R32\_UINT as a UAV.</span></span>

<dl> <dt>

<span data-ttu-id="f89f2-145"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>\_Formato dxgi \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="f89f2-145"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f89f2-146"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>\_Formato dxgi \_ R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="f89f2-146"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f89f2-147"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>\_Formato dxgi \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="f89f2-147"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f89f2-148"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>\_Formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="f89f2-148"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="f89f2-149">A \_ função inexata tipo usa as instruções do sombreador que não têm precisão alta o suficiente para fornecer a resposta exata.</span><span class="sxs-lookup"><span data-stu-id="f89f2-149">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="f89f2-150">A função alternativa usa uma tabela de pesquisa armazenada no sombreador para fornecer uma conversão exata de >flutuante de SRGB.</span><span class="sxs-lookup"><span data-stu-id="f89f2-150">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="f89f2-151"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>\_Formato dxgi \_ R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="f89f2-151"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f89f2-152"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>\_Formato dxgi \_ R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="f89f2-152"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f89f2-153"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>\_Formato dxgi \_ R8G8B8A8 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="f89f2-153"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f89f2-154"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>\_Formato dxgi \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="f89f2-154"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f89f2-155"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>\_Formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="f89f2-155"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="f89f2-156">A \_ função inexata tipo usa as instruções do sombreador que não têm precisão alta o suficiente para fornecer a resposta exata.</span><span class="sxs-lookup"><span data-stu-id="f89f2-156">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="f89f2-157">A função alternativa usa uma tabela de pesquisa armazenada no sombreador para fornecer uma conversão exata de >flutuante de SRGB.</span><span class="sxs-lookup"><span data-stu-id="f89f2-157">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="f89f2-158"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>\_Formato dxgi \_ B8G8R8X8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="f89f2-158"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f89f2-159"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>\_Formato dxgi \_ B8G8R8X8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="f89f2-159"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="f89f2-160">A \_ função inexata tipo usa as instruções do sombreador que não têm precisão alta o suficiente para fornecer a resposta exata.</span><span class="sxs-lookup"><span data-stu-id="f89f2-160">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="f89f2-161">A função alternativa usa uma tabela de pesquisa armazenada no sombreador para fornecer uma conversão exata de >flutuante de SRGB.</span><span class="sxs-lookup"><span data-stu-id="f89f2-161">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="f89f2-162"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>\_ \_ Float R16G16 de formato dxgi \_</span><span class="sxs-lookup"><span data-stu-id="f89f2-162"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI\_FORMAT\_R16G16\_FLOAT</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f89f2-163"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>\_Formato dxgi \_ R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="f89f2-163"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI\_FORMAT\_R16G16\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f89f2-164"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>\_Formato dxgi \_ R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="f89f2-164"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI\_FORMAT\_R16G16\_UINT</span></span>
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f89f2-165"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>\_Formato dxgi \_ R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="f89f2-165"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI\_FORMAT\_R16G16\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f89f2-166"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>\_Formato dxgi \_ R16G16 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="f89f2-166"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>DXGI\_FORMAT\_R16G16\_SINT</span></span>
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f89f2-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f89f2-167">Related Topics</span></span>

[<span data-ttu-id="f89f2-168">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="f89f2-168">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="f89f2-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f89f2-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f89f2-170">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="f89f2-170">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




