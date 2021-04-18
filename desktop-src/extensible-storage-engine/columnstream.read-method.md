---
description: 'Saiba mais sobre: método ColumnStream. Read'
title: Método ColumnStream. Read
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e407a9069807d10eaabf4f7ac3fce3919576bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753311"
---
# <a name="columnstreamread-method"></a><span data-ttu-id="8150f-103">Método ColumnStream. Read</span><span class="sxs-lookup"><span data-stu-id="8150f-103">ColumnStream.Read method</span></span>

<span data-ttu-id="8150f-104">Lê uma sequência de bytes do fluxo atual e avança a posição no fluxo até o número de bytes lidos.</span><span class="sxs-lookup"><span data-stu-id="8150f-104">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span>

<span data-ttu-id="8150f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8150f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8150f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8150f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8150f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8150f-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="8150f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8150f-108">Parameters</span></span>

  - <span data-ttu-id="8150f-109">Buffer</span><span class="sxs-lookup"><span data-stu-id="8150f-109">buffer</span></span>  
    <span data-ttu-id="8150f-110">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="8150f-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="8150f-111">O buffer para leitura.</span><span class="sxs-lookup"><span data-stu-id="8150f-111">The buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="8150f-112">deslocamento</span><span class="sxs-lookup"><span data-stu-id="8150f-112">offset</span></span>  
    <span data-ttu-id="8150f-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8150f-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8150f-114">O deslocamento no buffer para leitura.</span><span class="sxs-lookup"><span data-stu-id="8150f-114">The offset in the buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="8150f-115">count</span><span class="sxs-lookup"><span data-stu-id="8150f-115">count</span></span>  
    <span data-ttu-id="8150f-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8150f-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8150f-117">O número de bytes a serem lidos.</span><span class="sxs-lookup"><span data-stu-id="8150f-117">The number of bytes to read.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8150f-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8150f-118">Return value</span></span>

<span data-ttu-id="8150f-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8150f-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="8150f-120">O número de bytes lidos no buffer.</span><span class="sxs-lookup"><span data-stu-id="8150f-120">The number of bytes read into the buffer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8150f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="8150f-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8150f-122">Referência</span><span class="sxs-lookup"><span data-stu-id="8150f-122">Reference</span></span>

[<span data-ttu-id="8150f-123">Classe ColumnStream</span><span class="sxs-lookup"><span data-stu-id="8150f-123">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="8150f-124">Membros do ColumnStream</span><span class="sxs-lookup"><span data-stu-id="8150f-124">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="8150f-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8150f-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
