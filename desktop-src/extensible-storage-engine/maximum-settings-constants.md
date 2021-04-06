---
description: 'Saiba mais sobre: as constantes de configurações máximas'
title: Constantes de configurações máximas
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827275"
---
# <a name="maximum-settings-constants"></a><span data-ttu-id="1d976-103">Constantes de configurações máximas</span><span class="sxs-lookup"><span data-stu-id="1d976-103">Maximum Settings Constants</span></span>


<span data-ttu-id="1d976-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1d976-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="maximum-settings-constants"></a><span data-ttu-id="1d976-105">Constantes de configurações máximas</span><span class="sxs-lookup"><span data-stu-id="1d976-105">Maximum Settings Constants</span></span>

<span data-ttu-id="1d976-106">Essas constantes fornecem as configurações máximas que são permitidas em itens em um banco de dados ESE.</span><span class="sxs-lookup"><span data-stu-id="1d976-106">These constants provide the maximum settings that are allowed on items in an ESE database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d976-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="1d976-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="1d976-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d976-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d976-109">JET_BASE_NAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="1d976-109">JET_BASE_NAME_LENGTH</span></span><br />
<span data-ttu-id="1d976-110">3</span><span class="sxs-lookup"><span data-stu-id="1d976-110">3</span></span></p></td>
<td><p><span data-ttu-id="1d976-111">Define o comprimento do prefixo usado para nomear arquivos que são usados pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1d976-111">Sets the length for the prefix used to name files that are used by the database engine.</span></span> <span data-ttu-id="1d976-112">Esse comprimento é aplicável ao nome definido para o parâmetro do sistema <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> .</span><span class="sxs-lookup"><span data-stu-id="1d976-112">This length is applicable to the name set for the <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> system parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d976-113">JET_MAX_COMPUTERNAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="1d976-113">JET_MAX_COMPUTERNAME_LENGTH</span></span><br />
<span data-ttu-id="1d976-114">15</span><span class="sxs-lookup"><span data-stu-id="1d976-114">15</span></span></p></td>
<td><p><span data-ttu-id="1d976-115">Define o comprimento máximo para <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</span><span class="sxs-lookup"><span data-stu-id="1d976-115">Sets the maximum length for <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d976-116">JET_cbBookmarkMost</span><span class="sxs-lookup"><span data-stu-id="1d976-116">JET_cbBookmarkMost</span></span><br />
<span data-ttu-id="1d976-117">256</span><span class="sxs-lookup"><span data-stu-id="1d976-117">256</span></span></p></td>
<td><p><span data-ttu-id="1d976-118">O tamanho máximo padrão de um indicador.</span><span class="sxs-lookup"><span data-stu-id="1d976-118">The default maximum size of a bookmark.</span></span> <span data-ttu-id="1d976-119">Isso é válido quando o tamanho da chave é deixado com seu valor padrão.</span><span class="sxs-lookup"><span data-stu-id="1d976-119">This is valid when the key size is left at its default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d976-120">JET_cbBookmarkMostMost</span><span class="sxs-lookup"><span data-stu-id="1d976-120">JET_cbBookmarkMostMost</span></span><br />
<span data-ttu-id="1d976-121">2000</span><span class="sxs-lookup"><span data-stu-id="1d976-121">2000</span></span></p></td>
<td><p><span data-ttu-id="1d976-122">O tamanho máximo de um indicador quando o ESENT é configurado para ter as maiores chaves possíveis.</span><span class="sxs-lookup"><span data-stu-id="1d976-122">The maximum size of a bookmark when esent is configured to have the largest keys possible.</span></span></p>
<p><span data-ttu-id="1d976-123"><strong>Windows 7:</strong> JET_cbBookmarkMostMost é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1d976-123"><strong>Windows 7:</strong> JET_cbBookmarkMostMost is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d976-124">JET_cbNameMost</span><span class="sxs-lookup"><span data-stu-id="1d976-124">JET_cbNameMost</span></span><br />
<span data-ttu-id="1d976-125">64</span><span class="sxs-lookup"><span data-stu-id="1d976-125">64</span></span></p></td>
<td><p><span data-ttu-id="1d976-126">O comprimento máximo de um objeto, coluna, índice ou nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1d976-126">The maximum length of a object, column, index, or property name.</span></span></p>
<p><span data-ttu-id="1d976-127"><strong>Observação</strong>  Se for Unicode, o valor será 128.</span><span class="sxs-lookup"><span data-stu-id="1d976-127"><strong>Note</strong>  If Unicode, the value is 128.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d976-128">JET_cbFullNameMost</span><span class="sxs-lookup"><span data-stu-id="1d976-128">JET_cbFullNameMost</span></span><br />
<span data-ttu-id="1d976-129">255</span><span class="sxs-lookup"><span data-stu-id="1d976-129">255</span></span></p></td>
<td><p><span data-ttu-id="1d976-130">O comprimento máximo de uma &quot; construção Name.Name.Name.. &quot; .</span><span class="sxs-lookup"><span data-stu-id="1d976-130">The maximum length of a &quot;name.name.name...&quot; construct.</span></span></p>
<p><span data-ttu-id="1d976-131"><strong>Observação</strong>  Se for Unicode, o valor será 510.</span><span class="sxs-lookup"><span data-stu-id="1d976-131"><strong>Note</strong>  If Unicode, the value is 510.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d976-132">JET_cbColumnLVPageOverhead</span><span class="sxs-lookup"><span data-stu-id="1d976-132">JET_cbColumnLVPageOverhead</span></span><br />
<span data-ttu-id="1d976-133">82</span><span class="sxs-lookup"><span data-stu-id="1d976-133">82</span></span></p></td>
<td><p><span data-ttu-id="1d976-134">Esse número pode ser usado para calcular a quantidade máxima de um BLOB que pode ser armazenado pelo mecanismo de banco de dados em uma única página de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1d976-134">This number can be used to compute the maximum amount of a BLOB that can be stored by the database engine on a single database page.</span></span> <span data-ttu-id="1d976-135">A fórmula tem tamanho máximo = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead.</span><span class="sxs-lookup"><span data-stu-id="1d976-135">The formula is max size = JET_paramDatabasePageSize–JET_cbColumnLVPageOverhead.</span></span></p>
<p><span data-ttu-id="1d976-136">Esse valor agora é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1d976-136">This value is now obsolete.</span></span> <span data-ttu-id="1d976-137">O tamanho da parte de valor longo deve ser recuperado com o parâmetro JET_paramLVChunkSizeMost.</span><span class="sxs-lookup"><span data-stu-id="1d976-137">The long-value chunk size should be retrieved with the JET_paramLVChunkSizeMost parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d976-138">JET_cbColumnMost</span><span class="sxs-lookup"><span data-stu-id="1d976-138">JET_cbColumnMost</span></span><br />
<span data-ttu-id="1d976-139">255</span><span class="sxs-lookup"><span data-stu-id="1d976-139">255</span></span></p></td>
<td><p><span data-ttu-id="1d976-140">O tamanho máximo de dados de coluna de valor não longo.</span><span class="sxs-lookup"><span data-stu-id="1d976-140">The maximum size of non-long-value column data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d976-141">JET_cbLVDefaultValueMost</span><span class="sxs-lookup"><span data-stu-id="1d976-141">JET_cbLVDefaultValueMost</span></span><br />
<span data-ttu-id="1d976-142">255</span><span class="sxs-lookup"><span data-stu-id="1d976-142">255</span></span></p></td>
<td><p><span data-ttu-id="1d976-143">O tamanho máximo de um valor padrão de coluna de valor longo (LongBinary ou LongText).</span><span class="sxs-lookup"><span data-stu-id="1d976-143">The maximum size of a long-value (LongBinary or LongText) column default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d976-144">JET_cbKeyMost</span><span class="sxs-lookup"><span data-stu-id="1d976-144">JET_cbKeyMost</span></span><br />
<span data-ttu-id="1d976-145">255</span><span class="sxs-lookup"><span data-stu-id="1d976-145">255</span></span></p></td>
<td><p><span data-ttu-id="1d976-146">O tamanho máximo padrão de uma chave de classificação ou de índice.</span><span class="sxs-lookup"><span data-stu-id="1d976-146">The default maximum size of a sort or index key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d976-147">JET_cbKeyMostMost</span><span class="sxs-lookup"><span data-stu-id="1d976-147">JET_cbKeyMostMost</span></span><br />
<span data-ttu-id="1d976-148">2000</span><span class="sxs-lookup"><span data-stu-id="1d976-148">2000</span></span></p></td>
<td><p><span data-ttu-id="1d976-149">O tamanho máximo configurável de uma chave de classificação ou de índice para qualquer tamanho de página.</span><span class="sxs-lookup"><span data-stu-id="1d976-149">The maximum configurable size of a sort or index key for any page size.</span></span> <span data-ttu-id="1d976-150">(Consulte JET_INDEXCREATE2. cbKeyMost)</span><span class="sxs-lookup"><span data-stu-id="1d976-150">(See JET_INDEXCREATE2.cbKeyMost)</span></span></p>
<p><span data-ttu-id="1d976-151"><strong>Windows 7:</strong> JET_cbKeyMostMost é introduzido no sistema operacional Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1d976-151"><strong>Windows 7:</strong> JET_cbKeyMostMost is introduced in the Windows 7 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d976-152">JET_cbKeyMost2KBytePage</span><span class="sxs-lookup"><span data-stu-id="1d976-152">JET_cbKeyMost2KBytePage</span></span><br />
<span data-ttu-id="1d976-153">500</span><span class="sxs-lookup"><span data-stu-id="1d976-153">500</span></span></p></td>
<td><p><span data-ttu-id="1d976-154">O tamanho máximo de configurável permitido para uma chave de índice em um banco de dados usando páginas de 2048 bytes.</span><span class="sxs-lookup"><span data-stu-id="1d976-154">The maximum allowable maximum configurable size for an index key in a database using 2048 byte pages.</span></span> <span data-ttu-id="1d976-155">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1d976-155">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="1d976-156"><strong>Windows Vista:</strong> O JET_cbKeyMost2KBytePage é introduzido no sistema operacional Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1d976-156"><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage is introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d976-157">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="1d976-157">JET_cbKeyMost4KBytePage</span></span><br />
<span data-ttu-id="1d976-158">1000</span><span class="sxs-lookup"><span data-stu-id="1d976-158">1000</span></span></p></td>
<td><p><span data-ttu-id="1d976-159">O tamanho máximo de configurável permitido para uma chave de índice em um banco de dados usando páginas de 4096 bytes.</span><span class="sxs-lookup"><span data-stu-id="1d976-159">The maximum allowable maximum configurable size for an index key in a database using 4096 byte pages.</span></span> <span data-ttu-id="1d976-160">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1d976-160">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="1d976-161"><strong>Windows Vista:</strong> O JET_cbKeyMost4KBytePage é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1d976-161"><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d976-162">JET_cbKeyMost8KBytePage</span><span class="sxs-lookup"><span data-stu-id="1d976-162">JET_cbKeyMost8KBytePage</span></span><br />
<span data-ttu-id="1d976-163">2000</span><span class="sxs-lookup"><span data-stu-id="1d976-163">2000</span></span></p></td>
<td><p><span data-ttu-id="1d976-164">O tamanho máximo de configurável permitido para uma chave de índice em um banco de dados usando páginas de 8192 bytes.</span><span class="sxs-lookup"><span data-stu-id="1d976-164">The maximum allowable maximum configurable size for an index key in a database using 8192 byte pages.</span></span> <span data-ttu-id="1d976-165">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1d976-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="1d976-166"><strong>Windows Vista:  </strong> JET_cbKeyMost8KBytePage é introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d976-166"><strong>Windows Vista:  </strong>JET_cbKeyMost8KBytePage is introduced in Windows Vista</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d976-167">JET_cbKeyMostMin</span><span class="sxs-lookup"><span data-stu-id="1d976-167">JET_cbKeyMostMin</span></span><br />
<span data-ttu-id="1d976-168">255</span><span class="sxs-lookup"><span data-stu-id="1d976-168">255</span></span></p></td>
<td><p><span data-ttu-id="1d976-169">O tamanho máximo permitido mínimo para uma chave de índice.</span><span class="sxs-lookup"><span data-stu-id="1d976-169">The minimum allowable maximum size for an index key.</span></span> <span data-ttu-id="1d976-170">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1d976-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="1d976-171"><strong>Windows Vista:  </strong> O JET_cbKeyMostMin é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1d976-171"><strong>Windows Vista:  </strong>JET_cbKeyMostMin is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d976-172">JET_cbLimitKeyMost</span><span class="sxs-lookup"><span data-stu-id="1d976-172">JET_cbLimitKeyMost</span></span><br />
<span data-ttu-id="1d976-173">256</span><span class="sxs-lookup"><span data-stu-id="1d976-173">256</span></span></p></td>
<td><p><span data-ttu-id="1d976-174">O tamanho máximo da chave quando a chave é formada usando um limite <em>grbit</em>, como JET_bitStrLimit, que é usado na função <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</span><span class="sxs-lookup"><span data-stu-id="1d976-174">The maximum key size when the key is formed by using a limit <em>grbit</em>, such as JET_bitStrLimit, which is used in the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d976-175">JET_cbPrimaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="1d976-175">JET_cbPrimaryKeyMost</span></span><br />
<span data-ttu-id="1d976-176">255</span><span class="sxs-lookup"><span data-stu-id="1d976-176">255</span></span></p></td>
<td><p><span data-ttu-id="1d976-177">O tamanho máximo do índice primário.</span><span class="sxs-lookup"><span data-stu-id="1d976-177">The maximum size of the primary index.</span></span> <span data-ttu-id="1d976-178">Isso agora é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1d976-178">This is now obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d976-179">JET_cbSecondaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="1d976-179">JET_cbSecondaryKeyMost</span></span><br />
<span data-ttu-id="1d976-180">255</span><span class="sxs-lookup"><span data-stu-id="1d976-180">255</span></span></p></td>
<td><p><span data-ttu-id="1d976-181">O tamanho máximo do índice secundário.</span><span class="sxs-lookup"><span data-stu-id="1d976-181">The maximum size of the secondary index.</span></span> <span data-ttu-id="1d976-182">Isso agora é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1d976-182">This is now obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d976-183">JET_ccolKeyMost</span><span class="sxs-lookup"><span data-stu-id="1d976-183">JET_ccolKeyMost</span></span><br />
<span data-ttu-id="1d976-184">12</span><span class="sxs-lookup"><span data-stu-id="1d976-184">12</span></span></p></td>
<td><p><span data-ttu-id="1d976-185">O número máximo de componentes em uma chave de classificação ou de índice.</span><span class="sxs-lookup"><span data-stu-id="1d976-185">The maximum number of components in a sort or index key.</span></span></p>
<p><span data-ttu-id="1d976-186"><strong>Windows Vista:  </strong> No Windows Vista e versões posteriores do Windows, o valor é 16.</span><span class="sxs-lookup"><span data-stu-id="1d976-186"><strong>Windows Vista:  </strong>In Windows Vista and later versions of Windows the value is 16.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d976-187">JET_ccolMost</span><span class="sxs-lookup"><span data-stu-id="1d976-187">JET_ccolMost</span></span><br />
<span data-ttu-id="1d976-188">0x0000fee0</span><span class="sxs-lookup"><span data-stu-id="1d976-188">0x0000fee0</span></span></p></td>
<td><p><span data-ttu-id="1d976-189">O número máximo de colunas permitidas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="1d976-189">The maximum number of columns allowed in a table.</span></span></p>
<p><span data-ttu-id="1d976-190"><strong>Windows XP:  </strong> O valor 0x0000fee0 é usado no Windows XP e versões posteriores e posteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="1d976-190"><strong>Windows XP:  </strong>The value 0x0000fee0 is used in Windows XP and later and later versions of Windows</span></span></p>
<p><span data-ttu-id="1d976-191"><strong>Windows 2000:  </strong> O valor 0x00007ffe é usado no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1d976-191"><strong>Windows 2000:  </strong>The value 0x00007ffe is used in Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d976-192">JET_ccolFixedMost</span><span class="sxs-lookup"><span data-stu-id="1d976-192">JET_ccolFixedMost</span></span><br />
<span data-ttu-id="1d976-193">interrupção</span><span class="sxs-lookup"><span data-stu-id="1d976-193">0x0000007f</span></span></p></td>
<td><p><span data-ttu-id="1d976-194">O número máximo de colunas fixas permitidas em uma tabela, atualmente 127.</span><span class="sxs-lookup"><span data-stu-id="1d976-194">The maximum number of fixed columns allowed in a table, currently 127.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d976-195">JET_ccolVarMost</span><span class="sxs-lookup"><span data-stu-id="1d976-195">JET_ccolVarMost</span></span><br />
<span data-ttu-id="1d976-196">0x00000080</span><span class="sxs-lookup"><span data-stu-id="1d976-196">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="1d976-197">O número máximo de colunas de comprimento variável que podem estar contidas em uma tabela, no momento, 128.</span><span class="sxs-lookup"><span data-stu-id="1d976-197">The maximum number of variable-length columns that can be contained in a table, currently 128.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d976-198">JET_ccolTaggedMost</span><span class="sxs-lookup"><span data-stu-id="1d976-198">JET_ccolTaggedMost</span></span><br />
<span data-ttu-id="1d976-199">(JET_ccolMost-0x000000FF)</span><span class="sxs-lookup"><span data-stu-id="1d976-199">( JET_ccolMost - 0x000000ff )</span></span></p></td>
<td><p><span data-ttu-id="1d976-200">O número máximo de colunas marcadas que podem estar contidas em uma tabela, no momento, 64993.</span><span class="sxs-lookup"><span data-stu-id="1d976-200">The maximum number of tagged columns that can be contained in a table, currently 64993.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="1d976-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d976-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d976-202"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="1d976-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1d976-203">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1d976-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d976-204"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="1d976-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1d976-205">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1d976-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d976-206"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="1d976-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1d976-207">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1d976-207">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

