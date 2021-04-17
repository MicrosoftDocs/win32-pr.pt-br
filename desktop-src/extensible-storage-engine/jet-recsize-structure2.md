---
description: 'Saiba mais sobre: estrutura de JET_RECSIZE'
title: Estrutura de JET_RECSIZE (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: JET_RECSIZE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize(v=EXCHG.10)
ms:contentKeyID: 39509765
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e741d91187a138d7b8d9a57d0c4e76f54979d99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760789"
---
# <a name="jet_recsize-structure"></a><span data-ttu-id="60c58-103">Estrutura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="60c58-103">JET_RECSIZE structure</span></span>

<span data-ttu-id="60c58-104">Usado por [JetGetRecordSize (JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) para retornar informações sobre os requisitos de uso de um registro no espaço de dados do usuário, o número de colunas definidas, o número de valores e o espaço de sobrecarga da estrutura do registro ESENT.</span><span class="sxs-lookup"><span data-stu-id="60c58-104">Used by [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESENT record structure overhead space.</span></span>

<span data-ttu-id="60c58-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="60c58-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="60c58-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="60c58-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="60c58-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="60c58-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_RECSIZE _
    Implements IEquatable(Of JET_RECSIZE)
'Usage
Dim instance As JET_RECSIZE
```

``` csharp
[SerializableAttribute]
public struct JET_RECSIZE : IEquatable<JET_RECSIZE>
```

## <a name="thread-safety"></a><span data-ttu-id="60c58-108">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="60c58-108">Thread safety</span></span>

<span data-ttu-id="60c58-109">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="60c58-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="60c58-110">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="60c58-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="60c58-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="60c58-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="60c58-112">Referência</span><span class="sxs-lookup"><span data-stu-id="60c58-112">Reference</span></span>

[<span data-ttu-id="60c58-113">Membros do JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="60c58-113">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="60c58-114">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="60c58-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
