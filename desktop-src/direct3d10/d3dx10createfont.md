---
description: Cria um objeto de fonte para um dispositivo e uma fonte. Observação em vez de usar essa função, recomendamos que você use DirectWrite e a biblioteca DirectXTK, SpriteFont Class.
ms.assetid: a0dd02f1-c512-46d3-9e83-a785ac3ad7ee
title: Função D3DX10CreateFont (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFont
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6e5966e50c9c997085d35854868a2a7dd0455c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807875"
---
# <a name="d3dx10createfont-function"></a><span data-ttu-id="75c32-103">Função D3DX10CreateFont</span><span class="sxs-lookup"><span data-stu-id="75c32-103">D3DX10CreateFont function</span></span>

<span data-ttu-id="75c32-104">Cria um objeto de fonte para um dispositivo e uma fonte.</span><span class="sxs-lookup"><span data-stu-id="75c32-104">Creates a font object for a device and font.</span></span>

> [!Note]  
> <span data-ttu-id="75c32-105">Em vez de usar essa função, recomendamos que você use [DirectWrite](../directwrite/direct-write-portal.md) e a biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteFont** Class.</span><span class="sxs-lookup"><span data-stu-id="75c32-105">Instead of using this function, we recommend that you use [DirectWrite](../directwrite/direct-write-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteFont** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="75c32-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75c32-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateFont(
  _In_  ID3D10Device *pDevice,
  _In_  INT          Height,
  _In_  UINT         Width,
  _In_  UINT         Weight,
  _In_  UINT         MipLevels,
  _In_  BOOL         Italic,
  _In_  UINT         CharSet,
  _In_  UINT         OutputPrecision,
  _In_  UINT         Quality,
  _In_  UINT         PitchAndFamily,
  _In_  LPCTSTR      pFaceName,
  _Out_ LPD3DX10FONT *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="75c32-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75c32-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c32-108">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75c32-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c32-109">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="75c32-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="75c32-110">Ponteiro para uma interface ID3D10Device, o dispositivo a ser associado ao objeto Font.</span><span class="sxs-lookup"><span data-stu-id="75c32-110">Pointer to an ID3D10Device interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="75c32-111">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75c32-111">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c32-112">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75c32-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75c32-113">A altura dos caracteres em unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="75c32-113">The height of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="75c32-114">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75c32-114">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c32-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75c32-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75c32-116">A largura dos caracteres em unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="75c32-116">The width of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="75c32-117">*Peso* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75c32-117">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c32-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75c32-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75c32-119">Espessura da face de tipos.</span><span class="sxs-lookup"><span data-stu-id="75c32-119">Typeface weight.</span></span> <span data-ttu-id="75c32-120">Um exemplo é negrito.</span><span class="sxs-lookup"><span data-stu-id="75c32-120">One example is bold.</span></span>

</dd> <dt>

<span data-ttu-id="75c32-121">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75c32-121">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c32-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75c32-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75c32-123">O número de níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="75c32-123">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="75c32-124">*Itálico* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75c32-124">*Italic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c32-125">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75c32-125">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75c32-126">True para a fonte em itálico; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="75c32-126">True for italic font, false otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="75c32-127">Conjunto de *caracteres* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75c32-127">*CharSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c32-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75c32-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75c32-129">O conjunto de caracteres da fonte.</span><span class="sxs-lookup"><span data-stu-id="75c32-129">The character set of the font.</span></span>

</dd> <dt>

<span data-ttu-id="75c32-130">*OutputPrecision* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75c32-130">*OutputPrecision* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c32-131">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75c32-131">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75c32-132">Especifica como o Windows deve tentar corresponder os tamanhos de fonte e as características desejadas com as fontes reais.</span><span class="sxs-lookup"><span data-stu-id="75c32-132">Specifies how Windows should attempt to match the desired font sizes and characteristics with actual fonts.</span></span> <span data-ttu-id="75c32-133">Use \_ apenas TT \_ \_ precis por exemplo, para garantir que sempre obtenha uma fonte TrueType.</span><span class="sxs-lookup"><span data-stu-id="75c32-133">Use OUT\_TT\_ONLY\_PRECIS for instance, to ensure that you always get a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="75c32-134">*Qualidade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="75c32-134">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c32-135">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75c32-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75c32-136">Especifica como o Windows deve corresponder à fonte desejada com uma fonte real.</span><span class="sxs-lookup"><span data-stu-id="75c32-136">Specifies how Windows should match the desired font with a real font.</span></span> <span data-ttu-id="75c32-137">Ele se aplica somente a fontes rasterizadas e não deve afetar as fontes TrueType.</span><span class="sxs-lookup"><span data-stu-id="75c32-137">It applies to raster fonts only and should not affect TrueType fonts.</span></span>

</dd> <dt>

<span data-ttu-id="75c32-138">*PitchAndFamily* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75c32-138">*PitchAndFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c32-139">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75c32-139">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75c32-140">Índice de densidade e família.</span><span class="sxs-lookup"><span data-stu-id="75c32-140">Pitch and family index.</span></span>

</dd> <dt>

<span data-ttu-id="75c32-141">*pFaceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75c32-141">*pFaceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c32-142">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75c32-142">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75c32-143">Cadeia de caracteres que contém o nome da face de tipos.</span><span class="sxs-lookup"><span data-stu-id="75c32-143">String containing the typeface name.</span></span> <span data-ttu-id="75c32-144">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="75c32-144">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="75c32-145">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="75c32-145">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="75c32-146">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="75c32-146">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="75c32-147">*ppFont* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="75c32-147">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75c32-148">Tipo: **[ **LPD3DX10FONT**](id3dx10font.md)\***</span><span class="sxs-lookup"><span data-stu-id="75c32-148">Type: **[**LPD3DX10FONT**](id3dx10font.md)\***</span></span>

<span data-ttu-id="75c32-149">Retorna um ponteiro para uma interface ID3DX10Font, representando o objeto Font criado.</span><span class="sxs-lookup"><span data-stu-id="75c32-149">Returns a pointer to an ID3DX10Font interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c32-150">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75c32-150">Return value</span></span>

<span data-ttu-id="75c32-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75c32-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75c32-152">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="75c32-152">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="75c32-153">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="75c32-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="75c32-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="75c32-154">Remarks</span></span>

<span data-ttu-id="75c32-155">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="75c32-155">The compiler setting also determines the function version.</span></span> <span data-ttu-id="75c32-156">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateFontW.</span><span class="sxs-lookup"><span data-stu-id="75c32-156">If Unicode is defined, the function call resolves to D3DXCreateFontW.</span></span> <span data-ttu-id="75c32-157">Caso contrário, a chamada de função é resolvida como D3DXCreateFontA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="75c32-157">Otherwise, the function call resolves to D3DXCreateFontA because ANSI strings are being used.</span></span>

<span data-ttu-id="75c32-158">Se você quiser obter mais informações sobre parâmetros de fonte, consulte [a fonte lógica](/previous-versions//ms533985(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="75c32-158">If you want more information about font parameters, see [The Logical Font](/previous-versions//ms533985(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="75c32-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75c32-159">Requirements</span></span>



| <span data-ttu-id="75c32-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="75c32-160">Requirement</span></span> | <span data-ttu-id="75c32-161">Valor</span><span class="sxs-lookup"><span data-stu-id="75c32-161">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75c32-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75c32-162">Header</span></span><br/>  | <dl> <span data-ttu-id="75c32-163"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="75c32-163"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="75c32-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75c32-164">Library</span></span><br/> | <dl> <span data-ttu-id="75c32-165"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75c32-165"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75c32-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="75c32-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c32-167">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="75c32-167">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
