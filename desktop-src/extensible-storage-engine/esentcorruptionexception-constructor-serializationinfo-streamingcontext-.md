---
description: 'Saiba mais sobre: Construtor EsentCorruptionException (SerializationInfo, StreamingContext)'
title: Construtor EsentCorruptionException (SerializationInfo, StreamingContext)
TOCTitle: EsentCorruptionException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentCorruptionException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101038
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0e80255d86ed6f953e4010541e98b794537f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922762"
---
# <a name="esentcorruptionexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="c709f-103">Construtor EsentCorruptionException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="c709f-103">EsentCorruptionException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="c709f-104">Inicializa uma nova instância da classe EsentCorruptionException.</span><span class="sxs-lookup"><span data-stu-id="c709f-104">Initializes a new instance of the EsentCorruptionException class.</span></span> <span data-ttu-id="c709f-105">Esse construtor é usado para desserializar uma exceção serializada.</span><span class="sxs-lookup"><span data-stu-id="c709f-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="c709f-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c709f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c709f-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c709f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c709f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c709f-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentCorruptionException(info, context)
```

``` csharp
protected EsentCorruptionException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="c709f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c709f-109">Parameters</span></span>

  - <span data-ttu-id="c709f-110">informações</span><span class="sxs-lookup"><span data-stu-id="c709f-110">info</span></span>  
    <span data-ttu-id="c709f-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="c709f-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="c709f-112">Os dados necessários para desserializar o objeto.</span><span class="sxs-lookup"><span data-stu-id="c709f-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="c709f-113">contexto</span><span class="sxs-lookup"><span data-stu-id="c709f-113">context</span></span>  
    <span data-ttu-id="c709f-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="c709f-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="c709f-115">O contexto de desserialização.</span><span class="sxs-lookup"><span data-stu-id="c709f-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="c709f-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="c709f-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c709f-117">Referência</span><span class="sxs-lookup"><span data-stu-id="c709f-117">Reference</span></span>

[<span data-ttu-id="c709f-118">Classe EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="c709f-118">EsentCorruptionException class</span></span>](./esentcorruptionexception-class.md)

[<span data-ttu-id="c709f-119">Membros do EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="c709f-119">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="c709f-120">Sobrecarga de EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="c709f-120">EsentCorruptionException overload</span></span>](./esentcorruptionexception-constructor.md)

[<span data-ttu-id="c709f-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c709f-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
