---
description: A interface ID3DXPRTBuffer é usada como um buffer de dados para armazenar dados de vértice e de pixel para uso com métodos e funções de PRT (transferência de radiante preputada).
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: Interface ID3DXPRTBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: daadb5b0ad8155062e75ea4eca566a0afbf3631b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771492"
---
# <a name="id3dxprtbuffer-interface"></a><span data-ttu-id="026da-103">Interface ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="026da-103">ID3DXPRTBuffer interface</span></span>

<span data-ttu-id="026da-104">A interface ID3DXPRTBuffer é usada como um buffer de dados para armazenar dados de vértice e de pixel para uso com métodos e funções de PRT (transferência de radiante preputada).</span><span class="sxs-lookup"><span data-stu-id="026da-104">The ID3DXPRTBuffer interface is used as a data buffer to store vertex and pixel data for use with precomputed radiance transfer (PRT) methods and functions.</span></span>

## <a name="members"></a><span data-ttu-id="026da-105">Membros</span><span class="sxs-lookup"><span data-stu-id="026da-105">Members</span></span>

<span data-ttu-id="026da-106">A interface **ID3DXPRTBuffer** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="026da-106">The **ID3DXPRTBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="026da-107">**ID3DXPRTBuffer** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="026da-107">**ID3DXPRTBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="026da-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="026da-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="026da-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="026da-109">Methods</span></span>

<span data-ttu-id="026da-110">A interface **ID3DXPRTBuffer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="026da-110">The **ID3DXPRTBuffer** interface has these methods.</span></span>



| <span data-ttu-id="026da-111">Método</span><span class="sxs-lookup"><span data-stu-id="026da-111">Method</span></span>                                                   | <span data-ttu-id="026da-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="026da-112">Description</span></span>                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="026da-113">**Addbuffer**</span><span class="sxs-lookup"><span data-stu-id="026da-113">**AddBuffer**</span></span>](id3dxprtbuffer--addbuffer.md)           | <span data-ttu-id="026da-114">Adiciona outro buffer ao **ID3DXPRTBuffer** e armazena os resultados em **ID3DXPRTBuffer**.</span><span class="sxs-lookup"><span data-stu-id="026da-114">Adds another buffer to the **ID3DXPRTBuffer** and stores the results in **ID3DXPRTBuffer**.</span></span><br/>                                                                                        |
| [<span data-ttu-id="026da-115">**AttachGH**</span><span class="sxs-lookup"><span data-stu-id="026da-115">**AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)             | <span data-ttu-id="026da-116">Associa um objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) ao objeto **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="026da-116">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="026da-117">**EvalGH**</span><span class="sxs-lookup"><span data-stu-id="026da-117">**EvalGH**</span></span>](id3dxprtbuffer--evalgh.md)                 | <span data-ttu-id="026da-118">Aplica dados de medianiz de textura armazenados a um buffer de textura **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="026da-118">Applies stored texture gutter data to an **ID3DXPRTBuffer** texture buffer.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="026da-119">**ExtractTexture**</span><span class="sxs-lookup"><span data-stu-id="026da-119">**ExtractTexture**</span></span>](id3dxprtbuffer--extracttexture.md) | <span data-ttu-id="026da-120">Extrai dados de coeficiente de um canal de cor do buffer para um intervalo especificado de coeficientes e adiciona os dados a um objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="026da-120">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="026da-121">**ExtractToMesh**</span><span class="sxs-lookup"><span data-stu-id="026da-121">**ExtractToMesh**</span></span>](id3dxprtbuffer--extracttomesh.md)   | <span data-ttu-id="026da-122">Extrai dados de coeficiente de um buffer de canal único e adiciona os dados a um objeto [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="026da-122">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                                                              |
| [<span data-ttu-id="026da-123">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="026da-123">**GetHeight**</span></span>](id3dxprtbuffer--getheight.md)           | <span data-ttu-id="026da-124">Recupera a altura da textura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="026da-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="026da-125">**GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="026da-125">**GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md) | <span data-ttu-id="026da-126">Recupera o número de canais de cores usados na memória para armazenar amostras.</span><span class="sxs-lookup"><span data-stu-id="026da-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="026da-127">**GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="026da-127">**GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)     | <span data-ttu-id="026da-128">Recupera o número de escalares por canal de cor usado na memória para armazenar amostras.</span><span class="sxs-lookup"><span data-stu-id="026da-128">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="026da-129">**GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="026da-129">**GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)   | <span data-ttu-id="026da-130">Recupera o número de vértices (ou texels) amostrados.</span><span class="sxs-lookup"><span data-stu-id="026da-130">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="026da-131">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="026da-131">**GetWidth**</span></span>](id3dxprtbuffer--getwidth.md)             | <span data-ttu-id="026da-132">Recupera a largura da textura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="026da-132">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="026da-133">**Istexture**</span><span class="sxs-lookup"><span data-stu-id="026da-133">**IsTexture**</span></span>](id3dxprtbuffer--istexture.md)           | <span data-ttu-id="026da-134">Indica se o buffer contém uma textura.</span><span class="sxs-lookup"><span data-stu-id="026da-134">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="026da-135">**LockBuffer**</span><span class="sxs-lookup"><span data-stu-id="026da-135">**LockBuffer**</span></span>](id3dxprtbuffer--lockbuffer.md)         | <span data-ttu-id="026da-136">Bloqueia um intervalo de dados de exemplo de vértice ou Texel e Obtém um ponteiro para o local na memória de buffer.</span><span class="sxs-lookup"><span data-stu-id="026da-136">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span><br/>                                                                               |
| [<span data-ttu-id="026da-137">**ReleaseGH**</span><span class="sxs-lookup"><span data-stu-id="026da-137">**ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)           | <span data-ttu-id="026da-138">Desassocia um objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) anexado ao objeto **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="026da-138">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                   |
| [<span data-ttu-id="026da-139">**Redimensionar**</span><span class="sxs-lookup"><span data-stu-id="026da-139">**Resize**</span></span>](id3dxprtbuffer--resize.md)                 | <span data-ttu-id="026da-140">Altera o número de amostras contidas no buffer.</span><span class="sxs-lookup"><span data-stu-id="026da-140">Changes the number of samples contained in the buffer.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="026da-141">**ScaleBuffer**</span><span class="sxs-lookup"><span data-stu-id="026da-141">**ScaleBuffer**</span></span>](id3dxprtbuffer--scalebuffer.md)       | <span data-ttu-id="026da-142">Multiplica cada valor no buffer por um valor constante.</span><span class="sxs-lookup"><span data-stu-id="026da-142">Multiplies every value in the buffer by a constant value.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="026da-143">**UnlockBuffer**</span><span class="sxs-lookup"><span data-stu-id="026da-143">**UnlockBuffer**</span></span>](id3dxprtbuffer--unlockbuffer.md)     | <span data-ttu-id="026da-144">Termina o ciclo de vida do ponteiro ppData retornado por [**ID3DXPRTBuffer:: LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="026da-144">Ends the lifespan of the ppData pointer returned by [**ID3DXPRTBuffer::LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="026da-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="026da-145">Remarks</span></span>

<span data-ttu-id="026da-146">A interface **ID3DXPRTBuffer** é obtida chamando as funções [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) ou [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) .</span><span class="sxs-lookup"><span data-stu-id="026da-146">The **ID3DXPRTBuffer** interface is obtained by calling the [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) functions.</span></span>

<span data-ttu-id="026da-147">O tipo LPD3DXPRTBUFFER é definido como um ponteiro para a interface **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="026da-147">The LPD3DXPRTBUFFER type is defined as a pointer to the **ID3DXPRTBuffer** interface.</span></span>


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="026da-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="026da-148">Requirements</span></span>



| <span data-ttu-id="026da-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="026da-149">Requirement</span></span> | <span data-ttu-id="026da-150">Valor</span><span class="sxs-lookup"><span data-stu-id="026da-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="026da-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="026da-151">Header</span></span><br/>  | <dl> <span data-ttu-id="026da-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="026da-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="026da-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="026da-153">Library</span></span><br/> | <dl> <span data-ttu-id="026da-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="026da-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="026da-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="026da-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="026da-156">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="026da-156">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="026da-157">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="026da-157">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="026da-158">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="026da-158">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> <dt>

[<span data-ttu-id="026da-159">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="026da-159">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
