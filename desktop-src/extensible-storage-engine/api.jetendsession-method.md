---
description: 'Saiba mais sobre: método API. JetEndSession'
title: Método API. JetEndSession
TOCTitle: 'JetEndSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndSession(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.EndSessionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendsession(v=EXCHG.10)
ms:contentKeyID: 55100690
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10412f6b01b14d63557bf024d65975c271bbe31b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501513"
---
# <a name="apijetendsession-method"></a><span data-ttu-id="ecd86-103">Método API. JetEndSession</span><span class="sxs-lookup"><span data-stu-id="ecd86-103">Api.JetEndSession method</span></span>

<span data-ttu-id="ecd86-104">Encerra uma sessão.</span><span class="sxs-lookup"><span data-stu-id="ecd86-104">Ends a session.</span></span>

<span data-ttu-id="ecd86-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ecd86-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ecd86-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ecd86-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd86-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ecd86-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndSession ( _
    sesid As JET_SESID, _
    grbit As EndSessionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As EndSessionGrbitApi.JetEndSession(sesid, grbit)
```

``` csharp
public static void JetEndSession(
    JET_SESID sesid,
    EndSessionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ecd86-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ecd86-108">Parameters</span></span>

  - <span data-ttu-id="ecd86-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ecd86-109">sesid</span></span>  
    <span data-ttu-id="ecd86-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ecd86-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ecd86-111">A sessão a ser encerrada.</span><span class="sxs-lookup"><span data-stu-id="ecd86-111">The session to end.</span></span>

<!-- end list -->

  - <span data-ttu-id="ecd86-112">grbit</span><span class="sxs-lookup"><span data-stu-id="ecd86-112">grbit</span></span>  
    <span data-ttu-id="ecd86-113">Tipo: [Microsoft. ISAM. ESENT. Interop. EndSessionGrbit](./endsessiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ecd86-113">Type: [Microsoft.Isam.Esent.Interop.EndSessionGrbit](./endsessiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ecd86-114">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="ecd86-114">This parameter is not used.</span></span>

## <a name="see-also"></a><span data-ttu-id="ecd86-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecd86-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ecd86-116">Referência</span><span class="sxs-lookup"><span data-stu-id="ecd86-116">Reference</span></span>

[<span data-ttu-id="ecd86-117">Classe de API</span><span class="sxs-lookup"><span data-stu-id="ecd86-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ecd86-118">Membros da API</span><span class="sxs-lookup"><span data-stu-id="ecd86-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ecd86-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ecd86-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
