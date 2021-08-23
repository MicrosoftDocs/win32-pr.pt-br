---
description: Uma associação que conecta um serviço com opção virtual a um serviço de ponte transparente.
ms.assetid: 4DFD73CA-38F0-4C06-BEBE-C684590E50E8
title: Msvm_HostedSwitchService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedSwitchService
- Msvm_HostedSwitchService.Antecedent
- Msvm_HostedSwitchService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 634cff066c602cc4eb684bd7e1a016f9f9c925f19db25a0556fd37cc1e27c5f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531266"
---
# <a name="msvm_hostedswitchservice-class"></a>Classe Msvm \_ HostedSwitchService

Uma associação que conecta um serviço com opção virtual a um serviço de ponte transparente.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedSwitchService : CIM_HostedService
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  CIM_Service                REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ HostedSwitchService** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ HostedSwitchService** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Uma referência a uma instância da [**classe Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa o comutadores virtuais.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Serviço CIM \_**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Uma referência a uma instância da [**classe Msvm \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) que representa o serviço de ponte.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe \_ HostedSwitchService do Msvm** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ HostedService**](cim-hostedservice.md)
</dt> <dt>

[**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> </dl>

 

