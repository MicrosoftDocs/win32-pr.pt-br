---
description: 'Saiba mais sobre: função JetCreateIndex'
title: Função JetCreateIndex
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785187"
---
# <a name="jetcreateindex-function"></a><span data-ttu-id="09062-103">Função JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="09062-103">JetCreateIndex Function</span></span>


<span data-ttu-id="09062-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="09062-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex-function"></a><span data-ttu-id="09062-105">Função JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="09062-105">JetCreateIndex Function</span></span>

<span data-ttu-id="09062-106">A função **JetCreateIndex** permite que você crie um índice de dados em um ESE (mecanismo de armazenamento extensível), que pode ser usado para localizar dados específicos rapidamente.</span><span class="sxs-lookup"><span data-stu-id="09062-106">The **JetCreateIndex** function enables you to create an index of data in an Extensible Storage Engine (ESE) database, which you can use to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a><span data-ttu-id="09062-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09062-107">Parameters</span></span>

<span data-ttu-id="09062-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="09062-108">*sesid*</span></span>

<span data-ttu-id="09062-109">O contexto da sessão de banco de dados a ser usado para uma chamada de API específica.</span><span class="sxs-lookup"><span data-stu-id="09062-109">The database session context to use for a particular API call.</span></span>

<span data-ttu-id="09062-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="09062-110">*tableid*</span></span>

<span data-ttu-id="09062-111">A tabela para a qual um índice será criado.</span><span class="sxs-lookup"><span data-stu-id="09062-111">The table that an index will be created for.</span></span>

<span data-ttu-id="09062-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="09062-112">*szIndexName*</span></span>

<span data-ttu-id="09062-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do índice a ser criado.</span><span class="sxs-lookup"><span data-stu-id="09062-113">A pointer to a null-terminated string that specifies the name of the index to be created.</span></span>

<span data-ttu-id="09062-114">O nome do índice deve estar de acordo com as seguintes diretrizes:</span><span class="sxs-lookup"><span data-stu-id="09062-114">The index name must conform to the following guidelines:</span></span>

  - <span data-ttu-id="09062-115">Ele deve conter menos caracteres que JET_cbNameMost, não incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="09062-115">It must contain fewer characters than JET_cbNameMost, not including the terminating null character.</span></span>

  - <span data-ttu-id="09062-116">Ele deve conter somente caracteres das seguintes categorias: 0 a 9, A a Z, a a z e todos os caracteres de pontuação, exceto para " \! "</span><span class="sxs-lookup"><span data-stu-id="09062-116">It must contain only characters from the following categories: 0 through 9, A through Z, a through z, and all punctuation characters except for "\!"</span></span> <span data-ttu-id="09062-117">(ponto de exclamação), "," (vírgula), " \[ " (colchete de abertura) e " \] " (colchete de fechamento) — ou seja, os caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c e 0x5d até 0x7F.</span><span class="sxs-lookup"><span data-stu-id="09062-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, the ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="09062-118">Ele não deve começar com um espaço.</span><span class="sxs-lookup"><span data-stu-id="09062-118">It must not begin with a space.</span></span>

  - <span data-ttu-id="09062-119">Ele deve conter pelo menos um caractere que não seja de espaço.</span><span class="sxs-lookup"><span data-stu-id="09062-119">It must contain at least one non-space character.</span></span>

<span data-ttu-id="09062-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="09062-120">*grbit*</span></span>

<span data-ttu-id="09062-121">Um grupo de bits que contém as opções a serem usadas para uma chamada específica.</span><span class="sxs-lookup"><span data-stu-id="09062-121">A group of bits that contains the options to be used for a particular call.</span></span> <span data-ttu-id="09062-122">Esse parâmetro pode incluir zero ou mais das opções encontradas na estrutura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="09062-122">This parameter can include zero or more of the options found in the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="09062-123">*szKey*</span><span class="sxs-lookup"><span data-stu-id="09062-123">*szKey*</span></span>

<span data-ttu-id="09062-124">Um ponteiro para uma cadeia de caracteres dupla com terminação nula de tokens delimitados por nulo.</span><span class="sxs-lookup"><span data-stu-id="09062-124">A pointer to a double null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="09062-125">Para obter mais informações sobre esse parâmetro, consulte a estrutura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="09062-125">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="09062-126">*cbKey*</span><span class="sxs-lookup"><span data-stu-id="09062-126">*cbKey*</span></span>

<span data-ttu-id="09062-127">O comprimento, em bytes, do parâmetro *szKey* , incluindo os dois caracteres nulos de terminação.</span><span class="sxs-lookup"><span data-stu-id="09062-127">The length, in bytes, of the *szKey* parameter, including the two terminating null characters.</span></span>

<span data-ttu-id="09062-128">*lDensity*</span><span class="sxs-lookup"><span data-stu-id="09062-128">*lDensity*</span></span>

<span data-ttu-id="09062-129">A densidade percentual da árvore inicial do índice B +.</span><span class="sxs-lookup"><span data-stu-id="09062-129">The percentage density of the initial index B+ tree.</span></span>

<span data-ttu-id="09062-130">Para obter mais informações sobre esse parâmetro, consulte a estrutura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="09062-130">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

### <a name="return-value"></a><span data-ttu-id="09062-131">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="09062-131">Return Value</span></span>

<span data-ttu-id="09062-132">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="09062-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="09062-133">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="09062-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09062-134">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="09062-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="09062-135">Significado</span><span class="sxs-lookup"><span data-stu-id="09062-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09062-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="09062-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="09062-137">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="09062-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09062-138">Para obter uma lista de erros adicionais que podem ser retornados pela função **JetCreateIndex** , consulte [JetCreateIndex2](./jetcreateindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="09062-138">For a list of additional errors that can be returned by the **JetCreateIndex** function, see [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="09062-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="09062-139">Remarks</span></span>

<span data-ttu-id="09062-140">Chamar a função **JetCreateIndex** é idêntico a chamar a função [JetCreateIndex2](./jetcreateindex2-function.md) com uma estrutura [JET_INDEXCREATE](./jet-indexcreate-structure.md) que contém as mesmas configurações que os parâmetros de **JetCreateIndex** e um parâmetro *cIndexCreate* igual a 1.</span><span class="sxs-lookup"><span data-stu-id="09062-140">Calling the **JetCreateIndex** function is identical to calling the [JetCreateIndex2](./jetcreateindex2-function.md) function with a [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure containing the same settings as the parameters of **JetCreateIndex**, and a *cIndexCreate* parameter equal to 1.</span></span> <span data-ttu-id="09062-141">Para os campos da estrutura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) que não têm parâmetros correspondentes em **JetCreateIndex**, é assumido um valor de 0.</span><span class="sxs-lookup"><span data-stu-id="09062-141">For the fields of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure that do not have corresponding parameters in **JetCreateIndex**, a value of 0 is assumed.</span></span>

<span data-ttu-id="09062-142">Observe que **JetCreateIndex** foi substituído pelo [JetCreateIndex2](./jetcreateindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="09062-142">Note that **JetCreateIndex** has been superseded by [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="09062-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09062-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09062-144">Cliente</span><span class="sxs-lookup"><span data-stu-id="09062-144">Client</span></span></p></td>
<td><p><span data-ttu-id="09062-145">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="09062-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09062-146">Servidor</span><span class="sxs-lookup"><span data-stu-id="09062-146">Server</span></span></p></td>
<td><p><span data-ttu-id="09062-147">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="09062-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09062-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09062-148">Header</span></span></p></td>
<td><p><span data-ttu-id="09062-149">É declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="09062-149">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09062-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09062-150">Library</span></span></p></td>
<td><p><span data-ttu-id="09062-151">Usa ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="09062-151">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09062-152">DLL</span><span class="sxs-lookup"><span data-stu-id="09062-152">DLL</span></span></p></td>
<td><p><span data-ttu-id="09062-153">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="09062-153">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09062-154">Unicode</span><span class="sxs-lookup"><span data-stu-id="09062-154">Unicode</span></span></p></td>
<td><p><span data-ttu-id="09062-155">É implementado como <strong>JetCreateIndexW</strong> (Unicode) e <strong>JetCreateIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="09062-155">Is implemented as <strong>JetCreateIndexW</strong> (Unicode) and <strong>JetCreateIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="09062-156">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="09062-156">See Also</span></span>

[<span data-ttu-id="09062-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="09062-157">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="09062-158">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="09062-158">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="09062-159">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="09062-159">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="09062-160">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="09062-160">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="09062-161">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="09062-161">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="09062-162">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="09062-162">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="09062-163">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="09062-163">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="09062-164">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="09062-164">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
