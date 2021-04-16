---
description: A interface ID3DXConstantTable é usada para acessar a tabela de constantes. Esta tabela contém as variáveis que são usadas por sombreadores e efeitos de linguagem de alto nível.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: Interface ID3DXConstantTable (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb2b7614c4d6a0e677f71e66ab94abdb89deb973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765094"
---
# <a name="id3dxconstanttable-interface"></a><span data-ttu-id="68fa8-104">Interface ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="68fa8-104">ID3DXConstantTable interface</span></span>

<span data-ttu-id="68fa8-105">A interface ID3DXConstantTable é usada para acessar a tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="68fa8-105">The ID3DXConstantTable interface is used to access the constant table.</span></span> <span data-ttu-id="68fa8-106">Esta tabela contém as variáveis que são usadas por sombreadores e efeitos de linguagem de alto nível.</span><span class="sxs-lookup"><span data-stu-id="68fa8-106">This table contains the variables that are used by high-level language shaders and effects.</span></span>

## <a name="members"></a><span data-ttu-id="68fa8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="68fa8-107">Members</span></span>

<span data-ttu-id="68fa8-108">A interface **ID3DXConstantTable** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="68fa8-108">The **ID3DXConstantTable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="68fa8-109">**ID3DXConstantTable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="68fa8-109">**ID3DXConstantTable** also has these types of members:</span></span>

-   [<span data-ttu-id="68fa8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="68fa8-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="68fa8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="68fa8-111">Methods</span></span>

<span data-ttu-id="68fa8-112">A interface **ID3DXConstantTable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="68fa8-112">The **ID3DXConstantTable** interface has these methods.</span></span>



| <span data-ttu-id="68fa8-113">Método</span><span class="sxs-lookup"><span data-stu-id="68fa8-113">Method</span></span>                                                                                       | <span data-ttu-id="68fa8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="68fa8-114">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68fa8-115">**GetBufferPointer**</span><span class="sxs-lookup"><span data-stu-id="68fa8-115">**GetBufferPointer**</span></span>](id3dxconstanttable--getbufferpointer.md)                             | <span data-ttu-id="68fa8-116">Obtém um ponteiro para o buffer que contém a tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="68fa8-116">Gets a pointer to the buffer that contains the constant table.</span></span><br/>                                                          |
| [<span data-ttu-id="68fa8-117">**Getbuffersize**</span><span class="sxs-lookup"><span data-stu-id="68fa8-117">**GetBufferSize**</span></span>](id3dxconstanttable--getbuffersize.md)                                   | <span data-ttu-id="68fa8-118">Obtém o tamanho do buffer da tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="68fa8-118">Gets the buffer size of the constant table.</span></span><br/>                                                                             |
| [<span data-ttu-id="68fa8-119">**Getconstant**</span><span class="sxs-lookup"><span data-stu-id="68fa8-119">**GetConstant**</span></span>](id3dxconstanttable--getconstant.md)                                       | <span data-ttu-id="68fa8-120">Obtém uma constante procurando seu índice.</span><span class="sxs-lookup"><span data-stu-id="68fa8-120">Gets a constant by looking up its index.</span></span><br/>                                                                                |
| [<span data-ttu-id="68fa8-121">**GetConstantByName**</span><span class="sxs-lookup"><span data-stu-id="68fa8-121">**GetConstantByName**</span></span>](id3dxconstanttable--getconstantbyname.md)                           | <span data-ttu-id="68fa8-122">Obtém uma constante procurando seu nome.</span><span class="sxs-lookup"><span data-stu-id="68fa8-122">Gets a constant by looking up its name.</span></span><br/>                                                                                 |
| [<span data-ttu-id="68fa8-123">**GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="68fa8-123">**GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)                               | <span data-ttu-id="68fa8-124">Obtém um ponteiro para uma matriz de descrições constantes na tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="68fa8-124">Gets a pointer to an array of constant descriptions in the constant table.</span></span><br/>                                              |
| [<span data-ttu-id="68fa8-125">**Getconstantelement**</span><span class="sxs-lookup"><span data-stu-id="68fa8-125">**GetConstantElement**</span></span>](id3dxconstanttable--getconstantelement.md)                         | <span data-ttu-id="68fa8-126">Obtém uma constante de uma matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="68fa8-126">Gets a constant from an array of constants.</span></span> <span data-ttu-id="68fa8-127">Uma matriz é composta de elementos.</span><span class="sxs-lookup"><span data-stu-id="68fa8-127">An array is made up of elements.</span></span><br/>                                            |
| [<span data-ttu-id="68fa8-128">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="68fa8-128">**GetDesc**</span></span>](id3dxconstanttable--getdesc.md)                                               | <span data-ttu-id="68fa8-129">Obtém uma descrição da tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="68fa8-129">Gets a description of the constant table.</span></span><br/>                                                                               |
| [<span data-ttu-id="68fa8-130">**GetSamplerIndex**</span><span class="sxs-lookup"><span data-stu-id="68fa8-130">**GetSamplerIndex**</span></span>](id3dxconstanttable--getsamplerindex.md)                               | <span data-ttu-id="68fa8-131">Retorna o índice de amostra.</span><span class="sxs-lookup"><span data-stu-id="68fa8-131">Returns the sampler index.</span></span><br/>                                                                                              |
| [<span data-ttu-id="68fa8-132">**Setbool**</span><span class="sxs-lookup"><span data-stu-id="68fa8-132">**SetBool**</span></span>](id3dxconstanttable--setbool.md)                                               | <span data-ttu-id="68fa8-133">Define um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="68fa8-133">Sets a Boolean value.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="68fa8-134">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="68fa8-134">**SetBoolArray**</span></span>](id3dxconstanttable--setboolarray.md)                                     | <span data-ttu-id="68fa8-135">Define uma matriz de valores Boolianos.</span><span class="sxs-lookup"><span data-stu-id="68fa8-135">Sets an array of Boolean values.</span></span><br/>                                                                                        |
| [<span data-ttu-id="68fa8-136">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="68fa8-136">**SetDefaults**</span></span>](id3dxconstanttable--setdefaults.md)                                       | <span data-ttu-id="68fa8-137">Define as constantes para seus valores padrão.</span><span class="sxs-lookup"><span data-stu-id="68fa8-137">Sets the constants to their default values.</span></span> <span data-ttu-id="68fa8-138">Os valores padrão são declarados nas declarações de variável no sombreador.</span><span class="sxs-lookup"><span data-stu-id="68fa8-138">The default values are declared in the variable declarations in the shader.</span></span><br/> |
| [<span data-ttu-id="68fa8-139">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="68fa8-139">**SetFloat**</span></span>](id3dxconstanttable--setfloat.md)                                             | <span data-ttu-id="68fa8-140">Define um número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="68fa8-140">Sets a floating-point number.</span></span><br/>                                                                                           |
| [<span data-ttu-id="68fa8-141">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="68fa8-141">**SetFloatArray**</span></span>](id3dxconstanttable--setfloatarray.md)                                   | <span data-ttu-id="68fa8-142">Define uma matriz de números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="68fa8-142">Sets an array of floating-point numbers.</span></span><br/>                                                                                |
| [<span data-ttu-id="68fa8-143">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="68fa8-143">**SetInt**</span></span>](id3dxconstanttable--setint.md)                                                 | <span data-ttu-id="68fa8-144">Define um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="68fa8-144">Sets an integer value.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="68fa8-145">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="68fa8-145">**SetIntArray**</span></span>](id3dxconstanttable--setintarray.md)                                       | <span data-ttu-id="68fa8-146">Define uma matriz de inteiros.</span><span class="sxs-lookup"><span data-stu-id="68fa8-146">Sets an array of integers.</span></span><br/>                                                                                              |
| [<span data-ttu-id="68fa8-147">**Setmatrix**</span><span class="sxs-lookup"><span data-stu-id="68fa8-147">**SetMatrix**</span></span>](id3dxconstanttable--setmatrix.md)                                           | <span data-ttu-id="68fa8-148">Define uma matriz nontransposed.</span><span class="sxs-lookup"><span data-stu-id="68fa8-148">Sets a nontransposed matrix.</span></span><br/>                                                                                            |
| [<span data-ttu-id="68fa8-149">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="68fa8-149">**SetMatrixArray**</span></span>](id3dxconstanttable--setmatrixarray.md)                                 | <span data-ttu-id="68fa8-150">Define uma matriz de matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="68fa8-150">Sets an array of nontransposed matrices.</span></span><br/>                                                                                |
| [<span data-ttu-id="68fa8-151">**SetMatrixPointerArray**</span><span class="sxs-lookup"><span data-stu-id="68fa8-151">**SetMatrixPointerArray**</span></span>](id3dxconstanttable--setmatrixpointerarray.md)                   | <span data-ttu-id="68fa8-152">Define uma matriz de ponteiros para matrizes nontransposed.</span><span class="sxs-lookup"><span data-stu-id="68fa8-152">Sets an array of pointers to nontransposed matrices.</span></span><br/>                                                                    |
| [<span data-ttu-id="68fa8-153">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="68fa8-153">**SetMatrixTranspose**</span></span>](id3dxconstanttable--setmatrixtranspose.md)                         | <span data-ttu-id="68fa8-154">Define uma matriz transposeda.</span><span class="sxs-lookup"><span data-stu-id="68fa8-154">Sets a transposed matrix.</span></span><br/>                                                                                               |
| [<span data-ttu-id="68fa8-155">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="68fa8-155">**SetMatrixTransposeArray**</span></span>](id3dxconstanttable--setmatrixtransposearray.md)               | <span data-ttu-id="68fa8-156">Define uma matriz de matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="68fa8-156">Sets an array of transposed matrices.</span></span><br/>                                                                                   |
| [<span data-ttu-id="68fa8-157">**SetMatrixTransposePointerArray**</span><span class="sxs-lookup"><span data-stu-id="68fa8-157">**SetMatrixTransposePointerArray**</span></span>](id3dxconstanttable--setmatrixtransposepointerarray.md) | <span data-ttu-id="68fa8-158">Define uma matriz de ponteiros para matrizes transpostas.</span><span class="sxs-lookup"><span data-stu-id="68fa8-158">Sets an array of pointers to transposed matrices.</span></span><br/>                                                                       |
| [<span data-ttu-id="68fa8-159">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="68fa8-159">**SetValue**</span></span>](id3dxconstanttable--setvalue.md)                                             | <span data-ttu-id="68fa8-160">Define o conteúdo do buffer para a tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="68fa8-160">Sets the contents of the buffer to the constant table.</span></span><br/>                                                                  |
| [<span data-ttu-id="68fa8-161">**Setvector**</span><span class="sxs-lookup"><span data-stu-id="68fa8-161">**SetVector**</span></span>](id3dxconstanttable--setvector.md)                                           | <span data-ttu-id="68fa8-162">Define um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="68fa8-162">Sets a 4D vector.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="68fa8-163">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="68fa8-163">**SetVectorArray**</span></span>](id3dxconstanttable--setvectorarray.md)                                 | <span data-ttu-id="68fa8-164">Define uma matriz de vetores 4D.</span><span class="sxs-lookup"><span data-stu-id="68fa8-164">Sets an array of 4D vectors.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="68fa8-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="68fa8-165">Remarks</span></span>

<span data-ttu-id="68fa8-166">O tipo LPD3DXCONSTANTTABLE é definido como um ponteiro para a interface **ID3DXConstantTable** .</span><span class="sxs-lookup"><span data-stu-id="68fa8-166">The LPD3DXCONSTANTTABLE type is defined as a pointer to the **ID3DXConstantTable** interface.</span></span>


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a><span data-ttu-id="68fa8-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68fa8-167">Requirements</span></span>



| <span data-ttu-id="68fa8-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="68fa8-168">Requirement</span></span> | <span data-ttu-id="68fa8-169">Valor</span><span class="sxs-lookup"><span data-stu-id="68fa8-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68fa8-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68fa8-170">Header</span></span><br/>  | <dl> <span data-ttu-id="68fa8-171"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="68fa8-171"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="68fa8-172">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68fa8-172">Library</span></span><br/> | <dl> <span data-ttu-id="68fa8-173"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68fa8-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="68fa8-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="68fa8-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68fa8-175">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="68fa8-175">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
