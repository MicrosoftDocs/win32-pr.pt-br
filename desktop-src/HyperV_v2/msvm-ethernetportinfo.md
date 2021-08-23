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
ms.openlocfilehash: 3ef8f8f4ab7191400cfead94d20c4f601b97e48d46ee160d31c7b26b8e567b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524886"
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
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

