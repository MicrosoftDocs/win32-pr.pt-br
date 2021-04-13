---
description: Carrega na memória um buffer de PRT (transferência de radiante de computação compactada) compactado que foi salvo em disco.
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: Função D3DXLoadPRTCompBufferFromFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTCompBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 505fca7d8cb2426a49a2992c249ba45b5b7afd11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298812"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a><span data-ttu-id="f968f-103">Função D3DXLoadPRTCompBufferFromFile</span><span class="sxs-lookup"><span data-stu-id="f968f-103">D3DXLoadPRTCompBufferFromFile function</span></span>

<span data-ttu-id="f968f-104">Carrega na memória um buffer de PRT (transferência de radiante de computação compactada) compactado que foi salvo em disco.</span><span class="sxs-lookup"><span data-stu-id="f968f-104">Loads into memory a compressed precomputed radiance transfer (PRT) buffer that was saved to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="f968f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f968f-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="f968f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f968f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f968f-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f968f-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f968f-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f968f-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f968f-109">Nome do arquivo do qual carregar os dados de buffer compactados.</span><span class="sxs-lookup"><span data-stu-id="f968f-109">Name of the file from which to load the compressed buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="f968f-110">*ppBuffer* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f968f-110">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f968f-111">Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f968f-111">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="f968f-112">Endereço de um ponteiro para o objeto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de saída.</span><span class="sxs-lookup"><span data-stu-id="f968f-112">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f968f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f968f-113">Return value</span></span>

<span data-ttu-id="f968f-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f968f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f968f-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f968f-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f968f-116">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f968f-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f968f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f968f-117">Remarks</span></span>

<span data-ttu-id="f968f-118">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="f968f-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="f968f-119">Se o Unicode for definido, a chamada de função será resolvida como D3DXLoadPRTCompBufferFromFileW.</span><span class="sxs-lookup"><span data-stu-id="f968f-119">If Unicode is defined, the function call resolves to D3DXLoadPRTCompBufferFromFileW.</span></span> <span data-ttu-id="f968f-120">Caso contrário, a chamada de função será resolvida como D3DXLoadPRTCompBufferFromFileA.</span><span class="sxs-lookup"><span data-stu-id="f968f-120">Otherwise, the function call resolves to D3DXLoadPRTCompBufferFromFileA.</span></span>

## <a name="requirements"></a><span data-ttu-id="f968f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f968f-121">Requirements</span></span>



| <span data-ttu-id="f968f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f968f-122">Requirement</span></span> | <span data-ttu-id="f968f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f968f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f968f-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f968f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f968f-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f968f-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f968f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f968f-126">Library</span></span><br/> | <dl> <span data-ttu-id="f968f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f968f-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f968f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f968f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f968f-129">Funções de transferência radiante preputadas</span><span class="sxs-lookup"><span data-stu-id="f968f-129">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
