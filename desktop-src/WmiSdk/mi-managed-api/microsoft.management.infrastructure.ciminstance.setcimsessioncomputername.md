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
ms.openlocfilehash: c3f3c3cbe93710f5f9a796463539ad754c1f2e50ce5524c90a5f639021e716bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131108"
---
# <a name="ciminstancesetcimsessioncomputername-method-string"></a>Método CimInstance. SetCimSessionComputerName (cadeia de caracteres)

Define o nome do computador usado para a sessão CIM.

**Namespace:**   [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))  
**Assembly:**  Microsoft. Management. Infrastructure (em Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Sintaxe

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

#### <a name="parameters"></a>Parâmetros

  - computerName  
    Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    O nome do computador usado para a sessão CIM. **NULL** se a instância atual for somente do lado do cliente ou se a instância foi recuperada do localhost.

## <a name="see-also"></a>Confira também

[Classe CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336\(v=vs.85\))  
[Namespace Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))
