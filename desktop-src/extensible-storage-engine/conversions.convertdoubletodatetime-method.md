---
description: 'Saiba mais sobre: método conversões. ConvertDoubleToDateTime'
title: Método conversões. ConvertDoubleToDateTime
TOCTitle: 'ConvertDoubleToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime(System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.convertdoubletodatetime(v=EXCHG.10)
ms:contentKeyID: 55101133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1d066780ade3da95f4d4d5500143700f7a7d5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785046"
---
# <a name="conversionsconvertdoubletodatetime-method"></a><span data-ttu-id="3979c-103">Método conversões. ConvertDoubleToDateTime</span><span class="sxs-lookup"><span data-stu-id="3979c-103">Conversions.ConvertDoubleToDateTime method</span></span>

<span data-ttu-id="3979c-104">Converta um Double (formato de data e hora do OA) em um DateTime.</span><span class="sxs-lookup"><span data-stu-id="3979c-104">Convert a double (OA date time format) to a DateTime.</span></span> <span data-ttu-id="3979c-105">Diferente de DateTime. FromOADate, isso não gera exceções.</span><span class="sxs-lookup"><span data-stu-id="3979c-105">Unlike DateTime.FromOADate this doesn't throw exceptions.</span></span>

<span data-ttu-id="3979c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3979c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3979c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3979c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3979c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3979c-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function ConvertDoubleToDateTime ( _
    d As Double _
) As DateTime
'Usage
Dim d As Double
Dim returnValue As DateTime

returnValue = Conversions.ConvertDoubleToDateTime(d)
```

``` csharp
public static DateTime ConvertDoubleToDateTime(
    double d
)
```

#### <a name="parameters"></a><span data-ttu-id="3979c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3979c-109">Parameters</span></span>

  - <span data-ttu-id="3979c-110">d</span><span class="sxs-lookup"><span data-stu-id="3979c-110">d</span></span>  
    <span data-ttu-id="3979c-111">Tipo: [System. Double](/dotnet/api/system.double)</span><span class="sxs-lookup"><span data-stu-id="3979c-111">Type: [System.Double](/dotnet/api/system.double)</span></span>  
    
    <span data-ttu-id="3979c-112">O valor Double.</span><span class="sxs-lookup"><span data-stu-id="3979c-112">The double value.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3979c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3979c-113">Return value</span></span>

<span data-ttu-id="3979c-114">Tipo: [System. DateTime](/dotnet/api/system.datetime)</span><span class="sxs-lookup"><span data-stu-id="3979c-114">Type: [System.DateTime](/dotnet/api/system.datetime)</span></span>  
<span data-ttu-id="3979c-115">Um DateTime.</span><span class="sxs-lookup"><span data-stu-id="3979c-115">A DateTime.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3979c-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="3979c-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3979c-117">Referência</span><span class="sxs-lookup"><span data-stu-id="3979c-117">Reference</span></span>

[<span data-ttu-id="3979c-118">Classe conversões</span><span class="sxs-lookup"><span data-stu-id="3979c-118">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="3979c-119">Membros de conversões</span><span class="sxs-lookup"><span data-stu-id="3979c-119">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="3979c-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3979c-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
