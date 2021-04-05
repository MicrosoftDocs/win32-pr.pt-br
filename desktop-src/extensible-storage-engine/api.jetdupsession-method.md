---
description: 'Saiba mais sobre: método API. JetDupSession'
title: Método API. JetDupSession
TOCTitle: 'JetDupSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupSession(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupsession(v=EXCHG.10)
ms:contentKeyID: 55100689
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9013c3c99c1d6c6067386038ec4a51f37f978650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090151"
---
# <a name="apijetdupsession-method"></a><span data-ttu-id="85704-103">Método API. JetDupSession</span><span class="sxs-lookup"><span data-stu-id="85704-103">Api.JetDupSession method</span></span>

<span data-ttu-id="85704-104">Inicialize uma nova sessão do ESE na mesma instância do sesid fornecido.</span><span class="sxs-lookup"><span data-stu-id="85704-104">Initialize a new ESE session in the same instance as the given sesid.</span></span>

<span data-ttu-id="85704-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="85704-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="85704-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="85704-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="85704-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85704-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDupSession ( _
    sesid As JET_SESID, _
    <OutAttribute> ByRef newSesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESID
Dim newSesid As JET_SESIDApi.JetDupSession(sesid, newSesid)
```

``` csharp
public static void JetDupSession(
    JET_SESID sesid,
    out JET_SESID newSesid
)
```

#### <a name="parameters"></a><span data-ttu-id="85704-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85704-108">Parameters</span></span>

  - <span data-ttu-id="85704-109">sesid</span><span class="sxs-lookup"><span data-stu-id="85704-109">sesid</span></span>  
    <span data-ttu-id="85704-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="85704-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="85704-111">A sessão a ser duplicada.</span><span class="sxs-lookup"><span data-stu-id="85704-111">The session to duplicate.</span></span>

<!-- end list -->

  - <span data-ttu-id="85704-112">newSesid</span><span class="sxs-lookup"><span data-stu-id="85704-112">newSesid</span></span>  
    <span data-ttu-id="85704-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="85704-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="85704-114">Retorna a nova sessão.</span><span class="sxs-lookup"><span data-stu-id="85704-114">Returns the new session.</span></span>

## <a name="see-also"></a><span data-ttu-id="85704-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="85704-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="85704-116">Referência</span><span class="sxs-lookup"><span data-stu-id="85704-116">Reference</span></span>

[<span data-ttu-id="85704-117">Classe de API</span><span class="sxs-lookup"><span data-stu-id="85704-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="85704-118">Membros da API</span><span class="sxs-lookup"><span data-stu-id="85704-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="85704-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="85704-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
