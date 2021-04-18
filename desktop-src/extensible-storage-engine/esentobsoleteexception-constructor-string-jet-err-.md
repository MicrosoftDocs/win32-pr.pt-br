---
description: 'Saiba mais sobre: Construtor EsentObsoleteException (cadeia de caracteres, JET_err)'
title: Construtor EsentObsoleteException (cadeia de caracteres, JET_err)
TOCTitle: EsentObsoleteException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102363
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 435a3db75cb09a47bccc311733b90fae30563c86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793624"
---
# <a name="esentobsoleteexception-constructor-string-jet_err"></a><span data-ttu-id="e8072-103">Construtor EsentObsoleteException (cadeia de caracteres, JET_err)</span><span class="sxs-lookup"><span data-stu-id="e8072-103">EsentObsoleteException constructor (String, JET_err)</span></span>

<span data-ttu-id="e8072-104">Inicializa uma nova instância da classe EsentObsoleteException.</span><span class="sxs-lookup"><span data-stu-id="e8072-104">Initializes a new instance of the EsentObsoleteException class.</span></span>

<span data-ttu-id="e8072-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e8072-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e8072-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e8072-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e8072-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8072-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentObsoleteException(description, _
    err)
```

``` csharp
protected EsentObsoleteException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="e8072-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8072-108">Parameters</span></span>

  - <span data-ttu-id="e8072-109">descrição</span><span class="sxs-lookup"><span data-stu-id="e8072-109">description</span></span>  
    <span data-ttu-id="e8072-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e8072-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e8072-111">A descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="e8072-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8072-112">erra</span><span class="sxs-lookup"><span data-stu-id="e8072-112">err</span></span>  
    <span data-ttu-id="e8072-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e8072-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="e8072-114">O código de erro da exceção.</span><span class="sxs-lookup"><span data-stu-id="e8072-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8072-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8072-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e8072-116">Referência</span><span class="sxs-lookup"><span data-stu-id="e8072-116">Reference</span></span>

[<span data-ttu-id="e8072-117">Classe EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="e8072-117">EsentObsoleteException class</span></span>](./esentobsoleteexception-class.md)

[<span data-ttu-id="e8072-118">Membros do EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="e8072-118">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="e8072-119">Sobrecarga de EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="e8072-119">EsentObsoleteException overload</span></span>](./esentobsoleteexception-constructor.md)

[<span data-ttu-id="e8072-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e8072-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
