---
description: Defina o valor de um parâmetro ou anotação arbitrária, incluindo tipos simples, structs, matrizes, cadeias de caracteres, sombreadores e texturas.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: 'Método ID3DXBaseEffect:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3281306240cefc0312ff9a2af7e056dab74a085b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091981"
---
# <a name="id3dxbaseeffectsetvalue-method"></a><span data-ttu-id="8658c-103">Método ID3DXBaseEffect:: SetValue</span><span class="sxs-lookup"><span data-stu-id="8658c-103">ID3DXBaseEffect::SetValue method</span></span>

<span data-ttu-id="8658c-104">Defina o valor de um parâmetro ou anotação arbitrária, incluindo tipos simples, structs, matrizes, cadeias de caracteres, sombreadores e texturas.</span><span class="sxs-lookup"><span data-stu-id="8658c-104">Set the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="8658c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8658c-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="8658c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8658c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8658c-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8658c-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8658c-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8658c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8658c-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="8658c-109">Unique identifier.</span></span> <span data-ttu-id="8658c-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8658c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="8658c-111">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8658c-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8658c-112">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8658c-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8658c-113">Ponteiro para um buffer que contém dados.</span><span class="sxs-lookup"><span data-stu-id="8658c-113">Pointer to a buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="8658c-114">*Bytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8658c-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8658c-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8658c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8658c-116">\[em \] número de bytes no buffer.</span><span class="sxs-lookup"><span data-stu-id="8658c-116">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="8658c-117">Passe D3DX \_ padrão se souber que o buffer é grande o suficiente para conter o parâmetro inteiro e você deseja ignorar a validação de tamanho.</span><span class="sxs-lookup"><span data-stu-id="8658c-117">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8658c-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8658c-118">Return value</span></span>

<span data-ttu-id="8658c-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8658c-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8658c-120">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8658c-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8658c-121">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8658c-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8658c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8658c-122">Remarks</span></span>

<span data-ttu-id="8658c-123">Esse método pode ser usado em vez de quase todas as chamadas de API de conjunto de efeitos.</span><span class="sxs-lookup"><span data-stu-id="8658c-123">This method can be used in place of nearly all the effect set API calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="8658c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8658c-124">Requirements</span></span>



| <span data-ttu-id="8658c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8658c-125">Requirement</span></span> | <span data-ttu-id="8658c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="8658c-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8658c-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8658c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8658c-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8658c-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8658c-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8658c-129">Library</span></span><br/> | <dl> <span data-ttu-id="8658c-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8658c-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8658c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8658c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8658c-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="8658c-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="8658c-133">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="8658c-133">**GetValue**</span></span>](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
