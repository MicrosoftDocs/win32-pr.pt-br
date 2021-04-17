---
description: Retorna informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'Método ID3DXFont:: GetGlyphData (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762063"
---
# <a name="id3dxfontgetglyphdata-method"></a><span data-ttu-id="0ad99-103">Método ID3DXFont:: GetGlyphData</span><span class="sxs-lookup"><span data-stu-id="0ad99-103">ID3DXFont::GetGlyphData method</span></span>

<span data-ttu-id="0ad99-104">Retorna informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.</span><span class="sxs-lookup"><span data-stu-id="0ad99-104">Returns information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad99-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ad99-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="0ad99-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ad99-107">*Glifo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0ad99-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ad99-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ad99-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ad99-109">Identificador de glifo.</span><span class="sxs-lookup"><span data-stu-id="0ad99-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0ad99-110">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0ad99-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ad99-111">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="0ad99-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="0ad99-112">Endereço de um ponteiro para um objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que contém o glifo.</span><span class="sxs-lookup"><span data-stu-id="0ad99-112">Address of a pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="0ad99-113">*pBlackBox* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0ad99-113">*pBlackBox* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ad99-114">Tipo: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="0ad99-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="0ad99-115">Ponteiro para o menor objeto Rectangle que inclui completamente o glifo.</span><span class="sxs-lookup"><span data-stu-id="0ad99-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="0ad99-116">*pCellInc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0ad99-116">*pCellInc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ad99-117">Tipo: **[ **ponto**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ad99-117">Type: **[**POINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0ad99-118">Ponteiro para o vetor bidimensional que conecta a origem da célula de caractere atual à origem da próxima célula de caractere.</span><span class="sxs-lookup"><span data-stu-id="0ad99-118">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="0ad99-119">Consulte o [**ponto**](../winprog/windows-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="0ad99-119">See [**POINT**](../winprog/windows-data-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ad99-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ad99-120">Return value</span></span>

<span data-ttu-id="0ad99-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ad99-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ad99-122">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0ad99-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0ad99-123">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="0ad99-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ad99-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ad99-124">Requirements</span></span>



| <span data-ttu-id="0ad99-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ad99-125">Requirement</span></span> | <span data-ttu-id="0ad99-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0ad99-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad99-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ad99-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0ad99-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ad99-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0ad99-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ad99-129">Library</span></span><br/> | <dl> <span data-ttu-id="0ad99-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ad99-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0ad99-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ad99-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ad99-132">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="0ad99-132">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
