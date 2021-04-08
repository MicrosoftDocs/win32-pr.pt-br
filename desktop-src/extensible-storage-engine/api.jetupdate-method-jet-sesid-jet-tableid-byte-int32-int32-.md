---
description: 'Saiba mais sobre: método API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)'
title: Método API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c85e424fc9b672944801da3d03cbaff0ca48017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827439"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a><span data-ttu-id="dd2fb-103">Método API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="dd2fb-103">Api.JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)</span></span>

<span data-ttu-id="dd2fb-104">A função JetUpdate executa uma operação de atualização, incluindo a inserção de uma nova linha em uma tabela ou a atualização de uma linha existente.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="dd2fb-105">A exclusão de uma linha de tabela é executada chamando [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="dd2fb-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="dd2fb-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dd2fb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dd2fb-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dd2fb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2fb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd2fb-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="dd2fb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd2fb-109">Parameters</span></span>

  - <span data-ttu-id="dd2fb-110">sesid</span><span class="sxs-lookup"><span data-stu-id="dd2fb-110">sesid</span></span>  
    <span data-ttu-id="dd2fb-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dd2fb-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="dd2fb-112">A sessão que iniciou a atualização.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="dd2fb-113">TableID</span><span class="sxs-lookup"><span data-stu-id="dd2fb-113">tableid</span></span>  
    <span data-ttu-id="dd2fb-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dd2fb-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="dd2fb-115">O cursor a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-115">The cursor to update.</span></span> <span data-ttu-id="dd2fb-116">Uma atualização deve ser preparada.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="dd2fb-117">indicador</span><span class="sxs-lookup"><span data-stu-id="dd2fb-117">bookmark</span></span>  
    <span data-ttu-id="dd2fb-118">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="dd2fb-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="dd2fb-119">Retorna o indicador do registro atualizado.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="dd2fb-120">Isso pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="dd2fb-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="dd2fb-121">bookmarkSize</span></span>  
    <span data-ttu-id="dd2fb-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="dd2fb-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="dd2fb-123">O tamanho do buffer do indicador.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="dd2fb-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="dd2fb-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="dd2fb-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="dd2fb-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="dd2fb-126">Retorna o tamanho real do indicador.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-126">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd2fb-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd2fb-127">Remarks</span></span>

<span data-ttu-id="dd2fb-128">JetUpdate é a etapa final na execução de uma inserção ou atualização.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-128">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="dd2fb-129">A atualização é iniciada chamando [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) e, em seguida, chamando [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) uma ou mais vezes para definir o estado do registro.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-129">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="dd2fb-130">Por fim, JetUpdate (JET_SESID, JET_TABLEID, \[ \] Int32, Int32) é chamado para concluir a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-130">Finally, JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32) is called to complete the update operation.</span></span> <span data-ttu-id="dd2fb-131">Os índices são atualizados somente por JetUpdate ou e não durante o JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-131">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd2fb-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd2fb-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dd2fb-133">Referência</span><span class="sxs-lookup"><span data-stu-id="dd2fb-133">Reference</span></span>

[<span data-ttu-id="dd2fb-134">Classe de API</span><span class="sxs-lookup"><span data-stu-id="dd2fb-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="dd2fb-135">Membros da API</span><span class="sxs-lookup"><span data-stu-id="dd2fb-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="dd2fb-136">Sobrecarga de JetUpdate</span><span class="sxs-lookup"><span data-stu-id="dd2fb-136">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="dd2fb-137">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="dd2fb-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
