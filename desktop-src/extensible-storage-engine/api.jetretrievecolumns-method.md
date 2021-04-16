---
description: 'Saiba mais sobre: método API. JetRetrieveColumns'
title: Método API. JetRetrieveColumns
TOCTitle: 'JetRetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100797
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3fd4db2ce8cbcad5f74db7d4c95363aa68e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765736"
---
# <a name="apijetretrievecolumns-method"></a><span data-ttu-id="7e1ef-103">Método API. JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="7e1ef-103">Api.JetRetrieveColumns method</span></span>

<span data-ttu-id="7e1ef-104">Recupera vários valores de coluna do registro atual em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="7e1ef-104">Retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="7e1ef-105">Uma matriz de estruturas de JET_RETRIEVECOLUMN é usada para descrever o conjunto de valores de coluna a serem recuperados e para descrever os buffers de saída para cada valor de coluna a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="7e1ef-105">An array of JET_RETRIEVECOLUMN structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

<span data-ttu-id="7e1ef-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e1ef-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e1ef-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7e1ef-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e1ef-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e1ef-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    retrievecolumns As JET_RETRIEVECOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim retrievecolumns As JET_RETRIEVECOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumns(sesid, _
    tableid, retrievecolumns, numColumns)
```

``` csharp
public static JET_wrn JetRetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RETRIEVECOLUMN[] retrievecolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="7e1ef-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e1ef-109">Parameters</span></span>

  - <span data-ttu-id="7e1ef-110">sesid</span><span class="sxs-lookup"><span data-stu-id="7e1ef-110">sesid</span></span>  
    <span data-ttu-id="7e1ef-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e1ef-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7e1ef-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="7e1ef-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e1ef-113">TableID</span><span class="sxs-lookup"><span data-stu-id="7e1ef-113">tableid</span></span>  
    <span data-ttu-id="7e1ef-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e1ef-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7e1ef-115">O cursor do qual recuperar os dados.</span><span class="sxs-lookup"><span data-stu-id="7e1ef-115">The cursor to retrieve the data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e1ef-116">retrievecolumns</span><span class="sxs-lookup"><span data-stu-id="7e1ef-116">retrievecolumns</span></span>  
    <span data-ttu-id="7e1ef-117">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="7e1ef-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="7e1ef-118">Uma matriz de um ou mais objetos de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) que descrevem os dados a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="7e1ef-118">An array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) objects describing the data to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e1ef-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="7e1ef-119">numColumns</span></span>  
    <span data-ttu-id="7e1ef-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7e1ef-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7e1ef-121">O número de entradas na matriz de colunas.</span><span class="sxs-lookup"><span data-stu-id="7e1ef-121">The number of entries in the columns array.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7e1ef-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e1ef-122">Return value</span></span>

<span data-ttu-id="7e1ef-123">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7e1ef-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="7e1ef-124">Se qualquer coluna recuperada for truncada devido a um buffer de comprimento insuficiente, a API retornará [BufferTruncated](./jet-wrn-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="7e1ef-124">If any column retrieved is truncated due to an insufficient length buffer, then the API will return [BufferTruncated](./jet-wrn-enumeration.md).</span></span> <span data-ttu-id="7e1ef-125">No entanto, outros erros JET_wrnColumnNull são retornados somente no campo de erro do objeto [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) .</span><span class="sxs-lookup"><span data-stu-id="7e1ef-125">However other errors JET_wrnColumnNull are returned only in the error field of the [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) object.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7e1ef-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e1ef-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e1ef-127">Referência</span><span class="sxs-lookup"><span data-stu-id="7e1ef-127">Reference</span></span>

[<span data-ttu-id="7e1ef-128">Classe de API</span><span class="sxs-lookup"><span data-stu-id="7e1ef-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7e1ef-129">Membros da API</span><span class="sxs-lookup"><span data-stu-id="7e1ef-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7e1ef-130">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7e1ef-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
