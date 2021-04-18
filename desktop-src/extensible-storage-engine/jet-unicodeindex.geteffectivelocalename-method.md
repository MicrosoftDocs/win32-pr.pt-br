---
description: 'Saiba mais sobre: JET_UNICODEINDEX. Método GetEffectiveLocaleName'
title: JET_UNICODEINDEX. Método GetEffectiveLocaleName
TOCTitle: 'GetEffectiveLocaleName method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_unicodeindex.geteffectivelocalename(v=EXCHG.10)
ms:contentKeyID: 55103988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 012ed93015705454efdf5e329d4b385924f1a343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813640"
---
# <a name="jet_unicodeindexgeteffectivelocalename-method"></a><span data-ttu-id="ea4ee-103">JET_UNICODEINDEX. Método GetEffectiveLocaleName</span><span class="sxs-lookup"><span data-stu-id="ea4ee-103">JET_UNICODEINDEX.GetEffectiveLocaleName method</span></span>

<span data-ttu-id="ea4ee-104">Como solução alternativa para sistemas que não têm suporte a LCID, converteremos um número muito limitado de LCIDs em nomes de localidade.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-104">As a workaround for systems that do not have LCID support, we will convert a VERY limited number of LCIDs to locale names.</span></span>

<span data-ttu-id="ea4ee-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ea4ee-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ea4ee-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ea4ee-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4ee-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea4ee-107">Syntax</span></span>

``` vb
'Declaration
Public Function GetEffectiveLocaleName As String
'Usage
Dim instance As JET_UNICODEINDEX
Dim returnValue As String

returnValue = instance.GetEffectiveLocaleName()
```

``` csharp
public string GetEffectiveLocaleName()
```

#### <a name="return-value"></a><span data-ttu-id="ea4ee-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea4ee-108">Return value</span></span>

<span data-ttu-id="ea4ee-109">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ea4ee-109">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="ea4ee-110">Um nome de localidade do estilo BCP-47.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-110">A BCP-47 style locale name.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ea4ee-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea4ee-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ea4ee-112">Referência</span><span class="sxs-lookup"><span data-stu-id="ea4ee-112">Reference</span></span>

[<span data-ttu-id="ea4ee-113">Classe JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="ea4ee-113">JET_UNICODEINDEX class</span></span>](./jet-unicodeindex-class.md)

[<span data-ttu-id="ea4ee-114">Membros do JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="ea4ee-114">JET_UNICODEINDEX members</span></span>](./jet-unicodeindex-members.md)

[<span data-ttu-id="ea4ee-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ea4ee-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
