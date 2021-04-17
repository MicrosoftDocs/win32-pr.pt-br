---
description: 'Saiba mais sobre a propriedade: JET_INSTANCE_INFO. szDatabaseFileName'
title: Propriedade JET_INSTANCE_INFO. szDatabaseFileName
TOCTitle: 'szDatabaseFileName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.szdatabasefilename(v=EXCHG.10)
ms:contentKeyID: 55103711
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_szDatabaseFileName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55414184fd25a90f3fbb57be8fb5d84264fde5dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761921"
---
# <a name="jet_instance_infoszdatabasefilename-property"></a><span data-ttu-id="5304b-103">Propriedade JET_INSTANCE_INFO. szDatabaseFileName</span><span class="sxs-lookup"><span data-stu-id="5304b-103">JET_INSTANCE_INFO.szDatabaseFileName property</span></span>

<span data-ttu-id="5304b-104">Obtém uma coleção de cadeias de caracteres, cada uma mantendo o nome de arquivo de um banco de dados anexado à instância do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5304b-104">Gets a collection of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="5304b-105">A matriz tem elementos cDatabases.</span><span class="sxs-lookup"><span data-stu-id="5304b-105">The array has cDatabases elements.</span></span>

<span data-ttu-id="5304b-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5304b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5304b-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5304b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5304b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5304b-108">Syntax</span></span>

``` vb
'Declaration
Public ReadOnly Property szDatabaseFileName As IList(Of String)
    Get
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As IList(Of String)

value = instance.szDatabaseFileName
```

``` csharp
public IList<string> szDatabaseFileName { get; }
```

#### <a name="property-value"></a><span data-ttu-id="5304b-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5304b-109">Property value</span></span>

<span data-ttu-id="5304b-110">Tipo: [System. Collections. Generic. IList](/dotnet/api/system.collections.generic.ilist-1)\<[String](/dotnet/api/system.string)\></span><span class="sxs-lookup"><span data-stu-id="5304b-110">Type: [System.Collections.Generic.IList](/dotnet/api/system.collections.generic.ilist-1)\<[String](/dotnet/api/system.string)\></span></span>  

## <a name="see-also"></a><span data-ttu-id="5304b-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="5304b-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5304b-112">Referência</span><span class="sxs-lookup"><span data-stu-id="5304b-112">Reference</span></span>

[<span data-ttu-id="5304b-113">Classe JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="5304b-113">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="5304b-114">Membros do JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="5304b-114">JET_INSTANCE_INFO members</span></span>](./jet-instance-info-members.md)

[<span data-ttu-id="5304b-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5304b-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
