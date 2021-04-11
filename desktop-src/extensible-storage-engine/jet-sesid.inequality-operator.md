---
description: 'Saiba mais sobre: JET_SESID. Operador de desigualdade'
title: JET_SESID. Operador de desigualdade
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39514305
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Inequality
- Microsoft.Isam.Esent.Interop.JET_SESID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e42b5e21937ae8af4ccd04708520ece40558c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090125"
---
# <a name="jet_sesidinequality-operator"></a><span data-ttu-id="452cf-103">JET_SESID. Operador de desigualdade</span><span class="sxs-lookup"><span data-stu-id="452cf-103">JET_SESID.Inequality operator</span></span>

<span data-ttu-id="452cf-104">Determina se duas instâncias especificadas do JET_SESID não são iguais.</span><span class="sxs-lookup"><span data-stu-id="452cf-104">Determines whether two specified instances of JET_SESID are not equal.</span></span>

<span data-ttu-id="452cf-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="452cf-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="452cf-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="452cf-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="452cf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="452cf-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_SESID, _
    rhs As JET_SESID _
) As Boolean
'Usage
Dim lhs As JET_SESID
Dim rhs As JET_SESID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_SESID lhs,
    JET_SESID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="452cf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="452cf-108">Parameters</span></span>

  - <span data-ttu-id="452cf-109">lhs</span><span class="sxs-lookup"><span data-stu-id="452cf-109">lhs</span></span>  
    <span data-ttu-id="452cf-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="452cf-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="452cf-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="452cf-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="452cf-112">rhs</span><span class="sxs-lookup"><span data-stu-id="452cf-112">rhs</span></span>  
    <span data-ttu-id="452cf-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="452cf-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="452cf-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="452cf-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="452cf-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="452cf-115">Return value</span></span>

<span data-ttu-id="452cf-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="452cf-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="452cf-117">True se as duas instâncias não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="452cf-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="452cf-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="452cf-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="452cf-119">Referência</span><span class="sxs-lookup"><span data-stu-id="452cf-119">Reference</span></span>

[<span data-ttu-id="452cf-120">Estrutura de JET_SESID</span><span class="sxs-lookup"><span data-stu-id="452cf-120">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="452cf-121">Membros do JET_SESID</span><span class="sxs-lookup"><span data-stu-id="452cf-121">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="452cf-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="452cf-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
