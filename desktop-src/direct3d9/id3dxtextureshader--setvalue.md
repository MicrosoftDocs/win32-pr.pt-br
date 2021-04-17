---
description: Define a tabela constante com os dados no buffer.
ms.assetid: 55cf5456-8f23-405d-9329-8ff737c5c139
title: 'Método ID3DXTextureShader:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2f18902c73f44bc4294e5152f8da5ea3e37f27ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762875"
---
# <a name="id3dxtextureshadersetvalue-method"></a><span data-ttu-id="a870e-103">Método ID3DXTextureShader:: SetValue</span><span class="sxs-lookup"><span data-stu-id="a870e-103">ID3DXTextureShader::SetValue method</span></span>

<span data-ttu-id="a870e-104">Define a tabela constante com os dados no buffer.</span><span class="sxs-lookup"><span data-stu-id="a870e-104">Sets the constant table with the data in the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a870e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a870e-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hConstant,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="a870e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a870e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a870e-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a870e-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a870e-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a870e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a870e-109">Identificador exclusivo para uma constante.</span><span class="sxs-lookup"><span data-stu-id="a870e-109">Unique identifier to a constant.</span></span> <span data-ttu-id="a870e-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="a870e-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="a870e-111">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a870e-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a870e-112">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a870e-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a870e-113">Um ponteiro para um buffer que contém os dados constantes.</span><span class="sxs-lookup"><span data-stu-id="a870e-113">A pointer to a buffer containing the constant data.</span></span>

</dd> <dt>

<span data-ttu-id="a870e-114">*Bytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a870e-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a870e-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a870e-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a870e-116">Tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="a870e-116">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a870e-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a870e-117">Return value</span></span>

<span data-ttu-id="a870e-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a870e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a870e-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a870e-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a870e-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a870e-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a870e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a870e-121">Requirements</span></span>



| <span data-ttu-id="a870e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a870e-122">Requirement</span></span> | <span data-ttu-id="a870e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a870e-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a870e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a870e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a870e-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a870e-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a870e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a870e-126">Library</span></span><br/> | <dl> <span data-ttu-id="a870e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a870e-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a870e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a870e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a870e-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="a870e-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
