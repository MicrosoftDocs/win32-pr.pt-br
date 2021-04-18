---
description: 'Saiba mais sobre: Construtor EsentStateException (cadeia de caracteres, JET_err)'
title: Construtor EsentStateException (cadeia de caracteres, JET_err)
TOCTitle: EsentStateException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentStateException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102995
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 611671bb488d4804fd31569f15ab89e3ddfed462
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798015"
---
# <a name="esentstateexception-constructor-string-jet_err"></a><span data-ttu-id="b8fb0-103">Construtor EsentStateException (cadeia de caracteres, JET_err)</span><span class="sxs-lookup"><span data-stu-id="b8fb0-103">EsentStateException constructor (String, JET_err)</span></span>

<span data-ttu-id="b8fb0-104">Inicializa uma nova instância da classe EsentStateException.</span><span class="sxs-lookup"><span data-stu-id="b8fb0-104">Initializes a new instance of the EsentStateException class.</span></span>

<span data-ttu-id="b8fb0-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8fb0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b8fb0-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b8fb0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8fb0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8fb0-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentStateException(description, _
    err)
```

``` csharp
protected EsentStateException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="b8fb0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8fb0-108">Parameters</span></span>

  - <span data-ttu-id="b8fb0-109">descrição</span><span class="sxs-lookup"><span data-stu-id="b8fb0-109">description</span></span>  
    <span data-ttu-id="b8fb0-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b8fb0-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b8fb0-111">A descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="b8fb0-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8fb0-112">erra</span><span class="sxs-lookup"><span data-stu-id="b8fb0-112">err</span></span>  
    <span data-ttu-id="b8fb0-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b8fb0-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="b8fb0-114">O código de erro da exceção.</span><span class="sxs-lookup"><span data-stu-id="b8fb0-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8fb0-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8fb0-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8fb0-116">Referência</span><span class="sxs-lookup"><span data-stu-id="b8fb0-116">Reference</span></span>

[<span data-ttu-id="b8fb0-117">Classe EsentStateException</span><span class="sxs-lookup"><span data-stu-id="b8fb0-117">EsentStateException class</span></span>](./esentstateexception-class.md)

[<span data-ttu-id="b8fb0-118">Membros do EsentStateException</span><span class="sxs-lookup"><span data-stu-id="b8fb0-118">EsentStateException members</span></span>](./esentstateexception-members.md)

[<span data-ttu-id="b8fb0-119">Sobrecarga de EsentStateException</span><span class="sxs-lookup"><span data-stu-id="b8fb0-119">EsentStateException overload</span></span>](./esentstateexception-constructor.md)

[<span data-ttu-id="b8fb0-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b8fb0-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
