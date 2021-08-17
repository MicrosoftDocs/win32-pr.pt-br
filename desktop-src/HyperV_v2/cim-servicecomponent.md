---
description: Representa uma associação na qual um serviço é um componente de um serviço pai, que juntos formam um serviço de nível superior.
ms.assetid: c629d59d-d9d3-4019-a378-cd1d4d31a5d9
title: CIM_ServiceComponent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceComponent
- CIM_ServiceComponent.GroupComponent
- CIM_ServiceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a7684b22bc7488093702e5050524ac6c36f719dd985f537570e0eb1395756e7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647541"
---
# <a name="cim_servicecomponent-class"></a>Classe CIM \_ ServiceComponent

Representa uma associação na qual um serviço é um componente de um serviço pai, que juntos formam um serviço de nível superior.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceComponent : CIM_Component
{
  CIM_Service REF GroupComponent;
  CIM_Service REF PartComponent;
};
```

## <a name="members"></a>Membros

A **classe \_ ServiceComponent cim** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ ServiceComponent cim** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Serviço CIM \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

O serviço pai.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Serviço CIM \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

O serviço de componente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Componente \_ CIM**](cim-component.md)
</dt> </dl>

 

