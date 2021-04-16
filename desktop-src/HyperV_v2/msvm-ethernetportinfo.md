---
description: Uma associação entre uma instância da classe Msvm \_ EthernetSwitchPort e uma instância da \_ classe Msvm EthernetPortData que representa os dados coletados sobre a porta por uma extensão de comutador.
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Classe Msvm_EthernetPortInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c78dca7adedcf52d93530efdab0da6113855c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759243"
---
# <a name="msvm_ethernetportinfo-class"></a>\_Classe Msvm EthernetPortInfo

Uma associação entre uma instância da classe [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) e uma instância da classe [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md) que representa os dados coletados sobre a porta por uma extensão de comutador.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ EthernetPortInfo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ EthernetPortInfo** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ EthernetSwitchPort**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. Antecedent")
</dt> </dl>

Uma instância da classe [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) que representa a porta do comutador.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ EthernetPortData**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. dependent")
</dt> </dl>

Uma instância da classe [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md) que representa os dados da porta.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

