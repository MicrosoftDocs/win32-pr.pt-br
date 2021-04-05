---
description: Cria um objeto de fonte para um dispositivo e uma fonte.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: Função D3DXCreateFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488a400928ecc270612a307fbede971e02b43b25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664053"
---
# <a name="d3dxcreatefont-function"></a><span data-ttu-id="e6ff9-103">Função D3DXCreateFont</span><span class="sxs-lookup"><span data-stu-id="e6ff9-103">D3DXCreateFont function</span></span>

<span data-ttu-id="e6ff9-104">Cria um objeto de fonte para um dispositivo e uma fonte.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-104">Creates a font object for a device and font.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6ff9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6ff9-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="e6ff9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6ff9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6ff9-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6ff9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff9-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e6ff9-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e6ff9-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o dispositivo a ser associado ao objeto Font.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="e6ff9-110">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6ff9-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff9-111">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ff9-111">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6ff9-112">A altura dos caracteres em unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-112">The height of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="e6ff9-113">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6ff9-113">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff9-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ff9-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6ff9-115">A largura dos caracteres em unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-115">The width of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="e6ff9-116">*Peso* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6ff9-116">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff9-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ff9-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6ff9-118">Espessura da face de tipos.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-118">Typeface weight.</span></span> <span data-ttu-id="e6ff9-119">Um exemplo é negrito.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-119">One example is bold.</span></span>

</dd> <dt>

<span data-ttu-id="e6ff9-120">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6ff9-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff9-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ff9-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6ff9-122">O número de níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-122">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="e6ff9-123">*Itálico* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6ff9-123">*Italic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff9-124">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ff9-124">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6ff9-125">True para a fonte em itálico; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-125">True for italic font, false otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="e6ff9-126">Conjunto de *caracteres* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6ff9-126">*CharSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff9-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ff9-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6ff9-128">O conjunto de caracteres da fonte.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-128">The character set of the font.</span></span>

</dd> <dt>

<span data-ttu-id="e6ff9-129">*OutputPrecision* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6ff9-129">*OutputPrecision* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff9-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ff9-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6ff9-131">Especifica como o Windows deve tentar corresponder os tamanhos de fonte e as características desejadas com as fontes reais.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-131">Specifies how Windows should attempt to match the desired font sizes and characteristics with actual fonts.</span></span> <span data-ttu-id="e6ff9-132">Use \_ apenas TT \_ \_ precis por exemplo, para garantir que sempre obtenha uma fonte TrueType.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-132">Use OUT\_TT\_ONLY\_PRECIS for instance, to ensure that you always get a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="e6ff9-133">*Qualidade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e6ff9-133">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff9-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ff9-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6ff9-135">Especifica como o Windows deve corresponder à fonte desejada com uma fonte real.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-135">Specifies how Windows should match the desired font with a real font.</span></span> <span data-ttu-id="e6ff9-136">Ele se aplica somente a fontes rasterizadas e não deve afetar as fontes TrueType.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-136">It applies to raster fonts only and should not affect TrueType fonts.</span></span>

</dd> <dt>

<span data-ttu-id="e6ff9-137">*PitchAndFamily* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6ff9-137">*PitchAndFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff9-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ff9-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6ff9-139">Índice de densidade e família.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-139">Pitch and family index.</span></span>

</dd> <dt>

<span data-ttu-id="e6ff9-140">*pFacename* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6ff9-140">*pFacename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff9-141">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ff9-141">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6ff9-142">Cadeia de caracteres que contém o nome da face de tipos.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-142">String containing the typeface name.</span></span> <span data-ttu-id="e6ff9-143">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-143">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="e6ff9-144">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-144">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="e6ff9-145">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-145">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e6ff9-146">*ppFont* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e6ff9-146">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ff9-147">Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6ff9-147">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="e6ff9-148">Retorna um ponteiro para uma interface [**ID3DXFont**](id3dxfont.md) , representando o objeto Font criado.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-148">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6ff9-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6ff9-149">Return value</span></span>

<span data-ttu-id="e6ff9-150">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e6ff9-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e6ff9-151">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-151">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e6ff9-152">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-152">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6ff9-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6ff9-153">Remarks</span></span>

<span data-ttu-id="e6ff9-154">A criação de um objeto ID3DXFont requer que o dispositivo dê suporte à cor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-154">The creation of an ID3DXFont object requires that the device supports 32-bit color.</span></span>

<span data-ttu-id="e6ff9-155">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-155">The compiler setting also determines the function version.</span></span> <span data-ttu-id="e6ff9-156">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateFontW.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-156">If Unicode is defined, the function call resolves to D3DXCreateFontW.</span></span> <span data-ttu-id="e6ff9-157">Caso contrário, a chamada de função é resolvida como D3DXCreateFontA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="e6ff9-157">Otherwise, the function call resolves to D3DXCreateFontA because ANSI strings are being used.</span></span>

<span data-ttu-id="e6ff9-158">Se você quiser obter mais informações sobre parâmetros de fonte, consulte [a fonte lógica](../gdi/creating-a-logical-font.md).</span><span class="sxs-lookup"><span data-stu-id="e6ff9-158">If you want more information about font parameters, see [The Logical Font](../gdi/creating-a-logical-font.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6ff9-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6ff9-159">Requirements</span></span>



| <span data-ttu-id="e6ff9-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6ff9-160">Requirement</span></span> | <span data-ttu-id="e6ff9-161">Valor</span><span class="sxs-lookup"><span data-stu-id="e6ff9-161">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ff9-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6ff9-162">Header</span></span><br/>  | <dl> <span data-ttu-id="e6ff9-163"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6ff9-163"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e6ff9-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6ff9-164">Library</span></span><br/> | <dl> <span data-ttu-id="e6ff9-165"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6ff9-165"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e6ff9-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6ff9-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ff9-167">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="e6ff9-167">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
