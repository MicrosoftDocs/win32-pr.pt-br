---
description: 'Saiba mais sobre: função JetAddColumn'
title: Função JetAddColumn
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b8c3eac113daeae43ec4a8e62b7fcda9ddbf9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791090"
---
# <a name="jetaddcolumn-function"></a><span data-ttu-id="759b0-103">Função JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="759b0-103">JetAddColumn Function</span></span>


<span data-ttu-id="759b0-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="759b0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetaddcolumn-function"></a><span data-ttu-id="759b0-105">Função JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="759b0-105">JetAddColumn Function</span></span>

<span data-ttu-id="759b0-106">A função **JetAddColumn** adiciona uma nova coluna a uma tabela existente em um banco de dados ESE.</span><span class="sxs-lookup"><span data-stu-id="759b0-106">The **JetAddColumn** function adds a new column to an existing table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="759b0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="759b0-107">Parameters</span></span>

<span data-ttu-id="759b0-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="759b0-108">*sesid*</span></span>

<span data-ttu-id="759b0-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="759b0-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="759b0-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="759b0-110">*tableid*</span></span>

<span data-ttu-id="759b0-111">A tabela à qual adicionar a coluna.</span><span class="sxs-lookup"><span data-stu-id="759b0-111">The table to which to add the column.</span></span>

<span data-ttu-id="759b0-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="759b0-112">*szColumnName*</span></span>

<span data-ttu-id="759b0-113">O nome da coluna a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="759b0-113">The name of the column to add.</span></span> <span data-ttu-id="759b0-114">O nome deve atender aos seguintes critérios:</span><span class="sxs-lookup"><span data-stu-id="759b0-114">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="759b0-115">Ele deve ter menos de JET_cbNameMost caracteres de comprimento, não incluindo o **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="759b0-115">It must be fewer than JET_cbNameMost characters in length, not including the terminating **NULL**.</span></span>

  - <span data-ttu-id="759b0-116">Ele deve conter caracteres somente dos seguintes conjuntos: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto para ponto de exclamação ( \! ), vírgula (,), colchete de abertura ( \[ ) e colchete de fechamento ( \] ) — ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c e 0x5d até 0x7F.</span><span class="sxs-lookup"><span data-stu-id="759b0-116">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="759b0-117">Ele não pode começar com um espaço.</span><span class="sxs-lookup"><span data-stu-id="759b0-117">It cannot begin with a space.</span></span>

  - <span data-ttu-id="759b0-118">Ele deve conter pelo menos um caractere que não seja de espaço.</span><span class="sxs-lookup"><span data-stu-id="759b0-118">It must contain at least one non-space character.</span></span>

<span data-ttu-id="759b0-119">*pcolumndef*</span><span class="sxs-lookup"><span data-stu-id="759b0-119">*pcolumndef*</span></span>

<span data-ttu-id="759b0-120">Um ponteiro para uma estrutura de [JET_COLUMNDEF](./jet-columndef-structure.md) , que define os dados que podem ser armazenados em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="759b0-120">A pointer to a [JET_COLUMNDEF](./jet-columndef-structure.md) structure, which defines the data that can be stored in a column.</span></span>

<span data-ttu-id="759b0-121">*pvDefault*</span><span class="sxs-lookup"><span data-stu-id="759b0-121">*pvDefault*</span></span>

<span data-ttu-id="759b0-122">Um ponteiro para um buffer que contém o valor padrão para a coluna.</span><span class="sxs-lookup"><span data-stu-id="759b0-122">A pointer to a buffer that contains the default value for the column.</span></span> <span data-ttu-id="759b0-123">O comprimento do buffer é **cbDefault**.</span><span class="sxs-lookup"><span data-stu-id="759b0-123">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="759b0-124">Se não houver nenhum padrão, defina **pvDefault** como **nulo** e **cbDefault** como zero.</span><span class="sxs-lookup"><span data-stu-id="759b0-124">If there is no default, set **pvDefault** to **NULL** and **cbDefault** to zero.</span></span> <span data-ttu-id="759b0-125">Os valores padrão não podem ser maiores que JET_cbColumnMost bytes para colunas fixas ou JET_cbLVDefaultValueMost bytes para valores longos.</span><span class="sxs-lookup"><span data-stu-id="759b0-125">Default values cannot be larger than JET_cbColumnMost bytes for fixed columns or JET_cbLVDefaultValueMost bytes for long values.</span></span> <span data-ttu-id="759b0-126">Se um valor padrão for maior que isso, ele será silenciosamente truncado.</span><span class="sxs-lookup"><span data-stu-id="759b0-126">If a default value is larger than that, it will be silently truncated.</span></span>

<span data-ttu-id="759b0-127">Se *grbit* tiver JET_bitColumnUserDefinedDefault definido, **pvDefault** será interpretado como um ponteiro para uma estrutura de [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="759b0-127">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure.</span></span>

<span data-ttu-id="759b0-128">*cbDefault*</span><span class="sxs-lookup"><span data-stu-id="759b0-128">*cbDefault*</span></span>

<span data-ttu-id="759b0-129">O tamanho, em bytes, do buffer especificado em **pvDefault**.</span><span class="sxs-lookup"><span data-stu-id="759b0-129">The size, in bytes, of the buffer that is specified in **pvDefault**.</span></span>

<span data-ttu-id="759b0-130">*pcolumnid*</span><span class="sxs-lookup"><span data-stu-id="759b0-130">*pcolumnid*</span></span>

<span data-ttu-id="759b0-131">Um ponteiro para uma estrutura de [JET_COLUMNID](./jet-columnid.md) , que, em caso de êxito, receberá o identificador da coluna recém-criada.</span><span class="sxs-lookup"><span data-stu-id="759b0-131">A pointer to a [JET_COLUMNID](./jet-columnid.md) structure, which, on success, will receive the identifier of the newly created column.</span></span> <span data-ttu-id="759b0-132">Em caso de falha, o valor é indefinido.</span><span class="sxs-lookup"><span data-stu-id="759b0-132">On failure, the value is undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="759b0-133">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="759b0-133">Return Value</span></span>

<span data-ttu-id="759b0-134">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="759b0-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="759b0-135">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="759b0-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="759b0-136">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="759b0-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="759b0-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="759b0-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="759b0-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="759b0-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="759b0-139">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="759b0-139">The operation was successful.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-140">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="759b0-140">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="759b0-141">Foi feita uma tentativa de modificar a definição de dados de uma tabela DDL fixa.</span><span class="sxs-lookup"><span data-stu-id="759b0-141">An attempt was made to modify the data definition of a fixed DDL table.</span></span> <span data-ttu-id="759b0-142">Um exemplo de uma tabela com DDL fixo é uma tabela de modelo.</span><span class="sxs-lookup"><span data-stu-id="759b0-142">An example of a table with fixed DDL is a Template Table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="759b0-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="759b0-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="759b0-144">Um parâmetro inválido foi passado para a API.</span><span class="sxs-lookup"><span data-stu-id="759b0-144">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="759b0-145">Alguns exemplos de parâmetros inválidos são:</span><span class="sxs-lookup"><span data-stu-id="759b0-145">Some examples of invalid parameters are:</span></span></p>
<ul>
<li><p><span data-ttu-id="759b0-146">Passando o tamanho errado da estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> em seu membro <em>cbStruct</em> .</span><span class="sxs-lookup"><span data-stu-id="759b0-146">Passing in the wrong size of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure in its <em>cbStruct</em> member.</span></span></p></li>
<li><p><span data-ttu-id="759b0-147">Passando JET_bitColumnUserDefinedDefault, mas não definindo <strong>cbDefault</strong> como sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span><span class="sxs-lookup"><span data-stu-id="759b0-147">Passing in JET_bitColumnUserDefinedDefault, but not setting <strong>cbDefault</strong> to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-148">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="759b0-148">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="759b0-149">Foi feita uma tentativa de adicionar uma coluna com o conjunto de bits JET_bitColumnUnversioned, mas a sessão está em uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="759b0-149">An attempt was made to add a column with the JET_bitColumnUnversioned bit set, but the session is currently in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="759b0-150">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="759b0-150">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="759b0-151">Já existe uma coluna.</span><span class="sxs-lookup"><span data-stu-id="759b0-151">A column already exists.</span></span> <span data-ttu-id="759b0-152">Foi feita uma tentativa de adicionar uma coluna sem informações de versão e essa coluna já existe.</span><span class="sxs-lookup"><span data-stu-id="759b0-152">An attempt was made to add a column without version information, and that column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-153">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="759b0-153">JET_errTableNotEmpty</span></span></p></td>
<td><p><span data-ttu-id="759b0-154">A tabela contém dados.</span><span class="sxs-lookup"><span data-stu-id="759b0-154">The table contains data.</span></span> <span data-ttu-id="759b0-155">Uma coluna de atualização de caução só pode ser adicionada a uma tabela vazia.</span><span class="sxs-lookup"><span data-stu-id="759b0-155">An Escrow Update column can only be added to an empty table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="759b0-156">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="759b0-156">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="759b0-157">O registro é muito grande.</span><span class="sxs-lookup"><span data-stu-id="759b0-157">The record is too big.</span></span> <span data-ttu-id="759b0-158">A soma do parâmetro <strong>cbMax</strong> para as colunas fixas não deve exceder um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="759b0-158">The sum of the <strong>cbMax</strong> parameter for the fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-159">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="759b0-159">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="759b0-160">Foi feita uma tentativa de adicionar muitas colunas à tabela.</span><span class="sxs-lookup"><span data-stu-id="759b0-160">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="759b0-161">Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</span><span class="sxs-lookup"><span data-stu-id="759b0-161">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="759b0-162">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="759b0-162">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="759b0-163">Foi feita uma tentativa de adicionar uma coluna redundante.</span><span class="sxs-lookup"><span data-stu-id="759b0-163">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="759b0-164">Não deve haver mais de uma coluna de incremento automático e não há mais de uma coluna de versão por tabela.</span><span class="sxs-lookup"><span data-stu-id="759b0-164">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-165">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="759b0-165">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="759b0-166">A função de retorno de chamada não pôde ser resolvida.</span><span class="sxs-lookup"><span data-stu-id="759b0-166">The callback function could not be resolved.</span></span> <span data-ttu-id="759b0-167">A DLL pode não ter sido encontrada ou a função na DLL pode não ter sido encontrada.</span><span class="sxs-lookup"><span data-stu-id="759b0-167">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="759b0-168">O log de eventos fornecerá mais detalhes se o registro em log suficiente estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="759b0-168">The event log will provide more details if sufficient logging is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="759b0-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="759b0-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="759b0-170">Um aviso que indica que o comprimento máximo (<strong>cbMax</strong>) de uma coluna fixa ou variável foi maior que JET_cbColumnMost.</span><span class="sxs-lookup"><span data-stu-id="759b0-170">A warning indicating that the maximum length (<strong>cbMax</strong>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="759b0-171">Esse limite não se aplica a valores longos ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> e <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="759b0-171">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-172">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="759b0-172">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="759b0-173">Um nome inválido foi passado como <strong>szColumnName</strong>.</span><span class="sxs-lookup"><span data-stu-id="759b0-173">An invalid name was passed as <strong>szColumnName</strong>.</span></span> <span data-ttu-id="759b0-174">Para obter mais informações sobre as restrições, consulte os critérios para <strong>szColumnName</strong>.</span><span class="sxs-lookup"><span data-stu-id="759b0-174">For more information about the restrictions, see the criteria for <strong>szColumnName</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="759b0-175">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="759b0-175">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="759b0-176">O campo <strong>coltyp</strong> não foi definido como um tipo de coluna válido.</span><span class="sxs-lookup"><span data-stu-id="759b0-176">The <strong>coltyp</strong> field was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-177">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="759b0-177">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="759b0-178">O parâmetro <strong>CP</strong> da estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como uma página de código válida.</span><span class="sxs-lookup"><span data-stu-id="759b0-178">The <strong>cp</strong> parameter of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="759b0-179">Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="759b0-179">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="759b0-180">Um valor de 0 significa que o padrão será usado (Inglês, 1252).</span><span class="sxs-lookup"><span data-stu-id="759b0-180">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="759b0-181">JET_errTaggedNotNULL</span><span class="sxs-lookup"><span data-stu-id="759b0-181">JET_errTaggedNotNULL</span></span></p></td>
<td><p><span data-ttu-id="759b0-182">JET_bitColumnNotNULL não pode ser usada com colunas marcadas, de valor longo ou SLV.</span><span class="sxs-lookup"><span data-stu-id="759b0-182">JET_bitColumnNotNULL cannot be used with tagged, Long Value, or SLV columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-183">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="759b0-183">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="759b0-184">Foi especificada uma combinação inválida de <em>grbits</em> .</span><span class="sxs-lookup"><span data-stu-id="759b0-184">An invalid combination of <em>grbits</em> was specified.</span></span> <span data-ttu-id="759b0-185">Alguns dos motivos para esse erro são:</span><span class="sxs-lookup"><span data-stu-id="759b0-185">Some of the reasons for this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="759b0-186">JET_bitColumnFixed foi usado em uma coluna marcada, de valor longo ou SLV.</span><span class="sxs-lookup"><span data-stu-id="759b0-186">JET_bitColumnFixed was used on a tagged, Long Value, or SLV column.</span></span></p></li>
<li><p><span data-ttu-id="759b0-187">JET_bitColumnEscrowUpdate foi usado em uma coluna que não era do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="759b0-187">JET_bitColumnEscrowUpdate was used on a column that was not of type <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="759b0-188">JET_bitColumnEscrowUpdate foi usado em uma coluna de versão (JET_bitColumnVersion).</span><span class="sxs-lookup"><span data-stu-id="759b0-188">JET_bitColumnEscrowUpdate was used on a Version column (JET_bitColumnVersion).</span></span></p></li>
<li><p><span data-ttu-id="759b0-189">JET_bitColumnEscrowUpdate foi usado em uma coluna AutoIncrememnt (JET_bitColumnAutoincrement).</span><span class="sxs-lookup"><span data-stu-id="759b0-189">JET_bitColumnEscrowUpdate was used on an AutoIncrememnt column (JET_bitColumnAutoincrement).</span></span></p></li>
<li><p><span data-ttu-id="759b0-190">JET_bitColumnEscrowUpdate foi usado em uma coluna que não tinha um valor padrão (<strong>cbDefault</strong> era igual a zero).</span><span class="sxs-lookup"><span data-stu-id="759b0-190">JET_bitColumnEscrowUpdate was used on a column that did not have a default value (<strong>cbDefault</strong> was equal to zero).</span></span></p></li>
<li><p><span data-ttu-id="759b0-191">JET_bitColumnFinalize foi usada em uma coluna que não era uma coluna de atualização de caução (JET_bitColumnEscrowUpdate não foi definida).</span><span class="sxs-lookup"><span data-stu-id="759b0-191">JET_bitColumnFinalize was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="759b0-192">JET_bitColumnDeleteOnZero foi usada em uma coluna que não era uma coluna de atualização de caução (JET_bitColumnEscrowUpdate não foi definida).</span><span class="sxs-lookup"><span data-stu-id="759b0-192">JET_bitColumnDeleteOnZero was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="759b0-193">JET_bitColumnAutoincrement foi usado em uma coluna que não foi <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="759b0-193">JET_bitColumnAutoincrement was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p>
<p><span data-ttu-id="759b0-194"><strong>Windows 2000:  </strong> Esse motivo para o código de erro é usado somente no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="759b0-194"><strong>Windows 2000:  </strong>This reason for the error code is used only in Windows 2000.</span></span></p>
<p><span data-ttu-id="759b0-195">JET_bitColumnAutoincrement foi usado em uma coluna que não foi <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> nem <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</span><span class="sxs-lookup"><span data-stu-id="759b0-195">JET_bitColumnAutoincrement was used on a column that was neither <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> nor <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</span></span></p>
<p><span data-ttu-id="759b0-196"><strong>Windows XP:  </strong> Esse motivo para o código de erro é usado no Windows XP e em sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="759b0-196"><strong>Windows XP:  </strong>This reason for the error code is used in Windows XP and later operating systems.</span></span></p></li>
<li><p><span data-ttu-id="759b0-197">JET_bitColumnVersion foi usado em uma coluna que não foi <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="759b0-197">JET_bitColumnVersion was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="759b0-198">JET_bitColumnVersion foi usado em uma coluna de incremento automático.</span><span class="sxs-lookup"><span data-stu-id="759b0-198">JET_bitColumnVersion was used on an autoincrement column.</span></span></p></li>
<li><p><span data-ttu-id="759b0-199">JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="759b0-199">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFixed.</span></span></p></li>
<li><p><span data-ttu-id="759b0-200">JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnNotNULL.</span><span class="sxs-lookup"><span data-stu-id="759b0-200">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnNotNULL.</span></span></p></li>
<li><p><span data-ttu-id="759b0-201">JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnVersion.</span><span class="sxs-lookup"><span data-stu-id="759b0-201">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnVersion.</span></span></p></li>
<li><p><span data-ttu-id="759b0-202">JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="759b0-202">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnAutoincrement.</span></span></p></li>
<li><p><span data-ttu-id="759b0-203">JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnUpdatable.</span><span class="sxs-lookup"><span data-stu-id="759b0-203">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnUpdatable.</span></span></p></li>
<li><p><span data-ttu-id="759b0-204">JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="759b0-204">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnEscrowUpdate.</span></span></p></li>
<li><p><span data-ttu-id="759b0-205">JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="759b0-205">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFinalize.</span></span></p></li>
<li><p><span data-ttu-id="759b0-206">JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="759b0-206">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnDeleteOnZero.</span></span></p></li>
<li><p><span data-ttu-id="759b0-207">JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="759b0-207">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnMaybeNull.</span></span></p></li>
<li><p><span data-ttu-id="759b0-208">JET_bitColumnUserDefinedDefault foi usado em uma coluna não marcada (que é fixed ou Variable).</span><span class="sxs-lookup"><span data-stu-id="759b0-208">JET_bitColumnUserDefinedDefault was used on a non-tagged column (that is fixed or variable).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="759b0-209">JET_errMultiValuedColumnMustBeTagged</span><span class="sxs-lookup"><span data-stu-id="759b0-209">JET_errMultiValuedColumnMustBeTagged</span></span></p></td>
<td><p><span data-ttu-id="759b0-210">Uma coluna com valores múltiplos (JET_bitColumnMultiValued) só pode ser usada em uma coluna marcada ou de valor longo (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="759b0-210">A multi-valued column (JET_bitColumnMultiValued) can only be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-211">JET_errCannotBeTagged</span><span class="sxs-lookup"><span data-stu-id="759b0-211">JET_errCannotBeTagged</span></span></p></td>
<td><p><span data-ttu-id="759b0-212">Foi feita uma tentativa de usar uma coluna marcada quando a coluna não pode ser marcada.</span><span class="sxs-lookup"><span data-stu-id="759b0-212">An attempt was made to use a tagged column when the column might not be tagged.</span></span> <span data-ttu-id="759b0-213">Algumas das restrições para desautorizar colunas marcadas são:</span><span class="sxs-lookup"><span data-stu-id="759b0-213">Some of the constraints for disallowing tagged columns are:</span></span></p>
<ul>
<li><p><span data-ttu-id="759b0-214">Uma coluna de atualização de caução (JET_bitColumnEscrowUpdate) não pode ser usada em uma coluna de valor marcado ou longo (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="759b0-214">An Escrow Update column (JET_bitColumnEscrowUpdate) cannot be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></li>
<li><p><span data-ttu-id="759b0-215">Uma coluna AutoIncrement não pode ser marcada.</span><span class="sxs-lookup"><span data-stu-id="759b0-215">An autoincrement column might not be tagged.</span></span></p></li>
<li><p><span data-ttu-id="759b0-216">Uma coluna de versão não pode ser marcada.</span><span class="sxs-lookup"><span data-stu-id="759b0-216">A Version column might not be tagged.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="759b0-217">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="759b0-217">JET_errExclusiveTableLockRequired</span></span></p></td>
<td><p><span data-ttu-id="759b0-218">Um bloqueio exclusivo na tabela era necessário para esta operação.</span><span class="sxs-lookup"><span data-stu-id="759b0-218">An exclusive lock on the table was required for this operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-219">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="759b0-219">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="759b0-220">Um aviso que indica que o comprimento máximo (<em>cbMax</em>) de uma coluna fixa ou variável foi maior que JET_cbColumnMost.</span><span class="sxs-lookup"><span data-stu-id="759b0-220">A warning indicating that the maximum length (<em>cbMax</em>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="759b0-221">Esse limite não se aplica a valores longos ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> e <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="759b0-221">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="759b0-222">Requisitos</span><span class="sxs-lookup"><span data-stu-id="759b0-222">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="759b0-223"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="759b0-223"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="759b0-224">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="759b0-224">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-225"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="759b0-225"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="759b0-226">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="759b0-226">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="759b0-227"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="759b0-227"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="759b0-228">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="759b0-228">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-229"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="759b0-229"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="759b0-230">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="759b0-230">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="759b0-231"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="759b0-231"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="759b0-232">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="759b0-232">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="759b0-233"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="759b0-233"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="759b0-234">Implementado como <strong>JetAddColumnW</strong> (Unicode) e <strong>JetAddColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="759b0-234">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="759b0-235">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="759b0-235">See Also</span></span>

[<span data-ttu-id="759b0-236">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="759b0-236">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="759b0-237">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="759b0-237">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="759b0-238">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="759b0-238">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="759b0-239">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="759b0-239">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="759b0-240">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="759b0-240">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="759b0-241">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="759b0-241">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="759b0-242">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="759b0-242">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="759b0-243">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="759b0-243">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="759b0-244">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="759b0-244">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="759b0-245">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="759b0-245">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
