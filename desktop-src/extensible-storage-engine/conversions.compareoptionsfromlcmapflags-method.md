---
description: 'Saiba mais sobre: método conversões. CompareOptionsFromLCMapFlags'
title: Método conversões. CompareOptionsFromLCMapFlags
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79e0d6a92aef75f3758adc16e9c82de81b8c6962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164797"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a><span data-ttu-id="9256f-103">Método conversões. CompareOptionsFromLCMapFlags</span><span class="sxs-lookup"><span data-stu-id="9256f-103">Conversions.CompareOptionsFromLCMapFlags method</span></span>

<span data-ttu-id="9256f-104">Determinados sinalizadores para LCMapFlags, transforme-os em opções de comparação.</span><span class="sxs-lookup"><span data-stu-id="9256f-104">Given flags for LCMapFlags, turn them into compare options.</span></span> <span data-ttu-id="9256f-105">Opções desconhecidas são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="9256f-105">Unknown options are ignored.</span></span>

<span data-ttu-id="9256f-106">Esta API não está em conformidade com CLS.</span><span class="sxs-lookup"><span data-stu-id="9256f-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="9256f-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9256f-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9256f-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9256f-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9256f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9256f-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a><span data-ttu-id="9256f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9256f-110">Parameters</span></span>

  - <span data-ttu-id="9256f-111">lcmapFlags</span><span class="sxs-lookup"><span data-stu-id="9256f-111">lcmapFlags</span></span>  
    <span data-ttu-id="9256f-112">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="9256f-112">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="9256f-113">Sinalizadores LCMapString.</span><span class="sxs-lookup"><span data-stu-id="9256f-113">LCMapString flags.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9256f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9256f-114">Return value</span></span>

<span data-ttu-id="9256f-115">Tipo: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="9256f-115">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
<span data-ttu-id="9256f-116">CompareOptions que descreve os sinalizadores (conhecidos).</span><span class="sxs-lookup"><span data-stu-id="9256f-116">CompareOptions describing the (known) flags.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9256f-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="9256f-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9256f-118">Referência</span><span class="sxs-lookup"><span data-stu-id="9256f-118">Reference</span></span>

[<span data-ttu-id="9256f-119">Classe conversões</span><span class="sxs-lookup"><span data-stu-id="9256f-119">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="9256f-120">Membros de conversões</span><span class="sxs-lookup"><span data-stu-id="9256f-120">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="9256f-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9256f-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
