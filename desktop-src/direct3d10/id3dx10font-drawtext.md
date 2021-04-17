---
description: Desenhar texto formatado. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: 'ID3DX10Font: método rawText de:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.DrawText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5fa23684be1b63cfbd8e3d07d3578d87fdfbf46a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813457"
---
# <a name="id3dx10fontdrawtext-method"></a><span data-ttu-id="90e40-104">ID3DX10Font: método rawText de:D</span><span class="sxs-lookup"><span data-stu-id="90e40-104">ID3DX10Font::DrawText method</span></span>

<span data-ttu-id="90e40-105">Desenhar texto formatado.</span><span class="sxs-lookup"><span data-stu-id="90e40-105">Draw formatted text.</span></span> <span data-ttu-id="90e40-106">Esse método dá suporte a cadeias de caracteres ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="90e40-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e40-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90e40-107">Syntax</span></span>


```C++
INT DrawText(
  [in] LPD3DX10SPRITE pSprite,
  [in] LPCTSTR        pString,
  [in] INT            Count,
  [in] LPRECT         pRect,
  [in] UINT           Format,
  [in] D3DXCOLOR      Color
);
```



## <a name="parameters"></a><span data-ttu-id="90e40-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90e40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90e40-109">*pSprite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90e40-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e40-110">Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**</span><span class="sxs-lookup"><span data-stu-id="90e40-110">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)**</span></span>

<span data-ttu-id="90e40-111">Ponteiro para um objeto ID3DX10Sprite que contém a cadeia de caracteres que você deseja desenhar.</span><span class="sxs-lookup"><span data-stu-id="90e40-111">Pointer to an ID3DX10Sprite object that contains the string you wish to draw.</span></span> <span data-ttu-id="90e40-112">Pode ser **NULL**; nesse caso, o Direct3D renderizará a cadeia de caracteres com seu próprio objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="90e40-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="90e40-113">Para melhorar a eficiência, um objeto Sprite deve ser especificado se ID3DX10Font::D rawText for ser chamado mais de uma vez em uma linha.</span><span class="sxs-lookup"><span data-stu-id="90e40-113">To improve efficiency, a sprite object should be specified if ID3DX10Font::DrawText is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="90e40-114">*pString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90e40-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e40-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90e40-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90e40-116">Ponteiro para uma cadeia de caracteres a ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="90e40-116">Pointer to a string to draw.</span></span> <span data-ttu-id="90e40-117">Se o UNICODE estiver definido, esse tipo de parâmetro será resolvido como um LPCWSTR, caso contrário, o tipo será resolvido para um LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="90e40-117">If UNICODE is defined, this parameter type resolves to an LPCWSTR, otherwise, the type resolves to an LPCSTR.</span></span> <span data-ttu-id="90e40-118">Se o parâmetro Count for-1, a cadeia de caracteres deverá ser terminada como **NULL** .</span><span class="sxs-lookup"><span data-stu-id="90e40-118">If the Count parameter is -1, the string must be **NULL** terminated.</span></span>

</dd> <dt>

<span data-ttu-id="90e40-119">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="90e40-119">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e40-120">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90e40-120">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90e40-121">O número de caracteres na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="90e40-121">The number of characters in the string.</span></span> <span data-ttu-id="90e40-122">Se Count for-1, o parâmetro pString será considerado um ponteiro para um Sprite contendo uma cadeia de caracteres terminada em nulo e ID3DX10Font::D rawText calculará automaticamente a contagem de caracteres.</span><span class="sxs-lookup"><span data-stu-id="90e40-122">If Count is -1, then the pString parameter is assumed to be a pointer to a sprite containing a NULL-terminated string and ID3DX10Font::DrawText computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="90e40-123">*pRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90e40-123">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e40-124">Tipo: **lpRect**</span><span class="sxs-lookup"><span data-stu-id="90e40-124">Type: **LPRECT**</span></span>

<span data-ttu-id="90e40-125">Ponteiro para uma estrutura [Rect](/previous-versions//ms536136(v=vs.85)) que contém o retângulo, em coordenadas lógicas, em que o texto deve ser formatado.</span><span class="sxs-lookup"><span data-stu-id="90e40-125">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="90e40-126">Assim como ocorre com qualquer objeto RECT, o valor da coordenada do lado direito do retângulo deve ser maior do que o do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="90e40-126">As with any RECT object, the coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="90e40-127">Da mesma forma, o valor da coordenada da parte inferior deve ser maior que o da parte superior.</span><span class="sxs-lookup"><span data-stu-id="90e40-127">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="90e40-128">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90e40-128">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e40-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90e40-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90e40-130">Especifique o método de formatação do texto.</span><span class="sxs-lookup"><span data-stu-id="90e40-130">Specify the method of formatting the text.</span></span> <span data-ttu-id="90e40-131">Pode ser qualquer combinação dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="90e40-131">It can be any combination of the following values:</span></span>



| <span data-ttu-id="90e40-132">Item</span><span class="sxs-lookup"><span data-stu-id="90e40-132">Item</span></span>                                                                                      | <span data-ttu-id="90e40-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="90e40-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90e40-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>\_parte inferior de DT</span><span class="sxs-lookup"><span data-stu-id="90e40-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT\_BOTTOM</span></span><br/>             | <span data-ttu-id="90e40-135">Justifique o texto na parte inferior do retângulo.</span><span class="sxs-lookup"><span data-stu-id="90e40-135">Justify the text to the bottom of the rectangle.</span></span> <span data-ttu-id="90e40-136">Esse valor deve ser combinado com \_ uma única de DT.</span><span class="sxs-lookup"><span data-stu-id="90e40-136">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="90e40-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>\_CALCRECT DT</span><span class="sxs-lookup"><span data-stu-id="90e40-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT\_CALCRECT</span></span><br/>       | <span data-ttu-id="90e40-138">Diga ao DrawText para calcular automaticamente a largura e a altura do retângulo com base no comprimento da cadeia de caracteres que você o informa para desenhar.</span><span class="sxs-lookup"><span data-stu-id="90e40-138">Tell DrawText to automatically calculate the width and height of the rectangle based on the length of the string you tell it to draw.</span></span> <span data-ttu-id="90e40-139">Se houver várias linhas de texto, ID3DX10Font::D rawText usará a largura do retângulo apontado pelo parâmetro pRect e estenderá a base do retângulo para associar a última linha de texto.</span><span class="sxs-lookup"><span data-stu-id="90e40-139">If there are multiple lines of text, ID3DX10Font::DrawText uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="90e40-140">Se houver apenas uma linha de texto, ID3DX10Font::D rawText modificar o lado direito do retângulo para que ele limite o último caractere na linha.</span><span class="sxs-lookup"><span data-stu-id="90e40-140">If there is only one line of text, ID3DX10Font::DrawText modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="90e40-141">Em ambos os casos, ID3DX10Font::D rawText retorna a altura do texto formatado, mas não desenha o texto.</span><span class="sxs-lookup"><span data-stu-id="90e40-141">In either case, ID3DX10Font::DrawText returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span data-ttu-id="90e40-142"><span id="DT_CENTER"></span><span id="dt_center"></span>Centro de DT \_</span><span class="sxs-lookup"><span data-stu-id="90e40-142"><span id="DT_CENTER"></span><span id="dt_center"></span>DT\_CENTER</span></span><br/>             | <span data-ttu-id="90e40-143">Centralizar o texto horizontalmente no retângulo.</span><span class="sxs-lookup"><span data-stu-id="90e40-143">Center text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="90e40-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>\_EXPANDTABS DT</span><span class="sxs-lookup"><span data-stu-id="90e40-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT\_EXPANDTABS</span></span><br/> | <span data-ttu-id="90e40-145">Expanda os caracteres de tabulação.</span><span class="sxs-lookup"><span data-stu-id="90e40-145">Expand tab characters.</span></span> <span data-ttu-id="90e40-146">O número padrão de caracteres por guia é oito.</span><span class="sxs-lookup"><span data-stu-id="90e40-146">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="90e40-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT \_ restante</span><span class="sxs-lookup"><span data-stu-id="90e40-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT\_LEFT</span></span><br/>                   | <span data-ttu-id="90e40-148">Alinhar texto à esquerda.</span><span class="sxs-lookup"><span data-stu-id="90e40-148">Align text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="90e40-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>noclip de DT \_</span><span class="sxs-lookup"><span data-stu-id="90e40-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT\_NOCLIP</span></span><br/>             | <span data-ttu-id="90e40-150">Desenhe sem recorte.</span><span class="sxs-lookup"><span data-stu-id="90e40-150">Draw without clipping.</span></span> <span data-ttu-id="90e40-151">ID3DX10Font::D rawText é um pouco mais rápido quando o DT \_ noclip é usado.</span><span class="sxs-lookup"><span data-stu-id="90e40-151">ID3DX10Font::DrawText is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="90e40-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>DT \_ à direita</span><span class="sxs-lookup"><span data-stu-id="90e40-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>DT\_RIGHT</span></span><br/>                | <span data-ttu-id="90e40-153">Alinhar texto à direita.</span><span class="sxs-lookup"><span data-stu-id="90e40-153">Align text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="90e40-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>\_RTLREADING DT</span><span class="sxs-lookup"><span data-stu-id="90e40-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT\_RTLREADING</span></span><br/> | <span data-ttu-id="90e40-155">Exibir texto na ordem de leitura da direita para a esquerda para texto bidirecional quando uma fonte hebraico ou árabe for selecionada.</span><span class="sxs-lookup"><span data-stu-id="90e40-155">Display text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="90e40-156">A ordem de leitura padrão para todo o texto é da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="90e40-156">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="90e40-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>única de DT \_</span><span class="sxs-lookup"><span data-stu-id="90e40-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT\_SINGLELINE</span></span><br/> | <span data-ttu-id="90e40-158">Exibir texto somente em uma única linha.</span><span class="sxs-lookup"><span data-stu-id="90e40-158">Display text on a single line only.</span></span> <span data-ttu-id="90e40-159">Retornos de carro e feeds de linha não quebram a linha.</span><span class="sxs-lookup"><span data-stu-id="90e40-159">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="90e40-160"><span id="DT_TOP"></span><span id="dt_top"></span>início da DT \_</span><span class="sxs-lookup"><span data-stu-id="90e40-160"><span id="DT_TOP"></span><span id="dt_top"></span>DT\_TOP</span></span><br/>                      | <span data-ttu-id="90e40-161">Justifica o texto de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="90e40-161">Top-justify text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="90e40-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>\_VCENTER DT</span><span class="sxs-lookup"><span data-stu-id="90e40-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT\_VCENTER</span></span><br/>          | <span data-ttu-id="90e40-163">Centralizar texto verticalmente (somente linha única).</span><span class="sxs-lookup"><span data-stu-id="90e40-163">Center text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="90e40-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>\_justificação DT</span><span class="sxs-lookup"><span data-stu-id="90e40-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT\_WORDBREAK</span></span><br/>    | <span data-ttu-id="90e40-165">Quebrar palavras.</span><span class="sxs-lookup"><span data-stu-id="90e40-165">Break words.</span></span> <span data-ttu-id="90e40-166">As linhas são quebradas automaticamente entre as palavras se uma palavra ultrapassar a borda do retângulo especificado pelo parâmetro pRect.</span><span class="sxs-lookup"><span data-stu-id="90e40-166">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="90e40-167">Uma sequência de retorno de carro/alimentação de linha também quebra a linha.</span><span class="sxs-lookup"><span data-stu-id="90e40-167">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="90e40-168">*Cor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="90e40-168">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e40-169">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="90e40-169">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="90e40-170">Cor do texto.</span><span class="sxs-lookup"><span data-stu-id="90e40-170">Color of the text.</span></span> <span data-ttu-id="90e40-171">Consulte [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span><span class="sxs-lookup"><span data-stu-id="90e40-171">See [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90e40-172">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90e40-172">Return value</span></span>

<span data-ttu-id="90e40-173">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90e40-173">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90e40-174">Se a função for realizada com sucesso, o valor de retorno será a altura do texto em unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="90e40-174">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="90e40-175">Se \_ \_ a parte inferior de DT VCENTER ou DT for especificada, o valor de retorno será o deslocamento de pRect (superior à parte inferior) do texto desenhado.</span><span class="sxs-lookup"><span data-stu-id="90e40-175">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="90e40-176">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="90e40-176">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="90e40-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="90e40-177">Remarks</span></span>

<span data-ttu-id="90e40-178">Os parâmetros desse método são muito semelhantes aos da função DrawText do [GDI](/previous-versions//ms533909(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="90e40-178">The parameters of this method are very similar to those of the [GDI DrawText](/previous-versions//ms533909(v=vs.85)) function.</span></span>

<span data-ttu-id="90e40-179">Esse método dá suporte a cadeias de caracteres ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="90e40-179">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="90e40-180">A menos que o \_ formato noclip de DT seja usado, esse método corta o texto para que ele não apareça fora do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="90e40-180">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="90e40-181">É presumida que toda a formatação tenha várias linhas, a menos que o formato de linha \_ simples DT seja especificado.</span><span class="sxs-lookup"><span data-stu-id="90e40-181">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="90e40-182">Se a fonte selecionada for muito grande para o retângulo, esse método não tentará substituir uma fonte menor.</span><span class="sxs-lookup"><span data-stu-id="90e40-182">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="90e40-183">Esse método dá suporte apenas a fontes cuja escape e orientação são zero.</span><span class="sxs-lookup"><span data-stu-id="90e40-183">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="90e40-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90e40-184">Requirements</span></span>



| <span data-ttu-id="90e40-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="90e40-185">Requirement</span></span> | <span data-ttu-id="90e40-186">Valor</span><span class="sxs-lookup"><span data-stu-id="90e40-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90e40-187">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90e40-187">Header</span></span><br/>  | <dl> <span data-ttu-id="90e40-188"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="90e40-188"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="90e40-189">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90e40-189">Library</span></span><br/> | <dl> <span data-ttu-id="90e40-190"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90e40-190"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90e40-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="90e40-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e40-192">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="90e40-192">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="90e40-193">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="90e40-193">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
