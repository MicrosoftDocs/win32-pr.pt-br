---
description: 'Saiba mais sobre: método Windows8Api. JetGetErrorInfo'
title: Método Windows8Api. JetGetErrorInfo (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetGetErrorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo(Microsoft.Isam.Esent.Interop.JET_err,Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetgeterrorinfo(v=EXCHG.10)
ms:contentKeyID: 55104459
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c94e6594c2d52769f5034bdf1c7253bee838edaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761292"
---
# <a name="windows8apijetgeterrorinfo-method"></a><span data-ttu-id="97071-103">Método Windows8Api. JetGetErrorInfo</span><span class="sxs-lookup"><span data-stu-id="97071-103">Windows8Api.JetGetErrorInfo method</span></span>

<span data-ttu-id="97071-104">Obtém informações estendidas sobre um erro.</span><span class="sxs-lookup"><span data-stu-id="97071-104">Gets extended information about an error.</span></span>

<span data-ttu-id="97071-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="97071-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="97071-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="97071-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="97071-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97071-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetErrorInfo ( _
    error As JET_err, _
    <OutAttribute> ByRef errinfo As JET_ERRINFOBASIC _
)
'Usage
Dim error As JET_err
Dim errinfo As JET_ERRINFOBASICWindows8Api.JetGetErrorInfo(error, errinfo)
```

``` csharp
public static void JetGetErrorInfo(
    JET_err error,
    out JET_ERRINFOBASIC errinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="97071-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97071-108">Parameters</span></span>

  - <span data-ttu-id="97071-109">erro</span><span class="sxs-lookup"><span data-stu-id="97071-109">error</span></span>  
    <span data-ttu-id="97071-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="97071-110">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="97071-111">O código de erro sobre o qual recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="97071-111">The error code about which to retrieve information.</span></span>

<!-- end list -->

  - <span data-ttu-id="97071-112">errinfo</span><span class="sxs-lookup"><span data-stu-id="97071-112">errinfo</span></span>  
    <span data-ttu-id="97071-113">Tipo: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)</span><span class="sxs-lookup"><span data-stu-id="97071-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)</span></span>  
    
    <span data-ttu-id="97071-114">Informações sobre o código de erro especificado.</span><span class="sxs-lookup"><span data-stu-id="97071-114">Information about the specified error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="97071-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="97071-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="97071-116">Referência</span><span class="sxs-lookup"><span data-stu-id="97071-116">Reference</span></span>

[<span data-ttu-id="97071-117">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="97071-117">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="97071-118">Membros do Windows8Api</span><span class="sxs-lookup"><span data-stu-id="97071-118">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="97071-119">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="97071-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
