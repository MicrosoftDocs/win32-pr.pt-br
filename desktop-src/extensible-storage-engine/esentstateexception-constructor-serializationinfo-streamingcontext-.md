---
description: 'Saiba mais sobre: Construtor EsentStateException (SerializationInfo, StreamingContext)'
title: Construtor EsentStateException (SerializationInfo, StreamingContext)
TOCTitle: EsentStateException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentStateException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102710
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
ms.openlocfilehash: 458efcde030559122085824a99660c3d5d7fc4c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297088"
---
# <a name="esentstateexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="db8c6-103">Construtor EsentStateException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="db8c6-103">EsentStateException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="db8c6-104">Inicializa uma nova instância da classe EsentStateException.</span><span class="sxs-lookup"><span data-stu-id="db8c6-104">Initializes a new instance of the EsentStateException class.</span></span> <span data-ttu-id="db8c6-105">Esse construtor é usado para desserializar uma exceção serializada.</span><span class="sxs-lookup"><span data-stu-id="db8c6-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="db8c6-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db8c6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="db8c6-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="db8c6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db8c6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db8c6-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentStateException(info, context)
```

``` csharp
protected EsentStateException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="db8c6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db8c6-109">Parameters</span></span>

  - <span data-ttu-id="db8c6-110">informações</span><span class="sxs-lookup"><span data-stu-id="db8c6-110">info</span></span>  
    <span data-ttu-id="db8c6-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="db8c6-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="db8c6-112">Os dados necessários para desserializar o objeto.</span><span class="sxs-lookup"><span data-stu-id="db8c6-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="db8c6-113">contexto</span><span class="sxs-lookup"><span data-stu-id="db8c6-113">context</span></span>  
    <span data-ttu-id="db8c6-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="db8c6-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="db8c6-115">O contexto de desserialização.</span><span class="sxs-lookup"><span data-stu-id="db8c6-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="db8c6-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="db8c6-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db8c6-117">Referência</span><span class="sxs-lookup"><span data-stu-id="db8c6-117">Reference</span></span>

[<span data-ttu-id="db8c6-118">Classe EsentStateException</span><span class="sxs-lookup"><span data-stu-id="db8c6-118">EsentStateException class</span></span>](./esentstateexception-class.md)

[<span data-ttu-id="db8c6-119">Membros do EsentStateException</span><span class="sxs-lookup"><span data-stu-id="db8c6-119">EsentStateException members</span></span>](./esentstateexception-members.md)

[<span data-ttu-id="db8c6-120">Sobrecarga de EsentStateException</span><span class="sxs-lookup"><span data-stu-id="db8c6-120">EsentStateException overload</span></span>](./esentstateexception-constructor.md)

[<span data-ttu-id="db8c6-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="db8c6-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
