---
description: 'Saiba mais sobre: método API. JetCommitTransaction'
title: Método API. JetCommitTransaction
TOCTitle: 'JetCommitTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcommittransaction(v=EXCHG.10)
ms:contentKeyID: 55100665
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edf0799af53c3da422f92f981f7a28ee7a283d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780699"
---
# <a name="apijetcommittransaction-method"></a><span data-ttu-id="6c833-103">Método API. JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="6c833-103">Api.JetCommitTransaction method</span></span>

<span data-ttu-id="6c833-104">Confirma as alterações feitas no estado do banco de dados durante o ponto de salvamento atual e os migra para o ponto de salvamento anterior.</span><span class="sxs-lookup"><span data-stu-id="6c833-104">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="6c833-105">Se o ponto de salvamento mais externo for confirmado, as alterações feitas durante esse ponto de salvamento serão confirmadas no estado do banco de dados e a sessão sairá da transação.</span><span class="sxs-lookup"><span data-stu-id="6c833-105">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="6c833-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6c833-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6c833-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6c833-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6c833-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c833-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCommitTransaction ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbitApi.JetCommitTransaction(sesid, _
    grbit)
```

``` csharp
public static void JetCommitTransaction(
    JET_SESID sesid,
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="6c833-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c833-109">Parameters</span></span>

  - <span data-ttu-id="6c833-110">sesid</span><span class="sxs-lookup"><span data-stu-id="6c833-110">sesid</span></span>  
    <span data-ttu-id="6c833-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6c833-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6c833-112">A sessão para a qual confirmar a transação.</span><span class="sxs-lookup"><span data-stu-id="6c833-112">The session to commit the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c833-113">grbit</span><span class="sxs-lookup"><span data-stu-id="6c833-113">grbit</span></span>  
    <span data-ttu-id="6c833-114">Tipo: [Microsoft. ISAM. ESENT. Interop. CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6c833-114">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6c833-115">Opções de confirmação.</span><span class="sxs-lookup"><span data-stu-id="6c833-115">Commit options.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c833-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c833-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c833-117">Referência</span><span class="sxs-lookup"><span data-stu-id="6c833-117">Reference</span></span>

[<span data-ttu-id="6c833-118">Classe de API</span><span class="sxs-lookup"><span data-stu-id="6c833-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6c833-119">Membros da API</span><span class="sxs-lookup"><span data-stu-id="6c833-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6c833-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6c833-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
