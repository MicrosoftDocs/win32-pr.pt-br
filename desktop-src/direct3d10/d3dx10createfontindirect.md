---
description: Cria um objeto Font. Observação em vez de usar essa função, recomendamos que você use DirectWrite e a biblioteca DirectXTK, SpriteFont Class.
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: Função D3DX10CreateFontIndirect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298546"
---
# <a name="d3dx10createfontindirect-function"></a><span data-ttu-id="3a1ca-103">Função D3DX10CreateFontIndirect</span><span class="sxs-lookup"><span data-stu-id="3a1ca-103">D3DX10CreateFontIndirect function</span></span>

<span data-ttu-id="3a1ca-104">Cria um objeto Font.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-104">Creates a font object.</span></span>

> [!Note]  
> <span data-ttu-id="3a1ca-105">Em vez de usar essa função, recomendamos que você use [DirectWrite](../directwrite/direct-write-portal.md) e a biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteFont** Class.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-105">Instead of using this function, we recommend that you use [DirectWrite](../directwrite/direct-write-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteFont** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3a1ca-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a1ca-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="3a1ca-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a1ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a1ca-108">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a1ca-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1ca-109">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="3a1ca-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="3a1ca-110">Ponteiro para uma interface de [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .</span><span class="sxs-lookup"><span data-stu-id="3a1ca-110">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ca-111">*pDesc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a1ca-111">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1ca-112">Tipo: **const [**D3DX10 \_ Font \_ desc**](d3dx10-font-desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="3a1ca-112">Type: **const [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="3a1ca-113">Ponteiro para uma [**estrutura \_ \_ desc de fonte D3DX10**](d3dx10-font-desc.md) , descrevendo os atributos do objeto Font a ser criado.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-113">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="3a1ca-114">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateFontIndirectW.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-114">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="3a1ca-115">Caso contrário, a chamada de função é resolvida como D3DXCreateFontIndirectA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-115">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ca-116">*ppFont* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3a1ca-116">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1ca-117">Tipo: **[ **LPD3DX10FONT**](id3dx10font.md)\***</span><span class="sxs-lookup"><span data-stu-id="3a1ca-117">Type: **[**LPD3DX10FONT**](id3dx10font.md)\***</span></span>

<span data-ttu-id="3a1ca-118">Retorna um ponteiro para uma [**interface ID3DX10Font**](id3dx10font.md).</span><span class="sxs-lookup"><span data-stu-id="3a1ca-118">Returns a pointer to an [**ID3DX10Font Interface**](id3dx10font.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a1ca-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a1ca-119">Return value</span></span>

<span data-ttu-id="3a1ca-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a1ca-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a1ca-121">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3a1ca-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a1ca-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a1ca-122">Requirements</span></span>



| <span data-ttu-id="3a1ca-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a1ca-123">Requirement</span></span> | <span data-ttu-id="3a1ca-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3a1ca-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a1ca-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a1ca-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3a1ca-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a1ca-126"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="3a1ca-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a1ca-127">Library</span></span><br/> | <dl> <span data-ttu-id="3a1ca-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a1ca-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3a1ca-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a1ca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a1ca-130">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="3a1ca-130">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
