---
description: Carrega na memória um buffer de PRT (transferência radiante em computação) que foi salvo no disco.
ms.assetid: b9296c9e-e8ff-4a18-8682-fcac4feb64e9
title: Função D3DXLoadPRTBufferFromFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10caedc9b77ef97f4d070ce82392b5da1de54fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298494"
---
# <a name="d3dxloadprtbufferfromfile-function"></a><span data-ttu-id="f4440-103">Função D3DXLoadPRTBufferFromFile</span><span class="sxs-lookup"><span data-stu-id="f4440-103">D3DXLoadPRTBufferFromFile function</span></span>

<span data-ttu-id="f4440-104">Carrega na memória um buffer de PRT (transferência radiante em computação) que foi salvo no disco.</span><span class="sxs-lookup"><span data-stu-id="f4440-104">Loads into memory a precomputed radiance transfer (PRT) buffer that was saved to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4440-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4440-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPRTBufferFromFile(
  _In_    LPCSTR          pFileName,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="f4440-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4440-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4440-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4440-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4440-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4440-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4440-109">Nome do arquivo do qual carregar os dados de buffer.</span><span class="sxs-lookup"><span data-stu-id="f4440-109">Name of the file from which to load the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="f4440-110">*ppBuffer* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f4440-110">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4440-111">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4440-111">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="f4440-112">Endereço de um ponteiro para o objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída.</span><span class="sxs-lookup"><span data-stu-id="f4440-112">Address of a pointer to the output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4440-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4440-113">Return value</span></span>

<span data-ttu-id="f4440-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f4440-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f4440-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f4440-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f4440-116">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f4440-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4440-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4440-117">Remarks</span></span>

<span data-ttu-id="f4440-118">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="f4440-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="f4440-119">Se o Unicode for definido, a chamada de função será resolvida como D3DXLoadPRTBufferFromFileW.</span><span class="sxs-lookup"><span data-stu-id="f4440-119">If Unicode is defined, the function call resolves to D3DXLoadPRTBufferFromFileW.</span></span> <span data-ttu-id="f4440-120">Caso contrário, a chamada de função será resolvida como D3DXLoadPRTBufferFromFileA.</span><span class="sxs-lookup"><span data-stu-id="f4440-120">Otherwise, the function call resolves to D3DXLoadPRTBufferFromFileA.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4440-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4440-121">Requirements</span></span>



| <span data-ttu-id="f4440-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4440-122">Requirement</span></span> | <span data-ttu-id="f4440-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f4440-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4440-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4440-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f4440-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4440-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f4440-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4440-126">Library</span></span><br/> | <dl> <span data-ttu-id="f4440-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4440-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f4440-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4440-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4440-129">Funções de transferência radiante preputadas</span><span class="sxs-lookup"><span data-stu-id="f4440-129">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
