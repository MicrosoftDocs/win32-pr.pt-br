---
description: Representa uma associação entre uma instância de Msvm \_ GuestServiceInterfaceComponent e uma instância de Msvm \_ GuestService, que representa um serviço em execução no convidado.
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Classe Msvm_RegisteredGuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf2e551a30f169477f9dc73e58ecd9e6c3a78b708c047eb0088f36782623da3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130436"
---
# <a name="msvm_registeredguestservice-class"></a>\_Classe Msvm RegisteredGuestService

Representa uma associação entre uma instância de [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) e uma instância de [**Msvm \_ GuestService**](msvm-guestservice.md), que representa um serviço em execução no convidado. Essa classe deriva da classe de [**\_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ RegisteredGuestService** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ RegisteredGuestService** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. Antecedent")
</dt> </dl>

Referência ao componente de interface do serviço de convidado nesta associação.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ GuestService**](msvm-guestservice.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. dependent")
</dt> </dl>

Referência ao serviço convidado registrado que é dependente da propriedade **Antecedent** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> <dt>

[**\_Dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

