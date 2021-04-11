---
description: 'Saiba mais sobre: método API. JetRollback'
title: Método API. JetRollback
TOCTitle: 'JetRollback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRollback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrollback(v=EXCHG.10)
ms:contentKeyID: 55100794
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9144bade272ddaea7501be5622c7263268c0f1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296260"
---
# <a name="apijetrollback-method"></a><span data-ttu-id="c66da-103">Método API. JetRollback</span><span class="sxs-lookup"><span data-stu-id="c66da-103">Api.JetRollback method</span></span>

<span data-ttu-id="c66da-104">Desfaz as alterações feitas no estado do banco de dados e retorna ao último ponto de salvamento.</span><span class="sxs-lookup"><span data-stu-id="c66da-104">Undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="c66da-105">O JetRollback também fechará todos os cursores abertos durante o ponto de salvamento.</span><span class="sxs-lookup"><span data-stu-id="c66da-105">JetRollback will also close any cursors opened during the save point.</span></span> <span data-ttu-id="c66da-106">Se o ponto de salvamento mais externo for desfeito, a sessão sairá da transação.</span><span class="sxs-lookup"><span data-stu-id="c66da-106">If the outermost save point is undone, the session will exit the transaction.</span></span>

<span data-ttu-id="c66da-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c66da-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c66da-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c66da-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c66da-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c66da-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRollback ( _
    sesid As JET_SESID, _
    grbit As RollbackTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As RollbackTransactionGrbitApi.JetRollback(sesid, grbit)
```

``` csharp
public static void JetRollback(
    JET_SESID sesid,
    RollbackTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c66da-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c66da-110">Parameters</span></span>

  - <span data-ttu-id="c66da-111">sesid</span><span class="sxs-lookup"><span data-stu-id="c66da-111">sesid</span></span>  
    <span data-ttu-id="c66da-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c66da-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c66da-113">A sessão para a qual reverter a transação.</span><span class="sxs-lookup"><span data-stu-id="c66da-113">The session to rollback the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="c66da-114">grbit</span><span class="sxs-lookup"><span data-stu-id="c66da-114">grbit</span></span>  
    <span data-ttu-id="c66da-115">Tipo: [Microsoft. ISAM. ESENT. Interop. RollbackTransactionGrbit](./rollbacktransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c66da-115">Type: [Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit](./rollbacktransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c66da-116">Opções de reversão.</span><span class="sxs-lookup"><span data-stu-id="c66da-116">Rollback options.</span></span>

## <a name="see-also"></a><span data-ttu-id="c66da-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="c66da-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c66da-118">Referência</span><span class="sxs-lookup"><span data-stu-id="c66da-118">Reference</span></span>

[<span data-ttu-id="c66da-119">Classe de API</span><span class="sxs-lookup"><span data-stu-id="c66da-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c66da-120">Membros da API</span><span class="sxs-lookup"><span data-stu-id="c66da-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c66da-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c66da-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
