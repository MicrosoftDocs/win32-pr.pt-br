---
description: Retorna o nome do perfil de HLSL (linguagem de sombreamento de alto nível) com suporte de um determinado dispositivo.
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: Função D3DXGetPixelShaderProfile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ad1f430a95b1ff2173dceb1e0561dccf3d0ee88d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930592"
---
# <a name="d3dxgetpixelshaderprofile-function"></a><span data-ttu-id="ff2eb-103">Função D3DXGetPixelShaderProfile</span><span class="sxs-lookup"><span data-stu-id="ff2eb-103">D3DXGetPixelShaderProfile function</span></span>

<span data-ttu-id="ff2eb-104">Retorna o nome do perfil de HLSL (linguagem de sombreamento de alto nível) com suporte de um determinado dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff2eb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff2eb-105">Syntax</span></span>


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="ff2eb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff2eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff2eb-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff2eb-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff2eb-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ff2eb-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ff2eb-109">Ponteiro para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-109">Pointer to the device.</span></span> <span data-ttu-id="ff2eb-110">Consulte [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="ff2eb-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff2eb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff2eb-111">Return value</span></span>

<span data-ttu-id="ff2eb-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff2eb-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff2eb-113">O nome do perfil HLSL.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-113">The HLSL profile name.</span></span>

<span data-ttu-id="ff2eb-114">Se o dispositivo não oferecer suporte a sombreadores de pixel, a função retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-114">If the device does not support pixel shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff2eb-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff2eb-115">Remarks</span></span>

<span data-ttu-id="ff2eb-116">Um perfil de sombreador especifica a versão do sombreador de assembly a ser usada e os recursos disponíveis para o compilador HLSL ao compilar um sombreador.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="ff2eb-117">A tabela a seguir lista os perfis de sombreador de pixel com suporte.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-117">The following table lists the pixel shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff2eb-118">Perfil do sombreador</span><span class="sxs-lookup"><span data-stu-id="ff2eb-118">Shader Profile</span></span></th>
<th><span data-ttu-id="ff2eb-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff2eb-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff2eb-120">ps_1_1</span><span class="sxs-lookup"><span data-stu-id="ff2eb-120">ps_1_1</span></span></td>
<td><span data-ttu-id="ff2eb-121">Compilar para ps_1_1 versão.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-121">Compile to ps_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff2eb-122">ps_1_2</span><span class="sxs-lookup"><span data-stu-id="ff2eb-122">ps_1_2</span></span></td>
<td><span data-ttu-id="ff2eb-123">Compilar para ps_1_2 versão.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-123">Compile to ps_1_2 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff2eb-124">ps_1_3</span><span class="sxs-lookup"><span data-stu-id="ff2eb-124">ps_1_3</span></span></td>
<td><span data-ttu-id="ff2eb-125">Compilar para ps_1_3 versão.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-125">Compile to ps_1_3 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff2eb-126">ps_1_4</span><span class="sxs-lookup"><span data-stu-id="ff2eb-126">ps_1_4</span></span></td>
<td><span data-ttu-id="ff2eb-127">Compilar para ps_1_4 versão.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-127">Compile to ps_1_4 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff2eb-128">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="ff2eb-128">ps_2_0</span></span></td>
<td><span data-ttu-id="ff2eb-129">Compilar para ps_2_0 versão.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-129">Compile to ps_2_0 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff2eb-130">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="ff2eb-130">ps_2_a</span></span></td>
<td><span data-ttu-id="ff2eb-131">O mesmo que o perfil de ps_2_0, com os seguintes recursos adicionais disponíveis para o compilador visar:</span><span class="sxs-lookup"><span data-stu-id="ff2eb-131">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="ff2eb-132">O número de registros temporários (r #) é maior ou igual a 22.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-132">Number of Temporary Registers (r#) is greater than or equal to 22.</span></span></li>
<li><span data-ttu-id="ff2eb-133">Swizzle de origem arbitrária.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-133">Arbitrary source swizzle.</span></span></li>
<li><span data-ttu-id="ff2eb-134">Instruções de gradiente: DSX, DSY.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-134">Gradient instructions: dsx, dsy.</span></span></li>
<li><span data-ttu-id="ff2eb-135">Predicação.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-135">Predication.</span></span></li>
<li><span data-ttu-id="ff2eb-136">Nenhum limite de leitura de textura dependente.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-136">No dependent texture read limit.</span></span></li>
<li><span data-ttu-id="ff2eb-137">Nenhum limite para o número de instruções de textura.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-137">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff2eb-138">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="ff2eb-138">ps_2_b</span></span></td>
<td><span data-ttu-id="ff2eb-139">O mesmo que o perfil de ps_2_0, com os seguintes recursos adicionais disponíveis para o compilador visar:</span><span class="sxs-lookup"><span data-stu-id="ff2eb-139">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="ff2eb-140">O número de registros temporários (r #) é maior ou igual a 32.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-140">Number of Temporary Registers (r#) is greater than or equal to 32.</span></span></li>
<li><span data-ttu-id="ff2eb-141">Nenhum limite para o número de instruções de textura.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-141">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff2eb-142">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="ff2eb-142">ps_3_0</span></span></td>
<td><span data-ttu-id="ff2eb-143">Compilar para ps_3_0 versão.</span><span class="sxs-lookup"><span data-stu-id="ff2eb-143">Compile to ps_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ff2eb-144">Para obter mais informações sobre as diferenças entre versões de sombreador, consulte [diferenças de sombreador de pixel](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ff2eb-144">For more information about the differences between shader versions, see [Pixel Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff2eb-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff2eb-145">Requirements</span></span>



| <span data-ttu-id="ff2eb-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff2eb-146">Requirement</span></span> | <span data-ttu-id="ff2eb-147">Valor</span><span class="sxs-lookup"><span data-stu-id="ff2eb-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff2eb-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff2eb-148">Header</span></span><br/>  | <dl> <span data-ttu-id="ff2eb-149"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff2eb-149"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ff2eb-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff2eb-150">Library</span></span><br/> | <dl> <span data-ttu-id="ff2eb-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff2eb-151"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ff2eb-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff2eb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff2eb-153">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="ff2eb-153">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
