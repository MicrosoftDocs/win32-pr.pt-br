---
description: 'Saiba mais sobre: Construtor EsentMemoryException (cadeia de caracteres, JET_err)'
title: Construtor EsentMemoryException (cadeia de caracteres, JET_err)
TOCTitle: EsentMemoryException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102199
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60cdb6fda03695a4afb41d82e83aaeeb9415f421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783679"
---
# <a name="esentmemoryexception-constructor-string-jet_err"></a><span data-ttu-id="572b4-103">Construtor EsentMemoryException (cadeia de caracteres, JET_err)</span><span class="sxs-lookup"><span data-stu-id="572b4-103">EsentMemoryException constructor (String, JET_err)</span></span>

<span data-ttu-id="572b4-104">Inicializa uma nova instância da classe EsentMemoryException.</span><span class="sxs-lookup"><span data-stu-id="572b4-104">Initializes a new instance of the EsentMemoryException class.</span></span>

<span data-ttu-id="572b4-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="572b4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="572b4-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="572b4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="572b4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="572b4-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentMemoryException(description, _
    err)
```

``` csharp
protected EsentMemoryException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="572b4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="572b4-108">Parameters</span></span>

  - <span data-ttu-id="572b4-109">descrição</span><span class="sxs-lookup"><span data-stu-id="572b4-109">description</span></span>  
    <span data-ttu-id="572b4-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="572b4-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="572b4-111">A descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="572b4-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="572b4-112">erra</span><span class="sxs-lookup"><span data-stu-id="572b4-112">err</span></span>  
    <span data-ttu-id="572b4-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="572b4-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="572b4-114">O código de erro da exceção.</span><span class="sxs-lookup"><span data-stu-id="572b4-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="572b4-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="572b4-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="572b4-116">Referência</span><span class="sxs-lookup"><span data-stu-id="572b4-116">Reference</span></span>

[<span data-ttu-id="572b4-117">Classe EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="572b4-117">EsentMemoryException class</span></span>](./esentmemoryexception-class.md)

[<span data-ttu-id="572b4-118">Membros do EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="572b4-118">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="572b4-119">Sobrecarga de EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="572b4-119">EsentMemoryException overload</span></span>](./esentmemoryexception-constructor.md)

[<span data-ttu-id="572b4-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="572b4-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
