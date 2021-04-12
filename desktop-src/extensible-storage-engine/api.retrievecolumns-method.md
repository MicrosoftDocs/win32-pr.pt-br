---
description: 'Saiba mais sobre: método API. RetrieveColumns'
title: Método API. RetrieveColumns
TOCTitle: 'RetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100867
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c981ad8b8e90db10bb8735aa349315b769e6641f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501216"
---
# <a name="apiretrievecolumns-method"></a><span data-ttu-id="38c87-103">Método API. RetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="38c87-103">Api.RetrieveColumns method</span></span>

<span data-ttu-id="38c87-104">Recupera colunas em objetos Columnvalue.</span><span class="sxs-lookup"><span data-stu-id="38c87-104">Retrieves columns into ColumnValue objects.</span></span>

<span data-ttu-id="38c87-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="38c87-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="38c87-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="38c87-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="38c87-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38c87-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub RetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.RetrieveColumns(sesid, tableid, _
    values)
```

``` csharp
public static void RetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a><span data-ttu-id="38c87-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38c87-108">Parameters</span></span>

  - <span data-ttu-id="38c87-109">sesid</span><span class="sxs-lookup"><span data-stu-id="38c87-109">sesid</span></span>  
    <span data-ttu-id="38c87-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="38c87-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="38c87-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="38c87-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="38c87-112">TableID</span><span class="sxs-lookup"><span data-stu-id="38c87-112">tableid</span></span>  
    <span data-ttu-id="38c87-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="38c87-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="38c87-114">O cursor recupera os dados do.</span><span class="sxs-lookup"><span data-stu-id="38c87-114">The cursor retrieve the data from.</span></span> <span data-ttu-id="38c87-115">O cursor deve ser posicionado em um registro.</span><span class="sxs-lookup"><span data-stu-id="38c87-115">The cursor should be positioned on a record.</span></span>

<!-- end list -->

  - <span data-ttu-id="38c87-116">valores</span><span class="sxs-lookup"><span data-stu-id="38c87-116">values</span></span>  
    <span data-ttu-id="38c87-117">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="38c87-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="38c87-118">Os valores a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="38c87-118">The values to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="38c87-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="38c87-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="38c87-120">Referência</span><span class="sxs-lookup"><span data-stu-id="38c87-120">Reference</span></span>

[<span data-ttu-id="38c87-121">Classe de API</span><span class="sxs-lookup"><span data-stu-id="38c87-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="38c87-122">Membros da API</span><span class="sxs-lookup"><span data-stu-id="38c87-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="38c87-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="38c87-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
