---
description: Cria uma malha que contém o texto especificado, usando a fonte associada ao contexto do dispositivo.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: Função D3DXCreateText (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f6202a534dde727e21b6513ad30077f2e3b3e52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788948"
---
# <a name="d3dxcreatetext-function"></a><span data-ttu-id="bd771-103">Função D3DXCreateText</span><span class="sxs-lookup"><span data-stu-id="bd771-103">D3DXCreateText function</span></span>

<span data-ttu-id="bd771-104">Cria uma malha que contém o texto especificado, usando a fonte associada ao contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd771-104">Creates a mesh containing the specified text, using the font associated with the device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd771-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd771-105">Syntax</span></span>


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="bd771-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd771-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd771-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bd771-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd771-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="bd771-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="bd771-109">Ponteiro para o dispositivo que criou a malha.</span><span class="sxs-lookup"><span data-stu-id="bd771-109">Pointer to the device that created the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="bd771-110">*HDC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bd771-110">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd771-111">Tipo: **HDC**</span><span class="sxs-lookup"><span data-stu-id="bd771-111">Type: **HDC**</span></span>

<span data-ttu-id="bd771-112">Contexto do dispositivo, que contém a fonte para saída.</span><span class="sxs-lookup"><span data-stu-id="bd771-112">Device context, containing the font for output.</span></span> <span data-ttu-id="bd771-113">A fonte selecionada pelo contexto do dispositivo deve ser uma fonte TrueType.</span><span class="sxs-lookup"><span data-stu-id="bd771-113">The font selected by the device context must be a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="bd771-114">*pText* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bd771-114">*pText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd771-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd771-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd771-116">Ponteiro para uma cadeia de caracteres que especifica o texto a ser gerado.</span><span class="sxs-lookup"><span data-stu-id="bd771-116">Pointer to a string that specifies the text to generate.</span></span> <span data-ttu-id="bd771-117">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="bd771-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="bd771-118">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="bd771-118">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="bd771-119">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="bd771-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="bd771-120">*Desvio* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bd771-120">*Deviation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd771-121">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd771-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd771-122">Desvio máximo de corda dos contornos de fonte TrueType.</span><span class="sxs-lookup"><span data-stu-id="bd771-122">Maximum chordal deviation from TrueType font outlines.</span></span>

</dd> <dt>

<span data-ttu-id="bd771-123">*Extrusão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bd771-123">*Extrusion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd771-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd771-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd771-125">Valor para o texto de extrusão na direção z negativa.</span><span class="sxs-lookup"><span data-stu-id="bd771-125">Amount to extrude text in the negative z-direction.</span></span>

</dd> <dt>

<span data-ttu-id="bd771-126">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bd771-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd771-127">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd771-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="bd771-128">Ponteiro para a malha retornada.</span><span class="sxs-lookup"><span data-stu-id="bd771-128">Pointer to the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="bd771-129">*ppAdjacency* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bd771-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd771-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd771-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bd771-131">Ponteiro para um buffer que contém informações de adjacência.</span><span class="sxs-lookup"><span data-stu-id="bd771-131">Pointer to a buffer containing adjacency information.</span></span> <span data-ttu-id="bd771-132">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bd771-132">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bd771-133">*pGlyphMetrics* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bd771-133">*pGlyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd771-134">Tipo: **[ **LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span><span class="sxs-lookup"><span data-stu-id="bd771-134">Type: **[**LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span></span>

<span data-ttu-id="bd771-135">Ponteiro para uma matriz de estruturas [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) que contêm os dados de métrica de glifo.</span><span class="sxs-lookup"><span data-stu-id="bd771-135">Pointer to an array of [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) structures that contain the glyph metric data.</span></span> <span data-ttu-id="bd771-136">Cada elemento contém informações sobre a posição e a orientação do glifo correspondente na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bd771-136">Each element contains information about the position and orientation of the corresponding glyph in the string.</span></span> <span data-ttu-id="bd771-137">O número de elementos na matriz deve ser igual ao número de caracteres na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bd771-137">The number of elements in the array should be equal to the number of characters in the string.</span></span> <span data-ttu-id="bd771-138">Observe que a origem em cada estrutura não é relativa à cadeia de caracteres inteira, mas é relativa a essa célula de caractere.</span><span class="sxs-lookup"><span data-stu-id="bd771-138">Note that the origin in each structure is not relative to the entire string, but rather is relative to that character cell.</span></span> <span data-ttu-id="bd771-139">Para calcular a caixa delimitadora inteira, adicione o incremento para cada glifo ao percorrer a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bd771-139">To compute the entire bounding box, add the increment for each glyph while traversing the string.</span></span> <span data-ttu-id="bd771-140">Se você não estiver preocupado com os tamanhos de glifo, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bd771-140">If you are not concerned with the glyph sizes, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd771-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd771-141">Return value</span></span>

<span data-ttu-id="bd771-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bd771-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bd771-143">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bd771-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bd771-144">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bd771-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd771-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd771-145">Remarks</span></span>

<span data-ttu-id="bd771-146">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="bd771-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="bd771-147">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateTextW.</span><span class="sxs-lookup"><span data-stu-id="bd771-147">If Unicode is defined, the function call resolves to D3DXCreateTextW.</span></span> <span data-ttu-id="bd771-148">Caso contrário, a chamada de função é resolvida como D3DXCreateTextA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="bd771-148">Otherwise, the function call resolves to D3DXCreateTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="bd771-149">Essa função cria uma malha com a \_ opção de criação gerenciada D3DXMESH e [D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) formato de vértice flexível normal (FVF).</span><span class="sxs-lookup"><span data-stu-id="bd771-149">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd771-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd771-150">Requirements</span></span>



| <span data-ttu-id="bd771-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd771-151">Requirement</span></span> | <span data-ttu-id="bd771-152">Valor</span><span class="sxs-lookup"><span data-stu-id="bd771-152">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd771-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd771-153">Header</span></span><br/>  | <dl> <span data-ttu-id="bd771-154"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd771-154"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="bd771-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd771-155">Library</span></span><br/> | <dl> <span data-ttu-id="bd771-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd771-156"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bd771-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd771-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd771-158">Funções de desenho de forma</span><span class="sxs-lookup"><span data-stu-id="bd771-158">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
