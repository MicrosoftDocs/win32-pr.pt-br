---
description: 'Saiba mais sobre: método ColumnStream. Seek'
title: Método ColumnStream. Seek
TOCTitle: 'Seek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Seek(System.Int64,System.IO.SeekOrigin)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.seek(v=EXCHG.10)
ms:contentKeyID: 55100949
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5489bb0ee9a4a1550166e14a945a2a6d58c45af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502158"
---
# <a name="columnstreamseek-method"></a><span data-ttu-id="9ef79-103">Método ColumnStream. Seek</span><span class="sxs-lookup"><span data-stu-id="9ef79-103">ColumnStream.Seek method</span></span>

<span data-ttu-id="9ef79-104">Define a posição no fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="9ef79-104">Sets the position in the current stream.</span></span>

<span data-ttu-id="9ef79-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9ef79-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9ef79-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9ef79-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9ef79-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ef79-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Seek ( _
    offset As Long, _
    origin As SeekOrigin _
) As Long
'Usage
Dim instance As ColumnStream
Dim offset As Long
Dim origin As SeekOrigin
Dim returnValue As Long

returnValue = instance.Seek(offset, origin)
```

``` csharp
public override long Seek(
    long offset,
    SeekOrigin origin
)
```

#### <a name="parameters"></a><span data-ttu-id="9ef79-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ef79-108">Parameters</span></span>

  - <span data-ttu-id="9ef79-109">deslocamento</span><span class="sxs-lookup"><span data-stu-id="9ef79-109">offset</span></span>  
    <span data-ttu-id="9ef79-110">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="9ef79-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="9ef79-111">Deslocamento de byte relativo ao parâmetro Origin.</span><span class="sxs-lookup"><span data-stu-id="9ef79-111">Byte offset relative to the origin parameter.</span></span>

<!-- end list -->

  - <span data-ttu-id="9ef79-112">origin</span><span class="sxs-lookup"><span data-stu-id="9ef79-112">origin</span></span>  
    <span data-ttu-id="9ef79-113">Tipo: [System. IO. SeekOrigin](/dotnet/api/system.io.seekorigin)</span><span class="sxs-lookup"><span data-stu-id="9ef79-113">Type: [System.IO.SeekOrigin](/dotnet/api/system.io.seekorigin)</span></span>  
    
    <span data-ttu-id="9ef79-114">Um SeekOrigin que indica o ponto de referência para a nova posição.</span><span class="sxs-lookup"><span data-stu-id="9ef79-114">A SeekOrigin indicating the reference point for the new position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9ef79-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ef79-115">Return value</span></span>

<span data-ttu-id="9ef79-116">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="9ef79-116">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
<span data-ttu-id="9ef79-117">A nova posição no fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="9ef79-117">The new position in the current stream.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9ef79-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ef79-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9ef79-119">Referência</span><span class="sxs-lookup"><span data-stu-id="9ef79-119">Reference</span></span>

[<span data-ttu-id="9ef79-120">Classe ColumnStream</span><span class="sxs-lookup"><span data-stu-id="9ef79-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="9ef79-121">Membros do ColumnStream</span><span class="sxs-lookup"><span data-stu-id="9ef79-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="9ef79-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9ef79-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
