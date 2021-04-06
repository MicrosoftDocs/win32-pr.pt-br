---
description: 'Saiba mais sobre: estrutura de JET_DBID'
title: Estrutura de JET_DBID
TOCTitle: JET_DBID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DBID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid(v=EXCHG.10)
ms:contentKeyID: 39515255
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e92373015b64593936ee8d447b619932d168157c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828766"
---
# <a name="jet_dbid-structure"></a><span data-ttu-id="da9b9-103">Estrutura de JET_DBID</span><span class="sxs-lookup"><span data-stu-id="da9b9-103">JET_DBID structure</span></span>

<span data-ttu-id="da9b9-104">Um JET_DBID contém o identificador para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="da9b9-104">A JET_DBID contains the handle to the database.</span></span> <span data-ttu-id="da9b9-105">Um identificador de banco de dados é usado para gerenciar o esquema de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="da9b9-105">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="da9b9-106">Ele também pode ser usado para gerenciar as tabelas dentro desse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="da9b9-106">It can also be used to manage the tables inside of that database.</span></span>

<span data-ttu-id="da9b9-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="da9b9-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="da9b9-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="da9b9-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="da9b9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="da9b9-109">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_DBID _
    Implements IEquatable(Of JET_DBID), IFormattable
'Usage
Dim instance As JET_DBID
```

``` csharp
public struct JET_DBID : IEquatable<JET_DBID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="da9b9-110">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="da9b9-110">Thread safety</span></span>

<span data-ttu-id="da9b9-111">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="da9b9-111">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="da9b9-112">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="da9b9-112">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="da9b9-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="da9b9-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="da9b9-114">Referência</span><span class="sxs-lookup"><span data-stu-id="da9b9-114">Reference</span></span>

[<span data-ttu-id="da9b9-115">Membros do JET_DBID</span><span class="sxs-lookup"><span data-stu-id="da9b9-115">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="da9b9-116">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="da9b9-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
