---
description: Representa uma especialização da associação de componentes do sistema que estabelece que o pool de recursos é definido no contexto do sistema.
ms.assetid: 72b68687-2b5f-4fef-bdca-a5c0bbfa3564
title: Msvm_HostedResourcePool classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedResourcePool
- Msvm_HostedResourcePool.GroupComponent
- Msvm_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ce61d5ee2c0b676e9c4ab6099bd592533e7821ae5cd529499c111f4c5349221e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531276"
---
# <a name="msvm_hostedresourcepool-class"></a>Classe \_ HostedResourcePool Msvm

Representa uma especialização da associação de componentes do sistema que estabelece que o pool de recursos é definido no contexto do sistema.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Composition, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedResourcePool : CIM_SystemComponent
{
  Msvm_ComputerSystem REF GroupComponent;
  CIM_ResourcePool    REF PartComponent;
};
```

## <a name="members"></a>Membros

A **classe \_ HostedResourcePool do Msvm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ HostedResourcePool Msvm** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

O sistema pai na associação.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ ResourcePool cim**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

O pool de recursos que é um componente do sistema.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

