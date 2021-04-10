---
description: 'Saiba mais sobre: Construtor EsentOperationException (SerializationInfo, StreamingContext)'
title: Construtor EsentOperationException (SerializationInfo, StreamingContext)
TOCTitle: EsentOperationException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentOperationException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102312
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ee281a47ae8e24ff51ffe5c3d6a4ef4f4b1873e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169156"
---
# <a name="esentoperationexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="e0b86-103">Construtor EsentOperationException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="e0b86-103">EsentOperationException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="e0b86-104">Inicializa uma nova instância da classe EsentOperationException.</span><span class="sxs-lookup"><span data-stu-id="e0b86-104">Initializes a new instance of the EsentOperationException class.</span></span> <span data-ttu-id="e0b86-105">Esse construtor é usado para desserializar uma exceção serializada.</span><span class="sxs-lookup"><span data-stu-id="e0b86-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="e0b86-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e0b86-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e0b86-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e0b86-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b86-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0b86-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentOperationException(info, context)
```

``` csharp
protected EsentOperationException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="e0b86-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0b86-109">Parameters</span></span>

  - <span data-ttu-id="e0b86-110">informações</span><span class="sxs-lookup"><span data-stu-id="e0b86-110">info</span></span>  
    <span data-ttu-id="e0b86-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="e0b86-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="e0b86-112">Os dados necessários para desserializar o objeto.</span><span class="sxs-lookup"><span data-stu-id="e0b86-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="e0b86-113">contexto</span><span class="sxs-lookup"><span data-stu-id="e0b86-113">context</span></span>  
    <span data-ttu-id="e0b86-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="e0b86-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="e0b86-115">O contexto de desserialização.</span><span class="sxs-lookup"><span data-stu-id="e0b86-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0b86-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0b86-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e0b86-117">Referência</span><span class="sxs-lookup"><span data-stu-id="e0b86-117">Reference</span></span>

[<span data-ttu-id="e0b86-118">Classe EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="e0b86-118">EsentOperationException class</span></span>](./esentoperationexception-class.md)

[<span data-ttu-id="e0b86-119">Membros do EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="e0b86-119">EsentOperationException members</span></span>](./esentoperationexception-members.md)

[<span data-ttu-id="e0b86-120">Sobrecarga de EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="e0b86-120">EsentOperationException overload</span></span>](./esentoperationexception-constructor.md)

[<span data-ttu-id="e0b86-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e0b86-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
