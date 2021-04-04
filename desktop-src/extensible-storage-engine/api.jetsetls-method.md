---
description: 'Saiba mais sobre: método API. JetSetLS'
title: Método API. JetSetLS
TOCTitle: 'JetSetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetls(v=EXCHG.10)
ms:contentKeyID: 55100808
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d11d0790bb1d9340c427fd1b836d927527c6ca63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171226"
---
# <a name="apijetsetls-method"></a><span data-ttu-id="20acc-103">Método API. JetSetLS</span><span class="sxs-lookup"><span data-stu-id="20acc-103">Api.JetSetLS method</span></span>

<span data-ttu-id="20acc-104">Permite que o aplicativo associe um identificador de contexto conhecido como armazenamento local com um cursor ou a tabela associada a esse cursor.</span><span class="sxs-lookup"><span data-stu-id="20acc-104">Enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="20acc-105">Esse identificador de contexto pode ser usado pelo aplicativo para armazenar dados auxiliares associados a um cursor ou tabela.</span><span class="sxs-lookup"><span data-stu-id="20acc-105">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="20acc-106">O aplicativo é notificado posteriormente usando um retorno de chamada de tempo de execução quando o identificador de contexto deve ser liberado.</span><span class="sxs-lookup"><span data-stu-id="20acc-106">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="20acc-107">Isso torna possível associar o estado alocado dinamicamente a um cursor ou tabela.</span><span class="sxs-lookup"><span data-stu-id="20acc-107">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="20acc-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="20acc-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="20acc-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="20acc-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="20acc-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20acc-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetSetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetSetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="20acc-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20acc-111">Parameters</span></span>

  - <span data-ttu-id="20acc-112">sesid</span><span class="sxs-lookup"><span data-stu-id="20acc-112">sesid</span></span>  
    <span data-ttu-id="20acc-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="20acc-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="20acc-114">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="20acc-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="20acc-115">TableID</span><span class="sxs-lookup"><span data-stu-id="20acc-115">tableid</span></span>  
    <span data-ttu-id="20acc-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="20acc-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="20acc-117">O cursor a ser usado.</span><span class="sxs-lookup"><span data-stu-id="20acc-117">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="20acc-118">ls</span><span class="sxs-lookup"><span data-stu-id="20acc-118">ls</span></span>  
    <span data-ttu-id="20acc-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="20acc-119">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="20acc-120">O identificador de contexto a ser associado à sessão ou ao cursor.</span><span class="sxs-lookup"><span data-stu-id="20acc-120">The context handle to be associated with the session or cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="20acc-121">grbit</span><span class="sxs-lookup"><span data-stu-id="20acc-121">grbit</span></span>  
    <span data-ttu-id="20acc-122">Tipo: [Microsoft. ISAM. ESENT. Interop. LsGrbit](./lsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="20acc-122">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="20acc-123">Definir opções.</span><span class="sxs-lookup"><span data-stu-id="20acc-123">Set options.</span></span>

## <a name="see-also"></a><span data-ttu-id="20acc-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="20acc-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="20acc-125">Referência</span><span class="sxs-lookup"><span data-stu-id="20acc-125">Reference</span></span>

[<span data-ttu-id="20acc-126">Classe de API</span><span class="sxs-lookup"><span data-stu-id="20acc-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="20acc-127">Membros da API</span><span class="sxs-lookup"><span data-stu-id="20acc-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="20acc-128">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="20acc-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
