---
description: 'Saiba mais sobre: função JetCreateTable'
title: Função JetCreateTable
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f385cfd668af934bfde2669277db7ed048a1fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808253"
---
# <a name="jetcreatetable-function"></a><span data-ttu-id="e0ce1-103">Função JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="e0ce1-103">JetCreateTable Function</span></span>


<span data-ttu-id="e0ce1-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e0ce1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetable-function"></a><span data-ttu-id="e0ce1-105">Função JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="e0ce1-105">JetCreateTable Function</span></span>

<span data-ttu-id="e0ce1-106">A função **JetCreateTable** cria uma tabela vazia em um banco de dados ESE.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-106">The **JetCreateTable** function creates an empty table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="e0ce1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0ce1-107">Parameters</span></span>

<span data-ttu-id="e0ce1-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e0ce1-108">*sesid*</span></span>

<span data-ttu-id="e0ce1-109">O contexto da sessão de banco de dados a ser usado.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-109">The database session context to use.</span></span>

<span data-ttu-id="e0ce1-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="e0ce1-110">*dbid*</span></span>

<span data-ttu-id="e0ce1-111">O identificador de banco de dados a ser usado.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-111">The database identifier to use.</span></span>

<span data-ttu-id="e0ce1-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="e0ce1-112">*szTableName*</span></span>

<span data-ttu-id="e0ce1-113">O nome do índice a ser criado.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-113">The name of the index to create.</span></span>

<span data-ttu-id="e0ce1-114">O nome deve ser formatado de acordo com as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="e0ce1-114">The name must be formatted according to the following rules:</span></span>

  - <span data-ttu-id="e0ce1-115">Ser menor que JET_cbNameMost, não incluindo o nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-115">Be less than JET_cbNameMost, not including the terminating NULL.</span></span>

  - <span data-ttu-id="e0ce1-116">Ser feita do seguinte conjunto de caracteres: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto para " \! "</span><span class="sxs-lookup"><span data-stu-id="e0ce1-116">Be made of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="e0ce1-117">(ponto de exclamação), "," (vírgula), " \[ " (colchete de abertura) e " \] " (colchete de fechamento) — ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c, 0x5d até 0x7F.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="e0ce1-118">Não comece com um espaço.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-118">Not begin with a space.</span></span>

  - <span data-ttu-id="e0ce1-119">Ser feita de pelo menos um caractere que não seja de espaço.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-119">Be made of at least one non-space character.</span></span>

<span data-ttu-id="e0ce1-120">*lPages*</span><span class="sxs-lookup"><span data-stu-id="e0ce1-120">*lPages*</span></span>

<span data-ttu-id="e0ce1-121">O número inicial de páginas de banco de dados a serem alocadas para a tabela.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-121">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="e0ce1-122">A especificação de um número maior que um pode reduzir a fragmentação se várias linhas forem inseridas nessa tabela.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-122">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="e0ce1-123">*lDensity*</span><span class="sxs-lookup"><span data-stu-id="e0ce1-123">*lDensity*</span></span>

<span data-ttu-id="e0ce1-124">A densidade da tabela, em pontos percentuais.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-124">The table density, in percentage points.</span></span> <span data-ttu-id="e0ce1-125">O número deve ser 0 ou estar no intervalo de 20 a 100.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-125">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="e0ce1-126">Passar 0 significa que o valor padrão deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-126">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="e0ce1-127">O padrão é 80.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-127">The default is 80.</span></span>

<span data-ttu-id="e0ce1-128">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="e0ce1-128">*ptableid*</span></span>

<span data-ttu-id="e0ce1-129">Em caso de sucesso, o identificador de tabela é retornado nesse campo.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-129">On success, the table identifier is returned in this field.</span></span> <span data-ttu-id="e0ce1-130">O valor será indefinido se a API não retornar JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-130">The value is undefined if the API does not return JET_errSuccess.</span></span>

### <a name="return-value"></a><span data-ttu-id="e0ce1-131">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e0ce1-131">Return Value</span></span>

<span data-ttu-id="e0ce1-132">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e0ce1-133">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0ce1-134">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e0ce1-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="e0ce1-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0ce1-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e0ce1-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-137">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-137">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-138">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="e0ce1-138">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-139">A função de retorno de chamada não pôde ser resolvida.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-139">The callback function could not be resolved.</span></span> <span data-ttu-id="e0ce1-140">A DLL pode não ter sido encontrada ou a função na DLL pode não ter sido encontrada.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-140">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="e0ce1-141">Com o registro em log suficiente habilitado, o log de eventos fornecerá mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-141">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-142">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="e0ce1-142">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-143">Foi feita uma tentativa de indexar uma coluna de atualização de caução ou SLV (Observe que as colunas SLV foram preteridas).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-143">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-144">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="e0ce1-144">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-145">Se ptablecreate- &gt; grbit especificar JET_bitTableCreateTemplateTable, mas ptablecreate- &gt; szTemplateTableName será definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-145">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-146">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="e0ce1-146">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-147">Já existe uma coluna.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-147">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-148">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="e0ce1-148">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-149">Foi feita uma tentativa de indexar uma coluna não existente.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-149">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="e0ce1-150">A tentativa de indexar condicionalmente uma coluna não existente também pode produzir esse erro.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-150">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-151">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="e0ce1-151">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-152">Foi feita uma tentativa de adicionar uma coluna redundante.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-152">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="e0ce1-153">Não deve haver mais de uma coluna de incremento automático e não há mais de uma coluna de versão por tabela.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-153">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-154">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="e0ce1-154">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-155">Uma densidade inválida foi passada no membro <em>ulDensity</em> na estrutura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="e0ce1-155">An invalid density was passed in the <em>ulDensity</em> member in the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-156">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="e0ce1-156">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-157">Significa que a tabela nomeada no membro <strong>szTemplateTableName</strong> da estrutura de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> não foi marcada como uma tabela de modelo (ou seja, essa tabela não tinha JET_bitTableCreateTemplateTable definido).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-157">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not a marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-158">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="e0ce1-158">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-159">Foi feita uma tentativa de definir dois índices idênticos.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-159">An attempt was made to define two identical indexes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-160">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="e0ce1-160">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-161">Foi feita uma tentativa de especificar mais de um índice primário para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-161">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="e0ce1-162">Uma tabela deve ter exatamente um índice primário.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-162">A table must have exactly one primary index.</span></span> <span data-ttu-id="e0ce1-163">Se nenhum índice primário for especificado, o mecanismo de banco de dados criará de forma transparente um.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-163">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-164">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="e0ce1-164">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-165">Uma definição de índice inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-165">An invalid index definition was specified.</span></span> <span data-ttu-id="e0ce1-166">Alguns dos motivos possíveis para receber esse erro são:</span><span class="sxs-lookup"><span data-stu-id="e0ce1-166">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="e0ce1-167">Um índice primário é condicional (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é maior que zero).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-167">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-168">Windows Server 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-168">Windows Server 2003 and later.</span></span> <span data-ttu-id="e0ce1-169">Tentativa de criar um índice de tupla com limites de tupla, mas sem passar o membro <strong>ptuplelimits</strong> na estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_BITINDEXTUPLELIMITS definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-169">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-170">Passando uma definição de chave inválida no membro <strong>szKey</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="e0ce1-170">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="e0ce1-171">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma discussão sobre definições válidas.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-171">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-172">Definir o membro <strong>cbVarSegMac</strong> em <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ser maior que JET_cbPrimaryKeyMost (para um índice primário) ou maior que JET_cbSecondaryKeyMost (para um índice secundário).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-172">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-173">Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o conjunto de bits JET_bitIndexUnicode no membro <strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-173">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="e0ce1-174">Algumas causas comuns incluem o membro <strong>pidxunicode</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é NULL ou o LCID especificado na estrutura <strong>pidxunicode</strong> é inválido.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-174">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-175">Especificando uma coluna com valores múltiplos para um índice primário.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-175">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-176">Tentando indexar muitas colunas condicionais.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-176">Trying to index too many conditional columns.</span></span> <span data-ttu-id="e0ce1-177">O membro <strong>cConditionalColumn</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ser maior que JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-177">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-178">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="e0ce1-178">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-179">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-179">Windows XP and later.</span></span> <span data-ttu-id="e0ce1-180">Uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> foi especificada e não há suporte para seus limites.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-180">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="e0ce1-181">Consulte a seção comentários da estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="e0ce1-181">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-182">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="e0ce1-182">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-183">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-183">Windows XP and later.</span></span> <span data-ttu-id="e0ce1-184">Um índice de tupla não pode ser exclusivo (ou seja, o membro <em>grbit</em> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ter JET_bitIndexPrimary e JET_bitIndexUnique definido).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-184">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-185">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="e0ce1-185">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-186">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-186">Windows XP and later.</span></span> <span data-ttu-id="e0ce1-187">Um índice de tupla só pode ser sobre uma única coluna (ou seja, se o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiver JET_bitIndexTuples definido e o membro <strong>szKey</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especificar mais de uma coluna).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-187">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-188">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="e0ce1-188">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-189">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-189">Windows XP and later.</span></span> <span data-ttu-id="e0ce1-190">Um índice de tupla não pode ser um índice primário (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definido).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-190">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-191">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="e0ce1-191">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-192">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-192">Windows XP and later.</span></span> <span data-ttu-id="e0ce1-193">Um índice de tupla não permite que o membro <strong>cbVarSegMac</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> seja definida.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-193">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-194">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="e0ce1-194">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-195">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-195">Windows XP and later.</span></span> <span data-ttu-id="e0ce1-196">Um índice de tupla só pode estar em uma coluna de texto ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-196">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="e0ce1-197">Uma tentativa de indexar outras colunas (como colunas binárias) resultará em JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-197">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-198">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="e0ce1-198">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-199">Foi feita uma tentativa de criar um índice sem informações de versão em uma transação.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-199">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-200">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="e0ce1-200">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-201">O membro <strong>CP</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como uma página de código válida.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-201">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="e0ce1-202">Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-202">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="e0ce1-203">Um valor de 0 significa que o padrão será usado (Inglês, 1252).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-203">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-204">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="e0ce1-204">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-205">O membro <strong>coltyp</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como um tipo de coluna válido.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-205">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-206">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="e0ce1-206">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-207">Alguns dos motivos pelos quais esse erro pode ocorrer:</span><span class="sxs-lookup"><span data-stu-id="e0ce1-207">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="e0ce1-208">O membro <strong>rgindexcreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-208">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-209">O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-210">O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não foi definido como um valor válido.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-210">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-211">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="e0ce1-211">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-212">Uma combinação inválida de membros <strong>grbit</strong> foi especificada em <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-212">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="e0ce1-213">A definição do índice é inválida porque o membro <strong>grbit</strong> contém valores inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-213">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="e0ce1-214">Alguns motivos possíveis são:</span><span class="sxs-lookup"><span data-stu-id="e0ce1-214">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="e0ce1-215">Um índice primário tinha um bit de ignorar especificado (ou seja, JET_bitIndexPrimary foi passado com JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-215">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-216">Um índice vazio não ignora quaisquer membros nulos (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull definido).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-216">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-217">Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-217">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-218">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="e0ce1-218">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-219">Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> da estrutura de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> que é apontada pelo membro <strong>pidxunicode</strong> na estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ou pelo campo <strong>LCID</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-219">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-220">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e0ce1-220">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-221">Um parâmetro inválido foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-221">An invalid parameter was given.</span></span> <span data-ttu-id="e0ce1-222">Alguns motivos possíveis são:</span><span class="sxs-lookup"><span data-stu-id="e0ce1-222">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="e0ce1-223">O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> é nulo.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-223">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-224">O membro <strong>cbStruct</strong> de uma das estruturas de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> dadas no membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> não foi definido como sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-224">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-225">O membro <strong>cbKey</strong> de uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-225">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="e0ce1-226">O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não está definido como sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-226">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-227">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="e0ce1-227">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-228">O registro é muito grande.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-228">The record is too big.</span></span> <span data-ttu-id="e0ce1-229">A soma do membro <strong>cbMax</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas as colunas fixas não deve exceder um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-229">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-230">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="e0ce1-230">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-231">A tabela já existe.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-231">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-232">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="e0ce1-232">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-233">Foi feita uma tentativa de adicionar muitas colunas à tabela.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-233">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="e0ce1-234">Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-234">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-235">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="e0ce1-235">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="e0ce1-236">Ocorreu um erro ao tentar normalizar uma coluna Unicode.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-236">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="e0ce1-237">Isso pode ser causado pela execução de recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-237">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="e0ce1-238">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0ce1-238">Remarks</span></span>

<span data-ttu-id="e0ce1-239">**JetCreateTable** cria uma tabela que não contém nenhuma coluna.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-239">**JetCreateTable** creates a table which does not contain any columns.</span></span> <span data-ttu-id="e0ce1-240">Para adicionar colunas, consulte [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-240">To add columns, see [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="e0ce1-241">Internamente, **JetCreateTable** chama [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), preenchendo uma estrutura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) com:</span><span class="sxs-lookup"><span data-stu-id="e0ce1-241">Internally, **JetCreateTable** calls [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), filling in a [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure with:</span></span>

  - <span data-ttu-id="e0ce1-242">JET_TABLECREATE2. cbStruct = sizeof (JET_TABLECREATE2)</span><span class="sxs-lookup"><span data-stu-id="e0ce1-242">JET_TABLECREATE2.cbStruct = sizeof( JET_TABLECREATE2 )</span></span>

  - <span data-ttu-id="e0ce1-243">JET_TABLECREATE2. szTableName = szTableName</span><span class="sxs-lookup"><span data-stu-id="e0ce1-243">JET_TABLECREATE2.szTableName = szTableName</span></span>

  - <span data-ttu-id="e0ce1-244">JET_TABLECREATE2. ulPages = lPage</span><span class="sxs-lookup"><span data-stu-id="e0ce1-244">JET_TABLECREATE2.ulPages = lPage</span></span>

  - <span data-ttu-id="e0ce1-245">JET_TABLECREATE2. ulDensity = lDensity</span><span class="sxs-lookup"><span data-stu-id="e0ce1-245">JET_TABLECREATE2.ulDensity = lDensity</span></span>

  - <span data-ttu-id="e0ce1-246">JET_TABLECREATE2. TableName = JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="e0ce1-246">JET_TABLECREATE2.tableid = JET_tableidNil</span></span>

<span data-ttu-id="e0ce1-247">Todos os outros campos da estrutura de [JET_TABLECREATE2](./jet-tablecreate2-structure.md) interna são definidos como zero ou nulos.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-247">All the other fields of the internal [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure are set to zero or NULL.</span></span> <span data-ttu-id="e0ce1-248">Na saída, *pTableID* será definido como JET_TABLECREATE2. TableName.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-248">On output, *ptableid* will be set to JET_TABLECREATE2.tableid.</span></span>

<span data-ttu-id="e0ce1-249">Consulte [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-249">See [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) for more details.</span></span>

<span data-ttu-id="e0ce1-250">Como o [JetOpenTable](./jetopentable-function.md), quando o aplicativo é feito usando o membro **TableName** retornado da estrutura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) , ele normalmente deve ser fechado com [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-250">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned **tableid** member from the [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="e0ce1-251">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0ce1-251">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-252"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e0ce1-252"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e0ce1-253">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-253">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-254"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="e0ce1-254"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e0ce1-255">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-255">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-256"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="e0ce1-256"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e0ce1-257">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-257">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-258"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="e0ce1-258"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e0ce1-259">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-259">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0ce1-260"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e0ce1-260"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e0ce1-261">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-261">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0ce1-262"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e0ce1-262"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e0ce1-263">Implementado como <strong>JetCreateTableW</strong> (Unicode) e <strong>JetCreateTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e0ce1-263">Implemented as <strong>JetCreateTableW</strong> (Unicode) and <strong>JetCreateTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e0ce1-264">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e0ce1-264">See Also</span></span>

[<span data-ttu-id="e0ce1-265">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="e0ce1-265">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="e0ce1-266">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e0ce1-266">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e0ce1-267">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e0ce1-267">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e0ce1-268">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e0ce1-268">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e0ce1-269">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="e0ce1-269">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="e0ce1-270">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="e0ce1-270">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="e0ce1-271">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="e0ce1-271">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="e0ce1-272">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="e0ce1-272">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
