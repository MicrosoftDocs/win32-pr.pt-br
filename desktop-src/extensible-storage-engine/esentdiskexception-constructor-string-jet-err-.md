---
description: 'Saiba mais sobre: Construtor EsentDiskException (cadeia de caracteres, JET_err)'
title: Construtor EsentDiskException (cadeia de caracteres, JET_err)
TOCTitle: EsentDiskException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDiskException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101616
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d518fcb263481c2563b92d0b579a686db13c0175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789527"
---
# <a name="esentdiskexception-constructor-string-jet_err"></a><span data-ttu-id="c3f78-103">Construtor EsentDiskException (cadeia de caracteres, JET_err)</span><span class="sxs-lookup"><span data-stu-id="c3f78-103">EsentDiskException constructor (String, JET_err)</span></span>

<span data-ttu-id="c3f78-104">Inicializa uma nova instância da classe EsentDiskException.</span><span class="sxs-lookup"><span data-stu-id="c3f78-104">Initializes a new instance of the EsentDiskException class.</span></span>

<span data-ttu-id="c3f78-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3f78-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c3f78-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c3f78-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f78-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3f78-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentDiskException(description, _
    err)
```

``` csharp
protected EsentDiskException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="c3f78-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3f78-108">Parameters</span></span>

  - <span data-ttu-id="c3f78-109">descrição</span><span class="sxs-lookup"><span data-stu-id="c3f78-109">description</span></span>  
    <span data-ttu-id="c3f78-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c3f78-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c3f78-111">A descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="c3f78-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3f78-112">erra</span><span class="sxs-lookup"><span data-stu-id="c3f78-112">err</span></span>  
    <span data-ttu-id="c3f78-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c3f78-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="c3f78-114">O código de erro da exceção.</span><span class="sxs-lookup"><span data-stu-id="c3f78-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3f78-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3f78-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3f78-116">Referência</span><span class="sxs-lookup"><span data-stu-id="c3f78-116">Reference</span></span>

[<span data-ttu-id="c3f78-117">Classe EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="c3f78-117">EsentDiskException class</span></span>](./esentdiskexception-class.md)

[<span data-ttu-id="c3f78-118">Membros do EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="c3f78-118">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="c3f78-119">Sobrecarga de EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="c3f78-119">EsentDiskException overload</span></span>](./esentdiskexception-constructor.md)

[<span data-ttu-id="c3f78-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c3f78-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
