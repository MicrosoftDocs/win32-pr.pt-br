---
description: 'Saiba mais sobre: método Windows8Api. JetCreateIndex4'
title: Método Windows8Api. JetCreateIndex4 (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetCreateIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcreateindex4(v=EXCHG.10)
ms:contentKeyID: 55104455
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc06fa47b8463c6c3b731a7e0e06b7ba13ae687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090983"
---
# <a name="windows8apijetcreateindex4-method"></a><span data-ttu-id="66ac1-103">Método Windows8Api. JetCreateIndex4</span><span class="sxs-lookup"><span data-stu-id="66ac1-103">Windows8Api.JetCreateIndex4 method</span></span>

<span data-ttu-id="66ac1-104">Cria índices em dados em um banco de dado ESE.</span><span class="sxs-lookup"><span data-stu-id="66ac1-104">Creates indexes over data in an ESE database.</span></span>

<span data-ttu-id="66ac1-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="66ac1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="66ac1-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="66ac1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="66ac1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66ac1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerWindows8Api.JetCreateIndex4(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEXCREATE[] indexcreates,
    int numIndexCreates
)
```

#### <a name="parameters"></a><span data-ttu-id="66ac1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66ac1-108">Parameters</span></span>

  - <span data-ttu-id="66ac1-109">sesid</span><span class="sxs-lookup"><span data-stu-id="66ac1-109">sesid</span></span>  
    <span data-ttu-id="66ac1-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="66ac1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="66ac1-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="66ac1-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="66ac1-112">TableID</span><span class="sxs-lookup"><span data-stu-id="66ac1-112">tableid</span></span>  
    <span data-ttu-id="66ac1-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="66ac1-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="66ac1-114">A tabela na qual criar o índice.</span><span class="sxs-lookup"><span data-stu-id="66ac1-114">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="66ac1-115">indexcreates</span><span class="sxs-lookup"><span data-stu-id="66ac1-115">indexcreates</span></span>  
    <span data-ttu-id="66ac1-116">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="66ac1-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="66ac1-117">Matriz de objetos que descreve os índices a serem criados.</span><span class="sxs-lookup"><span data-stu-id="66ac1-117">Array of objects describing the indexes to be created.</span></span>

<!-- end list -->

  - <span data-ttu-id="66ac1-118">numIndexCreates</span><span class="sxs-lookup"><span data-stu-id="66ac1-118">numIndexCreates</span></span>  
    <span data-ttu-id="66ac1-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="66ac1-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="66ac1-120">Número de objetos de descrição do índice.</span><span class="sxs-lookup"><span data-stu-id="66ac1-120">Number of index description objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="66ac1-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="66ac1-121">Remarks</span></span>

<span data-ttu-id="66ac1-122">Ao criar vários índices (ou seja, com numIndexCreates maior que 1), esse método deve ser chamado fora de qualquer transação e com acesso exclusivo à tabela.</span><span class="sxs-lookup"><span data-stu-id="66ac1-122">When creating multiple indexes (i.e. with numIndexCreates greater than 1) this method MUST be called outside of any transactions and with exclusive access to the table.</span></span> <span data-ttu-id="66ac1-123">O JET_TABLEID retornado por "API. JetCreateTable" terá acesso de L2 exclusivas ou a tabela poderá ser aberta para acesso exclusivo, passando [DenyRead](./opentablegrbit-enumeration.md) para [JetOpenTable (JET_SESID, JET_DBID, Cadeia de caracteres, \[ \] Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md).</span><span class="sxs-lookup"><span data-stu-id="66ac1-123">The JET_TABLEID returned by "Api.JetCreateTable" will have exlusive access or the table can be opened for exclusive access by passing [DenyRead](./opentablegrbit-enumeration.md) to [JetOpenTable(JET_SESID, JET_DBID, String, \[\], Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="66ac1-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="66ac1-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="66ac1-125">Referência</span><span class="sxs-lookup"><span data-stu-id="66ac1-125">Reference</span></span>

[<span data-ttu-id="66ac1-126">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="66ac1-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="66ac1-127">Membros do Windows8Api</span><span class="sxs-lookup"><span data-stu-id="66ac1-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="66ac1-128">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="66ac1-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
