---
description: 'Saiba mais sobre: método API. JetDeleteIndex'
title: Método API. JetDeleteIndex
TOCTitle: 'JetDeleteIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeleteindex(v=EXCHG.10)
ms:contentKeyID: 55100682
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de04966aae4aee3f4ab7b14a846b898f55f887be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501516"
---
# <a name="apijetdeleteindex-method"></a><span data-ttu-id="c7e97-103">Método API. JetDeleteIndex</span><span class="sxs-lookup"><span data-stu-id="c7e97-103">Api.JetDeleteIndex method</span></span>

<span data-ttu-id="c7e97-104">Exclui um índice de uma tabela de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c7e97-104">Deletes an index from a database table.</span></span>

<span data-ttu-id="c7e97-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c7e97-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c7e97-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c7e97-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e97-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7e97-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As StringApi.JetDeleteIndex(sesid, tableid, _
    index)
```

``` csharp
public static void JetDeleteIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index
)
```

#### <a name="parameters"></a><span data-ttu-id="c7e97-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7e97-108">Parameters</span></span>

  - <span data-ttu-id="c7e97-109">sesid</span><span class="sxs-lookup"><span data-stu-id="c7e97-109">sesid</span></span>  
    <span data-ttu-id="c7e97-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c7e97-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c7e97-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c7e97-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c7e97-112">TableID</span><span class="sxs-lookup"><span data-stu-id="c7e97-112">tableid</span></span>  
    <span data-ttu-id="c7e97-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c7e97-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c7e97-114">Um cursor na tabela da qual excluir o índice.</span><span class="sxs-lookup"><span data-stu-id="c7e97-114">A cursor on the table to delete the index from.</span></span>

<!-- end list -->

  - <span data-ttu-id="c7e97-115">índice</span><span class="sxs-lookup"><span data-stu-id="c7e97-115">index</span></span>  
    <span data-ttu-id="c7e97-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c7e97-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c7e97-117">O nome do índice a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="c7e97-117">The name of the index to be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7e97-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7e97-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c7e97-119">Referência</span><span class="sxs-lookup"><span data-stu-id="c7e97-119">Reference</span></span>

[<span data-ttu-id="c7e97-120">Classe de API</span><span class="sxs-lookup"><span data-stu-id="c7e97-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c7e97-121">Membros da API</span><span class="sxs-lookup"><span data-stu-id="c7e97-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c7e97-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c7e97-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
