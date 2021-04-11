---
description: Desenha texto formatado. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: 'ID3DXFont: método rawText de:D (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.DrawText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96636c372ee48d516286935f03d80b8e9815ffc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172994"
---
# <a name="id3dxfontdrawtext-method"></a><span data-ttu-id="650cb-104">ID3DXFont: método rawText de:D</span><span class="sxs-lookup"><span data-stu-id="650cb-104">ID3DXFont::DrawText method</span></span>

<span data-ttu-id="650cb-105">Desenha texto formatado.</span><span class="sxs-lookup"><span data-stu-id="650cb-105">Draws formatted text.</span></span> <span data-ttu-id="650cb-106">Esse método dá suporte a cadeias de caracteres ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="650cb-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="650cb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="650cb-107">Syntax</span></span>


```C++
INT DrawText(
  [in] LPD3DXSPRITE pSprite,
  [in] LPCTSTR      pString,
  [in] INT          Count,
  [in] LPRECT       pRect,
  [in] DWORD        Format,
  [in] D3DCOLOR     Color
);
```



## <a name="parameters"></a><span data-ttu-id="650cb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="650cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="650cb-109">*pSprite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="650cb-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="650cb-110">Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)**</span><span class="sxs-lookup"><span data-stu-id="650cb-110">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)**</span></span>

<span data-ttu-id="650cb-111">Ponteiro para um objeto [**ID3DXSprite**](id3dxsprite.md) que contém a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="650cb-111">Pointer to an [**ID3DXSprite**](id3dxsprite.md) object that contains the string.</span></span> <span data-ttu-id="650cb-112">Pode ser **NULL**; nesse caso, o Direct3D renderizará a cadeia de caracteres com seu próprio objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="650cb-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="650cb-113">Para melhorar a eficiência, um objeto Sprite deve ser especificado se o **DrawText** for ser chamado mais de uma vez em uma linha.</span><span class="sxs-lookup"><span data-stu-id="650cb-113">To improve efficiency, a sprite object should be specified if **DrawText** is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="650cb-114">*pString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="650cb-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="650cb-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="650cb-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="650cb-116">Ponteiro para uma cadeia de caracteres a ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="650cb-116">Pointer to a string to draw.</span></span> <span data-ttu-id="650cb-117">Se o parâmetro Count for-1, a cadeia de caracteres deverá ser terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="650cb-117">If the Count parameter is -1, the string must be null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="650cb-118">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="650cb-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="650cb-119">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="650cb-119">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="650cb-120">Especifica o número de caracteres na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="650cb-120">Specifies the number of characters in the string.</span></span> <span data-ttu-id="650cb-121">Se Count for-1, o parâmetro pString será considerado como um ponteiro para uma cadeia de caracteres terminada em nulo e o **DrawText** calculará automaticamente a contagem de caracteres.</span><span class="sxs-lookup"><span data-stu-id="650cb-121">If Count is -1, then the pString parameter is assumed to be a pointer to a null-terminated string and **DrawText** computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="650cb-122">*pRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="650cb-122">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="650cb-123">Tipo: **[ **lpRect**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="650cb-123">Type: **[**LPRECT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="650cb-124">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém o retângulo, em coordenadas lógicas, em que o texto deve ser formatado.</span><span class="sxs-lookup"><span data-stu-id="650cb-124">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="650cb-125">O valor da coordenada do lado direito do retângulo deve ser maior do que o do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="650cb-125">The coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="650cb-126">Da mesma forma, o valor da coordenada da parte inferior deve ser maior que o da parte superior.</span><span class="sxs-lookup"><span data-stu-id="650cb-126">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="650cb-127">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="650cb-127">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="650cb-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="650cb-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="650cb-129">Especifica o método de formatação do texto.</span><span class="sxs-lookup"><span data-stu-id="650cb-129">Specifies the method of formatting the text.</span></span> <span data-ttu-id="650cb-130">Pode ser qualquer combinação dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="650cb-130">It can be any combination of the following values:</span></span>



| <span data-ttu-id="650cb-131">Valor</span><span class="sxs-lookup"><span data-stu-id="650cb-131">Value</span></span>                                                                                                                                                         | <span data-ttu-id="650cb-132">Significado</span><span class="sxs-lookup"><span data-stu-id="650cb-132">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <span data-ttu-id="650cb-133"><dt>**\_parte inferior de DT**</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-133"><dt>**DT\_BOTTOM**</dt></span></span> </dl>             | <span data-ttu-id="650cb-134">Justifica o texto na parte inferior do retângulo.</span><span class="sxs-lookup"><span data-stu-id="650cb-134">Justifies the text to the bottom of the rectangle.</span></span> <span data-ttu-id="650cb-135">Esse valor deve ser combinado com \_ uma única de DT.</span><span class="sxs-lookup"><span data-stu-id="650cb-135">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <span data-ttu-id="650cb-136"><dt>**\_CALCRECT DT**</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-136"><dt>**DT\_CALCRECT**</dt></span></span> </dl>       | <span data-ttu-id="650cb-137">Determina a largura e a altura do retângulo.</span><span class="sxs-lookup"><span data-stu-id="650cb-137">Determines the width and height of the rectangle.</span></span> <span data-ttu-id="650cb-138">Se houver várias linhas de texto, o **DrawText** usará a largura do retângulo apontado pelo parâmetro pRect e estenderá a base do retângulo para associar a última linha de texto.</span><span class="sxs-lookup"><span data-stu-id="650cb-138">If there are multiple lines of text, **DrawText** uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="650cb-139">Se houver apenas uma linha de texto, **DrawText** modificará o lado direito do retângulo para que ele limite o último caractere na linha.</span><span class="sxs-lookup"><span data-stu-id="650cb-139">If there is only one line of text, **DrawText** modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="650cb-140">Em ambos os casos, **DrawText** retorna a altura do texto formatado, mas não desenha o texto.</span><span class="sxs-lookup"><span data-stu-id="650cb-140">In either case, **DrawText** returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <span data-ttu-id="650cb-141"><dt>**Centro de DT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-141"><dt>**DT\_CENTER**</dt></span></span> </dl>             | <span data-ttu-id="650cb-142">Centraliza o texto horizontalmente no retângulo.</span><span class="sxs-lookup"><span data-stu-id="650cb-142">Centers text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <span data-ttu-id="650cb-143"><dt>**\_EXPANDTABS DT**</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-143"><dt>**DT\_EXPANDTABS**</dt></span></span> </dl> | <span data-ttu-id="650cb-144">Amplia os caracteres da guia.</span><span class="sxs-lookup"><span data-stu-id="650cb-144">Expands tab characters.</span></span> <span data-ttu-id="650cb-145">O número padrão de caracteres por guia é oito.</span><span class="sxs-lookup"><span data-stu-id="650cb-145">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <span data-ttu-id="650cb-146"><dt>**DT \_ restante**</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-146"><dt>**DT\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="650cb-147">Alinha o texto à esquerda.</span><span class="sxs-lookup"><span data-stu-id="650cb-147">Aligns text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <span data-ttu-id="650cb-148"><dt>**noclip de DT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-148"><dt>**DT\_NOCLIP**</dt></span></span> </dl>             | <span data-ttu-id="650cb-149">Desenha sem recorte.</span><span class="sxs-lookup"><span data-stu-id="650cb-149">Draws without clipping.</span></span> <span data-ttu-id="650cb-150">O **DrawText** é um pouco mais rápido quando o DT \_ noclip é usado.</span><span class="sxs-lookup"><span data-stu-id="650cb-150">**DrawText** is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <span data-ttu-id="650cb-151"><dt>**DT \_ à direita**</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-151"><dt>**DT\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="650cb-152">Alinha o texto à direita.</span><span class="sxs-lookup"><span data-stu-id="650cb-152">Aligns text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <span data-ttu-id="650cb-153"><dt>**\_RTLREADING DT**</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-153"><dt>**DT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="650cb-154">Exibe o texto na ordem de leitura da direita para a esquerda para texto bidirecional quando uma fonte hebraico ou árabe é selecionada.</span><span class="sxs-lookup"><span data-stu-id="650cb-154">Displays text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="650cb-155">A ordem de leitura padrão para todo o texto é da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="650cb-155">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <span data-ttu-id="650cb-156"><dt>**única de DT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-156"><dt>**DT\_SINGLELINE**</dt></span></span> </dl> | <span data-ttu-id="650cb-157">Exibe o texto somente em uma única linha.</span><span class="sxs-lookup"><span data-stu-id="650cb-157">Displays text on a single line only.</span></span> <span data-ttu-id="650cb-158">Retornos de carro e feeds de linha não quebram a linha.</span><span class="sxs-lookup"><span data-stu-id="650cb-158">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <span data-ttu-id="650cb-159"><dt>**início da DT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-159"><dt>**DT\_TOP**</dt></span></span> </dl>                      | <span data-ttu-id="650cb-160">Justifica o texto na parte superior.</span><span class="sxs-lookup"><span data-stu-id="650cb-160">Top-justifies text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <span data-ttu-id="650cb-161"><dt>**\_VCENTER DT**</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-161"><dt>**DT\_VCENTER**</dt></span></span> </dl>          | <span data-ttu-id="650cb-162">Centraliza o texto verticalmente (somente linha única).</span><span class="sxs-lookup"><span data-stu-id="650cb-162">Centers text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <span data-ttu-id="650cb-163"><dt>**\_justificação DT**</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-163"><dt>**DT\_WORDBREAK**</dt></span></span> </dl>    | <span data-ttu-id="650cb-164">Quebra palavras.</span><span class="sxs-lookup"><span data-stu-id="650cb-164">Breaks words.</span></span> <span data-ttu-id="650cb-165">As linhas são quebradas automaticamente entre as palavras se uma palavra ultrapassar a borda do retângulo especificado pelo parâmetro pRect.</span><span class="sxs-lookup"><span data-stu-id="650cb-165">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="650cb-166">Uma sequência de retorno de carro/alimentação de linha também quebra a linha.</span><span class="sxs-lookup"><span data-stu-id="650cb-166">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="650cb-167">*Cor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="650cb-167">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="650cb-168">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="650cb-168">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="650cb-169">Cor do texto.</span><span class="sxs-lookup"><span data-stu-id="650cb-169">Color of the text.</span></span> <span data-ttu-id="650cb-170">Para obter mais informações, consulte [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="650cb-170">For more information, see [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="650cb-171">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="650cb-171">Return value</span></span>

<span data-ttu-id="650cb-172">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="650cb-172">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="650cb-173">Se a função for realizada com sucesso, o valor de retorno será a altura do texto em unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="650cb-173">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="650cb-174">Se \_ \_ a parte inferior de DT VCENTER ou DT for especificada, o valor de retorno será o deslocamento de pRect (superior à parte inferior) do texto desenhado.</span><span class="sxs-lookup"><span data-stu-id="650cb-174">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="650cb-175">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="650cb-175">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="650cb-176">Comentários</span><span class="sxs-lookup"><span data-stu-id="650cb-176">Remarks</span></span>

<span data-ttu-id="650cb-177">Os parâmetros desse método são muito semelhantes aos da função [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) do GDI.</span><span class="sxs-lookup"><span data-stu-id="650cb-177">The parameters of this method are very similar to those of the GDI [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) function.</span></span>

<span data-ttu-id="650cb-178">Esse método dá suporte a cadeias de caracteres ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="650cb-178">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="650cb-179">Este método deve ser chamado dentro de um [**BeginScene**](/windows/desktop/api) ... Bloco [**endcena**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .</span><span class="sxs-lookup"><span data-stu-id="650cb-179">This method must be called inside a [**BeginScene**](/windows/desktop/api) ... [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) block.</span></span> <span data-ttu-id="650cb-180">A única exceção é quando um aplicativo chama **DrawText** com \_ CALCRECT DT para calcular o tamanho de um determinado bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="650cb-180">The only exception is when an application calls **DrawText** with DT\_CALCRECT to calculate the size of a given block of text.</span></span>

<span data-ttu-id="650cb-181">A menos que o \_ formato noclip de DT seja usado, esse método corta o texto para que ele não apareça fora do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="650cb-181">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="650cb-182">É presumida que toda a formatação tenha várias linhas, a menos que o formato de linha \_ simples DT seja especificado.</span><span class="sxs-lookup"><span data-stu-id="650cb-182">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="650cb-183">Se a fonte selecionada for muito grande para o retângulo, esse método não tentará substituir uma fonte menor.</span><span class="sxs-lookup"><span data-stu-id="650cb-183">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="650cb-184">Esse método dá suporte apenas a fontes cuja escape e orientação são zero.</span><span class="sxs-lookup"><span data-stu-id="650cb-184">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="650cb-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="650cb-185">Requirements</span></span>



| <span data-ttu-id="650cb-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="650cb-186">Requirement</span></span> | <span data-ttu-id="650cb-187">Valor</span><span class="sxs-lookup"><span data-stu-id="650cb-187">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="650cb-188">parâmetro</span><span class="sxs-lookup"><span data-stu-id="650cb-188">Header</span></span><br/>  | <dl> <span data-ttu-id="650cb-189"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-189"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="650cb-190">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="650cb-190">Library</span></span><br/> | <dl> <span data-ttu-id="650cb-191"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="650cb-191"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="650cb-192">Confira também</span><span class="sxs-lookup"><span data-stu-id="650cb-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="650cb-193">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="650cb-193">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
