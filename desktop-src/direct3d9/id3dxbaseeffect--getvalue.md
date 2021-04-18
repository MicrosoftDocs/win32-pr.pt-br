---
description: Obtenha o valor de um parâmetro ou anotação arbitrária, incluindo tipos simples, structs, matrizes, cadeias de caracteres, sombreadores e texturas. Esse método pode ser usado no lugar de quase todas as chamadas GetXXX em ID3DXBaseEffect.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: 'Método ID3DXBaseEffect:: GetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 166635b22875692da0396f1c7c2145f13ca08df3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814132"
---
# <a name="id3dxbaseeffectgetvalue-method"></a><span data-ttu-id="bd6d7-104">Método ID3DXBaseEffect:: GetValue</span><span class="sxs-lookup"><span data-stu-id="bd6d7-104">ID3DXBaseEffect::GetValue method</span></span>

<span data-ttu-id="bd6d7-105">Obtenha o valor de um parâmetro ou anotação arbitrária, incluindo tipos simples, structs, matrizes, cadeias de caracteres, sombreadores e texturas.</span><span class="sxs-lookup"><span data-stu-id="bd6d7-105">Get the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span> <span data-ttu-id="bd6d7-106">Esse método pode ser usado no lugar de quase todas as chamadas GetXXX em [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="bd6d7-106">This method can be used in place of nearly all the Getxxx calls in [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd6d7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd6d7-107">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="bd6d7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd6d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd6d7-109">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bd6d7-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd6d7-110">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bd6d7-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bd6d7-111">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="bd6d7-111">Unique identifier.</span></span> <span data-ttu-id="bd6d7-112">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="bd6d7-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd6d7-113">*pData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bd6d7-113">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd6d7-114">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd6d7-114">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd6d7-115">Retorna um buffer que contém o valor.</span><span class="sxs-lookup"><span data-stu-id="bd6d7-115">Returns a buffer containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="bd6d7-116">*Bytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bd6d7-116">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd6d7-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd6d7-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd6d7-118">\[em \] número de bytes no buffer.</span><span class="sxs-lookup"><span data-stu-id="bd6d7-118">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="bd6d7-119">Passe D3DX \_ padrão se souber que o buffer é grande o suficiente para conter o parâmetro inteiro e você deseja ignorar a validação de tamanho.</span><span class="sxs-lookup"><span data-stu-id="bd6d7-119">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd6d7-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd6d7-120">Return value</span></span>

<span data-ttu-id="bd6d7-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bd6d7-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bd6d7-122">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bd6d7-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bd6d7-123">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bd6d7-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd6d7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd6d7-124">Requirements</span></span>



| <span data-ttu-id="bd6d7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd6d7-125">Requirement</span></span> | <span data-ttu-id="bd6d7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="bd6d7-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6d7-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd6d7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="bd6d7-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd6d7-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bd6d7-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd6d7-129">Library</span></span><br/> | <dl> <span data-ttu-id="bd6d7-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd6d7-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bd6d7-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd6d7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd6d7-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="bd6d7-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="bd6d7-133">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="bd6d7-133">**SetValue**</span></span>](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
