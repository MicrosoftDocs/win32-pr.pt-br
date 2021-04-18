---
description: 'Saiba mais sobre: método conversões. LCMapFlagsFromCompareOptions'
title: Método conversões. LCMapFlagsFromCompareOptions
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808322"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a><span data-ttu-id="4191d-103">Método conversões. LCMapFlagsFromCompareOptions</span><span class="sxs-lookup"><span data-stu-id="4191d-103">Conversions.LCMapFlagsFromCompareOptions method</span></span>

<span data-ttu-id="4191d-104">Forneça CompareOptions, transforme-os em sinalizadores de LCMapString.</span><span class="sxs-lookup"><span data-stu-id="4191d-104">Give CompareOptions, turn them into flags from LCMapString.</span></span> <span data-ttu-id="4191d-105">Opções desconhecidas são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="4191d-105">Unknown options are ignored.</span></span>

<span data-ttu-id="4191d-106">Esta API não está em conformidade com CLS.</span><span class="sxs-lookup"><span data-stu-id="4191d-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="4191d-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4191d-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4191d-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4191d-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4191d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4191d-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a><span data-ttu-id="4191d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4191d-110">Parameters</span></span>

  - <span data-ttu-id="4191d-111">compareOptions</span><span class="sxs-lookup"><span data-stu-id="4191d-111">compareOptions</span></span>  
    <span data-ttu-id="4191d-112">Tipo: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="4191d-112">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
    
    <span data-ttu-id="4191d-113">As opções a serem convertidas.</span><span class="sxs-lookup"><span data-stu-id="4191d-113">The options to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4191d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4191d-114">Return value</span></span>

<span data-ttu-id="4191d-115">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="4191d-115">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
<span data-ttu-id="4191d-116">Os sinalizadores LCMapString que correspondem às opções de comparação.</span><span class="sxs-lookup"><span data-stu-id="4191d-116">The LCMapString flags that match the compare options.</span></span> <span data-ttu-id="4191d-117">As opções sem suporte são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="4191d-117">Unsupported options are ignored.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4191d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="4191d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4191d-119">Referência</span><span class="sxs-lookup"><span data-stu-id="4191d-119">Reference</span></span>

[<span data-ttu-id="4191d-120">Classe conversões</span><span class="sxs-lookup"><span data-stu-id="4191d-120">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="4191d-121">Membros de conversões</span><span class="sxs-lookup"><span data-stu-id="4191d-121">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="4191d-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4191d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
