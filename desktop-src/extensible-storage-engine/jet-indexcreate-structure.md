---
description: 'Saiba mais sobre: estrutura de JET_INDEXCREATE'
title: Estrutura JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE Structure
ms:assetid: 0c55f25c-d42a-49ba-a1fe-549850fdc9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269186(v=EXCHG.10)
ms:contentKeyID: 32765489
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4c465d81dce628497b1b9210fb08b37a3003e2e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662634"
---
# <a name="jet_indexcreate-structure"></a><span data-ttu-id="9e74e-103">Estrutura JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="9e74e-103">JET_INDEXCREATE Structure</span></span>


<span data-ttu-id="9e74e-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9e74e-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="9e74e-105">A estrutura de **JET_INDEXCREATE** contém as informações necessárias para criar um índice sobre os dados em um mecanismo de armazenamento extensível (ESE).</span><span class="sxs-lookup"><span data-stu-id="9e74e-105">The **JET_INDEXCREATE** structure contains the information needed to create an index over data in an Extensible Storage Engine (ESE) database.</span></span> <span data-ttu-id="9e74e-106">A estrutura é usada por funções como [JetCreateIndex2](./jetcreateindex2-function.md)e em estruturas como [JET_TABLECREATE](./jet-tablecreate-structure.md) e [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span><span class="sxs-lookup"><span data-stu-id="9e74e-106">The structure is used by functions such as [JetCreateIndex2](./jetcreateindex2-function.md), and in structures such as [JET_TABLECREATE](./jet-tablecreate-structure.md) and [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span></span>

``` c++
typedef struct tagJET_INDEXCREATE {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
  unsigned long cbKeyMost;
} JET_INDEXCREATE;
```

### <a name="members"></a><span data-ttu-id="9e74e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9e74e-107">Members</span></span>

<span data-ttu-id="9e74e-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="9e74e-108">**cbStruct**</span></span>

<span data-ttu-id="9e74e-109">O tamanho, em bytes, dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="9e74e-109">The size, in bytes, of this structure.</span></span> <span data-ttu-id="9e74e-110">Defina este membro como sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="9e74e-110">Set this member to sizeof( JET_INDEXCREATE ).</span></span>

<span data-ttu-id="9e74e-111">**szIndexName**</span><span class="sxs-lookup"><span data-stu-id="9e74e-111">**szIndexName**</span></span>

<span data-ttu-id="9e74e-112">O nome do índice a ser criado.</span><span class="sxs-lookup"><span data-stu-id="9e74e-112">The name of the index to create.</span></span>

<span data-ttu-id="9e74e-113">O nome do índice deve atender às seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="9e74e-113">The name of the index must meet the following conditions:</span></span>

  - <span data-ttu-id="9e74e-114">Ele deve ser menor que JET_cbNameMost, não incluindo o nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="9e74e-114">It must be less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="9e74e-115">Ele deve consistir nos seguintes caracteres: 0 (zero) a 9, A a Z, a a z e todas as outras pontuações, exceto para " \! "</span><span class="sxs-lookup"><span data-stu-id="9e74e-115">It must consist of the following characters: 0 (zero) through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="9e74e-116">(ponto de exclamação), "," (vírgula), " \[ " (colchete de abertura) e " \] " (colchete de fechamento) — ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c, 0x5d até 0x7F.</span><span class="sxs-lookup"><span data-stu-id="9e74e-116">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="9e74e-117">Ele não deve começar com um espaço.</span><span class="sxs-lookup"><span data-stu-id="9e74e-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="9e74e-118">Ele deve consistir em pelo menos um caractere que não seja de espaço.</span><span class="sxs-lookup"><span data-stu-id="9e74e-118">It must consist of at least one nonspace character.</span></span>

<span data-ttu-id="9e74e-119">**szKey**</span><span class="sxs-lookup"><span data-stu-id="9e74e-119">**szKey**</span></span>

<span data-ttu-id="9e74e-120">Um ponteiro para uma cadeia de caracteres com terminação de nulo duplo de tokens delimitados por nulo.</span><span class="sxs-lookup"><span data-stu-id="9e74e-120">A pointer to a double-null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="9e74e-121">Cada token tem o formato " \<direction-specifier\> \<column-name\> ", onde a especificação de direção é "+" ou "-".</span><span class="sxs-lookup"><span data-stu-id="9e74e-121">Each token is of the form "\<direction-specifier\>\<column-name\>", where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="9e74e-122">Por exemplo, um **szKey** de "+ ABC \\ 0-Def \\ 0 + GHI \\ 0" irá indexar as três colunas "ABC" (em ordem crescente), "def" (em ordem decrescente) e "GHI" (em ordem crescente).</span><span class="sxs-lookup"><span data-stu-id="9e74e-122">For example, a **szKey** of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span> <span data-ttu-id="9e74e-123">Na linguagem C, literais de cadeia de caracteres têm um terminador **NULL** implícito; Portanto, a cadeia de caracteres acima será encerrada por um duplo nulo.</span><span class="sxs-lookup"><span data-stu-id="9e74e-123">In the C language, string literals have an implied **NULL** terminator; therefore, the above string will be terminated by a double-NULL.</span></span>

<span data-ttu-id="9e74e-124">O número de colunas especificado em **szKey** não pode exceder o valor de **JET_ccolKeyMost** (uma constante dependente de versão).</span><span class="sxs-lookup"><span data-stu-id="9e74e-124">The number of columns specified in **szKey** may not exceed the value of **JET_ccolKeyMost** (a version-dependent constant).</span></span>

<span data-ttu-id="9e74e-125">Pelo menos uma coluna deve ser nomeada em **szKey**.</span><span class="sxs-lookup"><span data-stu-id="9e74e-125">At least one column must be named in **szKey**.</span></span>

<span data-ttu-id="9e74e-126">Comportamento obsoleto: após o terminador de nulo duplo, é possível especificar uma ID de idioma (uma palavra que é passada em MAKELCID (LangID, SORT_DEFAULT)) como uma maneira de especificar o LCID para o índice.</span><span class="sxs-lookup"><span data-stu-id="9e74e-126">Obsolete behavior: After the double-NULL terminator, it is possible to specify a language ID (a WORD which gets passed into MAKELCID( langid, SORT_DEFAULT ) ) as a way to specify the LCID for the index.</span></span> <span data-ttu-id="9e74e-127">É ilegal especificar uma ID de idioma em **szKey** e um LCID em [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (definindo JET_bitIndexUnicode em *grbit*).</span><span class="sxs-lookup"><span data-stu-id="9e74e-127">It is illegal to specify both a language ID in **szKey** and an LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (by setting JET_bitIndexUnicode in *grbit*).</span></span>

<span data-ttu-id="9e74e-128">Preterido: após a ID do idioma, é possível passar **cbVarSegMac** como um ushort.</span><span class="sxs-lookup"><span data-stu-id="9e74e-128">Deprecated: After the language ID, it is possible to pass **cbVarSegMac** as a USHORT.</span></span> <span data-ttu-id="9e74e-129">O comportamento será indefinido se USHORT estiver definido em **szKey** e se **cbVarSegMac** for definido na estrutura.</span><span class="sxs-lookup"><span data-stu-id="9e74e-129">The behavior is undefined if the USHORT is set both in **szKey** and if **cbVarSegMac** is set in the structure.</span></span>

<span data-ttu-id="9e74e-130">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="9e74e-130">**cbKey**</span></span>

<span data-ttu-id="9e74e-131">O comprimento, em bytes, de **szKey** , incluindo os dois nulos de terminação.</span><span class="sxs-lookup"><span data-stu-id="9e74e-131">The length, in bytes, of **szKey** including the two terminating nulls.</span></span>

<span data-ttu-id="9e74e-132">**grbit**</span><span class="sxs-lookup"><span data-stu-id="9e74e-132">**grbit**</span></span>

<span data-ttu-id="9e74e-133">Um grupo de bits que inclui zero ou mais valores listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9e74e-133">A group of bits that includes zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e74e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="9e74e-134">Value</span></span></p></th>
<th><p><span data-ttu-id="9e74e-135">Significado</span><span class="sxs-lookup"><span data-stu-id="9e74e-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e74e-136">JET_bitIndexUnique</span><span class="sxs-lookup"><span data-stu-id="9e74e-136">JET_bitIndexUnique</span></span></p></td>
<td><p><span data-ttu-id="9e74e-137">Não são permitidas entradas de índice duplicadas (chaves).</span><span class="sxs-lookup"><span data-stu-id="9e74e-137">Duplicate index entries (keys) are not allowed.</span></span> <span data-ttu-id="9e74e-138">Isso é imposto quando <a href="gg269288(v=exchg.10).md">JetUpdate</a> é chamado, não quando <a href="gg294137(v=exchg.10).md">JetSetColumn</a> é chamado.</span><span class="sxs-lookup"><span data-stu-id="9e74e-138">This is enforced when <a href="gg269288(v=exchg.10).md">JetUpdate</a> is called, not when <a href="gg294137(v=exchg.10).md">JetSetColumn</a> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e74e-139">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="9e74e-139">JET_bitIndexPrimary</span></span></p></td>
<td><p><span data-ttu-id="9e74e-140">O índice é um índice primário (clusterizado).</span><span class="sxs-lookup"><span data-stu-id="9e74e-140">The index is a primary (clustered) index.</span></span> <span data-ttu-id="9e74e-141">Cada tabela deve ter exatamente um índice primário.</span><span class="sxs-lookup"><span data-stu-id="9e74e-141">Every table must have exactly one primary index.</span></span> <span data-ttu-id="9e74e-142">Se nenhum índice primário for explicitamente definido em uma tabela, o mecanismo de banco de dados criará seu próprio índice primário.</span><span class="sxs-lookup"><span data-stu-id="9e74e-142">If no primary index is explicitly defined over a table, the database engine will create its own primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e74e-143">JET_bitIndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="9e74e-143">JET_bitIndexDisallowNull</span></span></p></td>
<td><p><span data-ttu-id="9e74e-144">Nenhuma das colunas sobre as quais o índice é criado pode conter um valor <strong>nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="9e74e-144">None of the columns over which the index is created can contain a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e74e-145">JET_bitIndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="9e74e-145">JET_bitIndexIgnoreNull</span></span></p></td>
<td><p><span data-ttu-id="9e74e-146">Não adicione uma entrada de índice para uma linha se todas as colunas que estão sendo indexadas forem <strong>nulas</strong>.</span><span class="sxs-lookup"><span data-stu-id="9e74e-146">Do not add an index entry for a row if all of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e74e-147">JET_bitIndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="9e74e-147">JET_bitIndexIgnoreAnyNull</span></span></p></td>
<td><p><span data-ttu-id="9e74e-148">Não adicione uma entrada de índice para uma linha se qualquer uma das colunas que estão sendo indexadas for <strong>nula</strong>.</span><span class="sxs-lookup"><span data-stu-id="9e74e-148">Do not add an index entry for a row if any of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e74e-149">JET_bitIndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="9e74e-149">JET_bitIndexIgnoreFirstNull</span></span></p></td>
<td><p><span data-ttu-id="9e74e-150">Não adicione uma entrada de índice para uma linha se a primeira coluna que está sendo indexada for <strong>nula</strong>.</span><span class="sxs-lookup"><span data-stu-id="9e74e-150">Do not add an index entry for a row if the first column being indexed is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e74e-151">JET_bitIndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="9e74e-151">JET_bitIndexLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="9e74e-152">As operações de índice serão registradas lentamente.</span><span class="sxs-lookup"><span data-stu-id="9e74e-152">Index operations will be logged lazily.</span></span></p>
<p><span data-ttu-id="9e74e-153">JET_bitIndexLazyFlush não afeta a ociosa das atualizações de dados.</span><span class="sxs-lookup"><span data-stu-id="9e74e-153">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="9e74e-154">Se a operação de indexação for interrompida pelo encerramento do processo, a recuperação simples ainda poderá obter o banco de dados para um estado consistente, mas o índice poderá não estar presente.</span><span class="sxs-lookup"><span data-stu-id="9e74e-154">If the indexing operation is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index might not be present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e74e-155">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="9e74e-155">JET_bitIndexEmpty</span></span></p></td>
<td><p><span data-ttu-id="9e74e-156">Não tente Compilar o índice, pois todas as entradas seriam avaliadas como <strong>nulas</strong>.</span><span class="sxs-lookup"><span data-stu-id="9e74e-156">Do not attempt to build the index, because all entries would evaluate to <strong>NULL</strong>.</span></span> <span data-ttu-id="9e74e-157"><strong>grbit</strong> também deve especificar JET_bitIgnoreAnyNull quando JET_bitIndexEmpty for passado.</span><span class="sxs-lookup"><span data-stu-id="9e74e-157"><strong>grbit</strong> must also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="9e74e-158">Esse é um aprimoramento de desempenho.</span><span class="sxs-lookup"><span data-stu-id="9e74e-158">This is a performance enhancement.</span></span> <span data-ttu-id="9e74e-159">Por exemplo, se uma nova coluna for adicionada a uma tabela, um índice será criado nessa coluna recém-adicionada e todos os registros na tabela serão verificados, mesmo que não sejam adicionados ao índice.</span><span class="sxs-lookup"><span data-stu-id="9e74e-159">For example, if a new column is added to a table, an index is created over this newly added column, and all the records in the table are scanned even though they are not added to the index.</span></span> <span data-ttu-id="9e74e-160">Especificar JET_bitIndexEmpty ignora a verificação da tabela, o que pode levar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="9e74e-160">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e74e-161">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="9e74e-161">JET_bitIndexUnversioned</span></span></p></td>
<td><p><span data-ttu-id="9e74e-162">Faz com que a criação do índice seja visível para outras transações.</span><span class="sxs-lookup"><span data-stu-id="9e74e-162">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="9e74e-163">Normalmente, uma sessão em uma transação não poderá ver uma operação de criação de índice em outra sessão.</span><span class="sxs-lookup"><span data-stu-id="9e74e-163">Typically a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="9e74e-164">Esse sinalizador pode ser útil se outra transação provavelmente criar o mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="9e74e-164">This flag can be useful if another transaction is likely to create the same index.</span></span> <span data-ttu-id="9e74e-165">O segundo índice-Create falhará em vez de causar muitas operações desnecessárias de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9e74e-165">The second index-create will fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="9e74e-166">A segunda transação pode não ser capaz de usar o índice imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9e74e-166">The second transaction might not be able to use the index immediately.</span></span> <span data-ttu-id="9e74e-167">A operação de criação de índice deve ser concluída antes de ser utilizável.</span><span class="sxs-lookup"><span data-stu-id="9e74e-167">The index creation operation has to complete before it is usable.</span></span> <span data-ttu-id="9e74e-168">A sessão não deve estar em uma transação no momento para criar um índice sem informações de versão.</span><span class="sxs-lookup"><span data-stu-id="9e74e-168">The session must not currently be in a transaction to create an index without version information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e74e-169">JET_bitIndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="9e74e-169">JET_bitIndexSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="9e74e-170">A especificação desse sinalizador faz com que valores <strong>nulos</strong> sejam classificados após os dados de todas as colunas no índice.</span><span class="sxs-lookup"><span data-stu-id="9e74e-170">Specifying this flag causes <strong>NULL</strong> values to be sorted after data for all columns in the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e74e-171">JET_bitIndexUnicode</span><span class="sxs-lookup"><span data-stu-id="9e74e-171">JET_bitIndexUnicode</span></span></p></td>
<td><p><span data-ttu-id="9e74e-172">A especificação desse sinalizador afeta a interpretação do campo de União LCID/pidxunicde na estrutura.</span><span class="sxs-lookup"><span data-stu-id="9e74e-172">Specifying this flag affects the interpretation of the lcid/pidxunicde union field in the structure.</span></span> <span data-ttu-id="9e74e-173">Definir o bit significa que o campo <strong>pidxunicode</strong> realmente aponta para uma estrutura de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> .</span><span class="sxs-lookup"><span data-stu-id="9e74e-173">Setting the bit means that the <strong>pidxunicode</strong> field actually points to a <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure.</span></span> <span data-ttu-id="9e74e-174">JET_bitIndexUnicode não é necessário para indexar dados Unicode.</span><span class="sxs-lookup"><span data-stu-id="9e74e-174">JET_bitIndexUnicode is not required in order to index Unicode data.</span></span> <span data-ttu-id="9e74e-175">Ele é usado apenas para personalizar a normalização de dados Unicode.</span><span class="sxs-lookup"><span data-stu-id="9e74e-175">It is only used to customize the normalization of Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e74e-176">JET_bitIndexTuples</span><span class="sxs-lookup"><span data-stu-id="9e74e-176">JET_bitIndexTuples</span></span></p></td>
<td><p><span data-ttu-id="9e74e-177">Especifica que o índice é um índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="9e74e-177">Specifies that the index is a tuple index.</span></span> <span data-ttu-id="9e74e-178">Consulte <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para obter uma descrição de um índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="9e74e-178">See <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> for a description of a tuple index.</span></span></p>
<p><span data-ttu-id="9e74e-179">JET_bitIndexTuples foi introduzido no sistema operacional Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9e74e-179">JET_bitIndexTuples was introduced in the Windows XP operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e74e-180">JET_bitIndexTupleLimits</span><span class="sxs-lookup"><span data-stu-id="9e74e-180">JET_bitIndexTupleLimits</span></span></p></td>
<td><p><span data-ttu-id="9e74e-181">A especificação desse sinalizador afeta a interpretação do campo de União <strong>cbVarSegMac/ptuplelimits</strong> na estrutura.</span><span class="sxs-lookup"><span data-stu-id="9e74e-181">Specifying this flag affects the interpretation of the <strong>cbVarSegMac/ptuplelimits</strong> union field in the structure.</span></span> <span data-ttu-id="9e74e-182">Definir esse bit significa que o campo <strong>ptuplelimits</strong> realmente aponta para uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para permitir limites de índice de tupla personalizados (implica JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="9e74e-182">Setting this bit means that the <strong>ptuplelimits</strong> field actually points to a <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure to allow custom tuple index limits (implies JET_bitIndexTuples).</span></span></p>
<p><span data-ttu-id="9e74e-183">JET_bitIndexTupleLimits foi introduzido no sistema operacional Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9e74e-183">JET_bitIndexTupleLimits was introduced in the Windows Server 2003 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e74e-184">JET_bitIndexCrossProduct 0x00004000</span><span class="sxs-lookup"><span data-stu-id="9e74e-184">JET_bitIndexCrossProduct 0x00004000</span></span></p></td>
<td><p><span data-ttu-id="9e74e-185">A especificação desse sinalizador para um índice que tenha mais de uma coluna de chave que seja uma coluna de vários valores resultará na criação de uma entrada de índice para cada resultado de um produto cruzado de todos os valores nessas colunas de chave.</span><span class="sxs-lookup"><span data-stu-id="9e74e-185">Specifying this flag for an index that has more than one key column that is a multivalued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="9e74e-186">Caso contrário, o índice terá apenas uma entrada para cada vários valores na coluna de chave mais significativa, que é uma coluna com vários valores, e cada uma dessas entradas de índice usará os primeiros valores de quaisquer outras colunas de chave que tenham colunas com vários valores.</span><span class="sxs-lookup"><span data-stu-id="9e74e-186">Otherwise, the index would only have one entry for each multivalue in the most significant key column that is a multivalued column and each of those index entries would use the first multivalue from any other key columns that are multivalued columns.</span></span></p>
<p><span data-ttu-id="9e74e-187">Por exemplo, se você tiver especificado esse sinalizador para um índice na coluna A que tem os valores &quot; vermelho &quot; e &quot; azul &quot; e acima da coluna B que tem os valores &quot; 1 &quot; e &quot; 2 &quot; , as seguintes entradas de índice serão criadas: &quot; vermelho &quot; , &quot; 1 &quot; ; &quot; vermelho &quot; , &quot; 2 &quot; ; &quot; azul &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9e74e-187">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="9e74e-188">Caso contrário, as seguintes entradas de índice seriam criadas: &quot; vermelho &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9e74e-188">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></p>
<p><span data-ttu-id="9e74e-189">JET_bitIndexCrossProduct foi introduzido no sistema operacional Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e74e-189">JET_bitIndexCrossProduct was introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e74e-190">JET_bitIndexKeyMost 0x00008000</span><span class="sxs-lookup"><span data-stu-id="9e74e-190">JET_bitIndexKeyMost 0x00008000</span></span></p></td>
<td><p><span data-ttu-id="9e74e-191">A especificação desse sinalizador fará com que o índice use o tamanho máximo de chave especificado no campo <strong>cbKeyMost</strong> na estrutura.</span><span class="sxs-lookup"><span data-stu-id="9e74e-191">Specifying this flag will cause the index to use the maximum key size specified in the <strong>cbKeyMost</strong> field in the structure.</span></span> <span data-ttu-id="9e74e-192">Caso contrário, o índice usará JET_cbKeyMost (255) como o tamanho máximo da chave.</span><span class="sxs-lookup"><span data-stu-id="9e74e-192">Otherwise, the index will use JET_cbKeyMost (255) as its maximum key size.</span></span></p>
<p><span data-ttu-id="9e74e-193">O JET_bitIndexKeyMost foi introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e74e-193">JET_bitIndexKeyMost was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e74e-194">JET_bitIndexDisallowTruncation 0x00010000</span><span class="sxs-lookup"><span data-stu-id="9e74e-194">JET_bitIndexDisallowTruncation 0x00010000</span></span></p></td>
<td><p><span data-ttu-id="9e74e-195">A especificação desse sinalizador fará com que qualquer atualização do índice que resulte em uma chave truncada falhe com JET_errKeyTruncated.</span><span class="sxs-lookup"><span data-stu-id="9e74e-195">Specifying this flag will cause any update to the index that would result in a truncated key to fail with JET_errKeyTruncated.</span></span> <span data-ttu-id="9e74e-196">Caso contrário, as chaves serão truncadas silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="9e74e-196">Otherwise, keys will be silently truncated.</span></span> <span data-ttu-id="9e74e-197">Para obter mais informações sobre o truncamento de chave, consulte a função <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</span><span class="sxs-lookup"><span data-stu-id="9e74e-197">For more information on key truncation, see the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p>
<p><span data-ttu-id="9e74e-198"><strong>Windows Vista: a JET_bitIndexDisallowTruncation</strong> é introduzida no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e74e-198"><strong>Windows Vista:  JET_bitIndexDisallowTruncation</strong> is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e74e-199">JET_bitIndexNestedTable 0x00020000</span><span class="sxs-lookup"><span data-stu-id="9e74e-199">JET_bitIndexNestedTable 0x00020000</span></span></p></td>
<td><p><span data-ttu-id="9e74e-200">A especificação desse sinalizador causará a atualização do índice em várias colunas com vários valores, mas somente com os valores do mesmo <strong>itagSequence</strong>.</span><span class="sxs-lookup"><span data-stu-id="9e74e-200">Specifying this flag will cause update the index over multiple multivalued columns but only with values of same <strong>itagSequence</strong>.</span></span></p>
<p><span data-ttu-id="9e74e-201">O JET_bitIndexNestedTable foi introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e74e-201">JET_bitIndexNestedTable was introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e74e-202">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="9e74e-202">**ulDensity**</span></span>

<span data-ttu-id="9e74e-203">A densidade percentual da árvore inicial do índice B +.</span><span class="sxs-lookup"><span data-stu-id="9e74e-203">The percentage density of the initial index B+ tree.</span></span> <span data-ttu-id="9e74e-204">A especificação de um número menor que 100 usa mais espaço para criar o índice inicialmente, mas permite que o crescimento futuro do índice esteja em vigor, evitando, assim, a fragmentação interna.</span><span class="sxs-lookup"><span data-stu-id="9e74e-204">Specifying a number less than 100 uses up more space to create the index initially, but allows future growth of the index to be in place, thus avoiding internal fragmentation.</span></span>

<span data-ttu-id="9e74e-205">**lcid**</span><span class="sxs-lookup"><span data-stu-id="9e74e-205">**lcid**</span></span>

<span data-ttu-id="9e74e-206">O LCID (identificador de localidade) a ser usado ao normalizar os dados quando o valor de JET_bitIndexUnicode não for especificado no parâmetro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="9e74e-206">The locale identifier (LCID) to use when normalizing the data when the JET_bitIndexUnicode value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="9e74e-207">O LCID afetará a normalização se o índice estiver sobre colunas Unicode.</span><span class="sxs-lookup"><span data-stu-id="9e74e-207">The LCID affects the normalization if the index is over Unicode columns.</span></span>

<span data-ttu-id="9e74e-208">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="9e74e-208">**pidxunicode**</span></span>

<span data-ttu-id="9e74e-209">Um ponteiro para uma estrutura de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) se o valor de JET_bitIndexUnicode for especificado no parâmetro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="9e74e-209">A pointer to a [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) structure if the JET_bitIndexUnicode value is specified in the *grbit* parameter.</span></span> <span data-ttu-id="9e74e-210">Isso permite que o usuário especifique sinalizadores personalizados que são passados para a função [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) durante a normalização Unicode.</span><span class="sxs-lookup"><span data-stu-id="9e74e-210">This allows the user to specify custom flags that get passed to the [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) function during Unicode normalization.</span></span>

<span data-ttu-id="9e74e-211">**cbVarSegMac**</span><span class="sxs-lookup"><span data-stu-id="9e74e-211">**cbVarSegMac**</span></span>

<span data-ttu-id="9e74e-212">O comprimento máximo, em bytes, de cada coluna a ser armazenada no índice quando o valor de JET_bitIndexTupleLimits não é especificado no parâmetro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="9e74e-212">The maximum length, in bytes, of each column to store in the index when the JET_bitIndexTupleLimits value is not specified in the *grbit* parameter.</span></span>

<span data-ttu-id="9e74e-213">A especificação de um valor de 0 (zero) para esse campo é equivalente a:</span><span class="sxs-lookup"><span data-stu-id="9e74e-213">Specifying a value of 0 (zero) for this field is equivalent to:</span></span>

  - <span data-ttu-id="9e74e-214">Especificando JET_cbPrimaryKeyMost para um índice primário.</span><span class="sxs-lookup"><span data-stu-id="9e74e-214">Specifying JET_cbPrimaryKeyMost for a primary index.</span></span>

  - <span data-ttu-id="9e74e-215">Especificando JET_cbSecondaryKeyMost para um índice secundário.</span><span class="sxs-lookup"><span data-stu-id="9e74e-215">Specifying JET_cbSecondaryKeyMost for a secondary index.</span></span>

<span data-ttu-id="9e74e-216">**ptuplelimits**</span><span class="sxs-lookup"><span data-stu-id="9e74e-216">**ptuplelimits**</span></span>

<span data-ttu-id="9e74e-217">Um ponteiro para uma estrutura de [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) se o valor de JET_bitIndexTupleLimits for especificado no parâmetro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="9e74e-217">A pointer to a [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure if the JET_bitIndexTupleLimits value is specified in the *grbit* parameter.</span></span>

<span data-ttu-id="9e74e-218">o ptuplelimits foi introduzido no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9e74e-218">ptuplelimits was introduced in Windows Server 2003.</span></span>

<span data-ttu-id="9e74e-219">**rgconditionalcolumn**</span><span class="sxs-lookup"><span data-stu-id="9e74e-219">**rgconditionalcolumn**</span></span>

<span data-ttu-id="9e74e-220">Um parâmetro opcional para uma matriz de estruturas [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , que são usadas para especificar as colunas condicionais no índice.</span><span class="sxs-lookup"><span data-stu-id="9e74e-220">An optional parameter to an array of [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) structures, which are used to specify the conditional columns in the index.</span></span>

<span data-ttu-id="9e74e-221">**cConditionalColumn**</span><span class="sxs-lookup"><span data-stu-id="9e74e-221">**cConditionalColumn**</span></span>

<span data-ttu-id="9e74e-222">A contagem de estruturas na matriz **rgconditionalcolumn** .</span><span class="sxs-lookup"><span data-stu-id="9e74e-222">The count of structures in the **rgconditionalcolumn** array.</span></span>

<span data-ttu-id="9e74e-223">**erra**</span><span class="sxs-lookup"><span data-stu-id="9e74e-223">**err**</span></span>

<span data-ttu-id="9e74e-224">Contém o código de retorno para a criação deste índice.</span><span class="sxs-lookup"><span data-stu-id="9e74e-224">Contains the return code for creating this index.</span></span>

<span data-ttu-id="9e74e-225">**cbKeyMost**</span><span class="sxs-lookup"><span data-stu-id="9e74e-225">**cbKeyMost**</span></span>

<span data-ttu-id="9e74e-226">Especifica o tamanho máximo permitido, em bytes, para chaves no índice.</span><span class="sxs-lookup"><span data-stu-id="9e74e-226">Specifies the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="9e74e-227">Esse parâmetro será ignorado se o valor de JET_bitIndexKeyMost não for especificado no parâmetro *grbit* .</span><span class="sxs-lookup"><span data-stu-id="9e74e-227">This parameter is ignored if the JET_bitIndexKeyMost value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="9e74e-228">Se esse parâmetro for definido como zero e JET_bitIndexKeyMost for especificado no parâmetro *grbit* , a função de chamada falhará com JET_err_InvalidDef.</span><span class="sxs-lookup"><span data-stu-id="9e74e-228">If this parameter is set to zero, and JET_bitIndexKeyMost is specified in the *grbit* parameter, the calling function will fail with JET_err_InvalidDef.</span></span>

<span data-ttu-id="9e74e-229">O tamanho mínimo de chave máximo suportado é JET_cbKeyMostMin (255), que é o tamanho de chave máximo herdado.</span><span class="sxs-lookup"><span data-stu-id="9e74e-229">The minimum supported maximum key size is JET_cbKeyMostMin (255), which is the legacy maximum key size.</span></span>

<span data-ttu-id="9e74e-230">O tamanho máximo da chave depende do tamanho da página do banco de dados (JET_paramDatabasePageSize), da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9e74e-230">The maximum key size is dependent on the database page size (JET_paramDatabasePageSize), as follows:</span></span>

  - <span data-ttu-id="9e74e-231">Se JET_paramDatabasePageSize = 2048, então JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)</span><span class="sxs-lookup"><span data-stu-id="9e74e-231">If JET_paramDatabasePageSize = 2048 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost2KBytePage (500)</span></span>

  - <span data-ttu-id="9e74e-232">Se JET_paramDatabasePageSize = 4096, então JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)</span><span class="sxs-lookup"><span data-stu-id="9e74e-232">If JET_paramDatabasePageSize = 4096 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost4KBytePage (1000)</span></span>

  - <span data-ttu-id="9e74e-233">Se JET_paramDatabasePageSize = 8192, então JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)</span><span class="sxs-lookup"><span data-stu-id="9e74e-233">If JET_paramDatabasePageSize = 8192 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost8KBytePage (2000)</span></span>

<span data-ttu-id="9e74e-234">O tamanho máximo de chave com suporte para a instância também pode ser lido a partir do parâmetro do sistema JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="9e74e-234">The maximum supported key size for the instance can also be read from the JET_paramKeyMost system parameter.</span></span>

<span data-ttu-id="9e74e-235">o **cbKeyMost** foi introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e74e-235">**cbKeyMost** was introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="9e74e-236">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e74e-236">Remarks</span></span>

<span data-ttu-id="9e74e-237">O ESE dá suporte à indexação em colunas de chave que contêm vários valores.</span><span class="sxs-lookup"><span data-stu-id="9e74e-237">ESE supports indexing over key columns containing multiple values.</span></span> <span data-ttu-id="9e74e-238">Para usar esse recurso, a coluna deve ser um tipo de coluna marcado (JET_bitColumnTagged) e deve ser sinalizada para ter vários valores indexados com JET_bitColumnMultiValued.</span><span class="sxs-lookup"><span data-stu-id="9e74e-238">To use this feature, the column must be a tagged column type (JET_bitColumnTagged), and it must be flagged to have its multiple values indexed with JET_bitColumnMultiValued.</span></span> <span data-ttu-id="9e74e-239">Em versões do Windows anteriores ao Windows Vista, somente a primeira coluna de chave com valores de várias valores no índice terá os respectivos valor expandido no índice.</span><span class="sxs-lookup"><span data-stu-id="9e74e-239">In versions of Windows earlier than Windows Vista, only the first multivalued key column in the index will have its values expanded in the index.</span></span> <span data-ttu-id="9e74e-240">Todas as outras colunas com e sem valores terão apenas seus primeiros valores expandidos no índice.</span><span class="sxs-lookup"><span data-stu-id="9e74e-240">All other multivalued and tagged columns will only have their first values expanded in the index.</span></span>

<span data-ttu-id="9e74e-241">Supondo que as linhas a seguir existam em uma tabela (a coluna Alpha não tem valores de multivalor, enquanto as colunas beta, gama e Delta têm valores de multivalor) e um índice é criado como "+ alfa \\ 0 + beta \\ 0 + gama \\ 0 + Delta \\ 0 \\ 0":</span><span class="sxs-lookup"><span data-stu-id="9e74e-241">Assuming the following rows exist in a table (column Alpha is not multivalued, while columns Beta, Gamma, and Delta are multivalued), and an index is created as "+Alpha\\0+Beta\\0+Gamma\\0+Delta\\0\\0":</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e74e-242">Alpha</span><span class="sxs-lookup"><span data-stu-id="9e74e-242">Alpha</span></span></p></th>
<th><p><span data-ttu-id="9e74e-243">Beta</span><span class="sxs-lookup"><span data-stu-id="9e74e-243">Beta</span></span></p></th>
<th><p><span data-ttu-id="9e74e-244">Gama</span><span class="sxs-lookup"><span data-stu-id="9e74e-244">Gamma</span></span></p></th>
<th><p><span data-ttu-id="9e74e-245">Delta</span><span class="sxs-lookup"><span data-stu-id="9e74e-245">Delta</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e74e-246">1</span><span class="sxs-lookup"><span data-stu-id="9e74e-246">1</span></span></p></td>
<td><p><span data-ttu-id="9e74e-247">ABC</span><span class="sxs-lookup"><span data-stu-id="9e74e-247">ABC</span></span><br />
<span data-ttu-id="9e74e-248">GHI</span><span class="sxs-lookup"><span data-stu-id="9e74e-248">GHI</span></span><br />
<span data-ttu-id="9e74e-249">JKL</span><span class="sxs-lookup"><span data-stu-id="9e74e-249">JKL</span></span></p></td>
<td><p><span data-ttu-id="9e74e-250">MNO</span><span class="sxs-lookup"><span data-stu-id="9e74e-250">MNO</span></span><br />
<span data-ttu-id="9e74e-251">PQR</span><span class="sxs-lookup"><span data-stu-id="9e74e-251">PQR</span></span><br />
<span data-ttu-id="9e74e-252">STU</span><span class="sxs-lookup"><span data-stu-id="9e74e-252">STU</span></span></p></td>
<td><p><span data-ttu-id="9e74e-253">VWX</span><span class="sxs-lookup"><span data-stu-id="9e74e-253">VWX</span></span><br />
<span data-ttu-id="9e74e-254">YZ</span><span class="sxs-lookup"><span data-stu-id="9e74e-254">YZ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e74e-255">2</span><span class="sxs-lookup"><span data-stu-id="9e74e-255">2</span></span></p></td>
<td><p><span data-ttu-id="9e74e-256">DOS</span><span class="sxs-lookup"><span data-stu-id="9e74e-256">THE</span></span></p></td>
<td><p><span data-ttu-id="9e74e-257">REDUNDANT</span><span class="sxs-lookup"><span data-stu-id="9e74e-257">RAIN</span></span><br />
<span data-ttu-id="9e74e-258">Espanha</span><span class="sxs-lookup"><span data-stu-id="9e74e-258">SPAIN</span></span></p></td>
<td><p><span data-ttu-id="9e74e-259">IN</span><span class="sxs-lookup"><span data-stu-id="9e74e-259">IN</span></span><br />
<span data-ttu-id="9e74e-260">QUADRA</span><span class="sxs-lookup"><span data-stu-id="9e74e-260">FALLS</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e74e-261">O índice de queda-tuplas serão armazenadas:</span><span class="sxs-lookup"><span data-stu-id="9e74e-261">The falling index-tuples will be stored:</span></span>

<span data-ttu-id="9e74e-262">{1, ABC, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="9e74e-262">{1,ABC,MNO,VWX}</span></span>  
<span data-ttu-id="9e74e-263">{1, GHI, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="9e74e-263">{1,GHI,MNO,VWX}</span></span>  
<span data-ttu-id="9e74e-264">{1, JKL, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="9e74e-264">{1,JKL,MNO,VWX}</span></span>  
<span data-ttu-id="9e74e-265">{2, A, CHUVA, IN}</span><span class="sxs-lookup"><span data-stu-id="9e74e-265">{2,THE,RAIN,IN}</span></span>

<span data-ttu-id="9e74e-266">Observe que {2, a, Espanha, IN} não é armazenada, mesmo que a coluna alfa na segunda linha tenha um único valores.</span><span class="sxs-lookup"><span data-stu-id="9e74e-266">Note that {2,THE,SPAIN,IN} is not stored, even though the Alpha column in the second row happens to have a single multivalue.</span></span>

<span data-ttu-id="9e74e-267">Em versões do Windows a partir do Windows Vista, todas as colunas com valores de multivalor podem ser expandidas no índice, especificando JET_bitIndexCrossProduct.</span><span class="sxs-lookup"><span data-stu-id="9e74e-267">In versions of Windows starting with Windows Vista, all multivalued columns can be expanded in the index by specifying JET_bitIndexCrossProduct.</span></span>

### <a name="requirements"></a><span data-ttu-id="9e74e-268">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e74e-268">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e74e-269"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9e74e-269"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9e74e-270">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9e74e-270">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e74e-271"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="9e74e-271"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9e74e-272">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9e74e-272">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e74e-273"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="9e74e-273"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9e74e-274">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9e74e-274">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e74e-275"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9e74e-275"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9e74e-276">Implementado como <strong>JET_ INDEXCREATE_W</strong> (Unicode) e <strong>JET_ INDEXCREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9e74e-276">Implemented as <strong>JET_ INDEXCREATE_W</strong> (Unicode) and <strong>JET_ INDEXCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9e74e-277">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e74e-277">See also</span></span>

[<span data-ttu-id="9e74e-278">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="9e74e-278">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="9e74e-279">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="9e74e-279">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="9e74e-280">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9e74e-280">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9e74e-281">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9e74e-281">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9e74e-282">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="9e74e-282">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="9e74e-283">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="9e74e-283">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="9e74e-284">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="9e74e-284">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="9e74e-285">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="9e74e-285">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="9e74e-286">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="9e74e-286">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="9e74e-287">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="9e74e-287">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="9e74e-288">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="9e74e-288">JetUpdate</span></span>](./jetupdate-function.md)
