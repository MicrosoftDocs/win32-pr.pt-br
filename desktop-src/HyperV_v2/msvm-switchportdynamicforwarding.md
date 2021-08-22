---
description: Conecta uma porta switch a uma entrada de encaminhamento dinâmico (endereço MAC aprendido).
ms.assetid: 70687D56-1282-46C7-AB4E-60E32B9DBA14
title: Msvm_SwitchPortDynamicForwarding classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SwitchPortDynamicForwarding
- Msvm_SwitchPortDynamicForwarding.Antecedent
- Msvm_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d5deb326877e7af639c7bc18a73a8c968e75c26b64d690d4a4582085833fa23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950065"
---
# <a name="msvm_switchportdynamicforwarding-class"></a>Classe Msvm \_ SwitchPortDynamicForwarding

Conecta uma porta switch a uma entrada de encaminhamento dinâmico (endereço MAC aprendido). Isso é útil para localizar todos os endereços MAC aprendidos para uma porta especificada.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SwitchPortDynamicForwarding : CIM_SwitchPortDynamicForwarding
{
  Msvm_EthernetSwitchPort     REF Antecedent;
  Msvm_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ SwitchPortDynamicForwarding** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ SwitchPortDynamicForwarding** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ EthernetSwitchPort Msvm**](msvm-ethernetswitchport.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

Uma referência a uma instância da [**classe \_ EthernetSwitchPort Msvm**](msvm-ethernetswitchport.md) que representa a porta do comutar.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

Uma referência a uma instância da [**classe Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) que representa a entrada de encaminhamento dinâmico do banco de dados de encaminhamento.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe Msvm \_ SwitchPortDynamicForwarding** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemplos

Consulte [Consultando objetos de rede](querying-networking-objects.md).

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

[**CIM \_ SwitchPortDynamicForwarding**](cim-switchportdynamicforwarding.md)
</dt> <dt>

[**CIM \_ SwitchPortDynamicForwarding**](/previous-versions//cc136921(v=vs.85))
</dt> </dl>

 

