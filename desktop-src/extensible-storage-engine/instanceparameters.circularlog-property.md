---
description: 'Saiba mais sobre a propriedade: Instanceparameters. CircularLog'
title: Propriedade instanceparameters. CircularLog
TOCTitle: 'CircularLog property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.circularlog(v=EXCHG.10)
ms:contentKeyID: 55103320
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CircularLog
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f9a77aa0d0f60b49269dc939787b165a3f2f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793633"
---
# <a name="instanceparameterscircularlog-property"></a><span data-ttu-id="14207-103">Propriedade instanceparameters. CircularLog</span><span class="sxs-lookup"><span data-stu-id="14207-103">InstanceParameters.CircularLog property</span></span>

<span data-ttu-id="14207-104">Obtém ou define um valor que indica se o log circular está ativado.</span><span class="sxs-lookup"><span data-stu-id="14207-104">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="14207-105">Quando o log circular está desativado, todos os arquivos de log de transações gerados são mantidos no disco até que não sejam mais necessários porque um backup completo do banco de dados foi executado.</span><span class="sxs-lookup"><span data-stu-id="14207-105">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="14207-106">Quando o log circular está ativado, somente os arquivos de log de transações mais jovens do que o ponto de verificação atual são mantidos no disco.</span><span class="sxs-lookup"><span data-stu-id="14207-106">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="14207-107">O benefício desse modo é que os backups não são necessários para desativar arquivos de log de transação antigos.</span><span class="sxs-lookup"><span data-stu-id="14207-107">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span>

<span data-ttu-id="14207-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="14207-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="14207-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="14207-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="14207-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="14207-110">Syntax</span></span>

``` vb
'Declaration
Public Property CircularLog As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CircularLog

instance.CircularLog = value
```

``` csharp
public bool CircularLog { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="14207-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="14207-111">Property value</span></span>

<span data-ttu-id="14207-112">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="14207-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="14207-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="14207-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="14207-114">Referência</span><span class="sxs-lookup"><span data-stu-id="14207-114">Reference</span></span>

[<span data-ttu-id="14207-115">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="14207-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="14207-116">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="14207-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="14207-117">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="14207-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
