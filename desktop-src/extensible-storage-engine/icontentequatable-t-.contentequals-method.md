---
description: 'Saiba mais sobre: IContentEquatable <T> . Método ContentEquals'
title: IContentEquatable (T). Método ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals(`0)
ms:mtpsurl: https://msdn.microsoft.com/library/Hh538970(v=EXCHG.10)
ms:contentKeyID: 39509953
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c3b06307f7c4ebc44242e02ee5ae99a182f9ab3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784049"
---
# <a name="icontentequatabletcontentequals-method"></a><span data-ttu-id="b28d8-103">IContentEquatable \<T\> . Método ContentEquals</span><span class="sxs-lookup"><span data-stu-id="b28d8-103">IContentEquatable\<T\>.ContentEquals method</span></span>

<span data-ttu-id="b28d8-104">Retorna um valor que indica se essa instância é igual a outra instância.</span><span class="sxs-lookup"><span data-stu-id="b28d8-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="b28d8-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b28d8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b28d8-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b28d8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b28d8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b28d8-107">Syntax</span></span>

``` vb
'Declaration
Function ContentEquals ( _
    other As T _
) As Boolean
'Usage
Dim instance As IContentEquatable
Dim other As T
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
bool ContentEquals(
    T other
)
```

#### <a name="parameters"></a><span data-ttu-id="b28d8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b28d8-108">Parameters</span></span>

  - <span data-ttu-id="b28d8-109">outros</span><span class="sxs-lookup"><span data-stu-id="b28d8-109">other</span></span>  
    <span data-ttu-id="b28d8-110">Tipo: [T](./icontentequatable-t-interface.md)</span><span class="sxs-lookup"><span data-stu-id="b28d8-110">Type: [T](./icontentequatable-t-interface.md)</span></span>  
    
    <span data-ttu-id="b28d8-111">Uma instância para comparar com esta instância.</span><span class="sxs-lookup"><span data-stu-id="b28d8-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b28d8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b28d8-112">Return value</span></span>

<span data-ttu-id="b28d8-113">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b28d8-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b28d8-114">True se as duas instâncias forem iguais.</span><span class="sxs-lookup"><span data-stu-id="b28d8-114">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b28d8-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="b28d8-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b28d8-116">Referência</span><span class="sxs-lookup"><span data-stu-id="b28d8-116">Reference</span></span>

[<span data-ttu-id="b28d8-117">\<T\>Interface IContentEquatable</span><span class="sxs-lookup"><span data-stu-id="b28d8-117">IContentEquatable\<T\> interface</span></span>](./icontentequatable-t-interface.md)

[<span data-ttu-id="b28d8-118">Membros do IContentEquatable \<T\></span><span class="sxs-lookup"><span data-stu-id="b28d8-118">IContentEquatable\<T\> members</span></span>](./icontentequatable-t-members.md)

[<span data-ttu-id="b28d8-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b28d8-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
