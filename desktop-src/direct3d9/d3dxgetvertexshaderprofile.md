---
description: Retorna o nome do perfil de HLSL (linguagem de sombreamento de alto nível) com suporte de um determinado dispositivo.
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: Função D3DXGetVertexShaderProfile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f7ccaeba60bdd1d7c512cee3fb4da29289408a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764168"
---
# <a name="d3dxgetvertexshaderprofile-function"></a><span data-ttu-id="15a5b-103">Função D3DXGetVertexShaderProfile</span><span class="sxs-lookup"><span data-stu-id="15a5b-103">D3DXGetVertexShaderProfile function</span></span>

<span data-ttu-id="15a5b-104">Retorna o nome do perfil de HLSL (linguagem de sombreamento de alto nível) com suporte de um determinado dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15a5b-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="15a5b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15a5b-105">Syntax</span></span>


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="15a5b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15a5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15a5b-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15a5b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a5b-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="15a5b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="15a5b-109">Ponteiro para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15a5b-109">Pointer to the device.</span></span> <span data-ttu-id="15a5b-110">Consulte [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="15a5b-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15a5b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15a5b-111">Return value</span></span>

<span data-ttu-id="15a5b-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15a5b-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15a5b-113">O nome do perfil HLSL.</span><span class="sxs-lookup"><span data-stu-id="15a5b-113">The HLSL profile name.</span></span>

<span data-ttu-id="15a5b-114">Se o dispositivo não oferecer suporte a sombreadores de vértice, a função retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="15a5b-114">If the device does not support vertex shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="15a5b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="15a5b-115">Remarks</span></span>

<span data-ttu-id="15a5b-116">Um perfil de sombreador especifica a versão do sombreador de assembly a ser usada e os recursos disponíveis para o compilador HLSL ao compilar um sombreador.</span><span class="sxs-lookup"><span data-stu-id="15a5b-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="15a5b-117">A tabela a seguir lista os perfis de sombreador de vértice que têm suporte.</span><span class="sxs-lookup"><span data-stu-id="15a5b-117">The following table lists the vertex shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15a5b-118">Perfil do sombreador</span><span class="sxs-lookup"><span data-stu-id="15a5b-118">Shader Profile</span></span></th>
<th><span data-ttu-id="15a5b-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="15a5b-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15a5b-120">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="15a5b-120">vs_1_1</span></span></td>
<td><span data-ttu-id="15a5b-121">Compilar para vs_1_1 versão.</span><span class="sxs-lookup"><span data-stu-id="15a5b-121">Compile to vs_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15a5b-122">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="15a5b-122">vs_2_0</span></span></td>
<td><span data-ttu-id="15a5b-123">Compilar para vs_2_0 versão.</span><span class="sxs-lookup"><span data-stu-id="15a5b-123">Compile to vs_2_0 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15a5b-124">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="15a5b-124">vs_2_a</span></span></td>
<td><span data-ttu-id="15a5b-125">O mesmo que o perfil de vs_2_0, com os seguintes recursos adicionais disponíveis para o compilador visar:</span><span class="sxs-lookup"><span data-stu-id="15a5b-125">Same as the vs_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="15a5b-126">O número de registros temporários (r #) é maior ou igual a 13.</span><span class="sxs-lookup"><span data-stu-id="15a5b-126">Number of Temporary Registers (r#) is greater than or equal to 13.</span></span></li>
<li><span data-ttu-id="15a5b-127">Instrução de controle de fluxo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="15a5b-127">Dynamic flow control instruction.</span></span></li>
<li><span data-ttu-id="15a5b-128">Predicação.</span><span class="sxs-lookup"><span data-stu-id="15a5b-128">Predication.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15a5b-129">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="15a5b-129">vs_3_0</span></span></td>
<td><span data-ttu-id="15a5b-130">Compilar para vs_3_0 versão.</span><span class="sxs-lookup"><span data-stu-id="15a5b-130">Compile to vs_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="15a5b-131">Para obter mais informações sobre as diferenças entre versões de sombreador, consulte [diferenças de sombreador de vértice](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span><span class="sxs-lookup"><span data-stu-id="15a5b-131">For more information about the differences between shader versions, see [Vertex Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15a5b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15a5b-132">Requirements</span></span>



| <span data-ttu-id="15a5b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="15a5b-133">Requirement</span></span> | <span data-ttu-id="15a5b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="15a5b-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="15a5b-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15a5b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="15a5b-136"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="15a5b-136"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="15a5b-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15a5b-137">Library</span></span><br/> | <dl> <span data-ttu-id="15a5b-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15a5b-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="15a5b-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="15a5b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a5b-140">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="15a5b-140">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
