---
description: 'Saiba mais sobre: estrutura de JET_OPENTEMPORARYTABLE'
title: Estrutura de JET_OPENTEMPORARYTABLE
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
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
ms.openlocfilehash: 51ae9026098e82538940bde2ef182ba0a7a11c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296820"
---
# <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="13001-103">Estrutura de JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="13001-103">JET_OPENTEMPORARYTABLE Structure</span></span>


<span data-ttu-id="13001-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="13001-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="13001-105">Estrutura de JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="13001-105">JET_OPENTEMPORARYTABLE Structure</span></span>

<span data-ttu-id="13001-106">A estrutura de **JET_OPENTEMPORARYTABLE** contém uma coleção facilmente extensível de parâmetros para a função **JET_OPENTEMPORARYTABLE** .</span><span class="sxs-lookup"><span data-stu-id="13001-106">The **JET_OPENTEMPORARYTABLE** structure contains an easily extensible collection of parameters for the **JET_OPENTEMPORARYTABLE** function.</span></span> <span data-ttu-id="13001-107">Essa estrutura é a tabela temporária equivalente da estrutura de [JET_TABLECREATE](./jet-tablecreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="13001-107">This structure is the temporary table equivalent of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure.</span></span>

<span data-ttu-id="13001-108">**Windows Vista:** A estrutura de **JET_OPENTEMPORARYTABLE** é introduzida no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="13001-108">**Windows Vista:** The **JET_OPENTEMPORARYTABLE** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a><span data-ttu-id="13001-109">Membros</span><span class="sxs-lookup"><span data-stu-id="13001-109">Members</span></span>

<span data-ttu-id="13001-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="13001-110">**cbStruct**</span></span>

<span data-ttu-id="13001-111">O tamanho dessa estrutura em bytes (para expansão futura).</span><span class="sxs-lookup"><span data-stu-id="13001-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="13001-112">Ele deve ser definido como sizeof (JET_TABLECREATE) em bytes.</span><span class="sxs-lookup"><span data-stu-id="13001-112">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="13001-113">**prgcolumndef**</span><span class="sxs-lookup"><span data-stu-id="13001-113">**prgcolumndef**</span></span>

<span data-ttu-id="13001-114">Definições de coluna para as colunas criadas na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="13001-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="13001-115">Existem limitações **importantes** para as opções de definição de coluna usadas com uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="13001-115">**Important** limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="13001-116">Consulte a seção Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="13001-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="13001-117">Além das opções de definição de coluna usual, zero ou mais das opções a seguir também podem ser especificadas, que são relevantes apenas no contexto de uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="13001-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13001-118">Valor</span><span class="sxs-lookup"><span data-stu-id="13001-118">Value</span></span></p></th>
<th><p><span data-ttu-id="13001-119">Significado</span><span class="sxs-lookup"><span data-stu-id="13001-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13001-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="13001-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="13001-121">A ordem de classificação da coluna de chave para a tabela temporária deve ser decrescente em vez de crescente.</span><span class="sxs-lookup"><span data-stu-id="13001-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="13001-122">Se essa opção for especificada sem JET_bitColumnTTKey, essa opção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="13001-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13001-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="13001-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="13001-124">A coluna será uma coluna de chave para a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="13001-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="13001-125">A ordem das definições de coluna com essa opção especificada na matriz de entrada determinará a precedência de cada coluna de chave para a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="13001-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="13001-126">A primeira definição de coluna na matriz que tem esse conjunto de opções será a coluna de chave mais significativa e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="13001-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="13001-127">Se mais colunas de chave forem solicitadas do que o mecanismo de banco de dados pode ter suporte, essa opção será ignorada para as colunas de chave sem suporte.</span><span class="sxs-lookup"><span data-stu-id="13001-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="13001-128">**ccolumn**</span><span class="sxs-lookup"><span data-stu-id="13001-128">**ccolumn**</span></span>

<span data-ttu-id="13001-129">Consulte *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="13001-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="13001-130">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="13001-130">**pidxunicode**</span></span>

<span data-ttu-id="13001-131">Os sinalizadores de ID de localidade e normalização a serem usados para comparar qualquer dado de coluna de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="13001-131">The locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="13001-132">Quando esse parâmetro não estiver presente e quando o parâmetro *LCID* não estiver presente, o LCID padrão será usado para comparar as colunas de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="13001-132">When this parameter is not present and when the *lcid* parameter is not present, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="13001-133">O LCID padrão é a localidade inglês dos EUA.</span><span class="sxs-lookup"><span data-stu-id="13001-133">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="13001-134">Quando esse parâmetro não estiver presente, os sinalizadores de normalização padrão serão usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="13001-134">When this parameter is not present, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="13001-135">Os sinalizadores de normalização padrão são: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="13001-135">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="13001-136">**grbit**</span><span class="sxs-lookup"><span data-stu-id="13001-136">**grbit**</span></span>

<span data-ttu-id="13001-137">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="13001-137">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13001-138">Valor</span><span class="sxs-lookup"><span data-stu-id="13001-138">Value</span></span></p></th>
<th><p><span data-ttu-id="13001-139">Significado</span><span class="sxs-lookup"><span data-stu-id="13001-139">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13001-140">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="13001-140">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="13001-141">Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir o uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para pesquisar registros por chave de índice.</span><span class="sxs-lookup"><span data-stu-id="13001-141">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="13001-142">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="13001-142">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="13001-143">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="13001-143">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13001-144">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="13001-144">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="13001-145">As solicitações que os registros com chaves de índice duplicadas são removidas do conjunto final de registros na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="13001-145">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="13001-146">Antes do Windows Server 2003, o mecanismo de banco de dados sempre assumiu que essa opção está em vigor devido ao fato de que todos os índices clusterizados também devem ser uma chave primária e, portanto, devem ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="13001-146">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="13001-147">A partir do Windows Server 2003, agora é possível criar uma tabela temporária que não remove duplicatas quando a opção de JET_bitTTForwardOnly também é especificada.</span><span class="sxs-lookup"><span data-stu-id="13001-147">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="13001-148">Não é possível saber qual duplicata terá sucesso e quais duplicatas serão descartadas, em geral.</span><span class="sxs-lookup"><span data-stu-id="13001-148">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="13001-149">No entanto, quando a opção JET_bitTTErrorOnDuplicateInsertion for solicitada, o primeiro registro com uma determinada chave de índice a ser inserida na tabela temporária sempre terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="13001-149">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13001-150">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="13001-150">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="13001-151">Solicita que a tabela temporária seja flexível o suficiente para permitir que os registros que foram inseridos anteriormente sejam alterados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="13001-151">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="13001-152">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="13001-152">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="13001-153">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="13001-153">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13001-154">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="13001-154">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="13001-155">Solicita que a tabela temporária seja flexível o suficiente para permitir que os registros sejam verificados em ordem e direção arbitrárias usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="13001-155">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="13001-156">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="13001-156">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="13001-157">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="13001-157">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13001-158">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="13001-158">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="13001-159">Solicita que os valores da coluna de chave <strong>nula</strong> sejam mais próximos do final do índice que os valores de coluna de chave não nulos.</span><span class="sxs-lookup"><span data-stu-id="13001-159">Requests that <strong>NULL</strong> key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13001-160">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="13001-160">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="13001-161">Força o Gerenciador de tabelas temporária a abandonar a pesquisa para que a melhor estratégia use o gerenciamento da tabela temporária, o que resultará em desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="13001-161">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13001-162">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="13001-162">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="13001-163">Qualquer tentativa de inserir um registro com a mesma chave de índice que um registro inserido anteriormente irá falhar imediatamente com JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="13001-163">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="13001-164">Se essa opção não for solicitada, uma duplicata será detectada imediatamente e falhará ou será removida silenciosamente mais tarde, dependendo da estratégia escolhida pelo mecanismo de banco de dados para implementar a tabela temporária, com base na funcionalidade solicitada.</span><span class="sxs-lookup"><span data-stu-id="13001-164">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="13001-165">Se essa funcionalidade não for necessária, é melhor não solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="13001-165">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="13001-166">Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="13001-166">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13001-167">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="13001-167">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="13001-168">A tabela temporária só será criada se o Gerenciador de tabelas temporárias puder usar a implementação otimizada para resultados de consulta intermediários.</span><span class="sxs-lookup"><span data-stu-id="13001-168">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="13001-169">Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="13001-169">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="13001-170">Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="13001-170">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="13001-171">Consulte JET_bitTTUnique para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="13001-171">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="13001-172"><strong>Windows Server 2003:  </strong> Essa opção só está disponível no Windows Server 2003 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="13001-172"><strong>Windows Server 2003:  </strong>This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="13001-173">**prgcolumnid**</span><span class="sxs-lookup"><span data-stu-id="13001-173">**prgcolumnid**</span></span>

<span data-ttu-id="13001-174">O buffer de saída que recebe a matriz de IDs de coluna geradas durante a criação da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="13001-174">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="13001-175">As IDs de coluna nessa matriz correspondem exatamente à matriz de entrada de definições de coluna.</span><span class="sxs-lookup"><span data-stu-id="13001-175">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="13001-176">Como resultado, o tamanho desse buffer deve corresponder ao tamanho da matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="13001-176">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

<span data-ttu-id="13001-177">**cbKeyMost**</span><span class="sxs-lookup"><span data-stu-id="13001-177">**cbKeyMost**</span></span>

<span data-ttu-id="13001-178">O tamanho máximo de uma chave que representa uma determinada linha.</span><span class="sxs-lookup"><span data-stu-id="13001-178">The maximum size for a key representing a given row.</span></span>

<span data-ttu-id="13001-179">O tamanho máximo da chave pode ser definido para controlar como as chaves são truncadas.</span><span class="sxs-lookup"><span data-stu-id="13001-179">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="13001-180">O truncamento de chave é importante porque pode afetar quando as linhas são consideradas distintas.</span><span class="sxs-lookup"><span data-stu-id="13001-180">Key truncation is important because it can affect when rows are considered to be distinct.</span></span>

<span data-ttu-id="13001-181">Se esse parâmetro for definido como 0 ou JET_cbKeyMostMin (255), o tamanho máximo da chave e sua semântica permanecerão idênticos ao tamanho máximo da chave com suporte no Windows Server 2003 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="13001-181">If this parameter is set to 0 or JET_cbKeyMostMin (255) then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003 and previous releases.</span></span> <span data-ttu-id="13001-182">Esse parâmetro também pode ser definido como um valor maior como uma função do tamanho da página do banco de dados para a instância (JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="13001-182">This parameter may also be set to a larger value as a function of the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="13001-183">Consulte JET_paramKeyMost para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="13001-183">See JET_paramKeyMost for more information.</span></span>

<span data-ttu-id="13001-184">**cbVarSegMac**</span><span class="sxs-lookup"><span data-stu-id="13001-184">**cbVarSegMac**</span></span>

<span data-ttu-id="13001-185">A quantidade máxima de dados que serão usados de qualquer coluna de comprimento variável para construir uma chave para uma determinada linha.</span><span class="sxs-lookup"><span data-stu-id="13001-185">The maximum amount of data that will be used from any variable length column to construct a key for a given row.</span></span>

<span data-ttu-id="13001-186">Esse parâmetro pode ser usado para controlar a quantidade de espaço de chave consumida por qualquer coluna de chave fornecida.</span><span class="sxs-lookup"><span data-stu-id="13001-186">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="13001-187">Esse limite está em bytes.</span><span class="sxs-lookup"><span data-stu-id="13001-187">This limit is in bytes.</span></span> <span data-ttu-id="13001-188">Se esse parâmetro for zero ou for o mesmo que o parâmetro *cbKeyMost* , nenhum limite estará em vigor.</span><span class="sxs-lookup"><span data-stu-id="13001-188">If this parameter is zero or is the same as the *cbKeyMost* parameter then no limit is in effect.</span></span>

<span data-ttu-id="13001-189">**TableID**</span><span class="sxs-lookup"><span data-stu-id="13001-189">**tableid**</span></span>

<span data-ttu-id="13001-190">O identificador de tabela para a tabela temporária criada como resultado de uma chamada bem-sucedida para [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="13001-190">The table handle for the temporary table created as a result of a successful call to [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="13001-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13001-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13001-192"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="13001-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="13001-193">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="13001-193">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13001-194"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="13001-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="13001-195">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="13001-195">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13001-196"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="13001-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="13001-197">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="13001-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="13001-198">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="13001-198">See Also</span></span>

[<span data-ttu-id="13001-199">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="13001-199">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="13001-200">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="13001-200">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="13001-201">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="13001-201">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="13001-202">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="13001-202">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="13001-203">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="13001-203">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="13001-204">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="13001-204">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="13001-205">JetOpenTemporaryTable</span><span class="sxs-lookup"><span data-stu-id="13001-205">JetOpenTemporaryTable</span></span>](./jetopentemporarytable-function.md)  
[<span data-ttu-id="13001-206">Parâmetros do sistema do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="13001-206">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
