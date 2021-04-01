---
description: 'Saiba mais sobre: Construtor de instância (cadeia de caracteres, Cadeia de caracteres, TermGrbit)'
title: Construtor de instância (cadeia de caracteres, Cadeia de caracteres, TermGrbit)
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9cf90f9678db1074594c7772eb67d895a8a5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647600"
---
# <a name="instance-constructor-string-string-termgrbit"></a><span data-ttu-id="ebe27-103">Construtor de instância (cadeia de caracteres, Cadeia de caracteres, TermGrbit)</span><span class="sxs-lookup"><span data-stu-id="ebe27-103">Instance constructor (String, String, TermGrbit)</span></span>

<span data-ttu-id="ebe27-104">Inicializa uma nova instância da classe de instância.</span><span class="sxs-lookup"><span data-stu-id="ebe27-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="ebe27-105">O JET_INSTANCE subjacente é alocado, mas não inicializado.</span><span class="sxs-lookup"><span data-stu-id="ebe27-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="ebe27-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ebe27-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ebe27-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ebe27-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe27-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebe27-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ebe27-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebe27-109">Parameters</span></span>

  - <span data-ttu-id="ebe27-110">name</span><span class="sxs-lookup"><span data-stu-id="ebe27-110">name</span></span>  
    <span data-ttu-id="ebe27-111">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ebe27-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ebe27-112">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="ebe27-112">The name of the instance.</span></span> <span data-ttu-id="ebe27-113">Essa cadeia de caracteres deve ser exclusiva em um determinado processo que hospeda o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ebe27-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="ebe27-114">displayName</span><span class="sxs-lookup"><span data-stu-id="ebe27-114">displayName</span></span>  
    <span data-ttu-id="ebe27-115">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ebe27-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ebe27-116">Um nome de exibição para a instância.</span><span class="sxs-lookup"><span data-stu-id="ebe27-116">A display name for the instance.</span></span> <span data-ttu-id="ebe27-117">Isso será usado em entradas do EventLog.</span><span class="sxs-lookup"><span data-stu-id="ebe27-117">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="ebe27-118">termGrbit</span><span class="sxs-lookup"><span data-stu-id="ebe27-118">termGrbit</span></span>  
    <span data-ttu-id="ebe27-119">Tipo: [Microsoft. ISAM. ESENT. Interop. TermGrbit](./termgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ebe27-119">Type: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ebe27-120">O TermGrbit a ser usado em JetTerm hora.</span><span class="sxs-lookup"><span data-stu-id="ebe27-120">The TermGrbit to be used at JetTerm time.</span></span>

## <a name="see-also"></a><span data-ttu-id="ebe27-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebe27-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ebe27-122">Referência</span><span class="sxs-lookup"><span data-stu-id="ebe27-122">Reference</span></span>

[<span data-ttu-id="ebe27-123">Classe de instância</span><span class="sxs-lookup"><span data-stu-id="ebe27-123">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="ebe27-124">Membros da Instância </span><span class="sxs-lookup"><span data-stu-id="ebe27-124">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="ebe27-125">Sobrecarga de instância</span><span class="sxs-lookup"><span data-stu-id="ebe27-125">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="ebe27-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ebe27-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
