---
description: Representa um elemento lógico que contém informações para representar e gerenciar a funcionalidade fornecida por um dispositivo ou recurso de software.
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: CIM_Service classe (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fc6182ce024b616c49552cf13878d9ec06da97bd0d0b4c7ff3696e7747a943a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899856"
---
# <a name="cim_service-class-hyper-v-management"></a>CIM_Service classe (gerenciamento do Hyper-V)

Representa um elemento lógico que contém informações para representar e gerenciar a funcionalidade fornecida por um dispositivo ou recurso de software. Um serviço é um objeto de uso geral para configurar e gerenciar a implementação da funcionalidade; não é a funcionalidade em si.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a>Membros

A **classe \_ serviço CIM** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ serviço CIM** tem esses métodos.



| Método                                           | Descrição                    |
|:-------------------------------------------------|:-------------------------------|
| [**Startservice**](cim-service-startservice.md) | Inicia o serviço.<br/> |
| [**StopService**](cim-service-stopservice.md)   | Interrompe o serviço.<br/>  |



 

### <a name="properties"></a>Propriedades

A **classe \_ serviço CIM** tem essas propriedades.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

O nome de classe usado para criar uma instância dessa classe. **CreationClassName** é combinado com outras propriedades de chave dessa classe para identificar exclusivamente as instâncias dessa classe e suas subclasses.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Um identificador exclusivo do serviço que indica a funcionalidade do serviço.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Informações gerais do DMTF \| \| 001.4")
</dt> </dl>

Informações de contato para o proprietário primário do serviço.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Informações gerais do DMTF \| \| 001.3")
</dt> </dl>

O nome do proprietário primário do serviço.

</dd> <dt>

**Iniciado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**true** se o serviço tiver sido iniciado; caso contrário, **false.**

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Serviço CIM \_**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Essa propriedade é preterida. Em vez disso, use **a propriedade EnabledDefault** herdada de [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).

> [!Note]  
> Descrição preterida: indica se o serviço é iniciado automaticamente (por exemplo, por um sistema operacional) ou iniciado somente mediante solicitação.

 

<dt>



 ("Automático")


</dt> <dd></dd> <dt>



 ("Manual")


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**")
</dt> </dl>

O nome de classe usado para criar uma instância do sistema que contém o serviço. **SystemCreationClassName** é combinado com outras propriedades de chave dessa classe para identificar exclusivamente as instâncias dessa classe e suas subclasses.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Nome**")
</dt> </dl>

O nome do sistema de scoping.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)
</dt> </dl>

 

