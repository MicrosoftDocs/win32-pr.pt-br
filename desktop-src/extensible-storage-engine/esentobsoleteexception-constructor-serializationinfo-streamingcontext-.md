---
description: 'Saiba mais sobre: Construtor EsentObsoleteException (SerializationInfo, StreamingContext)'
title: Construtor EsentObsoleteException (SerializationInfo, StreamingContext)
TOCTitle: EsentObsoleteException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102167
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b287a61396f0d908c888b84553e5dc67df907be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793623"
---
# <a name="esentobsoleteexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="e2152-103">Construtor EsentObsoleteException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="e2152-103">EsentObsoleteException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="e2152-104">Inicializa uma nova instância da classe EsentObsoleteException.</span><span class="sxs-lookup"><span data-stu-id="e2152-104">Initializes a new instance of the EsentObsoleteException class.</span></span> <span data-ttu-id="e2152-105">Esse construtor é usado para desserializar uma exceção serializada.</span><span class="sxs-lookup"><span data-stu-id="e2152-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="e2152-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2152-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e2152-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2152-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2152-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2152-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentObsoleteException(info, context)
```

``` csharp
protected EsentObsoleteException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="e2152-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2152-109">Parameters</span></span>

  - <span data-ttu-id="e2152-110">informações</span><span class="sxs-lookup"><span data-stu-id="e2152-110">info</span></span>  
    <span data-ttu-id="e2152-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="e2152-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="e2152-112">Os dados necessários para desserializar o objeto.</span><span class="sxs-lookup"><span data-stu-id="e2152-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2152-113">contexto</span><span class="sxs-lookup"><span data-stu-id="e2152-113">context</span></span>  
    <span data-ttu-id="e2152-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="e2152-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="e2152-115">O contexto de desserialização.</span><span class="sxs-lookup"><span data-stu-id="e2152-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2152-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2152-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2152-117">Referência</span><span class="sxs-lookup"><span data-stu-id="e2152-117">Reference</span></span>

[<span data-ttu-id="e2152-118">Classe EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="e2152-118">EsentObsoleteException class</span></span>](./esentobsoleteexception-class.md)

[<span data-ttu-id="e2152-119">Membros do EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="e2152-119">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="e2152-120">Sobrecarga de EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="e2152-120">EsentObsoleteException overload</span></span>](./esentobsoleteexception-constructor.md)

[<span data-ttu-id="e2152-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e2152-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
