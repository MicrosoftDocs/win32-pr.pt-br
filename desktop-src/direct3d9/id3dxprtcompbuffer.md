---
description: A interface ID3DXPRTCompBuffer armazena uma versão compactada de um buffer ID3DXPRTBuffer para uso com o PCA (análise de componente principal).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: Interface ID3DXPRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 323ed6f2bbe9ce4caf495a00330c1b1e0e83e158
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760641"
---
# <a name="id3dxprtcompbuffer-interface"></a><span data-ttu-id="562de-103">Interface ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="562de-103">ID3DXPRTCompBuffer interface</span></span>

<span data-ttu-id="562de-104">A interface **ID3DXPRTCompBuffer** armazena uma versão compactada de um buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) para uso com o PCA (análise de componente principal).</span><span class="sxs-lookup"><span data-stu-id="562de-104">The **ID3DXPRTCompBuffer** interface stores a compressed version of a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer, for use with principal component analysis (PCA).</span></span>

## <a name="members"></a><span data-ttu-id="562de-105">Membros</span><span class="sxs-lookup"><span data-stu-id="562de-105">Members</span></span>

<span data-ttu-id="562de-106">A interface **ID3DXPRTCompBuffer** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="562de-106">The **ID3DXPRTCompBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="562de-107">**ID3DXPRTCompBuffer** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="562de-107">**ID3DXPRTCompBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="562de-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="562de-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="562de-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="562de-109">Methods</span></span>

<span data-ttu-id="562de-110">A interface **ID3DXPRTCompBuffer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="562de-110">The **ID3DXPRTCompBuffer** interface has these methods.</span></span>



| <span data-ttu-id="562de-111">Método</span><span class="sxs-lookup"><span data-stu-id="562de-111">Method</span></span>                                                             | <span data-ttu-id="562de-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="562de-112">Description</span></span>                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="562de-113">**ExtractBasis**</span><span class="sxs-lookup"><span data-stu-id="562de-113">**ExtractBasis**</span></span>](id3dxprtcompbuffer--extractbasis.md)           | <span data-ttu-id="562de-114">Extrai os vetores de base de ACP (análise de componente principal) para um determinado cluster de um buffer de dados compactado **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="562de-114">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                       |
| [<span data-ttu-id="562de-115">**ExtractClusterIDs**</span><span class="sxs-lookup"><span data-stu-id="562de-115">**ExtractClusterIDs**</span></span>](id3dxprtcompbuffer--extractclusterids.md) | <span data-ttu-id="562de-116">Extrai as IDs de cluster por amostra de um buffer de dados compactado **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="562de-116">Extracts the per-sample cluster IDs from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="562de-117">**ExtractPCA**</span><span class="sxs-lookup"><span data-stu-id="562de-117">**ExtractPCA**</span></span>](id3dxprtcompbuffer--extractpca.md)               | <span data-ttu-id="562de-118">Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="562de-118">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                               |
| [<span data-ttu-id="562de-119">**ExtractTexture**</span><span class="sxs-lookup"><span data-stu-id="562de-119">**ExtractTexture**</span></span>](id3dxprtcompbuffer--extracttexture.md)       | <span data-ttu-id="562de-120">Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado **ID3DXPRTCompBuffer** e adiciona os dados a um objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="562de-120">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="562de-121">**ExtractToMesh**</span><span class="sxs-lookup"><span data-stu-id="562de-121">**ExtractToMesh**</span></span>](id3dxprtcompbuffer--extracttomesh.md)         | <span data-ttu-id="562de-122">Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado **ID3DXPRTCompBuffer** e adiciona os dados a um objeto [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="562de-122">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                 |
| [<span data-ttu-id="562de-123">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="562de-123">**GetHeight**</span></span>](id3dxprtcompbuffer--getheight.md)                 | <span data-ttu-id="562de-124">Recupera a altura da textura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="562de-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="562de-125">**GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="562de-125">**GetNumChannels**</span></span>](id3dxprtcompbuffer--getnumchannels.md)       | <span data-ttu-id="562de-126">Recupera o número de canais de cores usados na memória para armazenar amostras.</span><span class="sxs-lookup"><span data-stu-id="562de-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="562de-127">**GetNumClusters**</span><span class="sxs-lookup"><span data-stu-id="562de-127">**GetNumClusters**</span></span>](id3dxprtcompbuffer--getnumclusters.md)       | <span data-ttu-id="562de-128">Recupera o número de clusters a serem usados para compactação.</span><span class="sxs-lookup"><span data-stu-id="562de-128">Retrieves the number of clusters to use for compression.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="562de-129">**GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="562de-129">**GetNumCoeffs**</span></span>](id3dxprtcompbuffer--getnumcoeffs.md)           | <span data-ttu-id="562de-130">Recupera o número de escalares por canal de cor usado na memória para armazenar amostras.</span><span class="sxs-lookup"><span data-stu-id="562de-130">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="562de-131">**GetNumPCA**</span><span class="sxs-lookup"><span data-stu-id="562de-131">**GetNumPCA**</span></span>](id3dxprtcompbuffer--getnumpca.md)                 | <span data-ttu-id="562de-132">Recupera o número de vetores de base do PCA (análise de componente principal) a serem usados em cada cluster.</span><span class="sxs-lookup"><span data-stu-id="562de-132">Retrieves the number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="562de-133">**GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="562de-133">**GetNumSamples**</span></span>](id3dxprtcompbuffer--getnumsamples.md)         | <span data-ttu-id="562de-134">Recupera o número de vértices (ou texels) amostrados.</span><span class="sxs-lookup"><span data-stu-id="562de-134">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="562de-135">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="562de-135">**GetWidth**</span></span>](id3dxprtcompbuffer--getwidth.md)                   | <span data-ttu-id="562de-136">Recupera a largura da textura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="562de-136">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="562de-137">**Istexture**</span><span class="sxs-lookup"><span data-stu-id="562de-137">**IsTexture**</span></span>](id3dxprtcompbuffer--istexture.md)                 | <span data-ttu-id="562de-138">Indica se o buffer contém uma textura.</span><span class="sxs-lookup"><span data-stu-id="562de-138">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="562de-139">**NormalizeData**</span><span class="sxs-lookup"><span data-stu-id="562de-139">**NormalizeData**</span></span>](id3dxprtcompbuffer--normalizedata.md)         | <span data-ttu-id="562de-140">Normaliza todos os pesos do PCA (análise de componente principal) para que fiquem entre-1 e 1.</span><span class="sxs-lookup"><span data-stu-id="562de-140">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="562de-141">Os vetores de base são modificados para refletir essa normalização.</span><span class="sxs-lookup"><span data-stu-id="562de-141">Basis vectors are modified to reflect this normalization.</span></span><br/>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="562de-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="562de-142">Remarks</span></span>

<span data-ttu-id="562de-143">A interface **ID3DXPRTCompBuffer** é obtida chamando a função [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="562de-143">The **ID3DXPRTCompBuffer** interface is obtained by calling the [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) function.</span></span>

<span data-ttu-id="562de-144">O tipo LPD3DXPRTCOMPBUFFER é definido como um ponteiro para a interface **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="562de-144">The LPD3DXPRTCOMPBUFFER type is defined as a pointer to the **ID3DXPRTCompBuffer** interface.</span></span>


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="562de-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="562de-145">Requirements</span></span>



| <span data-ttu-id="562de-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="562de-146">Requirement</span></span> | <span data-ttu-id="562de-147">Valor</span><span class="sxs-lookup"><span data-stu-id="562de-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="562de-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="562de-148">Header</span></span><br/>  | <dl> <span data-ttu-id="562de-149"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="562de-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="562de-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="562de-150">Library</span></span><br/> | <dl> <span data-ttu-id="562de-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="562de-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="562de-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="562de-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562de-153">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="562de-153">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="562de-154">**D3DXCreatePRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="562de-154">**D3DXCreatePRTCompBuffer**</span></span>](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="562de-155">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="562de-155">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
