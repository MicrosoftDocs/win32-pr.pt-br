---
description: 'Saiba mais sobre: função JetOpenTempTable2'
title: Função JetOpenTempTable2
TOCTitle: JetOpenTempTable2 Function
ms:assetid: 788ec4f9-b0c3-409b-850c-7567dec47024
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269302(v=EXCHG.10)
ms:contentKeyID: 32765594
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 324bcde75c0ba9376c8ad9f5e98df585b1d341e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810707"
---
# <a name="jetopentemptable2-function"></a><span data-ttu-id="781df-103">Função JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="781df-103">JetOpenTempTable2 Function</span></span>


<span data-ttu-id="781df-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="781df-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable2-function"></a><span data-ttu-id="781df-105">Função JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="781df-105">JetOpenTempTable2 Function</span></span>

<span data-ttu-id="781df-106">A função **JetOpenTempTable2** cria uma tabela temporária com um único índice que pode ser usado para armazenar e recuperar registros, assim como uma tabela comum criada usando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="781df-106">The **JetOpenTempTable2** function creates a temporary table with a single index that can be used to store and retrieve records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="781df-107">Essa função também tem uma ID de localidade que pode ser usada para comparar dados de coluna de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="781df-107">This function also has a Locale ID that can be used to compare Unicode key column data in the temporary table.</span></span> <span data-ttu-id="781df-108">No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil.</span><span class="sxs-lookup"><span data-stu-id="781df-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="781df-109">Eles também podem ser usados para classificar e executar com muita rapidez a remoção de duplicidades em conjuntos de registros quando acessados de forma puramente sequencial.</span><span class="sxs-lookup"><span data-stu-id="781df-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable2(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          unsigned long lcid,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="781df-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="781df-110">Parameters</span></span>

<span data-ttu-id="781df-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="781df-111">*sesid*</span></span>

<span data-ttu-id="781df-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="781df-112">The session to use.</span></span>

<span data-ttu-id="781df-113">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="781df-113">*prgcolumndef*</span></span>

<span data-ttu-id="781df-114">As definições de coluna das colunas a serem criadas na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="781df-114">The column definitions of the columns to be created in the temporary table.</span></span>

<span data-ttu-id="781df-115">Existem limitações importantes para as opções de definição de coluna usadas com uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="781df-115">Important limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="781df-116">Consulte a seção Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="781df-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="781df-117">Além das opções de definição de coluna usual, zero ou mais das opções a seguir também podem ser especificadas, que são relevantes apenas no contexto de uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="781df-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="781df-118">Valor</span><span class="sxs-lookup"><span data-stu-id="781df-118">Value</span></span></p></th>
<th><p><span data-ttu-id="781df-119">Significado</span><span class="sxs-lookup"><span data-stu-id="781df-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="781df-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="781df-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="781df-121">A ordem de classificação da coluna de chave para a tabela temporária deve ser decrescente em vez de crescente.</span><span class="sxs-lookup"><span data-stu-id="781df-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="781df-122">Se essa opção for especificada sem JET_bitColumnTTKey, essa opção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="781df-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="781df-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="781df-124">A coluna será uma coluna de chave para a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="781df-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="781df-125">A ordem das definições de coluna com essa opção especificada na matriz de entrada determinará a precedência de cada coluna de chave para a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="781df-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="781df-126">A primeira definição de coluna na matriz com esse conjunto de opções será a coluna de chave mais significativa e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="781df-126">The first column definition in the array with this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="781df-127">Se mais colunas de chave forem solicitadas do que o mecanismo de banco de dados pode ter suporte, essa opção será ignorada para as colunas de chave sem suporte.</span><span class="sxs-lookup"><span data-stu-id="781df-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="781df-128">*ccolumn*</span><span class="sxs-lookup"><span data-stu-id="781df-128">*ccolumn*</span></span>

<span data-ttu-id="781df-129">Consulte *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="781df-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="781df-130">*lcid*</span><span class="sxs-lookup"><span data-stu-id="781df-130">*lcid*</span></span>

<span data-ttu-id="781df-131">A ID de localidade a ser usada para comparar qualquer dado de coluna de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="781df-131">The locale ID to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="781df-132">Qualquer localidade pode ser usada, desde que o pacote de idiomas apropriado tenha sido instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="781df-132">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="781df-133">A única exceção é que a localidade neutra do idioma (LCID de zero) é inválida.</span><span class="sxs-lookup"><span data-stu-id="781df-133">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="781df-134">No Windows Server 2003 e posterior, se a localidade neutra de idioma for especificada para esse parâmetro, a ID de localidade padrão (inglês dos EUA) será usada em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="781df-134">On Windows Server 2003 and later, if the Language Neutral locale is specified for this parameter then the default locale ID (U.S. English) will be used instead.</span></span> <span data-ttu-id="781df-135">Isso é para permitir que um valor de zero detenha o padrão, em vez de um valor ilegal.</span><span class="sxs-lookup"><span data-stu-id="781df-135">This is to allow a value of zero to signify the default rather than an illegal value.</span></span>

<span data-ttu-id="781df-136">Quando esse parâmetro não estiver presente e quando o parâmetro *pidxunicode* não estiver presente, o LCID padrão será usado para comparar quaisquer dados de coluna de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="781df-136">When this parameter is not present and when the *pidxunicode* parameter is not present, then the default LCID will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="781df-137">O LCID padrão é a localidade inglês dos EUA.</span><span class="sxs-lookup"><span data-stu-id="781df-137">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="781df-138">*grbit*</span><span class="sxs-lookup"><span data-stu-id="781df-138">*grbit*</span></span>

<span data-ttu-id="781df-139">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="781df-139">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="781df-140">Valor</span><span class="sxs-lookup"><span data-stu-id="781df-140">Value</span></span></p></th>
<th><p><span data-ttu-id="781df-141">Significado</span><span class="sxs-lookup"><span data-stu-id="781df-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="781df-142">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="781df-142">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="781df-143">Essa opção solicita que qualquer tentativa de inserir um registro com a mesma chave de índice que um registro inserido anteriormente falhará imediatamente com JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="781df-143">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="781df-144">Se essa opção não for solicitada, uma duplicata poderá ser detectada imediatamente e falhará ou poderá ser removida silenciosamente mais tarde, dependendo da estratégia escolhida pelo mecanismo de banco de dados para implementar a tabela temporária com base na funcionalidade solicitada.</span><span class="sxs-lookup"><span data-stu-id="781df-144">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span></p>
<p><span data-ttu-id="781df-145">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="781df-145">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="781df-146">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="781df-146">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-147">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="781df-147">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="781df-148">Essa opção força o Gerenciador de tabelas temporária a abandonar qualquer tentativa de escolher uma estratégia inteligente para gerenciar a tabela temporária que resultará em desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="781df-148">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-149">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="781df-149">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="781df-150">Essa opção solicita que a tabela temporária só seja criada se o Gerenciador de tabelas temporárias puder usar a implementação otimizada para resultados de consulta intermediários.</span><span class="sxs-lookup"><span data-stu-id="781df-150">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="781df-151">Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="781df-151">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="781df-152">Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="781df-152">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="781df-153">Consulte JET_bitTTUnique para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="781df-153">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="781df-154">Essa opção só está disponível no Windows Server 2003 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="781df-154">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-155">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="781df-155">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="781df-156">Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir o uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para pesquisar registros por chave de índice.</span><span class="sxs-lookup"><span data-stu-id="781df-156">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="781df-157">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="781df-157">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="781df-158">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="781df-158">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-159">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="781df-159">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="781df-160">Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir que os registros sejam verificados em ordem e direção arbitrárias usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="781df-160">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="781df-161">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="781df-161">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="781df-162">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="781df-162">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-163">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="781df-163">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="781df-164">Essa opção solicita que os valores da coluna de chave nula se aproximem do final do índice que os valores de coluna de chave não nulos.</span><span class="sxs-lookup"><span data-stu-id="781df-164">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-165">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="781df-165">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="781df-166">Essa opção solicita que os registros com chaves de índice duplicados sejam removidos do conjunto final de registros na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="781df-166">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="781df-167">Antes do Windows Server 2003, o mecanismo de banco de dados sempre assumiu que essa opção está em vigor devido ao fato de que todos os índices clusterizados também devem ser uma chave primária e, portanto, devem ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="781df-167">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="781df-168">A partir do Windows Server 2003, agora é possível criar uma tabela temporária que não remove duplicatas quando a opção de JET_bitTTForwardOnly também é especificada.</span><span class="sxs-lookup"><span data-stu-id="781df-168">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="781df-169">Não é possível saber qual duplicata será vencedora e quais duplicatas serão descartadas em geral.</span><span class="sxs-lookup"><span data-stu-id="781df-169">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="781df-170">No entanto, quando a opção JET_bitTTErrorOnDuplicateInsertion for solicitada, o primeiro registro com uma determinada chave de índice a ser inserida na tabela temporária sempre vencerá.</span><span class="sxs-lookup"><span data-stu-id="781df-170">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-171">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="781df-171">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="781df-172">Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir que os registros que foram inseridos anteriormente sejam alterados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="781df-172">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="781df-173">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="781df-173">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="781df-174">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="781df-174">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-175">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="781df-175">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="781df-176">Solicitações para permitir somente valores longos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="781df-176">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="781df-177"><strong>Windows 7</strong>: o <strong>JET_bitTTIntrinsicLVsOnly</strong> é introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="781df-177"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="781df-178">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="781df-178">*ptableid*</span></span>

<span data-ttu-id="781df-179">O buffer de saída que receberá o novo cursor aberto na tabela temporária recém-criada.</span><span class="sxs-lookup"><span data-stu-id="781df-179">The output buffer that will receive the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="781df-180">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="781df-180">*prgcolumnid*</span></span>

<span data-ttu-id="781df-181">O buffer de saída que receberá a matriz de IDs de coluna geradas durante a criação da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="781df-181">The output buffer that will receive the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="781df-182">As IDs de coluna nessa matriz correspondem exatamente à matriz de entrada de definições de coluna.</span><span class="sxs-lookup"><span data-stu-id="781df-182">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="781df-183">Como resultado, o tamanho desse buffer deve corresponder ao tamanho da matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="781df-183">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="781df-184">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="781df-184">Return Value</span></span>

<span data-ttu-id="781df-185">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="781df-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="781df-186">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="781df-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="781df-187">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="781df-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="781df-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="781df-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="781df-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="781df-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="781df-190">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="781df-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-191">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="781df-191">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="781df-192"><strong>JetOpenTempTable2</strong> falhou porque JET_bitTTForwardOnly foi especificado e a tabela temporária como especificada não pôde ser criada usando a otimização somente de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="781df-192"><strong>JetOpenTempTable2</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="781df-193">Esse erro só será retornado pelo Windows Server 2003 e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="781df-193">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-194">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="781df-194">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="781df-195">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="781df-195">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-196">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="781df-196">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="781df-197">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="781df-197">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="781df-198">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="781df-198">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-199">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="781df-199">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="781df-200">O campo CP do <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como uma página de código válida.</span><span class="sxs-lookup"><span data-stu-id="781df-200">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="781df-201">Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="781df-201">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="781df-202">Um valor de 0 significa que o padrão será usado (Inglês, 1252).</span><span class="sxs-lookup"><span data-stu-id="781df-202">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-203">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="781df-203">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="781df-204">O campo <em>coltyp</em> da <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como um tipo de coluna válido.</span><span class="sxs-lookup"><span data-stu-id="781df-204">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-205">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="781df-205">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="781df-206">Não foi possível criar o índice porque uma definição de índice inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="781df-206">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="781df-207"><strong>JetOpenTempTable2</strong> retornará este erro quando:</span><span class="sxs-lookup"><span data-stu-id="781df-207"><strong>JetOpenTempTable2</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="781df-208">A localidade neutra do idioma é especificada.</span><span class="sxs-lookup"><span data-stu-id="781df-208">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="781df-209">Um conjunto inválido de sinalizadores de normalização foi especificado.</span><span class="sxs-lookup"><span data-stu-id="781df-209">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="781df-210">Esse erro só será retornado pelo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="781df-210">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-211">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="781df-211">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="781df-212">Não foi possível criar o índice porque foi feita uma tentativa de usar uma identificação de localidade inválida.</span><span class="sxs-lookup"><span data-stu-id="781df-212">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="781df-213">A ID de localidade pode ser completamente inválida ou o pacote de idiomas associado pode não estar instalado.</span><span class="sxs-lookup"><span data-stu-id="781df-213">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-214">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="781df-214">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="781df-215">Não foi possível criar o índice porque foi feita uma tentativa de usar um conjunto inválido de sinalizadores de normalização.</span><span class="sxs-lookup"><span data-stu-id="781df-215">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="781df-216">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="781df-216">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="781df-217">No Windows 2000, sinalizadores de normalização inválidos resultarão em JET_errIndexInvalidDef em vez disso.</span><span class="sxs-lookup"><span data-stu-id="781df-217">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-218">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="781df-218">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="781df-219">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="781df-219">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-220">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="781df-220">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="781df-221">A operação falhou porque o mecanismo não pode alocar os recursos necessários para abrir um novo cursor.</span><span class="sxs-lookup"><span data-stu-id="781df-221">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="781df-222">Os recursos de cursor são configurados usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="781df-222">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-223">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="781df-223">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="781df-224">A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</span><span class="sxs-lookup"><span data-stu-id="781df-224">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="781df-225"><strong>JetOpenTempTable2</strong> pode retornar JET_errOutOfMemory se o espaço de endereço do processo do host se tornar muito fragmentado.</span><span class="sxs-lookup"><span data-stu-id="781df-225"><strong>JetOpenTempTable2</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="781df-226">O Gerenciador de tabela temporária sempre alocará um bloco de 1 MB de espaço de endereço para cada tabela temporária criada, independentemente da quantidade de dados a serem armazenados.</span><span class="sxs-lookup"><span data-stu-id="781df-226">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-227">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="781df-227">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="781df-228">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="781df-228">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-229">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="781df-229">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="781df-230">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="781df-230">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="781df-231">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="781df-231">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-232">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="781df-232">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="781df-233">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="781df-233">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-234">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="781df-234">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="781df-235">Foi feita uma tentativa de adicionar muitas colunas à tabela.</span><span class="sxs-lookup"><span data-stu-id="781df-235">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="781df-236">Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</span><span class="sxs-lookup"><span data-stu-id="781df-236">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-237">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="781df-237">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="781df-238">A operação falhou porque o mecanismo não pode alocar os recursos necessários para armazenar em cache os índices da tabela.</span><span class="sxs-lookup"><span data-stu-id="781df-238">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="781df-239">O número de índices cujo esquema pode ser armazenado em cache é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="781df-239">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-240">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="781df-240">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="781df-241">A operação falhou porque o mecanismo não pode alocar os recursos necessários para armazenar em cache o esquema da tabela.</span><span class="sxs-lookup"><span data-stu-id="781df-241">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="781df-242">O número de tabelas cujo esquema pode ser armazenado em cache é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="781df-242">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-243">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="781df-243">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="781df-244">A operação falhou porque o mecanismo não pode alocar os recursos necessários para criar uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="781df-244">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="781df-245">Os recursos de tabela temporária são configurados usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="781df-245">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="781df-246">Em caso de sucesso, será retornado um cursor aberto na tabela temporária recém-criada.</span><span class="sxs-lookup"><span data-stu-id="781df-246">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="781df-247">O estado do banco de dados temporário será preparado para conter a nova tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="781df-247">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="781df-248">O estado de qualquer banco de dados comum em uso pelo mecanismo de banco de dados permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="781df-248">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="781df-249">Em caso de falha, a tabela temporária não será criada e um cursor não será retornado.</span><span class="sxs-lookup"><span data-stu-id="781df-249">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="781df-250">O estado do banco de dados temporário pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="781df-250">The state of the temporary database may be changed.</span></span> <span data-ttu-id="781df-251">O estado de qualquer banco de dados comum em uso pelo mecanismo de banco de dados permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="781df-251">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="781df-252">Comentários</span><span class="sxs-lookup"><span data-stu-id="781df-252">Remarks</span></span>

<span data-ttu-id="781df-253">Consulte [JetOpenTempTable](./jetopentemptable-function.md).</span><span class="sxs-lookup"><span data-stu-id="781df-253">See [JetOpenTempTable](./jetopentemptable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="781df-254">Requisitos</span><span class="sxs-lookup"><span data-stu-id="781df-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="781df-255"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="781df-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="781df-256">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="781df-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-257"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="781df-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="781df-258">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="781df-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-259"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="781df-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="781df-260">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="781df-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="781df-261"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="781df-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="781df-262">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="781df-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="781df-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="781df-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="781df-264">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="781df-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="781df-265">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="781df-265">See Also</span></span>

[<span data-ttu-id="781df-266">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="781df-266">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="781df-267">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="781df-267">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="781df-268">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="781df-268">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="781df-269">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="781df-269">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="781df-270">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="781df-270">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="781df-271">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="781df-271">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="781df-272">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="781df-272">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="781df-273">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="781df-273">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="781df-274">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="781df-274">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="781df-275">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="781df-275">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="781df-276">JetMove</span><span class="sxs-lookup"><span data-stu-id="781df-276">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="781df-277">JetRollback</span><span class="sxs-lookup"><span data-stu-id="781df-277">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="781df-278">JetSeek</span><span class="sxs-lookup"><span data-stu-id="781df-278">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="781df-279">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="781df-279">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="781df-280">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="781df-280">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
