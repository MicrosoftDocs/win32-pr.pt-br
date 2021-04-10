---
description: 'Saiba mais sobre: função JetGetVersion'
title: Função JetGetVersion
TOCTitle: JetGetVersion Function
ms:assetid: f25c3639-ae2b-4357-9947-563ef3df72c6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294133(v=EXCHG.10)
ms:contentKeyID: 32765747
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetVersion
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38128358d814ea85cf087c270a65a3fada976e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171621"
---
# <a name="jetgetversion-function"></a><span data-ttu-id="49fa9-103">Função JetGetVersion</span><span class="sxs-lookup"><span data-stu-id="49fa9-103">JetGetVersion Function</span></span>


<span data-ttu-id="49fa9-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="49fa9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetversion-function"></a><span data-ttu-id="49fa9-105">Função JetGetVersion</span><span class="sxs-lookup"><span data-stu-id="49fa9-105">JetGetVersion Function</span></span>

<span data-ttu-id="49fa9-106">A função **JetGetVersion** recupera a versão do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="49fa9-106">The **JetGetVersion** function retrieves the version of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetVersion(
      __in          JET_SESID sesid,
      __out         unsigned long* pwVersion
    );
```

### <a name="parameters"></a><span data-ttu-id="49fa9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49fa9-107">Parameters</span></span>

<span data-ttu-id="49fa9-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="49fa9-108">*sesid*</span></span>

<span data-ttu-id="49fa9-109">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="49fa9-109">The session to use for this call.</span></span>

<span data-ttu-id="49fa9-110">*pwVersion*</span><span class="sxs-lookup"><span data-stu-id="49fa9-110">*pwVersion*</span></span>

<span data-ttu-id="49fa9-111">Um ponteiro para o número de versão do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="49fa9-111">A pointer to the version number of the database engine.</span></span>

### <a name="return-value"></a><span data-ttu-id="49fa9-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="49fa9-112">Return Value</span></span>

<span data-ttu-id="49fa9-113">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="49fa9-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="49fa9-114">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="49fa9-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49fa9-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="49fa9-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="49fa9-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="49fa9-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49fa9-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="49fa9-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="49fa9-118">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="49fa9-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49fa9-119">Se essa função for realizada com sucesso, a versão do mecanismo de banco de dados será recuperada.</span><span class="sxs-lookup"><span data-stu-id="49fa9-119">If this function succeeds, the version of the database engine is retrieved.</span></span>

<span data-ttu-id="49fa9-120">Não há modos de falha conhecidos.</span><span class="sxs-lookup"><span data-stu-id="49fa9-120">There are no known failure modes.</span></span>

#### <a name="requirements"></a><span data-ttu-id="49fa9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49fa9-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49fa9-122"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="49fa9-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="49fa9-123">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="49fa9-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49fa9-124"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="49fa9-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="49fa9-125">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="49fa9-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49fa9-126"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="49fa9-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="49fa9-127">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="49fa9-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49fa9-128"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="49fa9-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="49fa9-129">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="49fa9-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49fa9-130"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="49fa9-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="49fa9-131">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="49fa9-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="49fa9-132">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="49fa9-132">See Also</span></span>

[<span data-ttu-id="49fa9-133">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="49fa9-133">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="49fa9-134">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="49fa9-134">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="49fa9-135">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="49fa9-135">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="49fa9-136">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="49fa9-136">JET_SESID</span></span>](./jet-sesid.md)
