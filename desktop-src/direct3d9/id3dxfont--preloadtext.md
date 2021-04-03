---
description: Carrega texto formatado em memória de vídeo para melhorar a eficiência da renderização para o dispositivo. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.
ms.assetid: f2a4e9f5-87c5-46c0-965d-ce1535a6921d
title: 'ID3DXFont: método reloadText de:P (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 958979e3008cf9ae0b79e2de3591635187df0f12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091997"
---
# <a name="id3dxfontpreloadtext-method"></a><span data-ttu-id="5706b-104">ID3DXFont: método reloadText de:P</span><span class="sxs-lookup"><span data-stu-id="5706b-104">ID3DXFont::PreloadText method</span></span>

<span data-ttu-id="5706b-105">Carrega texto formatado em memória de vídeo para melhorar a eficiência da renderização para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5706b-105">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="5706b-106">Esse método dá suporte a cadeias de caracteres ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="5706b-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="5706b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5706b-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCTSTR *pString,
  [in] INT     Count
);
```



## <a name="parameters"></a><span data-ttu-id="5706b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5706b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5706b-109">*pString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5706b-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5706b-110">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5706b-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5706b-111">Ponteiro para uma cadeia de caracteres a ser carregada na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5706b-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="5706b-112">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR; caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5706b-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="5706b-113">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="5706b-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5706b-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="5706b-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5706b-115">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5706b-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5706b-116">Número de caracteres na cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="5706b-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5706b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5706b-117">Return value</span></span>

<span data-ttu-id="5706b-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5706b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5706b-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5706b-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5706b-120">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="5706b-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="5706b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5706b-121">Remarks</span></span>

<span data-ttu-id="5706b-122">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="5706b-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="5706b-123">Se o Unicode for definido, a chamada de função será resolvida como PreloadTextW.</span><span class="sxs-lookup"><span data-stu-id="5706b-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="5706b-124">Caso contrário, a chamada de função é resolvida como PreloadTextA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="5706b-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="5706b-125">Esse método gera texturas que contêm glifos que representam o texto de entrada.</span><span class="sxs-lookup"><span data-stu-id="5706b-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="5706b-126">Os glifos são desenhados como uma série de triângulos.</span><span class="sxs-lookup"><span data-stu-id="5706b-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="5706b-127">O texto não será renderizado para o dispositivo; O [**DrawText**](id3dxfont--drawtext.md) ainda deve ser chamado para renderizar o texto.</span><span class="sxs-lookup"><span data-stu-id="5706b-127">Text will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the text.</span></span> <span data-ttu-id="5706b-128">No entanto, ao carregar texto em memória de vídeo, o **DrawText** usará substancialmente menos recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="5706b-128">However, by preloading text into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="5706b-129">Esse método converte internamente os caracteres em glifos usando a função GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span><span class="sxs-lookup"><span data-stu-id="5706b-129">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="5706b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5706b-130">Requirements</span></span>



| <span data-ttu-id="5706b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5706b-131">Requirement</span></span> | <span data-ttu-id="5706b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="5706b-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5706b-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5706b-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5706b-134"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="5706b-134"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="5706b-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5706b-135">Library</span></span><br/> | <dl> <span data-ttu-id="5706b-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5706b-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5706b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5706b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5706b-138">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="5706b-138">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
