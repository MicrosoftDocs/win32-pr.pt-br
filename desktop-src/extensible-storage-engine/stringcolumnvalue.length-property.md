---
description: 'Saiba mais sobre a propriedade: StringColumnValue. Length'
title: Propriedade StringColumnValue. Length
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55104090
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Length
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed7313f66bd25653a66ebd8567a21c0ad5431ec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170722"
---
# <a name="stringcolumnvaluelength-property"></a><span data-ttu-id="78aaf-103">Propriedade StringColumnValue. Length</span><span class="sxs-lookup"><span data-stu-id="78aaf-103">StringColumnValue.Length property</span></span>

<span data-ttu-id="78aaf-104">Obtém o comprimento de bytes de um valor de coluna, que será zero se a coluna for nula, caso contrário, ela corresponderá ao comprimento de byte do valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="78aaf-104">Gets the byte length of a column value, which is zero if column is null, otherwise it matches the byte length of the string value.</span></span> <span data-ttu-id="78aaf-105">O comprimento do byte é determinado na suposição de dois bytes por caractere.</span><span class="sxs-lookup"><span data-stu-id="78aaf-105">The byte length is determined in assumption of two bytes per character.</span></span>

<span data-ttu-id="78aaf-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="78aaf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="78aaf-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="78aaf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="78aaf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="78aaf-108">Syntax</span></span>

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As StringColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public override int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="78aaf-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="78aaf-109">Property value</span></span>

<span data-ttu-id="78aaf-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="78aaf-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="78aaf-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="78aaf-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="78aaf-112">Referência</span><span class="sxs-lookup"><span data-stu-id="78aaf-112">Reference</span></span>

[<span data-ttu-id="78aaf-113">Classe StringColumnValue</span><span class="sxs-lookup"><span data-stu-id="78aaf-113">StringColumnValue class</span></span>](./stringcolumnvalue-class.md)

[<span data-ttu-id="78aaf-114">Membros do StringColumnValue</span><span class="sxs-lookup"><span data-stu-id="78aaf-114">StringColumnValue members</span></span>](./stringcolumnvalue-members.md)

[<span data-ttu-id="78aaf-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="78aaf-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
