---
description: 'Saiba mais sobre: método API. JetGetLS'
title: Método API. JetGetLS
TOCTitle: 'JetGetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS@,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetls(v=EXCHG.10)
ms:contentKeyID: 55100734
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 611f92e21dad83121b4e4a6226838ac9ebce2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164374"
---
# <a name="apijetgetls-method"></a><span data-ttu-id="3225a-103">Método API. JetGetLS</span><span class="sxs-lookup"><span data-stu-id="3225a-103">Api.JetGetLS method</span></span>

<span data-ttu-id="3225a-104">Permite que o aplicativo recupere o identificador de contexto conhecido como armazenamento local associado a um cursor ou à tabela associada a esse cursor.</span><span class="sxs-lookup"><span data-stu-id="3225a-104">Enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="3225a-105">Esse identificador de contexto deve ter sido definido anteriormente usando [JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="3225a-105">This context handle must have been previously set using [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span></span> <span data-ttu-id="3225a-106">JetGetLS também pode ser usado para buscar simultaneamente o identificador de contexto atual para um cursor ou uma tabela e redefinir esse identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="3225a-106">JetGetLS can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="3225a-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3225a-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3225a-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3225a-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3225a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3225a-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetGetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetGetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3225a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3225a-110">Parameters</span></span>

  - <span data-ttu-id="3225a-111">sesid</span><span class="sxs-lookup"><span data-stu-id="3225a-111">sesid</span></span>  
    <span data-ttu-id="3225a-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3225a-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3225a-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="3225a-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3225a-114">TableID</span><span class="sxs-lookup"><span data-stu-id="3225a-114">tableid</span></span>  
    <span data-ttu-id="3225a-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3225a-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3225a-116">O cursor a ser usado.</span><span class="sxs-lookup"><span data-stu-id="3225a-116">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3225a-117">ls</span><span class="sxs-lookup"><span data-stu-id="3225a-117">ls</span></span>  
    <span data-ttu-id="3225a-118">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3225a-118">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="3225a-119">Retorna o identificador de contexto recuperado.</span><span class="sxs-lookup"><span data-stu-id="3225a-119">Returns the retrieved context handle.</span></span>

<!-- end list -->

  - <span data-ttu-id="3225a-120">grbit</span><span class="sxs-lookup"><span data-stu-id="3225a-120">grbit</span></span>  
    <span data-ttu-id="3225a-121">Tipo: [Microsoft. ISAM. ESENT. Interop. LsGrbit](./lsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3225a-121">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3225a-122">Recuperar opções.</span><span class="sxs-lookup"><span data-stu-id="3225a-122">Retrieve options.</span></span>

## <a name="see-also"></a><span data-ttu-id="3225a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3225a-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3225a-124">Referência</span><span class="sxs-lookup"><span data-stu-id="3225a-124">Reference</span></span>

[<span data-ttu-id="3225a-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="3225a-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3225a-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="3225a-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3225a-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3225a-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
