---
description: Define os atributos de uma fonte.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: Estrutura de D3DXFONT_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812402"
---
# <a name="d3dxfont_desc-structure"></a><span data-ttu-id="9437e-103">\_Estrutura desc de D3DXFONT</span><span class="sxs-lookup"><span data-stu-id="9437e-103">D3DXFONT\_DESC structure</span></span>

<span data-ttu-id="9437e-104">Define os atributos de uma fonte.</span><span class="sxs-lookup"><span data-stu-id="9437e-104">Defines the attributes of a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="9437e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9437e-105">Syntax</span></span>


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a><span data-ttu-id="9437e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9437e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9437e-107">**Altura**</span><span class="sxs-lookup"><span data-stu-id="9437e-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="9437e-108">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9437e-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9437e-109">Altura, em unidades lógicas, da célula ou do caractere de caractere da fonte.</span><span class="sxs-lookup"><span data-stu-id="9437e-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="9437e-110">**Largura**</span><span class="sxs-lookup"><span data-stu-id="9437e-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="9437e-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9437e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9437e-112">Largura, em unidades lógicas, de caracteres na fonte.</span><span class="sxs-lookup"><span data-stu-id="9437e-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="9437e-113">**Weight**</span><span class="sxs-lookup"><span data-stu-id="9437e-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="9437e-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9437e-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9437e-115">Peso da fonte no intervalo de 0 a 1000.</span><span class="sxs-lookup"><span data-stu-id="9437e-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="9437e-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="9437e-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="9437e-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9437e-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9437e-118">Número de níveis de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="9437e-118">Number of mip levels requested.</span></span> <span data-ttu-id="9437e-119">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="9437e-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="9437e-120">Se o valor for 1, o espaço de textura será mapeado de forma idêntica ao espaço da tela.</span><span class="sxs-lookup"><span data-stu-id="9437e-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="9437e-121">**Itálico**</span><span class="sxs-lookup"><span data-stu-id="9437e-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="9437e-122">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9437e-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9437e-123">Defina como **true** para uma fonte em itálico.</span><span class="sxs-lookup"><span data-stu-id="9437e-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="9437e-124">**CharSet**</span><span class="sxs-lookup"><span data-stu-id="9437e-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="9437e-125">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9437e-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9437e-126">Conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9437e-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="9437e-127">**OutputPrecision**</span><span class="sxs-lookup"><span data-stu-id="9437e-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="9437e-128">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9437e-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9437e-129">Precisão de saída.</span><span class="sxs-lookup"><span data-stu-id="9437e-129">Output precision.</span></span> <span data-ttu-id="9437e-130">A precisão de saída define o quão próximo a saída deve corresponder à altura da fonte, largura, orientação do caractere, escape, Tom e tipo de fonte solicitados.</span><span class="sxs-lookup"><span data-stu-id="9437e-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="9437e-131">**Qualidade**</span><span class="sxs-lookup"><span data-stu-id="9437e-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="9437e-132">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9437e-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9437e-133">Qualidade de saída.</span><span class="sxs-lookup"><span data-stu-id="9437e-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="9437e-134">**PitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="9437e-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="9437e-135">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9437e-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9437e-136">Densidade e família da fonte.</span><span class="sxs-lookup"><span data-stu-id="9437e-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="9437e-137">**FaceName**</span><span class="sxs-lookup"><span data-stu-id="9437e-137">**FaceName**</span></span>
</dt> <dd>

<span data-ttu-id="9437e-138">Tipo: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="9437e-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="9437e-139">Uma cadeia de caracteres terminada em nulo que especifica o nome de tipo da fonte.</span><span class="sxs-lookup"><span data-stu-id="9437e-139">A null-terminated string or characters that specifies the typeface name of the font.</span></span> <span data-ttu-id="9437e-140">O comprimento da cadeia de caracteres não deve exceder 32 caracteres, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="9437e-140">The length of the string must not exceed 32 characters, including the terminating null character.</span></span> <span data-ttu-id="9437e-141">Se facename for uma cadeia de caracteres vazia, a primeira fonte que corresponde aos outros atributos especificados será usada.</span><span class="sxs-lookup"><span data-stu-id="9437e-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="9437e-142">Se as configurações do compilador exigirem Unicode, o tipo de dados TCHAR será resolvido para WCHAR; caso contrário, o tipo de dados será resolvido para CHAR.</span><span class="sxs-lookup"><span data-stu-id="9437e-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="9437e-143">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="9437e-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9437e-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="9437e-144">Remarks</span></span>

<span data-ttu-id="9437e-145">A configuração do compilador também determina o tipo de estrutura.</span><span class="sxs-lookup"><span data-stu-id="9437e-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="9437e-146">Se o Unicode estiver definido, o \_ tipo de estrutura desc D3DXFONT resolverá para um D3DXFONT \_ DESCW; caso contrário, o tipo de estrutura será resolvido para um D3DXFONT \_ desca.</span><span class="sxs-lookup"><span data-stu-id="9437e-146">If Unicode is defined, the D3DXFONT\_DESC structure type resolves to a D3DXFONT\_DESCW; otherwise the structure type resolves to a D3DXFONT\_DESCA.</span></span>

<span data-ttu-id="9437e-147">Os valores possíveis dos membros acima são fornecidos na estrutura GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="9437e-147">Possible values of the above members are given in the GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9437e-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9437e-148">Requirements</span></span>



| <span data-ttu-id="9437e-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="9437e-149">Requirement</span></span> | <span data-ttu-id="9437e-150">Valor</span><span class="sxs-lookup"><span data-stu-id="9437e-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9437e-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9437e-151">Header</span></span><br/> | <dl> <span data-ttu-id="9437e-152"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9437e-152"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9437e-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="9437e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9437e-154">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="9437e-154">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="9437e-155">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="9437e-155">**GetDesc**</span></span>](id3dxfont--getdesc.md)
</dt> </dl>

 

 
