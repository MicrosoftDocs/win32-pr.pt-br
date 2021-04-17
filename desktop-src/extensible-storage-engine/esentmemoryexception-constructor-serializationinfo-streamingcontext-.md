---
description: 'Saiba mais sobre: Construtor EsentMemoryException (SerializationInfo, StreamingContext)'
title: Construtor EsentMemoryException (SerializationInfo, StreamingContext)
TOCTitle: EsentMemoryException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102121
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
ms.openlocfilehash: 7bf198808de480964b02801c809ab3cff50d35fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761149"
---
# <a name="esentmemoryexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="4a7d8-103">Construtor EsentMemoryException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="4a7d8-103">EsentMemoryException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="4a7d8-104">Inicializa uma nova instância da classe EsentMemoryException.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-104">Initializes a new instance of the EsentMemoryException class.</span></span> <span data-ttu-id="4a7d8-105">Esse construtor é usado para desserializar uma exceção serializada.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="4a7d8-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4a7d8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4a7d8-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4a7d8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4a7d8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a7d8-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentMemoryException(info, context)
```

``` csharp
protected EsentMemoryException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="4a7d8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a7d8-109">Parameters</span></span>

  - <span data-ttu-id="4a7d8-110">informações</span><span class="sxs-lookup"><span data-stu-id="4a7d8-110">info</span></span>  
    <span data-ttu-id="4a7d8-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="4a7d8-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="4a7d8-112">Os dados necessários para desserializar o objeto.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a7d8-113">contexto</span><span class="sxs-lookup"><span data-stu-id="4a7d8-113">context</span></span>  
    <span data-ttu-id="4a7d8-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="4a7d8-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="4a7d8-115">O contexto de desserialização.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a7d8-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a7d8-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4a7d8-117">Referência</span><span class="sxs-lookup"><span data-stu-id="4a7d8-117">Reference</span></span>

[<span data-ttu-id="4a7d8-118">Classe EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="4a7d8-118">EsentMemoryException class</span></span>](./esentmemoryexception-class.md)

[<span data-ttu-id="4a7d8-119">Membros do EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="4a7d8-119">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="4a7d8-120">Sobrecarga de EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="4a7d8-120">EsentMemoryException overload</span></span>](./esentmemoryexception-constructor.md)

[<span data-ttu-id="4a7d8-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4a7d8-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
