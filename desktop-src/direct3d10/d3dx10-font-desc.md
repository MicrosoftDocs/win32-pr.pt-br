---
description: Define atributos de fonte.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: Estrutura de D3DX10_FONT_DESC (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 0b358c57e6410827177e76e3da30b2f5f9896ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105747693"
---
# <a name="d3dx10_font_desc-structure"></a><span data-ttu-id="943f9-103">\_Estrutura desc de fonte D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="943f9-103">D3DX10\_FONT\_DESC structure</span></span>

<span data-ttu-id="943f9-104">Define atributos de fonte.</span><span class="sxs-lookup"><span data-stu-id="943f9-104">Defines font attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="943f9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="943f9-105">Syntax</span></span>


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
```



## <a name="members"></a><span data-ttu-id="943f9-106">Membros</span><span class="sxs-lookup"><span data-stu-id="943f9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="943f9-107">**Altura**</span><span class="sxs-lookup"><span data-stu-id="943f9-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="943f9-108">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="943f9-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="943f9-109">Altura, em unidades lógicas, da célula ou do caractere de caractere da fonte.</span><span class="sxs-lookup"><span data-stu-id="943f9-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="943f9-110">**Largura**</span><span class="sxs-lookup"><span data-stu-id="943f9-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="943f9-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="943f9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="943f9-112">Largura, em unidades lógicas, de caracteres na fonte.</span><span class="sxs-lookup"><span data-stu-id="943f9-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="943f9-113">**Weight**</span><span class="sxs-lookup"><span data-stu-id="943f9-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="943f9-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="943f9-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="943f9-115">Peso da fonte no intervalo de 0 a 1000.</span><span class="sxs-lookup"><span data-stu-id="943f9-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="943f9-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="943f9-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="943f9-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="943f9-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="943f9-118">Número de níveis de mipmap solicitados.</span><span class="sxs-lookup"><span data-stu-id="943f9-118">Number of mipmap levels requested.</span></span> <span data-ttu-id="943f9-119">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="943f9-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="943f9-120">Se o valor for 1, o espaço de textura será mapeado de forma idêntica ao espaço da tela.</span><span class="sxs-lookup"><span data-stu-id="943f9-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="943f9-121">**Itálico**</span><span class="sxs-lookup"><span data-stu-id="943f9-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="943f9-122">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="943f9-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="943f9-123">Defina como **true** para uma fonte em itálico.</span><span class="sxs-lookup"><span data-stu-id="943f9-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="943f9-124">**CharSet**</span><span class="sxs-lookup"><span data-stu-id="943f9-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="943f9-125">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="943f9-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="943f9-126">Conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="943f9-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="943f9-127">**OutputPrecision**</span><span class="sxs-lookup"><span data-stu-id="943f9-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="943f9-128">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="943f9-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="943f9-129">Precisão de saída.</span><span class="sxs-lookup"><span data-stu-id="943f9-129">Output precision.</span></span> <span data-ttu-id="943f9-130">A precisão de saída define o quão próximo a saída deve corresponder à altura da fonte, largura, orientação do caractere, escape, Tom e tipo de fonte solicitados.</span><span class="sxs-lookup"><span data-stu-id="943f9-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="943f9-131">**Qualidade**</span><span class="sxs-lookup"><span data-stu-id="943f9-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="943f9-132">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="943f9-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="943f9-133">Qualidade de saída.</span><span class="sxs-lookup"><span data-stu-id="943f9-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="943f9-134">**PitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="943f9-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="943f9-135">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="943f9-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="943f9-136">Densidade e família da fonte.</span><span class="sxs-lookup"><span data-stu-id="943f9-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="943f9-137">**Face \[ Al LF \_ faces\]**</span><span class="sxs-lookup"><span data-stu-id="943f9-137">**FaceName\[LF\_FACESIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="943f9-138">Tipo: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="943f9-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="943f9-139">Uma cadeia de caracteres terminada em nulo que especifica o nome de tipo da fonte.</span><span class="sxs-lookup"><span data-stu-id="943f9-139">A NULL-terminated string that specifies the typeface name of the font.</span></span> <span data-ttu-id="943f9-140">O comprimento da cadeia de caracteres não deve exceder 32 caracteres, incluindo o caractere **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="943f9-140">The length of the string must not exceed 32 characters, including the terminating **NULL** character.</span></span> <span data-ttu-id="943f9-141">Se facename for uma cadeia de caracteres vazia, a primeira fonte que corresponde aos outros atributos especificados será usada.</span><span class="sxs-lookup"><span data-stu-id="943f9-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="943f9-142">Se as configurações do compilador exigirem Unicode, o tipo de dados TCHAR será resolvido para WCHAR; caso contrário, o tipo de dados será resolvido para CHAR.</span><span class="sxs-lookup"><span data-stu-id="943f9-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="943f9-143">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="943f9-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="943f9-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="943f9-144">Remarks</span></span>

<span data-ttu-id="943f9-145">A configuração do compilador também determina o tipo de estrutura.</span><span class="sxs-lookup"><span data-stu-id="943f9-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="943f9-146">Se o Unicode estiver definido, o \_ tipo de estrutura desc de fonte D3DX10 será \_ resolvido para uma \_ fonte D3DX10 \_ DESCW; caso contrário, o tipo de estrutura será resolvido para uma \_ fonte D3DX10 \_ desca.</span><span class="sxs-lookup"><span data-stu-id="943f9-146">If Unicode is defined, the D3DX10\_FONT\_DESC structure type resolves to a D3DX10\_FONT\_DESCW; otherwise the structure type resolves to a D3DX10\_FONT\_DESCA.</span></span>

<span data-ttu-id="943f9-147">Os valores possíveis dos membros acima são fornecidos na estrutura GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="943f9-147">Possible values of the above members are given in the GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="943f9-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="943f9-148">Requirements</span></span>



| <span data-ttu-id="943f9-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="943f9-149">Requirement</span></span> | <span data-ttu-id="943f9-150">Valor</span><span class="sxs-lookup"><span data-stu-id="943f9-150">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="943f9-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="943f9-151">Header</span></span><br/> | <dl> <span data-ttu-id="943f9-152"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="943f9-152"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="943f9-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="943f9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943f9-154">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="943f9-154">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
