---
description: 'Saiba mais sobre: método API. JetGetVersion'
title: Método API. JetGetVersion
TOCTitle: 'JetGetVersion method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetVersion(Microsoft.Isam.Esent.Interop.JET_SESID,System.UInt32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetversion(v=EXCHG.10)
ms:contentKeyID: 55100744
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetVersion
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetVersion
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8860b21ec2b5db3841b866aa9c1c2cc7cff300aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502164"
---
# <a name="apijetgetversion-method"></a><span data-ttu-id="81d6a-103">Método API. JetGetVersion</span><span class="sxs-lookup"><span data-stu-id="81d6a-103">Api.JetGetVersion method</span></span>

<span data-ttu-id="81d6a-104">Recupera a versão do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="81d6a-104">Retrieves the version of the database engine.</span></span>

<span data-ttu-id="81d6a-105">Esta API não está em conformidade com CLS.</span><span class="sxs-lookup"><span data-stu-id="81d6a-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="81d6a-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="81d6a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="81d6a-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="81d6a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="81d6a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81d6a-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetVersion ( _
    sesid As JET_SESID, _
    <OutAttribute> ByRef version As UInteger _
)
'Usage
Dim sesid As JET_SESID
Dim version As UIntegerApi.JetGetVersion(sesid, version)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetVersion(
    JET_SESID sesid,
    out uint version
)
```

#### <a name="parameters"></a><span data-ttu-id="81d6a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81d6a-109">Parameters</span></span>

  - <span data-ttu-id="81d6a-110">sesid</span><span class="sxs-lookup"><span data-stu-id="81d6a-110">sesid</span></span>  
    <span data-ttu-id="81d6a-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="81d6a-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="81d6a-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="81d6a-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="81d6a-113">version</span><span class="sxs-lookup"><span data-stu-id="81d6a-113">version</span></span>  
    <span data-ttu-id="81d6a-114">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="81d6a-114">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="81d6a-115">Retorna o número de versão do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="81d6a-115">Returns the version number of the database engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="81d6a-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="81d6a-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="81d6a-117">Referência</span><span class="sxs-lookup"><span data-stu-id="81d6a-117">Reference</span></span>

[<span data-ttu-id="81d6a-118">Classe de API</span><span class="sxs-lookup"><span data-stu-id="81d6a-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="81d6a-119">Membros da API</span><span class="sxs-lookup"><span data-stu-id="81d6a-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="81d6a-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="81d6a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
