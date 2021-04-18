---
description: Carregue uma série de caracteres na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.
ms.assetid: 935a6248-e6b7-4fce-aaa7-b7f0c94c1f79
title: 'ID3DX10Font: método reloadCharacters de:P (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadCharacters
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fafa34d4a243e254e929f7c9a1d65d2a3fb9c8dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780906"
---
# <a name="id3dx10fontpreloadcharacters-method"></a><span data-ttu-id="2d945-103">ID3DX10Font: método reloadCharacters de:P</span><span class="sxs-lookup"><span data-stu-id="2d945-103">ID3DX10Font::PreloadCharacters method</span></span>

<span data-ttu-id="2d945-104">Carregue uma série de caracteres na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2d945-104">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d945-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d945-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="2d945-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d945-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d945-107">*Primeiro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d945-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d945-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d945-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d945-109">ID do primeiro caractere a ser carregado na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2d945-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="2d945-110">*Último* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d945-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d945-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d945-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d945-112">ID do último caractere a ser carregado na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2d945-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d945-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d945-113">Return value</span></span>

<span data-ttu-id="2d945-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d945-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d945-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2d945-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2d945-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="2d945-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d945-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d945-117">Remarks</span></span>

<span data-ttu-id="2d945-118">Esse método gera texturas contendo glifos que representam os caracteres de entrada.</span><span class="sxs-lookup"><span data-stu-id="2d945-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="2d945-119">Os glifos são desenhados como uma série de triângulos.</span><span class="sxs-lookup"><span data-stu-id="2d945-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="2d945-120">Os caracteres não serão renderizados para o dispositivo; ID3DX10Font::D rawText ainda deve ser chamado para renderizar os caracteres.</span><span class="sxs-lookup"><span data-stu-id="2d945-120">Characters will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the characters.</span></span> <span data-ttu-id="2d945-121">No entanto, ao pré-carregar caracteres na memória de vídeo, ID3DX10Font:D: o rawText usará substancialmente menos recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="2d945-121">However, by pre-loading characters into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="2d945-122">Esse método converte internamente os caracteres em glifos usando a função GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2d945-122">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d945-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d945-123">Requirements</span></span>



| <span data-ttu-id="2d945-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d945-124">Requirement</span></span> | <span data-ttu-id="2d945-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2d945-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d945-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d945-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2d945-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d945-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d945-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d945-128">Library</span></span><br/> | <dl> <span data-ttu-id="2d945-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d945-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d945-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d945-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d945-131">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="2d945-131">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="2d945-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="2d945-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
