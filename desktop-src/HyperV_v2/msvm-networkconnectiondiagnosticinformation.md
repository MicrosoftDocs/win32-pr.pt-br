---
description: Fornece informações sobre a conectividade de rede para uma máquina virtual.
ms.assetid: 59503c1b-203b-46ec-8a65-f21a746f170f
title: Classe Msvm_NetworkConnectionDiagnosticInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticInformation
- Msvm_NetworkConnectionDiagnosticInformation.RoundTripTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 416392702e5bc06e54fe5a23b6784b87e98b7027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922695"
---
# <a name="msvm_networkconnectiondiagnosticinformation-class"></a>\_Classe Msvm NetworkConnectionDiagnosticInformation

Fornece informações sobre a conectividade de rede para uma máquina virtual.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticInformation
{
  uint32 RoundTripTime;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ NetworkConnectionDiagnosticInformation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ NetworkConnectionDiagnosticInformation** tem essas propriedades.

<dl> <dt>

**RoundTripTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tempo de ida e volta para a solicitação ping.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




