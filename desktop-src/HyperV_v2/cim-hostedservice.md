---
description: Representa uma associação entre um serviço e o sistema que hospeda o serviço. Um Sistema pode hospedar muitos serviços, no entanto, essa classe não representa serviços hospedados em vários sistemas.
ms.assetid: ede67a81-cf1b-41aa-b907-5b635cf80423
title: CIM_HostedService classe (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Antecedent
- CIM_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65667d46ea3af91f33a118d49902c77e411fc56959eb1f1345d4b42fab372270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648551"
---
# <a name="cim_hostedservice-class-hyper-v-management"></a>CIM_HostedService classe (gerenciamento do Hyper-V)

Representa uma associação entre um serviço e o sistema que hospeda o serviço. Um Sistema pode hospedar muitos serviços, no entanto, essa classe não representa serviços hospedados em vários sistemas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_HostedService : CIM_HostedDependency
{
  CIM_System  REF Antecedent;
  CIM_Service REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ HostedService** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ HostedService** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Sistema CIM \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

O sistema de hospedagem.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Serviço CIM \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente"), [**Fraco**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

O serviço hospedado no sistema.

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

[**CIM \_ HostedDependency**](cim-hosteddependency.md)
</dt> </dl>

 

