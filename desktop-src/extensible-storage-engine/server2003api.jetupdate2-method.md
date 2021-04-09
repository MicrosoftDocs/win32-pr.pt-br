---
description: 'Saiba mais sobre: método Server2003Api. JetUpdate2'
title: Método Server2003Api. JetUpdate2 (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fff3687d42160df331bfe52660be232fe3b41d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089874"
---
# <a name="server2003apijetupdate2-method"></a><span data-ttu-id="52799-103">Método Server2003Api. JetUpdate2</span><span class="sxs-lookup"><span data-stu-id="52799-103">Server2003Api.JetUpdate2 method</span></span>

<span data-ttu-id="52799-104">A função JetUpdate executa uma operação de atualização, incluindo a inserção de uma nova linha em uma tabela ou a atualização de uma linha existente.</span><span class="sxs-lookup"><span data-stu-id="52799-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="52799-105">A exclusão de uma linha de tabela é executada chamando [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="52799-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="52799-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="52799-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="52799-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="52799-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="52799-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52799-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="52799-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52799-109">Parameters</span></span>

  - <span data-ttu-id="52799-110">sesid</span><span class="sxs-lookup"><span data-stu-id="52799-110">sesid</span></span>  
    <span data-ttu-id="52799-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="52799-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="52799-112">A sessão que iniciou a atualização.</span><span class="sxs-lookup"><span data-stu-id="52799-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="52799-113">TableID</span><span class="sxs-lookup"><span data-stu-id="52799-113">tableid</span></span>  
    <span data-ttu-id="52799-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="52799-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="52799-115">O cursor a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="52799-115">The cursor to update.</span></span> <span data-ttu-id="52799-116">Uma atualização deve ser preparada.</span><span class="sxs-lookup"><span data-stu-id="52799-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="52799-117">indicador</span><span class="sxs-lookup"><span data-stu-id="52799-117">bookmark</span></span>  
    <span data-ttu-id="52799-118">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="52799-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="52799-119">Retorna o indicador do registro atualizado.</span><span class="sxs-lookup"><span data-stu-id="52799-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="52799-120">Isso pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="52799-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="52799-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="52799-121">bookmarkSize</span></span>  
    <span data-ttu-id="52799-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="52799-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="52799-123">O tamanho do buffer do indicador.</span><span class="sxs-lookup"><span data-stu-id="52799-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="52799-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="52799-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="52799-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="52799-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="52799-126">Retorna o tamanho real do indicador.</span><span class="sxs-lookup"><span data-stu-id="52799-126">Returns the actual size of the bookmark.</span></span>

<!-- end list -->

  - <span data-ttu-id="52799-127">grbit</span><span class="sxs-lookup"><span data-stu-id="52799-127">grbit</span></span>  
    <span data-ttu-id="52799-128">Tipo: [Microsoft. ISAM. ESENT. Interop. Server2003. UpdateGrbit](./updategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="52799-128">Type: [Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit](./updategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="52799-129">Opções de atualização.</span><span class="sxs-lookup"><span data-stu-id="52799-129">Update options.</span></span>

## <a name="remarks"></a><span data-ttu-id="52799-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="52799-130">Remarks</span></span>

<span data-ttu-id="52799-131">JetUpdate é a etapa final na execução de uma inserção ou atualização.</span><span class="sxs-lookup"><span data-stu-id="52799-131">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="52799-132">A atualização é iniciada chamando [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) e, em seguida, chamando [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) uma ou mais vezes para definir o estado do registro.</span><span class="sxs-lookup"><span data-stu-id="52799-132">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="52799-133">Por fim, JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, UpdateGrbit) é chamado para concluir a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="52799-133">Finally, JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit) is called to complete the update operation.</span></span> <span data-ttu-id="52799-134">Os índices são atualizados somente por JetUpdate ou e não durante o JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="52799-134">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="52799-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="52799-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="52799-136">Referência</span><span class="sxs-lookup"><span data-stu-id="52799-136">Reference</span></span>

[<span data-ttu-id="52799-137">Classe Server2003Api</span><span class="sxs-lookup"><span data-stu-id="52799-137">Server2003Api class</span></span>](./server2003api-class.md)

[<span data-ttu-id="52799-138">Membros do Server2003Api</span><span class="sxs-lookup"><span data-stu-id="52799-138">Server2003Api members</span></span>](./server2003api-members.md)

[<span data-ttu-id="52799-139">Namespace Microsoft. ISAM. ESENT. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="52799-139">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
