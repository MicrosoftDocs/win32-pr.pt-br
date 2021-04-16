---
description: 'Saiba mais sobre: Propriedade SystemParameters. EnableAdvanced'
title: Propriedade SystemParameters. EnableAdvanced
TOCTitle: 'EnableAdvanced property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableadvanced(v=EXCHG.10)
ms:contentKeyID: 55104116
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e311685bf5ef436be11d4593523aceee73b955b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765043"
---
# <a name="systemparametersenableadvanced-property"></a><span data-ttu-id="d931d-103">Propriedade SystemParameters. EnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="d931d-103">SystemParameters.EnableAdvanced property</span></span>

<span data-ttu-id="d931d-104">Obtém ou define um valor que indica se o mecanismo de banco de dados aceita ou rejeita alterações em um subconjunto dos parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="d931d-104">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="d931d-105">Esse parâmetro é usado em conjunto com a [configuração](./systemparameters.configuration-property.md) para impedir que alguns parâmetros do sistema sejam definidos fora dos padrões da configuração selecionada.</span><span class="sxs-lookup"><span data-stu-id="d931d-105">This parameter is used in conjunction with [Configuration](./systemparameters.configuration-property.md) to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="d931d-106">Com suporte no Windows Vista e em cima.</span><span class="sxs-lookup"><span data-stu-id="d931d-106">Supported on Windows Vista and up.</span></span> <span data-ttu-id="d931d-107">Ignorado no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d931d-107">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="d931d-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d931d-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d931d-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d931d-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d931d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d931d-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Property EnableAdvanced As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableAdvanced

SystemParameters.EnableAdvanced = value
```

``` csharp
public static bool EnableAdvanced { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="d931d-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d931d-111">Property value</span></span>

<span data-ttu-id="d931d-112">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="d931d-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="d931d-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="d931d-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d931d-114">Referência</span><span class="sxs-lookup"><span data-stu-id="d931d-114">Reference</span></span>

[<span data-ttu-id="d931d-115">Classe SystemParameters</span><span class="sxs-lookup"><span data-stu-id="d931d-115">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="d931d-116">Membros do SystemParameters</span><span class="sxs-lookup"><span data-stu-id="d931d-116">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="d931d-117">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d931d-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
