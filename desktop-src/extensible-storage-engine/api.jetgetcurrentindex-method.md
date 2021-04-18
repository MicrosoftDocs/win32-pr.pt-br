---
description: 'Saiba mais sobre: método API. JetGetCurrentIndex'
title: Método API. JetGetCurrentIndex
TOCTitle: 'JetGetCurrentIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcurrentindex(v=EXCHG.10)
ms:contentKeyID: 55100699
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bacc6973b1a105e128533a1116abdeb4c6cfafa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815597"
---
# <a name="apijetgetcurrentindex-method"></a><span data-ttu-id="7e83f-103">Método API. JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="7e83f-103">Api.JetGetCurrentIndex method</span></span>

<span data-ttu-id="7e83f-104">Ddetermines o nome do índice atual de um determinado cursor.</span><span class="sxs-lookup"><span data-stu-id="7e83f-104">Ddetermines the name of the current index of a given cursor.</span></span> <span data-ttu-id="7e83f-105">Esse nome também é usado posteriormente para selecionar novamente esse índice como o índice atual usando [JetSetCurrentIndex (JET_SESID, JET_TABLEID, String)](./api.jetsetcurrentindex-method.md).</span><span class="sxs-lookup"><span data-stu-id="7e83f-105">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex(JET_SESID, JET_TABLEID, String)](./api.jetsetcurrentindex-method.md).</span></span> <span data-ttu-id="7e83f-106">Ele também pode ser usado para descobrir as propriedades desse índice usando JetGetTableIndexInfo.</span><span class="sxs-lookup"><span data-stu-id="7e83f-106">It can also be used to discover the properties of that index using JetGetTableIndexInfo.</span></span>

<span data-ttu-id="7e83f-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e83f-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e83f-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7e83f-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e83f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e83f-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCurrentIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef indexName As String, _
    maxNameLength As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim maxNameLength As IntegerApi.JetGetCurrentIndex(sesid, tableid, _
    indexName, maxNameLength)
```

``` csharp
public static void JetGetCurrentIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out string indexName,
    int maxNameLength
)
```

#### <a name="parameters"></a><span data-ttu-id="7e83f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e83f-110">Parameters</span></span>

  - <span data-ttu-id="7e83f-111">sesid</span><span class="sxs-lookup"><span data-stu-id="7e83f-111">sesid</span></span>  
    <span data-ttu-id="7e83f-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e83f-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7e83f-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="7e83f-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e83f-114">TableID</span><span class="sxs-lookup"><span data-stu-id="7e83f-114">tableid</span></span>  
    <span data-ttu-id="7e83f-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e83f-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7e83f-116">O cursor para o qual obter o nome do índice.</span><span class="sxs-lookup"><span data-stu-id="7e83f-116">The cursor to get the index name for.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e83f-117">indexName</span><span class="sxs-lookup"><span data-stu-id="7e83f-117">indexName</span></span>  
    <span data-ttu-id="7e83f-118">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7e83f-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7e83f-119">Retorna o nome do índice.</span><span class="sxs-lookup"><span data-stu-id="7e83f-119">Returns the name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e83f-120">maxNameLength</span><span class="sxs-lookup"><span data-stu-id="7e83f-120">maxNameLength</span></span>  
    <span data-ttu-id="7e83f-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7e83f-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7e83f-122">O comprimento máximo do nome do índice.</span><span class="sxs-lookup"><span data-stu-id="7e83f-122">The maximum length of the index name.</span></span> <span data-ttu-id="7e83f-123">Os nomes de índice não têm mais de [NameMost](./systemparameters.namemost-field.md) caracteres.</span><span class="sxs-lookup"><span data-stu-id="7e83f-123">Index names are no more than [NameMost](./systemparameters.namemost-field.md) characters.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e83f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e83f-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e83f-125">Referência</span><span class="sxs-lookup"><span data-stu-id="7e83f-125">Reference</span></span>

[<span data-ttu-id="7e83f-126">Classe de API</span><span class="sxs-lookup"><span data-stu-id="7e83f-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7e83f-127">Membros da API</span><span class="sxs-lookup"><span data-stu-id="7e83f-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7e83f-128">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7e83f-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
