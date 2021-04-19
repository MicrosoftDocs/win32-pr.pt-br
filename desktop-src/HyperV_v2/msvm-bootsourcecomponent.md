---
description: Associa o Msvm \_ BootSourceSettingData ao VirtualSystemSettingData Msvm geral \_ .
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Classe Msvm_BootSourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dfe86fa7882b1b20e5b5abbbdaa9d4f37f231f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778752"
---
# <a name="msvm_bootsourcecomponent-class"></a>\_Classe Msvm BootSourceComponent

Associa o [**Msvm \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md) ao [**\_ VirtualSystemSettingData Msvm**](msvm-virtualsystemsettingdata.md)geral. Essa classe deriva do [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ BootSourceComponent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ BootSourceComponent** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao elemento pai na associação. Esta propriedade é herdada [**do \_ componente CIM**](cim-component.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao elemento filho na associação. Esta propriedade é herdada [**do \_ componente CIM**](cim-component.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Componente CIM**](cim-component.md)
</dt> <dt>

[**\_Componente CIM**](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[**Msvm \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md)
</dt> <dt>

[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 

