---
description: 'Saiba mais sobre: método API. JetEnumerateColumns'
title: Método API. JetEnumerateColumns
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9a9848d4470d54cc2a146098343b664c9bd3419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010422"
---
# <a name="apijetenumeratecolumns-method"></a><span data-ttu-id="5e89d-103">Método API. JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="5e89d-103">Api.JetEnumerateColumns method</span></span>

<span data-ttu-id="5e89d-104">Recupera com eficiência um conjunto de colunas e seus valores do registro atual de um cursor ou o buffer de cópia desse cursor.</span><span class="sxs-lookup"><span data-stu-id="5e89d-104">Efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="5e89d-105">As colunas e os valores recuperados podem ser restringidos por uma lista de IDs de coluna, números de itagSequence e outras características.</span><span class="sxs-lookup"><span data-stu-id="5e89d-105">The columns and values retrieved can be restricted by a list of column IDs, itagSequence numbers, and other characteristics.</span></span> <span data-ttu-id="5e89d-106">Essa API de recuperação de coluna é exclusiva, pois retorna informações na memória alocada dinamicamente que é obtida usando um retorno de chamada compatível de realocação fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5e89d-106">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided realloc compatible callback.</span></span> <span data-ttu-id="5e89d-107">Essa nova flexibilidade permite a recuperação eficiente de dados de coluna com características específicas (como tamanho e multiplicidade) que são desconhecidos para o chamador.</span><span class="sxs-lookup"><span data-stu-id="5e89d-107">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="5e89d-108">Isso elimina a necessidade de usar os modos de descoberta de JetRetrieveColumn para determinar essas características a fim de configurar uma chamada final para JetRetrieveColumn que recuperará com êxito os dados desejados.</span><span class="sxs-lookup"><span data-stu-id="5e89d-108">This eliminates the need for the use of the discovery modes of JetRetrieveColumn to determine those characteristics in order to setup a final call to JetRetrieveColumn that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="5e89d-109">Esta API não está em conformidade com CLS.</span><span class="sxs-lookup"><span data-stu-id="5e89d-109">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="5e89d-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5e89d-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5e89d-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5e89d-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5e89d-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e89d-112">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5e89d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e89d-113">Parameters</span></span>

  - <span data-ttu-id="5e89d-114">sesid</span><span class="sxs-lookup"><span data-stu-id="5e89d-114">sesid</span></span>  
    <span data-ttu-id="5e89d-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5e89d-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5e89d-116">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="5e89d-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e89d-117">TableID</span><span class="sxs-lookup"><span data-stu-id="5e89d-117">tableid</span></span>  
    <span data-ttu-id="5e89d-118">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5e89d-118">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5e89d-119">O cursor do qual recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="5e89d-119">The cursor to retrieve data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e89d-120">numColumnids</span><span class="sxs-lookup"><span data-stu-id="5e89d-120">numColumnids</span></span>  
    <span data-ttu-id="5e89d-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5e89d-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5e89d-122">Os números de JET_ENUMCOLUMNIDS.</span><span class="sxs-lookup"><span data-stu-id="5e89d-122">The numbers of JET_ENUMCOLUMNIDS.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e89d-123">columnids</span><span class="sxs-lookup"><span data-stu-id="5e89d-123">columnids</span></span>  
    <span data-ttu-id="5e89d-124">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="5e89d-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="5e89d-125">Uma matriz opcional de IDs de coluna, cada uma com uma matriz opcional de números itagSequence para enumerar.</span><span class="sxs-lookup"><span data-stu-id="5e89d-125">An optional array of column IDs, each with an optional array of itagSequence numbers to enumerate.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e89d-126">numColumnValues</span><span class="sxs-lookup"><span data-stu-id="5e89d-126">numColumnValues</span></span>  
    <span data-ttu-id="5e89d-127">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5e89d-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5e89d-128">Retorna o número de valores de coluna recuperados.</span><span class="sxs-lookup"><span data-stu-id="5e89d-128">Returns the number of column values retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e89d-129">columnValues</span><span class="sxs-lookup"><span data-stu-id="5e89d-129">columnValues</span></span>  
    <span data-ttu-id="5e89d-130">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="5e89d-130">Type: \[\]</span></span>  
    
    <span data-ttu-id="5e89d-131">Retorna os valores da coluna enumerada.</span><span class="sxs-lookup"><span data-stu-id="5e89d-131">Returns the enumerated column values.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e89d-132">allocator</span><span class="sxs-lookup"><span data-stu-id="5e89d-132">allocator</span></span>  
    <span data-ttu-id="5e89d-133">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="5e89d-133">Type: [Microsoft.Isam.Esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span></span>  
    
    <span data-ttu-id="5e89d-134">Retorno de chamada usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="5e89d-134">Callback used to allocate memory.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e89d-135">allocatorContext</span><span class="sxs-lookup"><span data-stu-id="5e89d-135">allocatorContext</span></span>  
    <span data-ttu-id="5e89d-136">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="5e89d-136">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="5e89d-137">Contexto para o retorno de chamada de alocação.</span><span class="sxs-lookup"><span data-stu-id="5e89d-137">Context for the allocation callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e89d-138">maxDataSize</span><span class="sxs-lookup"><span data-stu-id="5e89d-138">maxDataSize</span></span>  
    <span data-ttu-id="5e89d-139">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5e89d-139">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5e89d-140">Define um limite na quantidade de dados a serem retornados de uma coluna longa de texto longo ou binário longo.</span><span class="sxs-lookup"><span data-stu-id="5e89d-140">Sets a cap on the amount of data to return from a long text or long binary column.</span></span> <span data-ttu-id="5e89d-141">Esse parâmetro pode ser usado para impedir a enumeração de um valor de coluna muito grande.</span><span class="sxs-lookup"><span data-stu-id="5e89d-141">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e89d-142">grbit</span><span class="sxs-lookup"><span data-stu-id="5e89d-142">grbit</span></span>  
    <span data-ttu-id="5e89d-143">Tipo: [Microsoft. ISAM. ESENT. Interop. EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5e89d-143">Type: [Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5e89d-144">Recuperar opções.</span><span class="sxs-lookup"><span data-stu-id="5e89d-144">Retrieve options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5e89d-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e89d-145">Return value</span></span>

<span data-ttu-id="5e89d-146">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5e89d-146">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="5e89d-147">Um aviso ou sucesso.</span><span class="sxs-lookup"><span data-stu-id="5e89d-147">A warning or success.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5e89d-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e89d-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5e89d-149">Referência</span><span class="sxs-lookup"><span data-stu-id="5e89d-149">Reference</span></span>

[<span data-ttu-id="5e89d-150">Classe de API</span><span class="sxs-lookup"><span data-stu-id="5e89d-150">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5e89d-151">Membros da API</span><span class="sxs-lookup"><span data-stu-id="5e89d-151">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5e89d-152">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5e89d-152">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
