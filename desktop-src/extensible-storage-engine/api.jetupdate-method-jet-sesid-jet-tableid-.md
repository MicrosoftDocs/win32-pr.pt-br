---
description: 'Saiba mais sobre: método API. JetUpdate (JET_SESID, JET_TABLEID)'
title: Método API. JetUpdate (JET_SESID, JET_TABLEID)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100831
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
ms.openlocfilehash: f1875353e8a5b4a23302a5f008af2cfa42a89b11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297566"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid"></a><span data-ttu-id="6a5aa-103">Método API. JetUpdate (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="6a5aa-103">Api.JetUpdate method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="6a5aa-104">A função JetUpdate executa uma operação de atualização, incluindo a inserção de uma nova linha em uma tabela ou a atualização de uma linha existente.</span><span class="sxs-lookup"><span data-stu-id="6a5aa-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="6a5aa-105">A exclusão de uma linha de tabela é executada chamando [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="6a5aa-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="6a5aa-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a5aa-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6a5aa-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6a5aa-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a5aa-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a5aa-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetUpdate(sesid, tableid)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="6a5aa-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a5aa-109">Parameters</span></span>

  - <span data-ttu-id="6a5aa-110">sesid</span><span class="sxs-lookup"><span data-stu-id="6a5aa-110">sesid</span></span>  
    <span data-ttu-id="6a5aa-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6a5aa-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6a5aa-112">A sessão que iniciou a atualização.</span><span class="sxs-lookup"><span data-stu-id="6a5aa-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="6a5aa-113">TableID</span><span class="sxs-lookup"><span data-stu-id="6a5aa-113">tableid</span></span>  
    <span data-ttu-id="6a5aa-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6a5aa-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6a5aa-115">O cursor a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="6a5aa-115">The cursor to update.</span></span> <span data-ttu-id="6a5aa-116">Uma atualização deve ser preparada.</span><span class="sxs-lookup"><span data-stu-id="6a5aa-116">An update should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a5aa-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a5aa-117">Remarks</span></span>

<span data-ttu-id="6a5aa-118">JetUpdate é a etapa final na execução de uma inserção ou atualização.</span><span class="sxs-lookup"><span data-stu-id="6a5aa-118">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="6a5aa-119">A atualização é iniciada chamando [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) e, em seguida, chamando [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) uma ou mais vezes para definir o estado do registro.</span><span class="sxs-lookup"><span data-stu-id="6a5aa-119">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="6a5aa-120">Por fim, [JetUpdate (JET_SESID, JET_TABLEID, \[ \] Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) é chamado para concluir a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="6a5aa-120">Finally, [JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) is called to complete the update operation.</span></span> <span data-ttu-id="6a5aa-121">Os índices são atualizados somente por JetUpdate ou e não durante o JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="6a5aa-121">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a5aa-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a5aa-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a5aa-123">Referência</span><span class="sxs-lookup"><span data-stu-id="6a5aa-123">Reference</span></span>

[<span data-ttu-id="6a5aa-124">Classe de API</span><span class="sxs-lookup"><span data-stu-id="6a5aa-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6a5aa-125">Membros da API</span><span class="sxs-lookup"><span data-stu-id="6a5aa-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6a5aa-126">Sobrecarga de JetUpdate</span><span class="sxs-lookup"><span data-stu-id="6a5aa-126">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="6a5aa-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6a5aa-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
