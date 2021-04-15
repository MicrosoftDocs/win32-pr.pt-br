---
description: 'Saiba mais sobre: Construtor EsentApiException (SerializationInfo, StreamingContext)'
title: Construtor EsentApiException (SerializationInfo, StreamingContext)
TOCTitle: EsentApiException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentApiException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101059
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a00204c254378956521a1ae5fe02480dd879c832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461348"
---
# <a name="esentapiexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="cd97c-103">Construtor EsentApiException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="cd97c-103">EsentApiException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="cd97c-104">Inicializa uma nova instância da classe EsentApiException.</span><span class="sxs-lookup"><span data-stu-id="cd97c-104">Initializes a new instance of the EsentApiException class.</span></span> <span data-ttu-id="cd97c-105">Esse construtor é usado para desserializar uma exceção serializada.</span><span class="sxs-lookup"><span data-stu-id="cd97c-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="cd97c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cd97c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cd97c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cd97c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cd97c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd97c-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentApiException(info, context)
```

``` csharp
protected EsentApiException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="cd97c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd97c-109">Parameters</span></span>

  - <span data-ttu-id="cd97c-110">informações</span><span class="sxs-lookup"><span data-stu-id="cd97c-110">info</span></span>  
    <span data-ttu-id="cd97c-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="cd97c-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="cd97c-112">Os dados necessários para desserializar o objeto.</span><span class="sxs-lookup"><span data-stu-id="cd97c-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="cd97c-113">contexto</span><span class="sxs-lookup"><span data-stu-id="cd97c-113">context</span></span>  
    <span data-ttu-id="cd97c-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="cd97c-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="cd97c-115">O contexto de desserialização.</span><span class="sxs-lookup"><span data-stu-id="cd97c-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd97c-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd97c-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cd97c-117">Referência</span><span class="sxs-lookup"><span data-stu-id="cd97c-117">Reference</span></span>

[<span data-ttu-id="cd97c-118">Classe EsentApiException</span><span class="sxs-lookup"><span data-stu-id="cd97c-118">EsentApiException class</span></span>](./esentapiexception-class.md)

[<span data-ttu-id="cd97c-119">Membros do EsentApiException</span><span class="sxs-lookup"><span data-stu-id="cd97c-119">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="cd97c-120">Sobrecarga de EsentApiException</span><span class="sxs-lookup"><span data-stu-id="cd97c-120">EsentApiException overload</span></span>](./esentapiexception-constructor.md)

[<span data-ttu-id="cd97c-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cd97c-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
