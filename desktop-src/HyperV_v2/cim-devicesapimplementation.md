---
description: Representa uma associação entre um ponto de acesso de serviço (SAP) e um dispositivo lógico que o implementa.
ms.assetid: 40c8111a-d439-4c0f-805e-9c10d7182eb4
title: Classe CIM_DeviceSAPImplementation (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Antecedent
- CIM_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e32676077cccd5c7e17fa551e904079f457b8d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787115"
---
# <a name="cim_devicesapimplementation-class-hyper-v-management"></a>Classe CIM_DeviceSAPImplementation (gerenciamento do Hyper-V)

Representa uma associação entre um ponto de acesso de serviço (SAP) e um dispositivo lógico que o implementa.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ DeviceSAPImplementation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ DeviceSAPImplementation** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ LogicalDevice CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

O dispositivo lógico.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

O SAP implementado pelo dispositivo lógico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

