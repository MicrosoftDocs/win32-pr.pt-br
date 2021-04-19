---
description: 'Saiba mais sobre: Construtor EsentIOException (cadeia de caracteres, JET_err)'
title: Construtor EsentIOException (cadeia de caracteres, JET_err)
TOCTitle: EsentIOException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentIOException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102030
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087f22d7836ff41ac97b65c15be1b51dfac84a8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781498"
---
# <a name="esentioexception-constructor-string-jet_err"></a><span data-ttu-id="d426d-103">Construtor EsentIOException (cadeia de caracteres, JET_err)</span><span class="sxs-lookup"><span data-stu-id="d426d-103">EsentIOException constructor (String, JET_err)</span></span>

<span data-ttu-id="d426d-104">Inicializa uma nova instância da classe EsentIOException.</span><span class="sxs-lookup"><span data-stu-id="d426d-104">Initializes a new instance of the EsentIOException class.</span></span>

<span data-ttu-id="d426d-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d426d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d426d-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d426d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d426d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d426d-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentIOException(description, _
    err)
```

``` csharp
protected EsentIOException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="d426d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d426d-108">Parameters</span></span>

  - <span data-ttu-id="d426d-109">descrição</span><span class="sxs-lookup"><span data-stu-id="d426d-109">description</span></span>  
    <span data-ttu-id="d426d-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d426d-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d426d-111">A descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="d426d-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="d426d-112">erra</span><span class="sxs-lookup"><span data-stu-id="d426d-112">err</span></span>  
    <span data-ttu-id="d426d-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d426d-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="d426d-114">O código de erro da exceção.</span><span class="sxs-lookup"><span data-stu-id="d426d-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="d426d-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="d426d-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d426d-116">Referência</span><span class="sxs-lookup"><span data-stu-id="d426d-116">Reference</span></span>

[<span data-ttu-id="d426d-117">Classe EsentIOException</span><span class="sxs-lookup"><span data-stu-id="d426d-117">EsentIOException class</span></span>](./esentioexception-class.md)

[<span data-ttu-id="d426d-118">Membros do EsentIOException</span><span class="sxs-lookup"><span data-stu-id="d426d-118">EsentIOException members</span></span>](./esentioexception-members.md)

[<span data-ttu-id="d426d-119">Sobrecarga de EsentIOException</span><span class="sxs-lookup"><span data-stu-id="d426d-119">EsentIOException overload</span></span>](./esentioexception-constructor.md)

[<span data-ttu-id="d426d-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d426d-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
