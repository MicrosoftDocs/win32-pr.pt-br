---
description: 'Saiba mais sobre: estrutura de JET_SESID'
title: Estrutura de JET_SESID
TOCTitle: JET_SESID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid(v=EXCHG.10)
ms:contentKeyID: 39516065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f547425f40b4336213ef69abe4bba07ee1baa513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758190"
---
# <a name="jet_sesid-structure"></a><span data-ttu-id="fbc9a-103">Estrutura de JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fbc9a-103">JET_SESID structure</span></span>

<span data-ttu-id="fbc9a-104">Um JET_SESID contém um identificador para a sessão a ser usado para chamadas para o JET APIr-.</span><span class="sxs-lookup"><span data-stu-id="fbc9a-104">A JET_SESID contains a handle to the session to use for calls to the JET APIr-.</span></span>

<span data-ttu-id="fbc9a-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fbc9a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fbc9a-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fbc9a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc9a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbc9a-107">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_SESID _
    Implements IEquatable(Of JET_SESID), IFormattable
'Usage
Dim instance As JET_SESID
```

``` csharp
public struct JET_SESID : IEquatable<JET_SESID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="fbc9a-108">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="fbc9a-108">Thread safety</span></span>

<span data-ttu-id="fbc9a-109">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="fbc9a-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="fbc9a-110">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="fbc9a-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="fbc9a-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbc9a-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fbc9a-112">Referência</span><span class="sxs-lookup"><span data-stu-id="fbc9a-112">Reference</span></span>

[<span data-ttu-id="fbc9a-113">Membros do JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fbc9a-113">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="fbc9a-114">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fbc9a-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
