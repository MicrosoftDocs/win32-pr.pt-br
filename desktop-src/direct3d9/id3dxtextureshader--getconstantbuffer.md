---
description: Obter um ponteiro para a tabela de constantes.
ms.assetid: 5d836d99-783f-41e1-b7bf-d874d09a4892
title: 'Método ID3DXTextureShader:: GetConstantBuffer (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c83a723dde56fc80f643d7209c56fc05ad6cce5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298549"
---
# <a name="id3dxtextureshadergetconstantbuffer-method"></a><span data-ttu-id="44f0e-103">Método ID3DXTextureShader:: GetConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="44f0e-103">ID3DXTextureShader::GetConstantBuffer method</span></span>

<span data-ttu-id="44f0e-104">Obter um ponteiro para a tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="44f0e-104">Get a pointer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="44f0e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44f0e-105">Syntax</span></span>


```C++
HRESULT GetConstantBuffer(
  [out] LPD3DXBUFFER *ppConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="44f0e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44f0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44f0e-107">*ppConstantBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="44f0e-107">*ppConstantBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44f0e-108">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="44f0e-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="44f0e-109">Ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , que contém as constantes.</span><span class="sxs-lookup"><span data-stu-id="44f0e-109">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains the constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44f0e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44f0e-110">Return value</span></span>

<span data-ttu-id="44f0e-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44f0e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44f0e-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="44f0e-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="44f0e-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="44f0e-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="44f0e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44f0e-114">Requirements</span></span>



| <span data-ttu-id="44f0e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="44f0e-115">Requirement</span></span> | <span data-ttu-id="44f0e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="44f0e-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44f0e-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44f0e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="44f0e-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="44f0e-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="44f0e-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44f0e-119">Library</span></span><br/> | <dl> <span data-ttu-id="44f0e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44f0e-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="44f0e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="44f0e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f0e-122">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="44f0e-122">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




