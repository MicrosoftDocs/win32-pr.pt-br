---
description: Retorna informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'Método ID3DX10Font:: GetGlyphData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 530206c4f351cb1ef073639a21dfa37e43af5bae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791524"
---
# <a name="id3dx10fontgetglyphdata-method"></a><span data-ttu-id="bc8e3-103">Método ID3DX10Font:: GetGlyphData</span><span class="sxs-lookup"><span data-stu-id="bc8e3-103">ID3DX10Font::GetGlyphData method</span></span>

<span data-ttu-id="bc8e3-104">Retorna informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-104">Return information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8e3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc8e3-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="bc8e3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc8e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc8e3-107">*Glifo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc8e3-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8e3-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc8e3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc8e3-109">Identificador de glifo.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bc8e3-110">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bc8e3-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8e3-111">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="bc8e3-111">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="bc8e3-112">Endereço de um ponteiro para um objeto ID3D10Texture que contém o glifo.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-112">Address of a pointer to a ID3D10Texture object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="bc8e3-113">*pBlackBox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc8e3-113">*pBlackBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8e3-114">Tipo: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="bc8e3-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="bc8e3-115">Ponteiro para o menor objeto Rectangle que inclui completamente o glifo.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span> <span data-ttu-id="bc8e3-116">Consulte [Rect](/previous-versions//ms536136(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc8e3-116">See [RECT](/previous-versions//ms536136(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bc8e3-117">*pCellInc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc8e3-117">*pCellInc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8e3-118">Tipo: **ponto \***</span><span class="sxs-lookup"><span data-stu-id="bc8e3-118">Type: **POINT\***</span></span>

<span data-ttu-id="bc8e3-119">Ponteiro para o vetor bidimensional que conecta a origem da célula de caractere atual à origem da próxima célula de caractere.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-119">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="bc8e3-120">Consulte o [ponto](/previous-versions//ms536119(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc8e3-120">See [POINT](/previous-versions//ms536119(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc8e3-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc8e3-121">Return value</span></span>

<span data-ttu-id="bc8e3-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc8e3-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc8e3-123">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bc8e3-124">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc8e3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc8e3-125">Requirements</span></span>



| <span data-ttu-id="bc8e3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc8e3-126">Requirement</span></span> | <span data-ttu-id="bc8e3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bc8e3-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8e3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc8e3-128">Header</span></span><br/>  | <dl> <span data-ttu-id="bc8e3-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc8e3-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc8e3-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc8e3-130">Library</span></span><br/> | <dl> <span data-ttu-id="bc8e3-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc8e3-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc8e3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc8e3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8e3-133">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="bc8e3-133">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="bc8e3-134">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="bc8e3-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
