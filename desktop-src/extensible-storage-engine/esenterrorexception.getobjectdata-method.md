---
description: 'Saiba mais sobre: método EsentErrorException. GetObjectData'
title: Método EsentErrorException. GetObjectData
TOCTitle: 'GetObjectData method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.getobjectdata(v=EXCHG.10)
ms:contentKeyID: 55101432
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86d951828da0f8bb8eb3ada13bb67b02e801709e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771491"
---
# <a name="esenterrorexceptiongetobjectdata-method"></a><span data-ttu-id="b2e10-103">Método EsentErrorException. GetObjectData</span><span class="sxs-lookup"><span data-stu-id="b2e10-103">EsentErrorException.GetObjectData method</span></span>

<span data-ttu-id="b2e10-104">Quando substituído em uma classe derivada, define [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) com informações sobre a exceção.</span><span class="sxs-lookup"><span data-stu-id="b2e10-104">When overridden in a derived class, sets the [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) with information about the exception.</span></span>

<span data-ttu-id="b2e10-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b2e10-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b2e10-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b2e10-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e10-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2e10-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Sub GetObjectData ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim instance As EsentErrorException
Dim info As SerializationInfo
Dim context As StreamingContext

instance.GetObjectData(info, context)
```

``` csharp
public override void GetObjectData(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="b2e10-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2e10-108">Parameters</span></span>

  - <span data-ttu-id="b2e10-109">informações</span><span class="sxs-lookup"><span data-stu-id="b2e10-109">info</span></span>  
    <span data-ttu-id="b2e10-110">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="b2e10-110">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="b2e10-111">O [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) que contém os dados do objeto serializado sobre a exceção que está sendo gerada.</span><span class="sxs-lookup"><span data-stu-id="b2e10-111">The [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) that holds the serialized object data about the exception being thrown.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2e10-112">contexto</span><span class="sxs-lookup"><span data-stu-id="b2e10-112">context</span></span>  
    <span data-ttu-id="b2e10-113">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="b2e10-113">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="b2e10-114">O [StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext) que contém informações contextuais sobre a origem ou o destino.</span><span class="sxs-lookup"><span data-stu-id="b2e10-114">The [StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext) that contains contextual information about the source or destination.</span></span>

#### <a name="implements"></a><span data-ttu-id="b2e10-115">Implementações</span><span class="sxs-lookup"><span data-stu-id="b2e10-115">Implements</span></span>

[<span data-ttu-id="b2e10-116">ISerializable. GetObjectData (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="b2e10-116">ISerializable.GetObjectData(SerializationInfo, StreamingContext)</span></span>](/dotnet/api/system.runtime.serialization.iserializable.getobjectdata#System_Runtime_Serialization_ISerializable_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  
[<span data-ttu-id="b2e10-117">_Exception. GetObjectData (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="b2e10-117">_Exception.GetObjectData(SerializationInfo, StreamingContext)</span></span>](/dotnet/api/system.runtime.interopservices._exception.getobjectdata#System_Runtime_InteropServices__Exception_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  

## <a name="exceptions"></a><span data-ttu-id="b2e10-118">Exceções</span><span class="sxs-lookup"><span data-stu-id="b2e10-118">Exceptions</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2e10-119">Exceção</span><span class="sxs-lookup"><span data-stu-id="b2e10-119">Exception</span></span></th>
<th><span data-ttu-id="b2e10-120">Condição</span><span class="sxs-lookup"><span data-stu-id="b2e10-120">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2e10-121"><a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a></span><span class="sxs-lookup"><span data-stu-id="b2e10-121"><a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a></span></span></td>
<td><p><span data-ttu-id="b2e10-122">O parâmetro info é uma referência nula (Nothing no Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="b2e10-122">The info parameter is a null reference (Nothing in Visual Basic).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b2e10-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2e10-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b2e10-124">Referência</span><span class="sxs-lookup"><span data-stu-id="b2e10-124">Reference</span></span>

[<span data-ttu-id="b2e10-125">Classe EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b2e10-125">EsentErrorException class</span></span>](./esenterrorexception-class.md)

[<span data-ttu-id="b2e10-126">Membros do EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b2e10-126">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="b2e10-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b2e10-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
