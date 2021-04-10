---
description: 'Saiba mais sobre: Construtor de instância (cadeia de caracteres, Cadeia de caracteres)'
title: Construtor de instância (cadeia de caracteres, Cadeia de caracteres)
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02cb629cdfaba17ce9a137b52eb1a6d6fdbaa56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296495"
---
# <a name="instance-constructor-string-string"></a><span data-ttu-id="34e20-103">Construtor de instância (cadeia de caracteres, Cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="34e20-103">Instance constructor (String, String)</span></span>

<span data-ttu-id="34e20-104">Inicializa uma nova instância da classe de instância.</span><span class="sxs-lookup"><span data-stu-id="34e20-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="34e20-105">O JET_INSTANCE subjacente é alocado, mas não inicializado.</span><span class="sxs-lookup"><span data-stu-id="34e20-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="34e20-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34e20-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="34e20-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="34e20-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="34e20-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34e20-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
)
```

#### <a name="parameters"></a><span data-ttu-id="34e20-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34e20-109">Parameters</span></span>

  - <span data-ttu-id="34e20-110">name</span><span class="sxs-lookup"><span data-stu-id="34e20-110">name</span></span>  
    <span data-ttu-id="34e20-111">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="34e20-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="34e20-112">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="34e20-112">The name of the instance.</span></span> <span data-ttu-id="34e20-113">Essa cadeia de caracteres deve ser exclusiva em um determinado processo que hospeda o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="34e20-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="34e20-114">displayName</span><span class="sxs-lookup"><span data-stu-id="34e20-114">displayName</span></span>  
    <span data-ttu-id="34e20-115">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="34e20-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="34e20-116">Um nome de exibição para a instância.</span><span class="sxs-lookup"><span data-stu-id="34e20-116">A display name for the instance.</span></span> <span data-ttu-id="34e20-117">Isso será usado em entradas do EventLog.</span><span class="sxs-lookup"><span data-stu-id="34e20-117">This will be used in eventlog entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="34e20-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="34e20-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="34e20-119">Referência</span><span class="sxs-lookup"><span data-stu-id="34e20-119">Reference</span></span>

[<span data-ttu-id="34e20-120">Classe de instância</span><span class="sxs-lookup"><span data-stu-id="34e20-120">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="34e20-121">Membros da Instância </span><span class="sxs-lookup"><span data-stu-id="34e20-121">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="34e20-122">Sobrecarga de instância</span><span class="sxs-lookup"><span data-stu-id="34e20-122">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="34e20-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="34e20-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
