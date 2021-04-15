---
title: Estrutura FONTDIRENTRY
description: Contém informações sobre uma fonte individual em um grupo de recursos de fonte. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Menus de estrutura FONTDIRENTRY e outros recursos
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1cee72a490fd2b94b1c810797f656d81418c0f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454831"
---
# <a name="fontdirentry-structure"></a><span data-ttu-id="e70de-105">Estrutura FONTDIRENTRY</span><span class="sxs-lookup"><span data-stu-id="e70de-105">FONTDIRENTRY structure</span></span>

<span data-ttu-id="e70de-106">Contém informações sobre uma fonte individual em um grupo de recursos de fonte.</span><span class="sxs-lookup"><span data-stu-id="e70de-106">Contains information about an individual font in a font resource group.</span></span> <span data-ttu-id="e70de-107">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="e70de-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70de-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e70de-108">Syntax</span></span>


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a><span data-ttu-id="e70de-109">Membros</span><span class="sxs-lookup"><span data-stu-id="e70de-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="e70de-110">**dfVersion**</span><span class="sxs-lookup"><span data-stu-id="e70de-110">**dfVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-112">Um número de versão definido pelo usuário para os dados de recurso que as ferramentas podem usar para ler e gravar arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="e70de-112">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-113">**dfSize**</span><span class="sxs-lookup"><span data-stu-id="e70de-113">**dfSize**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e70de-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-115">O tamanho do arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="e70de-115">The size of the file, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-116">**dfCopyright \[ 60\]**</span><span class="sxs-lookup"><span data-stu-id="e70de-116">**dfCopyright\[60\]**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-117">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="e70de-117">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-118">As informações de direitos autorais do fornecedor de fontes.</span><span class="sxs-lookup"><span data-stu-id="e70de-118">The font supplier's copyright information.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-119">**dfType**</span><span class="sxs-lookup"><span data-stu-id="e70de-119">**dfType**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-120">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-120">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-121">O tipo de arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="e70de-121">The type of font file.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-122">**dfPoints**</span><span class="sxs-lookup"><span data-stu-id="e70de-122">**dfPoints**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-123">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-123">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-124">O tamanho do ponto em que esse conjunto de caracteres tem a melhor aparência.</span><span class="sxs-lookup"><span data-stu-id="e70de-124">The point size at which this character set looks best.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-125">**dfVertRes**</span><span class="sxs-lookup"><span data-stu-id="e70de-125">**dfVertRes**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-126">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-127">A resolução vertical, em pontos por polegada, na qual esse conjunto de caracteres foi digitalizado.</span><span class="sxs-lookup"><span data-stu-id="e70de-127">The vertical resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-128">**dfHorizRes**</span><span class="sxs-lookup"><span data-stu-id="e70de-128">**dfHorizRes**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-129">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-129">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-130">A resolução horizontal, em pontos por polegada, na qual esse conjunto de caracteres foi digitalizado.</span><span class="sxs-lookup"><span data-stu-id="e70de-130">The horizontal resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-131">**dfAscent**</span><span class="sxs-lookup"><span data-stu-id="e70de-131">**dfAscent**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-132">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-132">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-133">A distância da parte superior de uma célula de definição de caractere para a linha de base da fonte tipográfica.</span><span class="sxs-lookup"><span data-stu-id="e70de-133">The distance from the top of a character definition cell to the baseline of the typographical font.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-134">**dfInternalLeading**</span><span class="sxs-lookup"><span data-stu-id="e70de-134">**dfInternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-135">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-135">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-136">A quantidade de entrelinha dentro dos limites definidos pelo membro **dfPixHeight** .</span><span class="sxs-lookup"><span data-stu-id="e70de-136">The amount of leading inside the bounds set by the **dfPixHeight** member.</span></span> <span data-ttu-id="e70de-137">As marcas de acentuação e outros caracteres diacríticos podem ocorrer nessa área.</span><span class="sxs-lookup"><span data-stu-id="e70de-137">Accent marks and other diacritical characters can occur in this area.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-138">**dfExternalLeading**</span><span class="sxs-lookup"><span data-stu-id="e70de-138">**dfExternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-139">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-140">A quantidade de entrelinha extra que o aplicativo adiciona entre linhas.</span><span class="sxs-lookup"><span data-stu-id="e70de-140">The amount of extra leading that the application adds between rows.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-141">**dfItalic**</span><span class="sxs-lookup"><span data-stu-id="e70de-141">**dfItalic**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-142">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="e70de-142">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-143">Uma fonte em itálico se não for igual a zero.</span><span class="sxs-lookup"><span data-stu-id="e70de-143">An italic font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-144">**dfUnderline**</span><span class="sxs-lookup"><span data-stu-id="e70de-144">**dfUnderline**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-145">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="e70de-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-146">Uma fonte sublinhada se não for igual a zero.</span><span class="sxs-lookup"><span data-stu-id="e70de-146">An underlined font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-147">**dfStrikeOut**</span><span class="sxs-lookup"><span data-stu-id="e70de-147">**dfStrikeOut**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-148">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="e70de-148">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-149">Uma fonte riscada se não for igual a zero.</span><span class="sxs-lookup"><span data-stu-id="e70de-149">A strikeout font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-150">**dfWeight**</span><span class="sxs-lookup"><span data-stu-id="e70de-150">**dfWeight**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-151">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-151">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-152">O peso da fonte no intervalo de 0 a 1000.</span><span class="sxs-lookup"><span data-stu-id="e70de-152">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="e70de-153">Por exemplo, 400 é romano e 700 é negrito.</span><span class="sxs-lookup"><span data-stu-id="e70de-153">For example, 400 is roman and 700 is bold.</span></span> <span data-ttu-id="e70de-154">Se esse valor for zero, será usado um peso padrão.</span><span class="sxs-lookup"><span data-stu-id="e70de-154">If this value is zero, a default weight is used.</span></span> <span data-ttu-id="e70de-155">Para obter valores adicionais definidos, consulte a descrição da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="e70de-155">For additional defined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-156">**dfCharSet**</span><span class="sxs-lookup"><span data-stu-id="e70de-156">**dfCharSet**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-157">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="e70de-157">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-158">O conjunto de caracteres da fonte.</span><span class="sxs-lookup"><span data-stu-id="e70de-158">The character set of the font.</span></span> <span data-ttu-id="e70de-159">Para valores predefinidos, consulte a descrição da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="e70de-159">For predefined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-160">**dfPixWidth**</span><span class="sxs-lookup"><span data-stu-id="e70de-160">**dfPixWidth**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-161">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-161">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-162">A largura da grade na qual uma fonte de vetor foi digitalizada.</span><span class="sxs-lookup"><span data-stu-id="e70de-162">The width of the grid on which a vector font was digitized.</span></span> <span data-ttu-id="e70de-163">Para fontes de varredura, se o membro não for igual a zero, ele representará a largura de todos os caracteres no bitmap.</span><span class="sxs-lookup"><span data-stu-id="e70de-163">For raster fonts, if the member is not equal to zero, it represents the width for all the characters in the bitmap.</span></span> <span data-ttu-id="e70de-164">Se o membro for igual a zero, a fonte terá caracteres de largura variável.</span><span class="sxs-lookup"><span data-stu-id="e70de-164">If the member is equal to zero, the font has variable-width characters.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-165">**dfPixHeight**</span><span class="sxs-lookup"><span data-stu-id="e70de-165">**dfPixHeight**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-166">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-166">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-167">A altura do bitmap de caractere para fontes de rasterização ou a altura da grade na qual uma fonte de vetor foi digitalizada.</span><span class="sxs-lookup"><span data-stu-id="e70de-167">The height of the character bitmap for raster fonts or the height of the grid on which a vector font was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-168">**dfPitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="e70de-168">**dfPitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-169">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="e70de-169">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-170">A inclinação e a família da fonte.</span><span class="sxs-lookup"><span data-stu-id="e70de-170">The pitch and the family of the font.</span></span> <span data-ttu-id="e70de-171">Para obter informações adicionais, consulte a descrição da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="e70de-171">For additional information, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-172">**dfAvgWidth**</span><span class="sxs-lookup"><span data-stu-id="e70de-172">**dfAvgWidth**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-173">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-173">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-174">A largura média de caracteres na fonte (geralmente definida como a largura da letra x).</span><span class="sxs-lookup"><span data-stu-id="e70de-174">The average width of characters in the font (generally defined as the width of the letter x).</span></span> <span data-ttu-id="e70de-175">Esse valor não inclui a folga necessária para caracteres em negrito ou itálico.</span><span class="sxs-lookup"><span data-stu-id="e70de-175">This value does not include the overhang required for bold or italic characters.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-176">**dfMaxWidth**</span><span class="sxs-lookup"><span data-stu-id="e70de-176">**dfMaxWidth**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-177">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-177">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-178">A largura do caractere mais largo na fonte.</span><span class="sxs-lookup"><span data-stu-id="e70de-178">The width of the widest character in the font.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-179">**dfFirstChar**</span><span class="sxs-lookup"><span data-stu-id="e70de-179">**dfFirstChar**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-180">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="e70de-180">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-181">O primeiro código de caractere definido na fonte.</span><span class="sxs-lookup"><span data-stu-id="e70de-181">The first character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-182">**dfLastChar**</span><span class="sxs-lookup"><span data-stu-id="e70de-182">**dfLastChar**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-183">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="e70de-183">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-184">O último código de caractere definido na fonte.</span><span class="sxs-lookup"><span data-stu-id="e70de-184">The last character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-185">**dfDefaultChar**</span><span class="sxs-lookup"><span data-stu-id="e70de-185">**dfDefaultChar**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-186">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="e70de-186">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-187">O caractere para substituir os caracteres que não estão na fonte.</span><span class="sxs-lookup"><span data-stu-id="e70de-187">The character to substitute for characters not in the font.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-188">**dfBreakChar**</span><span class="sxs-lookup"><span data-stu-id="e70de-188">**dfBreakChar**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-189">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="e70de-189">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-190">O caractere que será usado para definir quebras de palavras para justificação de texto.</span><span class="sxs-lookup"><span data-stu-id="e70de-190">The character that will be used to define word breaks for text justification.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-191">**dfWidthBytes**</span><span class="sxs-lookup"><span data-stu-id="e70de-191">**dfWidthBytes**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-192">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e70de-192">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-193">O número de bytes em cada linha do bitmap.</span><span class="sxs-lookup"><span data-stu-id="e70de-193">The number of bytes in each row of the bitmap.</span></span> <span data-ttu-id="e70de-194">Esse valor é sempre mesmo para que as linhas iniciem em limites de palavras.</span><span class="sxs-lookup"><span data-stu-id="e70de-194">This value is always even so that the rows start on word boundaries.</span></span> <span data-ttu-id="e70de-195">Para fontes de vetor, esse membro não tem significado.</span><span class="sxs-lookup"><span data-stu-id="e70de-195">For vector fonts, this member has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-196">**dfDevice**</span><span class="sxs-lookup"><span data-stu-id="e70de-196">**dfDevice**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-197">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e70de-197">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-198">O deslocamento no arquivo para uma cadeia de caracteres terminada em nulo que especifica um nome de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e70de-198">The offset in the file to a null-terminated string that specifies a device name.</span></span> <span data-ttu-id="e70de-199">Para uma fonte genérica, esse valor é zero.</span><span class="sxs-lookup"><span data-stu-id="e70de-199">For a generic font, this value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-200">**dfFace**</span><span class="sxs-lookup"><span data-stu-id="e70de-200">**dfFace**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-201">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e70de-201">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-202">O deslocamento no arquivo para uma cadeia de caracteres terminada em nulo que nomeia a face de tipos.</span><span class="sxs-lookup"><span data-stu-id="e70de-202">The offset in the file to a null-terminated string that names the typeface.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-203">**dfReserved**</span><span class="sxs-lookup"><span data-stu-id="e70de-203">**dfReserved**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-204">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e70de-204">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-205">Este membro está reservado.</span><span class="sxs-lookup"><span data-stu-id="e70de-205">This member is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-206">**szDeviceName**</span><span class="sxs-lookup"><span data-stu-id="e70de-206">**szDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-207">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="e70de-207">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-208">O nome do dispositivo se esse arquivo de fonte for designado para um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="e70de-208">The name of the device if this font file is designated for a specific device.</span></span>

</dd> <dt>

<span data-ttu-id="e70de-209">**szFaceName**</span><span class="sxs-lookup"><span data-stu-id="e70de-209">**szFaceName**</span></span>
</dt> <dd>

<span data-ttu-id="e70de-210">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="e70de-210">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="e70de-211">O nome da face de tipos da fonte.</span><span class="sxs-lookup"><span data-stu-id="e70de-211">The typeface name of the font.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e70de-212">Comentários</span><span class="sxs-lookup"><span data-stu-id="e70de-212">Remarks</span></span>

<span data-ttu-id="e70de-213">Há uma estrutura **FONTDIRENTRY** para cada fonte no arquivo. res.</span><span class="sxs-lookup"><span data-stu-id="e70de-213">There is one **FONTDIRENTRY** structure for every font in the .res file.</span></span> <span data-ttu-id="e70de-214">Os aplicativos que geram arquivos. res com recursos de fonte também devem adicionar ao arquivo uma estrutura **FONTDIRENTRY** para cada fonte.</span><span class="sxs-lookup"><span data-stu-id="e70de-214">Applications that generate .res files with font resources must also add to the file a **FONTDIRENTRY** structure for each font.</span></span>

<span data-ttu-id="e70de-215">As declarações de fonte podem ser misturadas com outras declarações de recurso no. O arquivo RC porque as fontes não precisam ser contíguas no arquivo. res.</span><span class="sxs-lookup"><span data-stu-id="e70de-215">Font declarations can be mixed with other resource declarations in the .RC file because fonts do not need to be contiguous in the .res file.</span></span>

## <a name="requirements"></a><span data-ttu-id="e70de-216">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e70de-216">Requirements</span></span>



| <span data-ttu-id="e70de-217">Requisito</span><span class="sxs-lookup"><span data-stu-id="e70de-217">Requirement</span></span> | <span data-ttu-id="e70de-218">Valor</span><span class="sxs-lookup"><span data-stu-id="e70de-218">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e70de-219">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e70de-219">Minimum supported client</span></span><br/> | <span data-ttu-id="e70de-220">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e70de-220">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e70de-221">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e70de-221">Minimum supported server</span></span><br/> | <span data-ttu-id="e70de-222">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e70de-222">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e70de-223">Confira também</span><span class="sxs-lookup"><span data-stu-id="e70de-223">See also</span></span>

<dl> <dt>

<span data-ttu-id="e70de-224">**Referência**</span><span class="sxs-lookup"><span data-stu-id="e70de-224">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e70de-225">**Dialugado**</span><span class="sxs-lookup"><span data-stu-id="e70de-225">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="e70de-226">**FONTGROUPHDR**</span><span class="sxs-lookup"><span data-stu-id="e70de-226">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="e70de-227">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="e70de-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e70de-228">Recursos</span><span class="sxs-lookup"><span data-stu-id="e70de-228">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="e70de-229">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="e70de-229">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e70de-230">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="e70de-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

