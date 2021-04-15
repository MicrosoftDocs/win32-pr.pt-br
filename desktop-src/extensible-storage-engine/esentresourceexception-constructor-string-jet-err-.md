---
description: 'Saiba mais sobre: Construtor EsentResourceException (cadeia de caracteres, JET_err)'
title: Construtor EsentResourceException (cadeia de caracteres, JET_err)
TOCTitle: EsentResourceException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResourceException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55107307
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 458b12a80fdc0e6d7883d966f2e50aa8c1f6d69b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505996"
---
# <a name="esentresourceexception-constructor-string-jet_err"></a><span data-ttu-id="4b5ce-103">Construtor EsentResourceException (cadeia de caracteres, JET_err)</span><span class="sxs-lookup"><span data-stu-id="4b5ce-103">EsentResourceException constructor (String, JET_err)</span></span>

<span data-ttu-id="4b5ce-104">Inicializa uma nova instância da classe EsentResourceException.</span><span class="sxs-lookup"><span data-stu-id="4b5ce-104">Initializes a new instance of the EsentResourceException class.</span></span>

<span data-ttu-id="4b5ce-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4b5ce-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4b5ce-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4b5ce-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4b5ce-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b5ce-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentResourceException(description, _
    err)
```

``` csharp
protected EsentResourceException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="4b5ce-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b5ce-108">Parameters</span></span>

  - <span data-ttu-id="4b5ce-109">descrição</span><span class="sxs-lookup"><span data-stu-id="4b5ce-109">description</span></span>  
    <span data-ttu-id="4b5ce-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4b5ce-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4b5ce-111">A descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="4b5ce-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="4b5ce-112">erra</span><span class="sxs-lookup"><span data-stu-id="4b5ce-112">err</span></span>  
    <span data-ttu-id="4b5ce-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4b5ce-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="4b5ce-114">O código de erro da exceção.</span><span class="sxs-lookup"><span data-stu-id="4b5ce-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b5ce-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b5ce-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4b5ce-116">Referência</span><span class="sxs-lookup"><span data-stu-id="4b5ce-116">Reference</span></span>

[<span data-ttu-id="4b5ce-117">Classe EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="4b5ce-117">EsentResourceException class</span></span>](./esentresourceexception-class.md)

[<span data-ttu-id="4b5ce-118">Membros do EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="4b5ce-118">EsentResourceException members</span></span>](./esentresourceexception-members.md)

[<span data-ttu-id="4b5ce-119">Sobrecarga de EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="4b5ce-119">EsentResourceException overload</span></span>](./esentresourceexception-constructor.md)

[<span data-ttu-id="4b5ce-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4b5ce-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
