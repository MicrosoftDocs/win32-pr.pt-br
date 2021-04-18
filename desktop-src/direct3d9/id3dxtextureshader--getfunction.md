---
description: Obtém um ponteiro para a função de fluxo DWORD.
ms.assetid: a051b51a-185c-4a9e-a8b9-4096615e2634
title: 'Método ID3DXTextureShader:: GetFunction (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetFunction
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80e504e65e4c8437247b2935794025e1b693433a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761541"
---
# <a name="id3dxtextureshadergetfunction-method"></a><span data-ttu-id="d73b8-103">Método ID3DXTextureShader:: GetFunction</span><span class="sxs-lookup"><span data-stu-id="d73b8-103">ID3DXTextureShader::GetFunction method</span></span>

<span data-ttu-id="d73b8-104">Obtém um ponteiro para a função de fluxo DWORD.</span><span class="sxs-lookup"><span data-stu-id="d73b8-104">Gets a pointer to the function DWORD stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="d73b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d73b8-105">Syntax</span></span>


```C++
HRESULT GetFunction(
  [in] LPD3DXBUFFER *ppFunction
);
```



## <a name="parameters"></a><span data-ttu-id="d73b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d73b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d73b8-107">*ppFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d73b8-107">*ppFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d73b8-108">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d73b8-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d73b8-109">Um ponteiro para a função de fluxo DWORD.</span><span class="sxs-lookup"><span data-stu-id="d73b8-109">A pointer to the function DWORD stream.</span></span> <span data-ttu-id="d73b8-110">Consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="d73b8-110">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d73b8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d73b8-111">Return value</span></span>

<span data-ttu-id="d73b8-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d73b8-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d73b8-113">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d73b8-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d73b8-114">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="d73b8-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="d73b8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d73b8-115">Requirements</span></span>



| <span data-ttu-id="d73b8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d73b8-116">Requirement</span></span> | <span data-ttu-id="d73b8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d73b8-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d73b8-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d73b8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d73b8-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d73b8-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d73b8-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d73b8-120">Library</span></span><br/> | <dl> <span data-ttu-id="d73b8-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d73b8-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d73b8-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d73b8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d73b8-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d73b8-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




