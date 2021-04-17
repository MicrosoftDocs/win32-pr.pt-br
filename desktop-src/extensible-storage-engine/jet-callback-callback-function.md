---
description: 'Saiba mais sobre: JET_CALLBACK função de retorno de chamada'
title: JET_CALLBACK função de retorno de chamada
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
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
ms.openlocfilehash: 5e6d26bd5e347757fce270d5f2c78ab471755c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768532"
---
# <a name="jet_callback-callback-function"></a><span data-ttu-id="155b0-103">JET_CALLBACK função de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="155b0-103">JET_CALLBACK Callback Function</span></span>


<span data-ttu-id="155b0-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="155b0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_callback-callback-function"></a><span data-ttu-id="155b0-105">JET_CALLBACK função de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="155b0-105">JET_CALLBACK Callback Function</span></span>

<span data-ttu-id="155b0-106">A função **JET_CALLBACK** é uma função de retorno de chamada de várias finalidades usada pelo mecanismo de banco de dados para informar o aplicativo de um evento que envolve a desfragmentação online e as notificações de estado do cursor.</span><span class="sxs-lookup"><span data-stu-id="155b0-106">The **JET_CALLBACK** function is a multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="155b0-107">Consulte [JET_CBTYP](./jet-cbtyp.md) para configurações específicas a serem usadas para os parâmetros dessa função, pois essas configurações serão diferentes dependendo da opção de **JET_CBTYP** selecionada para uso no parâmetro *CBTYP* .</span><span class="sxs-lookup"><span data-stu-id="155b0-107">See [JET_CBTYP](./jet-cbtyp.md) for specific settings to use for the parameters of this function, as these settings will differ depending upon the **JET_CBTYP** option that is selected for use in the *cbtyp* parameter.</span></span>

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a><span data-ttu-id="155b0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="155b0-108">Parameters</span></span>

<span data-ttu-id="155b0-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="155b0-109">*sesid*</span></span>

<span data-ttu-id="155b0-110">A sessão para a qual o retorno de chamada está sendo feito.</span><span class="sxs-lookup"><span data-stu-id="155b0-110">The session for which the callback is being made.</span></span>

<span data-ttu-id="155b0-111">*DBID*</span><span class="sxs-lookup"><span data-stu-id="155b0-111">*dbid*</span></span>

<span data-ttu-id="155b0-112">O banco de dados para o qual o retorno de chamada está sendo feito.</span><span class="sxs-lookup"><span data-stu-id="155b0-112">The database for which the callback is being made.</span></span>

<span data-ttu-id="155b0-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="155b0-113">*tableid*</span></span>

<span data-ttu-id="155b0-114">O cursor para o qual o retorno de chamada está sendo feito.</span><span class="sxs-lookup"><span data-stu-id="155b0-114">The cursor for which the callback is being made.</span></span>

<span data-ttu-id="155b0-115">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="155b0-115">*cbtyp*</span></span>

<span data-ttu-id="155b0-116">O ponto na operação em que o retorno de chamada está sendo feito.</span><span class="sxs-lookup"><span data-stu-id="155b0-116">The point in the operation at which the callback is being made.</span></span> <span data-ttu-id="155b0-117">Consulte [JET_CBTYP](./jet-cbtyp.md) para obter uma lista de valores e o significado dos parâmetros a seguir em cada caso.</span><span class="sxs-lookup"><span data-stu-id="155b0-117">See [JET_CBTYP](./jet-cbtyp.md) for a list of values and the meaning of the following parameters in each case.</span></span>

<span data-ttu-id="155b0-118">*pvArg1*</span><span class="sxs-lookup"><span data-stu-id="155b0-118">*pvArg1*</span></span>

<span data-ttu-id="155b0-119">Um parâmetro usado para se comunicar com o aplicativo usando o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="155b0-119">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="155b0-120">Consulte [JET_CBTYP](./jet-cbtyp.md) para obter informações sobre o uso desse parâmetro para cada retorno de chamada suportado pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="155b0-120">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="155b0-121">*pvArg2*</span><span class="sxs-lookup"><span data-stu-id="155b0-121">*pvArg2*</span></span>

<span data-ttu-id="155b0-122">Um parâmetro usado para se comunicar com o aplicativo usando o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="155b0-122">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="155b0-123">Consulte [JET_CBTYP](./jet-cbtyp.md) para obter informações sobre o uso desse parâmetro para cada retorno de chamada suportado pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="155b0-123">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="155b0-124">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="155b0-124">*pvContext*</span></span>

<span data-ttu-id="155b0-125">Um parâmetro usado para se comunicar com o aplicativo usando o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="155b0-125">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="155b0-126">Consulte [JET_CBTYP](./jet-cbtyp.md) para obter informações sobre o uso desse parâmetro para cada retorno de chamada suportado pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="155b0-126">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="155b0-127">*ulUnused*</span><span class="sxs-lookup"><span data-stu-id="155b0-127">*ulUnused*</span></span>

<span data-ttu-id="155b0-128">Um parâmetro usado para se comunicar com o aplicativo usando o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="155b0-128">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="155b0-129">Consulte [JET_CBTYP](./jet-cbtyp.md) para obter informações sobre o uso desse parâmetro para cada retorno de chamada suportado pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="155b0-129">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

#### <a name="return-value"></a><span data-ttu-id="155b0-130">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="155b0-130">Return Value</span></span>

<span data-ttu-id="155b0-131">A função retorna um dos [códigos de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="155b0-131">The function returns one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="155b0-132">Para obter informações sobre como retornar esses códigos como HRESULTs, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="155b0-132">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="155b0-133">Em caso de sucesso, a operação que emitiu o retorno de chamada pode continuar normalmente.</span><span class="sxs-lookup"><span data-stu-id="155b0-133">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="155b0-134">Em alguns casos, o retorno de chamada pode retornar um aviso que influencia essa operação.</span><span class="sxs-lookup"><span data-stu-id="155b0-134">In some cases, the callback may return a warning that influences that operation.</span></span> <span data-ttu-id="155b0-135">Consulte [JET_CBTYP](./jet-cbtyp.md) para obter informações sobre o uso desses avisos pela operação.</span><span class="sxs-lookup"><span data-stu-id="155b0-135">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of these warnings by the operation.</span></span>

<span data-ttu-id="155b0-136">Em caso de falha, a operação que emitiu o retorno de chamada pode continuar normalmente ou pode falhar.</span><span class="sxs-lookup"><span data-stu-id="155b0-136">On failure, the operation that issued the callback may proceed normally or may fail.</span></span> <span data-ttu-id="155b0-137">Consulte [JET_CBTYP](./jet-cbtyp.md) para obter informações sobre o uso do código de erro pela operação.</span><span class="sxs-lookup"><span data-stu-id="155b0-137">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of the error code by the operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="155b0-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="155b0-138">Remarks</span></span>

<span data-ttu-id="155b0-139">Se o retorno de chamada passar um cursor para o aplicativo, será importante saber que esse cursor está intencionalmente limitado a um conjunto menor de funcionalidade para evitar a recursão e outros ugliness.</span><span class="sxs-lookup"><span data-stu-id="155b0-139">If the callback passes a cursor to the application then it is important to know that this cursor is intentionally limited to a smaller set of functionality to avoid recursion and other ugliness.</span></span> <span data-ttu-id="155b0-140">As seguintes operações são permitidas:</span><span class="sxs-lookup"><span data-stu-id="155b0-140">The following operations are allowed:</span></span>

  - [<span data-ttu-id="155b0-141">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="155b0-141">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="155b0-142">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="155b0-142">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="155b0-143">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="155b0-143">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="155b0-144">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="155b0-144">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)

  - [<span data-ttu-id="155b0-145">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="155b0-145">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="155b0-146">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="155b0-146">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="155b0-147">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="155b0-147">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)

  - [<span data-ttu-id="155b0-148">JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="155b0-148">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)

  - [<span data-ttu-id="155b0-149">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="155b0-149">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)

  - [<span data-ttu-id="155b0-150">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="155b0-150">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)

  - [<span data-ttu-id="155b0-151">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="155b0-151">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="155b0-152">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="155b0-152">JetRegisterCallback</span></span>](./jetregistercallback-function.md)

  - [<span data-ttu-id="155b0-153">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="155b0-153">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="155b0-154">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="155b0-154">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="155b0-155">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="155b0-155">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="155b0-156">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="155b0-156">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="155b0-157">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="155b0-157">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="155b0-158">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="155b0-158">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="155b0-159">JetUnregisterCallback</span><span class="sxs-lookup"><span data-stu-id="155b0-159">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)

<span data-ttu-id="155b0-160">Ao projetar seu retorno de chamada, leve em conta que, mesmo com essas restrições, ainda é possível que o retorno de chamada falhe.</span><span class="sxs-lookup"><span data-stu-id="155b0-160">When you design your callback, take into account that even with these restrictions, it is still possible for the callback to fail.</span></span>

#### <a name="requirements"></a><span data-ttu-id="155b0-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="155b0-161">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="155b0-162"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="155b0-162"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="155b0-163">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="155b0-163">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="155b0-164"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="155b0-164"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="155b0-165">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="155b0-165">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="155b0-166"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="155b0-166"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="155b0-167">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="155b0-167">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="155b0-168">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="155b0-168">See Also</span></span>

[<span data-ttu-id="155b0-169">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="155b0-169">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="155b0-170">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="155b0-170">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="155b0-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="155b0-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="155b0-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="155b0-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="155b0-173">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="155b0-173">JET_CBTYP</span></span>](./jet-cbtyp.md)
