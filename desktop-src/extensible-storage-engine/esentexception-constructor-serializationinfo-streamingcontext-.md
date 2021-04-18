---
description: 'Saiba mais sobre: Construtor EsentException (SerializationInfo, StreamingContext)'
title: Construtor EsentException (SerializationInfo, StreamingContext) (Microsoft. ISAM. ESENT)
TOCTitle: EsentException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100719
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bdcfe5c3b37746f50926850b45763f9d70de893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810850"
---
# <a name="esentexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="db095-103">Construtor EsentException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="db095-103">EsentException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="db095-104">Inicializa uma nova instância da classe EsentException.</span><span class="sxs-lookup"><span data-stu-id="db095-104">Initializes a new instance of the EsentException class.</span></span> <span data-ttu-id="db095-105">Esse construtor é usado para desserializar uma exceção serializada.</span><span class="sxs-lookup"><span data-stu-id="db095-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="db095-106">**Namespace:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db095-106">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="db095-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="db095-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db095-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db095-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentException(info, context)
```

``` csharp
protected EsentException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="db095-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db095-109">Parameters</span></span>

  - <span data-ttu-id="db095-110">informações</span><span class="sxs-lookup"><span data-stu-id="db095-110">info</span></span>  
    <span data-ttu-id="db095-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="db095-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="db095-112">Os dados necessários para desserializar o objeto.</span><span class="sxs-lookup"><span data-stu-id="db095-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="db095-113">contexto</span><span class="sxs-lookup"><span data-stu-id="db095-113">context</span></span>  
    <span data-ttu-id="db095-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="db095-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="db095-115">O contexto de desserialização.</span><span class="sxs-lookup"><span data-stu-id="db095-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="db095-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="db095-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db095-117">Referência</span><span class="sxs-lookup"><span data-stu-id="db095-117">Reference</span></span>

[<span data-ttu-id="db095-118">Classe EsentException</span><span class="sxs-lookup"><span data-stu-id="db095-118">EsentException class</span></span>](./esentexception-class.md)

[<span data-ttu-id="db095-119">Membros do EsentException</span><span class="sxs-lookup"><span data-stu-id="db095-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="db095-120">Sobrecarga de EsentException</span><span class="sxs-lookup"><span data-stu-id="db095-120">EsentException overload</span></span>](./esentexception-constructor.md)

[<span data-ttu-id="db095-121">Namespace Microsoft. ISAM. ESENT</span><span class="sxs-lookup"><span data-stu-id="db095-121">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
