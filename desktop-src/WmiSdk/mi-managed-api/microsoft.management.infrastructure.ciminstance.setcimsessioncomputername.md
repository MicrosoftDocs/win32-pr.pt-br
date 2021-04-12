---
description: 'Saiba mais sobre: método CimInstance. SetCimSessionComputerName (cadeia de caracteres)'
title: Método CimInstance.SetCimSessionComputerName (Microsoft.Management.Infrastructure)
TOCTitle: CimInstance.SetCimSessionComputerName method (Microsoft.Management.Infrastructure)
ms:assetid: M:Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName(System.String)
ms.date: 11/12/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName
- Microsoft::Management::Infrastructure::CimInstance::SetCimSessionComputerName
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: b9f4cd9d308617a2369eaa542705e4ad7f854fa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296948"
---
# <a name="ciminstancesetcimsessioncomputername-method-string"></a><span data-ttu-id="91651-103">Método CimInstance. SetCimSessionComputerName (cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="91651-103">CimInstance.SetCimSessionComputerName method (String)</span></span>

<span data-ttu-id="91651-104">Define o nome do computador usado para a sessão CIM.</span><span class="sxs-lookup"><span data-stu-id="91651-104">Sets the name of the computer used for the CIM session.</span></span>

<span data-ttu-id="91651-105">**Namespace:**   [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="91651-105">**Namespace:**   [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))</span></span>  
<span data-ttu-id="91651-106">**Assembly:**  Microsoft. Management. Infrastructure (em Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="91651-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="91651-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91651-107">Syntax</span></span>

``` csharp
public void SetCimSessionComputerName(
    string computerName
)
```

``` c++
public:
void SetCimSessionComputerName(
    String^ computerName
)
```

``` fsharp
member SetCimSessionComputerName : 
        computerName:string -> unit
```

``` vb
Public Sub SetCimSessionComputerName (
    computerName As String
)
```

#### <a name="parameters"></a><span data-ttu-id="91651-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91651-108">Parameters</span></span>

  - <span data-ttu-id="91651-109">computerName</span><span class="sxs-lookup"><span data-stu-id="91651-109">computerName</span></span>  
    <span data-ttu-id="91651-110">Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="91651-110">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="91651-111">O nome do computador usado para a sessão CIM.</span><span class="sxs-lookup"><span data-stu-id="91651-111">The name of the computer used for the CIM session.</span></span> <span data-ttu-id="91651-112">**NULL** se a instância atual for somente do lado do cliente ou se a instância foi recuperada do localhost.</span><span class="sxs-lookup"><span data-stu-id="91651-112">**null** if the current instance is client-side only, or if the instance was retrieved from localhost.</span></span>

## <a name="see-also"></a><span data-ttu-id="91651-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="91651-113">See also</span></span>

<span data-ttu-id="91651-114">[Classe CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="91651-114">[CimInstance Class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336\(v=vs.85\))</span></span>  
<span data-ttu-id="91651-115">[Namespace Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="91651-115">[Microsoft.Management.Infrastructure namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))</span></span>
