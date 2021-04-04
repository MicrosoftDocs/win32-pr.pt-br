---
description: 'Saiba mais sobre: método API. JetSetColumns'
title: Método API. JetSetColumns
TOCTitle: 'JetSetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_SETCOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumns(v=EXCHG.10)
ms:contentKeyID: 55100800
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 59d1d16a21996937357d0358625772a4b6712019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646963"
---
# <a name="apijetsetcolumns-method"></a><span data-ttu-id="43dc4-103">Método API. JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="43dc4-103">Api.JetSetColumns method</span></span>

<span data-ttu-id="43dc4-104">Permite que um aplicativo defina vários valores de coluna em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="43dc4-104">Allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="43dc4-105">Uma matriz de estruturas de [JET_SETCOLUMN](./jet-setcolumn-class.md) é usada para descrever o conjunto de valores de coluna a ser definido e para descrever os buffers de entrada para cada valor de coluna a ser definido.</span><span class="sxs-lookup"><span data-stu-id="43dc4-105">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

<span data-ttu-id="43dc4-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43dc4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43dc4-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43dc4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43dc4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43dc4-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Shared Function JetSetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    setcolumns As JET_SETCOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim setcolumns As JET_SETCOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumns(sesid, _
    tableid, setcolumns, numColumns)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public static JET_wrn JetSetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_SETCOLUMN[] setcolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="43dc4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43dc4-109">Parameters</span></span>

  - <span data-ttu-id="43dc4-110">sesid</span><span class="sxs-lookup"><span data-stu-id="43dc4-110">sesid</span></span>  
    <span data-ttu-id="43dc4-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43dc4-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="43dc4-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="43dc4-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="43dc4-113">TableID</span><span class="sxs-lookup"><span data-stu-id="43dc4-113">tableid</span></span>  
    <span data-ttu-id="43dc4-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43dc4-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="43dc4-115">O cursor no qual definir as colunas.</span><span class="sxs-lookup"><span data-stu-id="43dc4-115">The cursor to set the columns on.</span></span>

<!-- end list -->

  - <span data-ttu-id="43dc4-116">colunas</span><span class="sxs-lookup"><span data-stu-id="43dc4-116">setcolumns</span></span>  
    <span data-ttu-id="43dc4-117">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="43dc4-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="43dc4-118">Uma matriz de estruturas de [JET_SETCOLUMN](./jet-setcolumn-class.md) que descreve os dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="43dc4-118">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures describing the data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="43dc4-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="43dc4-119">numColumns</span></span>  
    <span data-ttu-id="43dc4-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="43dc4-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="43dc4-121">Número de entradas no parâmetro SetColumns.</span><span class="sxs-lookup"><span data-stu-id="43dc4-121">Number of entries in the setcolumns parameter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="43dc4-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43dc4-122">Return value</span></span>

<span data-ttu-id="43dc4-123">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="43dc4-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="43dc4-124">Um aviso.</span><span class="sxs-lookup"><span data-stu-id="43dc4-124">A warning.</span></span> <span data-ttu-id="43dc4-125">Se o último conjunto de colunas tiver um aviso, esse aviso será retornado do JetSetColumns em si.</span><span class="sxs-lookup"><span data-stu-id="43dc4-125">If the last column set has a warning, then this warning will be returned from JetSetColumns itself.</span></span>  

## <a name="see-also"></a><span data-ttu-id="43dc4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="43dc4-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43dc4-127">Referência</span><span class="sxs-lookup"><span data-stu-id="43dc4-127">Reference</span></span>

[<span data-ttu-id="43dc4-128">Classe de API</span><span class="sxs-lookup"><span data-stu-id="43dc4-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="43dc4-129">Membros da API</span><span class="sxs-lookup"><span data-stu-id="43dc4-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="43dc4-130">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="43dc4-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
