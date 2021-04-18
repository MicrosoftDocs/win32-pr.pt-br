---
description: Carrega uma série de caracteres na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: 'ID3DXFont: método reloadCharacters de:P (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9262fcb386b9362093ad563bd851946fd2305c7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793819"
---
# <a name="id3dxfontpreloadcharacters-method"></a><span data-ttu-id="a53dd-103">ID3DXFont: método reloadCharacters de:P</span><span class="sxs-lookup"><span data-stu-id="a53dd-103">ID3DXFont::PreloadCharacters method</span></span>

<span data-ttu-id="a53dd-104">Carrega uma série de caracteres na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a53dd-104">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a53dd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a53dd-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="a53dd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a53dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a53dd-107">*Primeiro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a53dd-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a53dd-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a53dd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a53dd-109">ID do primeiro caractere a ser carregado na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a53dd-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="a53dd-110">*Último* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a53dd-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a53dd-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a53dd-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a53dd-112">ID do último caractere a ser carregado na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a53dd-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a53dd-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a53dd-113">Return value</span></span>

<span data-ttu-id="a53dd-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a53dd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a53dd-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a53dd-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a53dd-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="a53dd-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a53dd-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a53dd-117">Remarks</span></span>

<span data-ttu-id="a53dd-118">Esse método gera texturas contendo glifos que representam os caracteres de entrada.</span><span class="sxs-lookup"><span data-stu-id="a53dd-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="a53dd-119">Os glifos são desenhados como uma série de triângulos.</span><span class="sxs-lookup"><span data-stu-id="a53dd-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="a53dd-120">Os caracteres não serão renderizados para o dispositivo; O [**DrawText**](id3dxfont--drawtext.md) ainda deve ser chamado para renderizar os caracteres.</span><span class="sxs-lookup"><span data-stu-id="a53dd-120">Characters will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the characters.</span></span> <span data-ttu-id="a53dd-121">No entanto, ao pré-carregar caracteres na memória de vídeo, o **DrawText** usará substancialmente menos recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="a53dd-121">However, by pre-loading characters into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="a53dd-122">Esse método converte internamente os caracteres em glifos usando a função GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span><span class="sxs-lookup"><span data-stu-id="a53dd-122">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="a53dd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a53dd-123">Requirements</span></span>



| <span data-ttu-id="a53dd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a53dd-124">Requirement</span></span> | <span data-ttu-id="a53dd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a53dd-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a53dd-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a53dd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a53dd-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a53dd-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a53dd-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a53dd-128">Library</span></span><br/> | <dl> <span data-ttu-id="a53dd-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a53dd-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a53dd-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a53dd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a53dd-131">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="a53dd-131">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
