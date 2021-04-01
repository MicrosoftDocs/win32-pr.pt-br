---
description: 'Saiba mais sobre: Construtor EsentInvalidColumnException (SerializationInfo, StreamingContext)'
title: Construtor EsentInvalidColumnException (SerializationInfo, StreamingContext)
TOCTitle: EsentInvalidColumnException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentInvalidColumnException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidcolumnexception.esentinvalidcolumnexception(v=EXCHG.10)
ms:contentKeyID: 55101741
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidColumnException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f439edeb0dad09f4c7f1bdd9521bb2410ca68be6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922966"
---
# <a name="esentinvalidcolumnexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="78b39-103">Construtor EsentInvalidColumnException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="78b39-103">EsentInvalidColumnException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="78b39-104">Inicializa uma nova instância da classe EsentInvalidColumnException.</span><span class="sxs-lookup"><span data-stu-id="78b39-104">Initializes a new instance of the EsentInvalidColumnException class.</span></span> <span data-ttu-id="78b39-105">Esse construtor é usado para desserializar uma exceção serializada.</span><span class="sxs-lookup"><span data-stu-id="78b39-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="78b39-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="78b39-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="78b39-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="78b39-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="78b39-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78b39-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentInvalidColumnException(info, context)
```

``` csharp
protected EsentInvalidColumnException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="78b39-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78b39-109">Parameters</span></span>

  - <span data-ttu-id="78b39-110">informações</span><span class="sxs-lookup"><span data-stu-id="78b39-110">info</span></span>  
    <span data-ttu-id="78b39-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="78b39-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="78b39-112">Os dados necessários para desserializar o objeto.</span><span class="sxs-lookup"><span data-stu-id="78b39-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="78b39-113">contexto</span><span class="sxs-lookup"><span data-stu-id="78b39-113">context</span></span>  
    <span data-ttu-id="78b39-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="78b39-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="78b39-115">O contexto de desserialização.</span><span class="sxs-lookup"><span data-stu-id="78b39-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="78b39-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="78b39-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="78b39-117">Referência</span><span class="sxs-lookup"><span data-stu-id="78b39-117">Reference</span></span>

[<span data-ttu-id="78b39-118">Classe EsentInvalidColumnException</span><span class="sxs-lookup"><span data-stu-id="78b39-118">EsentInvalidColumnException class</span></span>](./esentinvalidcolumnexception-class.md)

[<span data-ttu-id="78b39-119">Membros do EsentInvalidColumnException</span><span class="sxs-lookup"><span data-stu-id="78b39-119">EsentInvalidColumnException members</span></span>](./esentinvalidcolumnexception-members.md)

[<span data-ttu-id="78b39-120">Sobrecarga de EsentInvalidColumnException</span><span class="sxs-lookup"><span data-stu-id="78b39-120">EsentInvalidColumnException overload</span></span>](./esentinvalidcolumnexception-constructor2.md)

[<span data-ttu-id="78b39-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="78b39-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
