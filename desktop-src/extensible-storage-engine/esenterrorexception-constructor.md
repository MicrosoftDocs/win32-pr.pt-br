---
description: 'Saiba mais sobre: Construtor EsentErrorException'
title: Construtor EsentErrorException
TOCTitle: 'EsentErrorException constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentErrorException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.esenterrorexception(v=EXCHG.10)
ms:contentKeyID: 55101320
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.EsentErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0728eb316c7d5a5d3cf4a1ad13c2e35451318225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297053"
---
# <a name="esenterrorexception-constructor"></a><span data-ttu-id="9971e-103">Construtor EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="9971e-103">EsentErrorException constructor</span></span>

<span data-ttu-id="9971e-104">Inicializa uma nova instância da classe EsentErrorException.</span><span class="sxs-lookup"><span data-stu-id="9971e-104">Initializes a new instance of the EsentErrorException class.</span></span> <span data-ttu-id="9971e-105">Esse construtor é usado para desserializar uma exceção serializada.</span><span class="sxs-lookup"><span data-stu-id="9971e-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="9971e-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9971e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9971e-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9971e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9971e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9971e-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentErrorException(info, context)
```

``` csharp
protected EsentErrorException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="9971e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9971e-109">Parameters</span></span>

  - <span data-ttu-id="9971e-110">informações</span><span class="sxs-lookup"><span data-stu-id="9971e-110">info</span></span>  
    <span data-ttu-id="9971e-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="9971e-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="9971e-112">Os dados necessários para desserializar o objeto.</span><span class="sxs-lookup"><span data-stu-id="9971e-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="9971e-113">contexto</span><span class="sxs-lookup"><span data-stu-id="9971e-113">context</span></span>  
    <span data-ttu-id="9971e-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="9971e-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="9971e-115">O contexto de desserialização.</span><span class="sxs-lookup"><span data-stu-id="9971e-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="9971e-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="9971e-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9971e-117">Referência</span><span class="sxs-lookup"><span data-stu-id="9971e-117">Reference</span></span>

[<span data-ttu-id="9971e-118">Classe EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="9971e-118">EsentErrorException class</span></span>](./esenterrorexception-class.md)

[<span data-ttu-id="9971e-119">Membros do EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="9971e-119">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="9971e-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9971e-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
