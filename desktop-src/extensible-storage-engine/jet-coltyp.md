---
description: 'Saiba mais sobre: JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836912"
---
# <a name="jet_coltyp"></a><span data-ttu-id="54544-103">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="54544-103">JET_COLTYP</span></span>


<span data-ttu-id="54544-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="54544-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_coltyp"></a><span data-ttu-id="54544-105">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="54544-105">JET_COLTYP</span></span>

<span data-ttu-id="54544-106">O **JET_COLTYP** grupo de constantes descreve todos os tipos de coluna possíveis que podem ser encontrados em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="54544-106">The **JET_COLTYP** group of constants describe all possible column types that can be found in a table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54544-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="54544-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="54544-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="54544-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54544-109">JET_coltypNil</span><span class="sxs-lookup"><span data-stu-id="54544-109">JET_coltypNil</span></span><br />
<span data-ttu-id="54544-110">0</span><span class="sxs-lookup"><span data-stu-id="54544-110">0</span></span></p></td>
<td><p><span data-ttu-id="54544-111">Um tipo de coluna inválido.</span><span class="sxs-lookup"><span data-stu-id="54544-111">An invalid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54544-112">JET_coltypBit</span><span class="sxs-lookup"><span data-stu-id="54544-112">JET_coltypBit</span></span><br />
<span data-ttu-id="54544-113">1</span><span class="sxs-lookup"><span data-stu-id="54544-113">1</span></span></p></td>
<td><p><span data-ttu-id="54544-114">Um tipo de coluna que permite três valores: <strong>true</strong>, <strong>false</strong>ou <strong>NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="54544-114">A column type that allows three values: <strong>True</strong>, <strong>False</strong>, or <strong>NULL</strong>.</span></span> <span data-ttu-id="54544-115">Esse tipo de coluna tem um byte de comprimento e é um tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="54544-115">This type of column is one byte in length and is a fixed size.</span></span> <span data-ttu-id="54544-116"><strong>Falso</strong> classifica antes de <strong>verdadeiro</strong>.</span><span class="sxs-lookup"><span data-stu-id="54544-116"><strong>False</strong> sorts before <strong>True</strong>.</span></span> <span data-ttu-id="54544-117">Observe que o tamanho desse tipo não corresponde ao tamanho do tipo booliano Variant.</span><span class="sxs-lookup"><span data-stu-id="54544-117">Note that the size of this type does not match the size of the variant Boolean type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54544-118">JET_coltypUnsignedByte</span><span class="sxs-lookup"><span data-stu-id="54544-118">JET_coltypUnsignedByte</span></span><br />
<span data-ttu-id="54544-119">2</span><span class="sxs-lookup"><span data-stu-id="54544-119">2</span></span></p></td>
<td><p><span data-ttu-id="54544-120">Um inteiro não assinado de 1 byte que pode assumir valores entre 0 (zero) e 255.</span><span class="sxs-lookup"><span data-stu-id="54544-120">A 1-byte unsigned integer that can take on values between 0 (zero) and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54544-121">JET_coltypShort</span><span class="sxs-lookup"><span data-stu-id="54544-121">JET_coltypShort</span></span><br />
<span data-ttu-id="54544-122">3</span><span class="sxs-lookup"><span data-stu-id="54544-122">3</span></span></p></td>
<td><p><span data-ttu-id="54544-123">Um inteiro com sinal de 2 bytes que pode assumir os valores entre-32768 e 32767.</span><span class="sxs-lookup"><span data-stu-id="54544-123">A 2-byte signed integer that can take on values between -32768 and 32767.</span></span> <span data-ttu-id="54544-124">Valores negativos são classificados antes de valores positivos.</span><span class="sxs-lookup"><span data-stu-id="54544-124">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54544-125">JET_coltypLong</span><span class="sxs-lookup"><span data-stu-id="54544-125">JET_coltypLong</span></span><br />
<span data-ttu-id="54544-126">4</span><span class="sxs-lookup"><span data-stu-id="54544-126">4</span></span></p></td>
<td><p><span data-ttu-id="54544-127">Um inteiro com sinal de 4 bytes que pode assumir os valores entre-2147483648 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="54544-127">A 4-byte signed integer that can take on values between - 2147483648 and 2147483647.</span></span> <span data-ttu-id="54544-128">Valores negativos são classificados antes de valores positivos.</span><span class="sxs-lookup"><span data-stu-id="54544-128">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54544-129">JET_coltypCurrency</span><span class="sxs-lookup"><span data-stu-id="54544-129">JET_coltypCurrency</span></span><br />
<span data-ttu-id="54544-130">5</span><span class="sxs-lookup"><span data-stu-id="54544-130">5</span></span></p></td>
<td><p><span data-ttu-id="54544-131">Um inteiro com sinal de 8 bytes que pode assumir os valores entre-9.223.372.036.854.775.808 e 9223372036854775807.</span><span class="sxs-lookup"><span data-stu-id="54544-131">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="54544-132">Valores negativos são classificados antes de valores positivos.</span><span class="sxs-lookup"><span data-stu-id="54544-132">Negative values sort before positive values.</span></span> <span data-ttu-id="54544-133">Esse tipo de coluna é idêntico ao tipo de moeda variante.</span><span class="sxs-lookup"><span data-stu-id="54544-133">This column type is identical to the variant currency type.</span></span> <span data-ttu-id="54544-134">Esse tipo de coluna também pode ser usado como um inteiro com sinal de 8 bytes nativo.</span><span class="sxs-lookup"><span data-stu-id="54544-134">This column type can also be used as a native 8-byte signed integer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54544-135">JET_coltypIEEESingle</span><span class="sxs-lookup"><span data-stu-id="54544-135">JET_coltypIEEESingle</span></span><br />
<span data-ttu-id="54544-136">6</span><span class="sxs-lookup"><span data-stu-id="54544-136">6</span></span></p></td>
<td><p><span data-ttu-id="54544-137">Um número de ponto flutuante de precisão única (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="54544-137">A single-precision (4-byte) floating point number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54544-138">JET_coltypIEEEDouble</span><span class="sxs-lookup"><span data-stu-id="54544-138">JET_coltypIEEEDouble</span></span><br />
<span data-ttu-id="54544-139">7</span><span class="sxs-lookup"><span data-stu-id="54544-139">7</span></span></p></td>
<td><p><span data-ttu-id="54544-140">Um número de ponto flutuante de precisão dupla (8 bytes).</span><span class="sxs-lookup"><span data-stu-id="54544-140">A double-precision (8-byte) floating point number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54544-141">JET_coltypDateTime</span><span class="sxs-lookup"><span data-stu-id="54544-141">JET_coltypDateTime</span></span><br />
<span data-ttu-id="54544-142">8</span><span class="sxs-lookup"><span data-stu-id="54544-142">8</span></span></p></td>
<td><p><span data-ttu-id="54544-143">Um número de ponto flutuante de precisão dupla (8 bytes) que representa uma data em dias fracionários desde o ano 1900.</span><span class="sxs-lookup"><span data-stu-id="54544-143">A double-precision (8-byte) floating point number that represents a date in fractional days since the year 1900.</span></span> <span data-ttu-id="54544-144">Esse tipo de coluna é idêntico ao tipo de data de variante.</span><span class="sxs-lookup"><span data-stu-id="54544-144">This column type is identical to the variant date type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54544-145">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="54544-145">JET_coltypBinary</span></span><br />
<span data-ttu-id="54544-146">9</span><span class="sxs-lookup"><span data-stu-id="54544-146">9</span></span></p></td>
<td><p><span data-ttu-id="54544-147">Uma coluna binária bruta de comprimento fixo ou variável que pode ter até 255 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="54544-147">A fixed or variable length, raw binary column that can be up to 255 bytes in length.</span></span></p>
<p><span data-ttu-id="54544-148">Esse tipo de coluna pode ser usado para implementar um GUID, se configurado como um comprimento fixo, coluna binária de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="54544-148">This column type can be used to implement a GUID if configured as a fixed length, 16-byte binary column.</span></span> <span data-ttu-id="54544-149">A única limitação é que a ordenação relativa de valores em um índice em uma coluna desse tipo não corresponderá à ordenação relativa da renderização de cadeia de caracteres de registro padrão de um GUID (ou seja, &quot; {0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b} &quot; ).</span><span class="sxs-lookup"><span data-stu-id="54544-149">The only caveat is that the relative ordering of values in an index over such a column will not match the relative ordering of the standard registry-string rendering of a GUID (that is &quot;{ 0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b}&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54544-150">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="54544-150">JET_coltypText</span></span><br />
<span data-ttu-id="54544-151">10</span><span class="sxs-lookup"><span data-stu-id="54544-151">10</span></span></p></td>
<td><p><span data-ttu-id="54544-152">Uma coluna de texto de comprimento fixo ou variável que pode ter até 255 caracteres ASCII de comprimento ou 127 caracteres Unicode de comprimento.</span><span class="sxs-lookup"><span data-stu-id="54544-152">A fixed or variable length text column that can be up to 255 ASCII characters in length or 127 Unicode characters in length.</span></span></p>
<p><span data-ttu-id="54544-153">Todas as cadeias são armazenadas como um número contado de caracteres.</span><span class="sxs-lookup"><span data-stu-id="54544-153">All strings are stored as a counted number of characters.</span></span> <span data-ttu-id="54544-154">As cadeias de caracteres não precisam ser terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="54544-154">The strings need not be null terminated.</span></span> <span data-ttu-id="54544-155">Além disso, não é necessário que a contagem inclua um terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="54544-155">Further, it is not necessary for the count to include a null terminator.</span></span> <span data-ttu-id="54544-156">Por fim, caracteres nulos inseridos podem ser armazenados.</span><span class="sxs-lookup"><span data-stu-id="54544-156">Finally, embedded null characters can be stored.</span></span></p>
<p><span data-ttu-id="54544-157">Cadeias de caracteres ASCII são sempre tratadas como não diferencia maiúsculas de minúsculas para fins de classificação e pesquisa.</span><span class="sxs-lookup"><span data-stu-id="54544-157">ASCII strings are always treated as case insensitive for sorting and searching purposes.</span></span> <span data-ttu-id="54544-158">Além disso, somente os caracteres que antecedem o primeiro caractere nulo (se houver) são considerados para classificação e pesquisa.</span><span class="sxs-lookup"><span data-stu-id="54544-158">Further, only the characters preceding the first null character (if any) are considered for sorting and searching.</span></span></p>
<p><span data-ttu-id="54544-159">As cadeias de caracteres Unicode usam a API do Win32 <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> para criar chaves de classificação que são usadas posteriormente para classificar e Pesquisar esses dados.</span><span class="sxs-lookup"><span data-stu-id="54544-159">Unicode strings use the Win32 API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> to create sort keys that are subsequently used for sorting and searching that data.</span></span> <span data-ttu-id="54544-160">Por padrão, as cadeias de caracteres Unicode são consideradas no idioma inglês dos EUA e são classificadas e pesquisadas usando os seguintes sinalizadores de normalização: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="54544-160">By default, Unicode strings are considered to be in the U.S. English locale and are sorted and searched using the following normalization flags: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="54544-161">No Windows 2000, é possível personalizar esses sinalizadores por índice para incluir também NORM_IGNORENONSPACE.</span><span class="sxs-lookup"><span data-stu-id="54544-161">In Windows 2000, it is possible to customize these flags per index to also include NORM_IGNORENONSPACE.</span></span> <span data-ttu-id="54544-162">No Windows XP e versões posteriores, é possível solicitar qualquer combinação dos seguintes sinalizadores de normalização por índice: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH e SORT_STRINGSORT.</span><span class="sxs-lookup"><span data-stu-id="54544-162">In Windows XP and later releases, it is possible to request any combination of the following normalization flags per index: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH, and SORT_STRINGSORT.</span></span></p>
<p><span data-ttu-id="54544-163">Em todas as versões, é possível personalizar a localidade por índice.</span><span class="sxs-lookup"><span data-stu-id="54544-163">In all releases, it is possible to customize the locale per index.</span></span> <span data-ttu-id="54544-164">Qualquer localidade pode ser usada, desde que o pacote de idiomas apropriado tenha sido instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="54544-164">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="54544-165">Por fim, todos os caracteres nulos encontrados em uma cadeia de caracteres Unicode são completamente ignorados.</span><span class="sxs-lookup"><span data-stu-id="54544-165">Finally, any null characters encountered in a Unicode string are completely ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54544-166">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="54544-166">JET_coltypLongBinary</span></span><br />
<span data-ttu-id="54544-167">11</span><span class="sxs-lookup"><span data-stu-id="54544-167">11</span></span></p></td>
<td><p><span data-ttu-id="54544-168">Uma coluna binária bruta de comprimento fixo ou variável que pode ter até 2147483647 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="54544-168">A fixed or variable length, raw binary column that can be up to 2147483647 bytes in length.</span></span> <span data-ttu-id="54544-169">Esse tipo é considerado um valor longo.</span><span class="sxs-lookup"><span data-stu-id="54544-169">This type is considered to be a Long Value.</span></span> <span data-ttu-id="54544-170">Um valor longo é especial porque pode ser grande e pode ser acessado como um fluxo.</span><span class="sxs-lookup"><span data-stu-id="54544-170">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="54544-171">De outra forma, esse tipo é idêntico ao JET_coltypBinary.</span><span class="sxs-lookup"><span data-stu-id="54544-171">This type is otherwise identical to JET_coltypBinary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54544-172">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="54544-172">JET_coltypLongText</span></span><br />
<span data-ttu-id="54544-173">12</span><span class="sxs-lookup"><span data-stu-id="54544-173">12</span></span></p></td>
<td><p><span data-ttu-id="54544-174">Uma coluna de texto fixa ou de comprimento variável que pode ter até 2147483647 caracteres ASCII de comprimento ou 1073741823 caracteres Unicode de comprimento.</span><span class="sxs-lookup"><span data-stu-id="54544-174">A fixed or variable length, text column that can be up to 2147483647 ASCII characters in length or 1073741823 Unicode characters in length.</span></span> <span data-ttu-id="54544-175">Esse tipo é considerado um valor longo.</span><span class="sxs-lookup"><span data-stu-id="54544-175">This type is considered to be a Long Value.</span></span> <span data-ttu-id="54544-176">Um valor longo é especial porque pode ser grande e pode ser acessado como um fluxo.</span><span class="sxs-lookup"><span data-stu-id="54544-176">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="54544-177">De outra forma, esse tipo é idêntico ao JET_coltypText.</span><span class="sxs-lookup"><span data-stu-id="54544-177">This type is otherwise identical to JET_coltypText.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54544-178">JET_coltypSLV</span><span class="sxs-lookup"><span data-stu-id="54544-178">JET_coltypSLV</span></span><br />
<span data-ttu-id="54544-179">13</span><span class="sxs-lookup"><span data-stu-id="54544-179">13</span></span></p></td>
<td><p><span data-ttu-id="54544-180">Este tipo de coluna é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="54544-180">This column type is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54544-181">JET_coltypUnsignedLong</span><span class="sxs-lookup"><span data-stu-id="54544-181">JET_coltypUnsignedLong</span></span><br />
<span data-ttu-id="54544-182">14</span><span class="sxs-lookup"><span data-stu-id="54544-182">14</span></span></p></td>
<td><p><span data-ttu-id="54544-183">Um inteiro sem sinal de 4 bytes que pode assumir valores entre 0 (zero) e 4294967295.</span><span class="sxs-lookup"><span data-stu-id="54544-183">A 4-byte unsigned integer that can take on values between 0 (zero) and 4294967295.</span></span></p>
<p><span data-ttu-id="54544-184"><strong>Windows Vista e Windows Server 2008:</strong>  Esse tipo de coluna tem suporte no Windows Vista, no Windows Server 2008 e em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="54544-184"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54544-185">JET_coltypLongLong</span><span class="sxs-lookup"><span data-stu-id="54544-185">JET_coltypLongLong</span></span><br />
<span data-ttu-id="54544-186">15</span><span class="sxs-lookup"><span data-stu-id="54544-186">15</span></span></p></td>
<td><p><span data-ttu-id="54544-187">Um inteiro com sinal de 8 bytes que pode assumir os valores entre-9.223.372.036.854.775.808 e 9223372036854775807.</span><span class="sxs-lookup"><span data-stu-id="54544-187">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="54544-188">Valores negativos são classificados antes de valores positivos.</span><span class="sxs-lookup"><span data-stu-id="54544-188">Negative values sort before positive values.</span></span></p>
<p><span data-ttu-id="54544-189"><strong>Windows Vista e Windows Server 2008:</strong>  Esse tipo de coluna tem suporte no Windows Vista, no Windows Server 2008 e em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="54544-189"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54544-190">JET_coltypGUID</span><span class="sxs-lookup"><span data-stu-id="54544-190">JET_coltypGUID</span></span><br />
<span data-ttu-id="54544-191">16</span><span class="sxs-lookup"><span data-stu-id="54544-191">16</span></span></p></td>
<td><p><span data-ttu-id="54544-192">Uma coluna binária de comprimento fixo de 16 bytes que representa nativamente o tipo de dados GUID.</span><span class="sxs-lookup"><span data-stu-id="54544-192">A fixed length 16 byte binary column that natively represents the GUID data type.</span></span> <span data-ttu-id="54544-193">Os valores de coluna de GUID são classificados da mesma maneira que esses valores seriam classificados como cadeias de caracteres na forma padrão (ou seja, {4999b5c0-7657-42d9-bdc1-4b779784e013}).</span><span class="sxs-lookup"><span data-stu-id="54544-193">GUID column values sort in the same way that those values would sort as strings when in standard form (i.e. {4999b5c0-7657-42d9-bdc1-4b779784e013}).</span></span></p>
<p><span data-ttu-id="54544-194"><strong>Windows Vista e Windows Server 2008:</strong>  Esse tipo de coluna tem suporte no Windows Vista, no Windows Server 2008 e em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="54544-194"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54544-195">JET_coltypUnsignedShort</span><span class="sxs-lookup"><span data-stu-id="54544-195">JET_coltypUnsignedShort</span></span><br />
<span data-ttu-id="54544-196">17</span><span class="sxs-lookup"><span data-stu-id="54544-196">17</span></span></p></td>
<td><p><span data-ttu-id="54544-197">Um inteiro sem sinal de 2 bytes que pode assumir valores entre 0 e 65535.</span><span class="sxs-lookup"><span data-stu-id="54544-197">A 2-byte unsigned integer that can take on values between 0 and 65535.</span></span></p>
<p><span data-ttu-id="54544-198"><strong>Windows Vista e Windows Server 2008:</strong>  Esse tipo de coluna tem suporte no Windows Vista, no Windows Server 2008 e em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="54544-198"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54544-199">JET_coltypMax</span><span class="sxs-lookup"><span data-stu-id="54544-199">JET_coltypMax</span></span><br />
<span data-ttu-id="54544-200">18</span><span class="sxs-lookup"><span data-stu-id="54544-200">18</span></span></p></td>
<td><p><span data-ttu-id="54544-201">Uma constante que descreve o máximo (ou seja, um que não é o maior número de colunas válido) com suporte no mecanismo.</span><span class="sxs-lookup"><span data-stu-id="54544-201">A constant describing the maximum (that is, one beyond the largest valid) column type supported by the engine.</span></span></p>
<p><span data-ttu-id="54544-202">Esse valor deve ser usado com cuidado porque ele será alterado à medida que novos tipos de coluna forem suportados.</span><span class="sxs-lookup"><span data-stu-id="54544-202">This value should be used with care because it will change as new column types are supported.</span></span> <span data-ttu-id="54544-203">Por exemplo, ele tem um valor literal diferente no Windows 2000 do que no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="54544-203">For example, it has a different literal value on Windows 2000 than it does on Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="54544-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54544-204">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54544-205"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="54544-205"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="54544-206">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="54544-206">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54544-207"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="54544-207"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="54544-208">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="54544-208">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54544-209"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="54544-209"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="54544-210">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="54544-210">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="54544-211">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="54544-211">See Also</span></span>

[<span data-ttu-id="54544-212">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="54544-212">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="54544-213">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="54544-213">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)
