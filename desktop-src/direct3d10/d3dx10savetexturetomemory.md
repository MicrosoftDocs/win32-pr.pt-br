---
description: Salve uma textura na memória.
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: Função D3DX10SaveTextureToMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f20278f9fc590e72f93051d5fdd4cfbd918098df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763194"
---
# <a name="d3dx10savetexturetomemory-function"></a><span data-ttu-id="b57ae-103">Função D3DX10SaveTextureToMemory</span><span class="sxs-lookup"><span data-stu-id="b57ae-103">D3DX10SaveTextureToMemory function</span></span>

<span data-ttu-id="b57ae-104">Salve uma textura na memória.</span><span class="sxs-lookup"><span data-stu-id="b57ae-104">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="b57ae-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b57ae-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToMemory(
  _In_  ID3D10Resource           *pSrcTexture,
  _In_  D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="b57ae-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b57ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b57ae-107">*pSrcTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b57ae-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b57ae-108">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="b57ae-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="b57ae-109">Ponteiro para a textura a ser salva.</span><span class="sxs-lookup"><span data-stu-id="b57ae-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="b57ae-110">Consulte a [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="b57ae-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="b57ae-111">*DestFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b57ae-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b57ae-112">Tipo: **[ **\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="b57ae-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="b57ae-113">O formato em que a textura será salva.</span><span class="sxs-lookup"><span data-stu-id="b57ae-113">The format the texture will be saved as.</span></span> <span data-ttu-id="b57ae-114">Consulte [**\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="b57ae-114">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="b57ae-115">*ppDestBuf* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b57ae-115">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b57ae-116">Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="b57ae-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="b57ae-117">Endereço de um ponteiro para a memória que contém a textura salva.</span><span class="sxs-lookup"><span data-stu-id="b57ae-117">Address of a pointer to the memory containing the saved texture.</span></span> <span data-ttu-id="b57ae-118">Consulte a [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).</span><span class="sxs-lookup"><span data-stu-id="b57ae-118">See [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="b57ae-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b57ae-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b57ae-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b57ae-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b57ae-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b57ae-121">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b57ae-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b57ae-122">Return value</span></span>

<span data-ttu-id="b57ae-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b57ae-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b57ae-124">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b57ae-124">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b57ae-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b57ae-125">Requirements</span></span>



| <span data-ttu-id="b57ae-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b57ae-126">Requirement</span></span> | <span data-ttu-id="b57ae-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b57ae-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b57ae-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b57ae-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b57ae-129"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b57ae-129"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b57ae-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b57ae-130">Library</span></span><br/> | <dl> <span data-ttu-id="b57ae-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b57ae-131"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b57ae-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b57ae-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b57ae-133">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="b57ae-133">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="b57ae-134">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="b57ae-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
