---
description: Descreve os dados contidos na enumeração.
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: Enumeração de D3DXPARAMETER_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 16ff89feb694bb6aae550422b6f9546c2268fc07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298480"
---
# <a name="d3dxparameter_type-enumeration"></a><span data-ttu-id="c7876-103">\_Enumeração de tipo D3DXPARAMETER</span><span class="sxs-lookup"><span data-stu-id="c7876-103">D3DXPARAMETER\_TYPE enumeration</span></span>

<span data-ttu-id="c7876-104">Descreve os dados contidos na enumeração.</span><span class="sxs-lookup"><span data-stu-id="c7876-104">Describes the data contained by the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7876-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7876-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c7876-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c7876-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c7876-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ void**</span><span class="sxs-lookup"><span data-stu-id="c7876-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT\_VOID**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-108">O parâmetro é um ponteiro void.</span><span class="sxs-lookup"><span data-stu-id="c7876-108">Parameter is a void pointer.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**\_Bool D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="c7876-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-110">O parâmetro é um booliano.</span><span class="sxs-lookup"><span data-stu-id="c7876-110">Parameter is a Boolean.</span></span> <span data-ttu-id="c7876-111">Qualquer valor diferente de zero transmitido para [**ID3DXConstantTable:: setbool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable:: SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable:: DefinirValor**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: setvector**](id3dxconstanttable--setvector.md)ou [**ID3DXCONSTANTTABLE:: SetVectorArray**](id3dxconstanttable--setvectorarray.md) será mapeado para 1 (true) antes de ser gravado na tabela de constantes; caso contrário, o valor será definido como 0 na tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="c7876-111">Any non-zero value passed into [**ID3DXConstantTable::SetBool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable::SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be mapped to 1 (TRUE) before being written into the constant table; otherwise, the value will be set to 0 in the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ int**</span><span class="sxs-lookup"><span data-stu-id="c7876-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT\_INT**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-113">O parâmetro é um inteiro.</span><span class="sxs-lookup"><span data-stu-id="c7876-113">Parameter is an integer.</span></span> <span data-ttu-id="c7876-114">Todos os valores de ponto flutuante passados em [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: setvector**](id3dxconstanttable--setvector.md)ou [**ID3DXConstantTable:: SetVectorArray**](id3dxconstanttable--setvectorarray.md) serão arredondados (para casas decimais zero) antes de serem gravados na tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="c7876-114">Any floating-point values passed into [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be rounded off (to zero decimal places) before being written into the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ float**</span><span class="sxs-lookup"><span data-stu-id="c7876-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT\_FLOAT**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-116">O parâmetro é um número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="c7876-116">Parameter is a floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**\_Cadeia de caracteres D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="c7876-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**D3DXPT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-118">O parâmetro é uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c7876-118">Parameter is a string.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**\_Textura D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="c7876-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**D3DXPT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-120">O parâmetro é uma textura.</span><span class="sxs-lookup"><span data-stu-id="c7876-120">Parameter is a texture.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**</span><span class="sxs-lookup"><span data-stu-id="c7876-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT\_TEXTURE1D**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-122">O parâmetro é uma textura 1D.</span><span class="sxs-lookup"><span data-stu-id="c7876-122">Parameter is a 1D texture.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**</span><span class="sxs-lookup"><span data-stu-id="c7876-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT\_TEXTURE2D**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-124">O parâmetro é uma textura 2D.</span><span class="sxs-lookup"><span data-stu-id="c7876-124">Parameter is a 2D texture.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT \_ TEXTURE3D**</span><span class="sxs-lookup"><span data-stu-id="c7876-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT\_TEXTURE3D**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-126">O parâmetro é uma textura 3D.</span><span class="sxs-lookup"><span data-stu-id="c7876-126">Parameter is a 3D texture.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ TEXTURECUBE**</span><span class="sxs-lookup"><span data-stu-id="c7876-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT\_TEXTURECUBE**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-128">O parâmetro é uma textura de cubo.</span><span class="sxs-lookup"><span data-stu-id="c7876-128">Parameter is a cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**Amostra de D3DXPT \_**</span><span class="sxs-lookup"><span data-stu-id="c7876-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**D3DXPT\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-130">O parâmetro é um amostra.</span><span class="sxs-lookup"><span data-stu-id="c7876-130">Parameter is a sampler.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**</span><span class="sxs-lookup"><span data-stu-id="c7876-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT\_SAMPLER1D**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-132">O parâmetro é uma amostra 1D.</span><span class="sxs-lookup"><span data-stu-id="c7876-132">Parameter is a 1D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**</span><span class="sxs-lookup"><span data-stu-id="c7876-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT\_SAMPLER2D**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-134">O parâmetro é um amostra 2D.</span><span class="sxs-lookup"><span data-stu-id="c7876-134">Parameter is a 2D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**</span><span class="sxs-lookup"><span data-stu-id="c7876-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT\_SAMPLER3D**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-136">O parâmetro é um amostra 3D.</span><span class="sxs-lookup"><span data-stu-id="c7876-136">Parameter is a 3D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ SAMPLERCUBE**</span><span class="sxs-lookup"><span data-stu-id="c7876-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT\_SAMPLERCUBE**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-138">O parâmetro é uma amostra de cubo.</span><span class="sxs-lookup"><span data-stu-id="c7876-138">Parameter is a cube sampler.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ PIXELSHADER**</span><span class="sxs-lookup"><span data-stu-id="c7876-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT\_PIXELSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-140">O parâmetro é um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="c7876-140">Parameter is a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ VERTEXSHADER**</span><span class="sxs-lookup"><span data-stu-id="c7876-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT\_VERTEXSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-142">O parâmetro é um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="c7876-142">Parameter is a vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ PIXELFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="c7876-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT\_PIXELFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-144">O parâmetro é um fragmento de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="c7876-144">Parameter is a pixel shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ VERTEXFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="c7876-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT\_VERTEXFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-146">O parâmetro é um fragmento de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="c7876-146">Parameter is a vertex shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT \_ sem suporte**</span><span class="sxs-lookup"><span data-stu-id="c7876-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT\_UNSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-148">Não há suporte para o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c7876-148">Parameter is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c7876-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c7876-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c7876-150">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="c7876-150">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c7876-151">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c7876-151">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c7876-152">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="c7876-152">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7876-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7876-153">Requirements</span></span>



| <span data-ttu-id="c7876-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7876-154">Requirement</span></span> | <span data-ttu-id="c7876-155">Valor</span><span class="sxs-lookup"><span data-stu-id="c7876-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7876-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7876-156">Header</span></span><br/> | <dl> <span data-ttu-id="c7876-157"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7876-157"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7876-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7876-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7876-159">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="c7876-159">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="c7876-160">**D3DXSHADER \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="c7876-160">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c7876-161">**D3DXCONSTANT \_ desc**</span><span class="sxs-lookup"><span data-stu-id="c7876-161">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




