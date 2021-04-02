---
description: 'Saiba mais sobre: função JetIdle'
title: Função JetIdle
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0adf2845997b97eb93b39b779da4ad19bb9ee066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829240"
---
# <a name="jetidle-function"></a><span data-ttu-id="ac443-103">Função JetIdle</span><span class="sxs-lookup"><span data-stu-id="ac443-103">JetIdle Function</span></span>


<span data-ttu-id="ac443-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ac443-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetidle-function"></a><span data-ttu-id="ac443-105">Função JetIdle</span><span class="sxs-lookup"><span data-stu-id="ac443-105">JetIdle Function</span></span>

<span data-ttu-id="ac443-106">A função **JetIdle** está expirada e deve ser usada somente para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="ac443-106">The **JetIdle** function is defunct, and should only be used for testing purposes.</span></span> <span data-ttu-id="ac443-107">**JetIdle** pode ser usado para executar tarefas de limpeza ociosas ou verificar o status do repositório de versão no ESE.</span><span class="sxs-lookup"><span data-stu-id="ac443-107">**JetIdle** can be used to perform idle cleanup tasks or check the version store status in ESE.</span></span>

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="ac443-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac443-108">Parameters</span></span>

<span data-ttu-id="ac443-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ac443-109">*sesid*</span></span>

<span data-ttu-id="ac443-110">A sessão que será usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="ac443-110">The session that will be used for this call.</span></span>

<span data-ttu-id="ac443-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ac443-111">*grbit*</span></span>

<span data-ttu-id="ac443-112">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes bits:</span><span class="sxs-lookup"><span data-stu-id="ac443-112">A group of bits that contain the options to be used for this call, which include zero or more of the following bits:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac443-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ac443-113">Value</span></span></p></th>
<th><p><span data-ttu-id="ac443-114">Significado</span><span class="sxs-lookup"><span data-stu-id="ac443-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac443-115">JET_bitIdleCompact</span><span class="sxs-lookup"><span data-stu-id="ac443-115">JET_bitIdleCompact</span></span></p></td>
<td><p><span data-ttu-id="ac443-116">Dispara a limpeza do repositório de versão.</span><span class="sxs-lookup"><span data-stu-id="ac443-116">Triggers cleanup of the version store.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac443-117">JET_bitIdleFlushBuffers</span><span class="sxs-lookup"><span data-stu-id="ac443-117">JET_bitIdleFlushBuffers</span></span></p></td>
<td><p><span data-ttu-id="ac443-118">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="ac443-118">Reserved for future use.</span></span> <span data-ttu-id="ac443-119">Se esse sinalizador for especificado, a API retornará JET_errInvalidgrbit.</span><span class="sxs-lookup"><span data-stu-id="ac443-119">If this flag is specified, the API will return JET_errInvalidgrbit.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac443-120">JET_bitIdleStatus</span><span class="sxs-lookup"><span data-stu-id="ac443-120">JET_bitIdleStatus</span></span></p></td>
<td><p><span data-ttu-id="ac443-121">Retorna JET_wrnIdleFull se o repositório de versão for maior que metade cheio.</span><span class="sxs-lookup"><span data-stu-id="ac443-121">Returns JET_wrnIdleFull if version store is more than half full.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ac443-122">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ac443-122">Return Value</span></span>

<span data-ttu-id="ac443-123">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac443-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ac443-124">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ac443-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac443-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ac443-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="ac443-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac443-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac443-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ac443-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ac443-128">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="ac443-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac443-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ac443-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ac443-130">Um parâmetro <em>grbit</em> fornecido à API não era válido.</span><span class="sxs-lookup"><span data-stu-id="ac443-130">A <em>grbit</em> parameter that was provided to the API was not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ac443-131">Se essa função for realizada com sucesso, a operação apropriada será disparada ou um código de erro indicando o quão completo o repositório de versão está dependendo do *grbit* fornecido.</span><span class="sxs-lookup"><span data-stu-id="ac443-131">If this function succeeds, the appropriate operation will be triggered, or an error code indicating how full the version store is depending on the *grbit* provided.</span></span>

<span data-ttu-id="ac443-132">Se essa função falhar, a operação solicitada não será concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="ac443-132">If this function fails, the requested operation will not have completed successfully.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ac443-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac443-133">Remarks</span></span>

<span data-ttu-id="ac443-134">O repositório de versão mantém o mecanismo de isolamento de instantâneo do ESE.</span><span class="sxs-lookup"><span data-stu-id="ac443-134">The version store maintains ESE's snapshot isolation mechanism.</span></span> <span data-ttu-id="ac443-135">Se o repositório de versão for mais do que metade cheio, o programa poderá fechar transações de longa execução.</span><span class="sxs-lookup"><span data-stu-id="ac443-135">If the version store is more than half full, the program might close long-running transactions.</span></span> <span data-ttu-id="ac443-136">Se uma transação de longa execução esgotar o armazenamento de versão, o ESE interromperá a permissão de operações de gravação no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ac443-136">If a long-running transaction exhausts the version store, ESE will stop allowing write operations to the database.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ac443-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac443-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac443-138"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ac443-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ac443-139">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ac443-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac443-140"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ac443-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ac443-141">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ac443-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac443-142"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ac443-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ac443-143">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ac443-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac443-144"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="ac443-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ac443-145">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ac443-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac443-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ac443-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ac443-147">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ac443-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ac443-148">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ac443-148">See Also</span></span>

[<span data-ttu-id="ac443-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ac443-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ac443-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ac443-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ac443-151">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ac443-151">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ac443-152">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="ac443-152">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
