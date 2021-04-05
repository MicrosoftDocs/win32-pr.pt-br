---
description: 'Saiba mais sobre: JET_INSTANCE_INFO. Método Equals (JET_INSTANCE_INFO)'
title: JET_INSTANCE_INFO. Método Equals (JET_INSTANCE_INFO)
TOCTitle: Equals method (JET_INSTANCE_INFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.Equals(Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.equals(v=EXCHG.10)
ms:contentKeyID: 55103697
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b601e018b51e6e95162478ff6c5fe12e77f7b469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921882"
---
# <a name="jet_instance_infoequals-method-jet_instance_info"></a><span data-ttu-id="3daa9-103">JET_INSTANCE_INFO. Método Equals (JET_INSTANCE_INFO)</span><span class="sxs-lookup"><span data-stu-id="3daa9-103">JET_INSTANCE_INFO.Equals method (JET_INSTANCE_INFO)</span></span>

<span data-ttu-id="3daa9-104">Retorna um valor que indica se essa instância é igual a outra instância.</span><span class="sxs-lookup"><span data-stu-id="3daa9-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="3daa9-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3daa9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3daa9-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3daa9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3daa9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3daa9-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_INSTANCE_INFO _
) As Boolean
'Usage
Dim instance As JET_INSTANCE_INFO
Dim other As JET_INSTANCE_INFO
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_INSTANCE_INFO other
)
```

#### <a name="parameters"></a><span data-ttu-id="3daa9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3daa9-108">Parameters</span></span>

  - <span data-ttu-id="3daa9-109">outros</span><span class="sxs-lookup"><span data-stu-id="3daa9-109">other</span></span>  
    <span data-ttu-id="3daa9-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE_INFO](./jet-instance-info-class.md)</span><span class="sxs-lookup"><span data-stu-id="3daa9-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO](./jet-instance-info-class.md)</span></span>  
    
    <span data-ttu-id="3daa9-111">Uma instância para comparar com esta instância.</span><span class="sxs-lookup"><span data-stu-id="3daa9-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3daa9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3daa9-112">Return value</span></span>

<span data-ttu-id="3daa9-113">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="3daa9-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="3daa9-114">True se as duas instâncias forem iguais.</span><span class="sxs-lookup"><span data-stu-id="3daa9-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="3daa9-115">Implementações</span><span class="sxs-lookup"><span data-stu-id="3daa9-115">Implements</span></span>

[<span data-ttu-id="3daa9-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="3daa9-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="3daa9-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="3daa9-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3daa9-118">Referência</span><span class="sxs-lookup"><span data-stu-id="3daa9-118">Reference</span></span>

[<span data-ttu-id="3daa9-119">Classe JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="3daa9-119">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="3daa9-120">Membros do JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="3daa9-120">JET_INSTANCE_INFO members</span></span>](./jet-instance-info-members.md)

[<span data-ttu-id="3daa9-121">Sobrecarga de Equals</span><span class="sxs-lookup"><span data-stu-id="3daa9-121">Equals overload</span></span>](./jet-instance-info.equals-method.md)

[<span data-ttu-id="3daa9-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3daa9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
