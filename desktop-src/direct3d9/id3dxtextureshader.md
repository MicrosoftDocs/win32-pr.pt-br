---
description: A interface ID3DXTextureShader.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: Interface ID3DXTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1b9581bced9d501800a8a8f3cb5d31a563ac261
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105755924"
---
# <a name="id3dxtextureshader-interface"></a><span data-ttu-id="ab7f2-103">Interface ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="ab7f2-103">ID3DXTextureShader interface</span></span>

<span data-ttu-id="ab7f2-104">A interface ID3DXTextureShader.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-104">The ID3DXTextureShader interface.</span></span>

## <a name="members"></a><span data-ttu-id="ab7f2-105">Membros</span><span class="sxs-lookup"><span data-stu-id="ab7f2-105">Members</span></span>

<span data-ttu-id="ab7f2-106">A interface **ID3DXTextureShader** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ab7f2-106">The **ID3DXTextureShader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ab7f2-107">**ID3DXTextureShader** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ab7f2-107">**ID3DXTextureShader** also has these types of members:</span></span>

-   [<span data-ttu-id="ab7f2-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="ab7f2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ab7f2-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ab7f2-109">Methods</span></span>

<span data-ttu-id="ab7f2-110">A interface **ID3DXTextureShader** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-110">The **ID3DXTextureShader** interface has these methods.</span></span>



| <span data-ttu-id="ab7f2-111">Método</span><span class="sxs-lookup"><span data-stu-id="ab7f2-111">Method</span></span>                                                                                       | <span data-ttu-id="ab7f2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab7f2-112">Description</span></span>                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="ab7f2-113">**Getconstant**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-113">**GetConstant**</span></span>](id3dxtextureshader--getconstant.md)                                       | <span data-ttu-id="ab7f2-114">Obtém uma constante procurando seu índice.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-114">Gets a constant by looking up its index.</span></span><br/>                         |
| [<span data-ttu-id="ab7f2-115">**GetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-115">**GetConstantBuffer**</span></span>](id3dxtextureshader--getconstantbuffer.md)                           | <span data-ttu-id="ab7f2-116">Obter um ponteiro para a tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-116">Get a pointer to the constant table.</span></span><br/>                             |
| [<span data-ttu-id="ab7f2-117">**GetConstantByName**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-117">**GetConstantByName**</span></span>](id3dxtextureshader--getconstantbyname.md)                           | <span data-ttu-id="ab7f2-118">Obtém uma constante procurando seu nome.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-118">Gets a constant by looking up its name.</span></span><br/>                          |
| [<span data-ttu-id="ab7f2-119">**GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-119">**GetConstantDesc**</span></span>](id3dxtextureshader--getconstantdesc.md)                               | <span data-ttu-id="ab7f2-120">Obtém um ponteiro para a matriz de constantes na tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-120">Gets a pointer to the array of constants in the constant table.</span></span><br/>  |
| [<span data-ttu-id="ab7f2-121">**Getconstantelement**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-121">**GetConstantElement**</span></span>](id3dxtextureshader--getconstantelement.md)                         | <span data-ttu-id="ab7f2-122">Obtenha uma constante da tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-122">Get a constant from the constant table.</span></span><br/>                          |
| [<span data-ttu-id="ab7f2-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-123">**GetDesc**</span></span>](id3dxtextureshader--getdesc.md)                                               | <span data-ttu-id="ab7f2-124">Obtém uma descrição da tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-124">Gets a description of the constant table.</span></span><br/>                        |
| [<span data-ttu-id="ab7f2-125">**GetFunction**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-125">**GetFunction**</span></span>](id3dxtextureshader--getfunction.md)                                       | <span data-ttu-id="ab7f2-126">Obtém um ponteiro para a função de fluxo DWORD.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-126">Gets a pointer to the function DWORD stream.</span></span><br/>                     |
| [<span data-ttu-id="ab7f2-127">**Setbool**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-127">**SetBool**</span></span>](id3dxtextureshader--setbool.md)                                               | <span data-ttu-id="ab7f2-128">Define um valor BOOL.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-128">Sets a BOOL value.</span></span><br/>                                               |
| [<span data-ttu-id="ab7f2-129">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-129">**SetBoolArray**</span></span>](id3dxtextureshader--setboolarray.md)                                     | <span data-ttu-id="ab7f2-130">Define uma matriz de valores BOOL.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-130">Sets an array of BOOL values.</span></span><br/>                                    |
| [<span data-ttu-id="ab7f2-131">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-131">**SetDefaults**</span></span>](id3dxtextureshader--setdefaults.md)                                       | <span data-ttu-id="ab7f2-132">Define as constantes para os valores padrão declarados no sombreador.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-132">Sets the constants to the default values declared in the shader.</span></span><br/> |
| [<span data-ttu-id="ab7f2-133">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-133">**SetFloat**</span></span>](id3dxtextureshader--setfloat.md)                                             | <span data-ttu-id="ab7f2-134">Define um número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-134">Sets a floating-point number.</span></span><br/>                                    |
| [<span data-ttu-id="ab7f2-135">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-135">**SetFloatArray**</span></span>](id3dxtextureshader--setfloatarray.md)                                   | <span data-ttu-id="ab7f2-136">Define uma matriz de números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-136">Sets an array of floating-point numbers.</span></span><br/>                         |
| [<span data-ttu-id="ab7f2-137">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-137">**SetInt**</span></span>](id3dxtextureshader--setint.md)                                                 | <span data-ttu-id="ab7f2-138">Define um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-138">Sets an integer value.</span></span><br/>                                           |
| [<span data-ttu-id="ab7f2-139">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-139">**SetIntArray**</span></span>](id3dxtextureshader--setintarray.md)                                       | <span data-ttu-id="ab7f2-140">Define uma matriz de inteiros.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-140">Sets an array of integers.</span></span><br/>                                       |
| [<span data-ttu-id="ab7f2-141">**Setmatrix**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-141">**SetMatrix**</span></span>](id3dxtextureshader--setmatrix.md)                                           | <span data-ttu-id="ab7f2-142">Define uma matriz não transposeda.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-142">Sets a non-transposed matrix.</span></span><br/>                                    |
| [<span data-ttu-id="ab7f2-143">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-143">**SetMatrixArray**</span></span>](id3dxtextureshader--setmatrixarray.md)                                 | <span data-ttu-id="ab7f2-144">Define uma matriz de matrizes não transpostas.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-144">Sets an array of non-transposed matrices.</span></span><br/>                        |
| [<span data-ttu-id="ab7f2-145">**SetMatrixPointerArray**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-145">**SetMatrixPointerArray**</span></span>](id3dxtextureshader--setmatrixpointerarray.md)                   | <span data-ttu-id="ab7f2-146">Define uma matriz de ponteiros para matrizes não transpostas.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-146">Sets an array of pointers to non-transposed matrices.</span></span><br/>            |
| [<span data-ttu-id="ab7f2-147">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-147">**SetMatrixTranspose**</span></span>](id3dxtextureshader--setmatrixtranspose.md)                         | <span data-ttu-id="ab7f2-148">Define uma matriz transposeda.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-148">Sets a transposed matrix.</span></span><br/>                                        |
| [<span data-ttu-id="ab7f2-149">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-149">**SetMatrixTransposeArray**</span></span>](id3dxtextureshader--setmatrixtransposearray.md)               | <span data-ttu-id="ab7f2-150">Define uma matriz de matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-150">Sets an array of transposed matrices.</span></span><br/>                            |
| [<span data-ttu-id="ab7f2-151">**SetMatrixTransposePointerArray**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-151">**SetMatrixTransposePointerArray**</span></span>](id3dxtextureshader--setmatrixtransposepointerarray.md) | <span data-ttu-id="ab7f2-152">Define uma matriz de ponteiros para matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-152">Sets an array of pointers to transposed matrices.</span></span><br/>                |
| [<span data-ttu-id="ab7f2-153">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-153">**SetValue**</span></span>](id3dxtextureshader--setvalue.md)                                             | <span data-ttu-id="ab7f2-154">Define a tabela constante com os dados no buffer.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-154">Sets the constant table with the data in the buffer.</span></span><br/>             |
| [<span data-ttu-id="ab7f2-155">**Setvector**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-155">**SetVector**</span></span>](id3dxtextureshader--setvector.md)                                           | <span data-ttu-id="ab7f2-156">Define um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-156">Sets a 4D vector.</span></span><br/>                                                |
| [<span data-ttu-id="ab7f2-157">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="ab7f2-157">**SetVectorArray**</span></span>](id3dxtextureshader--setvectorarray.md)                                 | <span data-ttu-id="ab7f2-158">Define uma matriz de vetores 4D.</span><span class="sxs-lookup"><span data-stu-id="ab7f2-158">Sets an array of 4D vectors.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="ab7f2-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab7f2-159">Remarks</span></span>

<span data-ttu-id="ab7f2-160">A interface **ID3DXTextureShader** é obtida chamando a função [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="ab7f2-160">The **ID3DXTextureShader** interface is obtained by calling the [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) function.</span></span>

<span data-ttu-id="ab7f2-161">A interface **ID3DXTextureShader** , como todas as interfaces com, herda a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ab7f2-161">The **ID3DXTextureShader** interface, like all COM interfaces, inherits the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

<span data-ttu-id="ab7f2-162">O tipo LPD3DXTEXTURESHADER é definido como um ponteiro para a interface **ID3DXTextureShader** .</span><span class="sxs-lookup"><span data-stu-id="ab7f2-162">The LPD3DXTEXTURESHADER type is defined as a pointer to the **ID3DXTextureShader** interface.</span></span>


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a><span data-ttu-id="ab7f2-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab7f2-163">Requirements</span></span>



| <span data-ttu-id="ab7f2-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab7f2-164">Requirement</span></span> | <span data-ttu-id="ab7f2-165">Valor</span><span class="sxs-lookup"><span data-stu-id="ab7f2-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab7f2-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab7f2-166">Header</span></span><br/>  | <dl> <span data-ttu-id="ab7f2-167"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab7f2-167"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ab7f2-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab7f2-168">Library</span></span><br/> | <dl> <span data-ttu-id="ab7f2-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab7f2-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ab7f2-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab7f2-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab7f2-171">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ab7f2-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
