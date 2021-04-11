---
description: Carregue o texto formatado na memória de vídeo para melhorar a eficiência da renderização para o dispositivo. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: 'ID3DX10Font: método reloadText de:P (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7294fb7e86b3532960a34a15e1118dc33f748f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173021"
---
# <a name="id3dx10fontpreloadtext-method"></a><span data-ttu-id="5991a-104">ID3DX10Font: método reloadText de:P</span><span class="sxs-lookup"><span data-stu-id="5991a-104">ID3DX10Font::PreloadText method</span></span>

<span data-ttu-id="5991a-105">Carregue o texto formatado na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5991a-105">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="5991a-106">Esse método dá suporte a cadeias de caracteres ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="5991a-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="5991a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5991a-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a><span data-ttu-id="5991a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5991a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5991a-109">*pString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5991a-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5991a-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5991a-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5991a-111">Ponteiro para uma cadeia de caracteres a ser carregada na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5991a-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="5991a-112">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR; caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5991a-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="5991a-113">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="5991a-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5991a-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="5991a-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5991a-115">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5991a-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5991a-116">Número de caracteres na cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="5991a-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5991a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5991a-117">Return value</span></span>

<span data-ttu-id="5991a-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5991a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5991a-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5991a-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5991a-120">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="5991a-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="5991a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5991a-121">Remarks</span></span>

<span data-ttu-id="5991a-122">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="5991a-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="5991a-123">Se o Unicode for definido, a chamada de função será resolvida como PreloadTextW.</span><span class="sxs-lookup"><span data-stu-id="5991a-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="5991a-124">Caso contrário, a chamada de função é resolvida como PreloadTextA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="5991a-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="5991a-125">Esse método gera texturas que contêm glifos que representam o texto de entrada.</span><span class="sxs-lookup"><span data-stu-id="5991a-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="5991a-126">Os glifos são desenhados como uma série de triângulos.</span><span class="sxs-lookup"><span data-stu-id="5991a-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="5991a-127">O texto não será renderizado para o dispositivo; ID3DX10Font::D rawText ainda deve ser chamado para renderizar o texto.</span><span class="sxs-lookup"><span data-stu-id="5991a-127">Text will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the text.</span></span> <span data-ttu-id="5991a-128">No entanto, ao carregar texto em memória de vídeo, ID3DX10Font:D: o rawText usará substancialmente menos recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="5991a-128">However, by preloading text into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="5991a-129">Esse método converte internamente os caracteres em glifos usando a função GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5991a-129">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="5991a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5991a-130">Requirements</span></span>



| <span data-ttu-id="5991a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5991a-131">Requirement</span></span> | <span data-ttu-id="5991a-132">Valor</span><span class="sxs-lookup"><span data-stu-id="5991a-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5991a-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5991a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5991a-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5991a-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5991a-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5991a-135">Library</span></span><br/> | <dl> <span data-ttu-id="5991a-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5991a-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5991a-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5991a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5991a-138">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="5991a-138">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="5991a-139">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="5991a-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
