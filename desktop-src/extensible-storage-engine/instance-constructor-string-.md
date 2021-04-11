---
description: 'Saiba mais sobre: Construtor de instância (cadeia de caracteres)'
title: Construtor de instância (cadeia de caracteres)
TOCTitle: Instance constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103263
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
ms.openlocfilehash: 8cf184fc9b8d921b1d8bd1003b960bc65a6ffb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172235"
---
# <a name="instance-constructor-string"></a><span data-ttu-id="c9625-103">Construtor de instância (cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="c9625-103">Instance constructor (String)</span></span>

<span data-ttu-id="c9625-104">Inicializa uma nova instância da classe de instância.</span><span class="sxs-lookup"><span data-stu-id="c9625-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="c9625-105">O JET_INSTANCE subjacente é alocado, mas não inicializado.</span><span class="sxs-lookup"><span data-stu-id="c9625-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="c9625-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c9625-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c9625-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c9625-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c9625-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9625-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String _
)
'Usage
Dim name As String

Dim instance As New Instance(name)
```

``` csharp
public Instance(
    string name
)
```

#### <a name="parameters"></a><span data-ttu-id="c9625-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9625-109">Parameters</span></span>

  - <span data-ttu-id="c9625-110">name</span><span class="sxs-lookup"><span data-stu-id="c9625-110">name</span></span>  
    <span data-ttu-id="c9625-111">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c9625-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c9625-112">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="c9625-112">The name of the instance.</span></span> <span data-ttu-id="c9625-113">Essa cadeia de caracteres deve ser exclusiva em um determinado processo que hospeda o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c9625-113">This string must be unique within a given process hosting the database engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9625-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9625-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c9625-115">Referência</span><span class="sxs-lookup"><span data-stu-id="c9625-115">Reference</span></span>

[<span data-ttu-id="c9625-116">Classe de instância</span><span class="sxs-lookup"><span data-stu-id="c9625-116">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="c9625-117">Membros da Instância </span><span class="sxs-lookup"><span data-stu-id="c9625-117">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="c9625-118">Sobrecarga de instância</span><span class="sxs-lookup"><span data-stu-id="c9625-118">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="c9625-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c9625-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
