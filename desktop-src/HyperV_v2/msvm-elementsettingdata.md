---
description: Associa um elemento gerenciado a seus dados de configuração.
ms.assetid: 4DB78E43-E387-478E-999C-770B35925721
title: Classe Msvm_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementSettingData
- Msvm_ElementSettingData.ManagedElement
- Msvm_ElementSettingData.SettingData
- Msvm_ElementSettingData.IsDefault
- Msvm_ElementSettingData.IsCurrent
- Msvm_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f4d2af614e3b161f49a0d37d1e4d1ee48ce0aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759244"
---
# <a name="msvm_elementsettingdata-class"></a>\_Classe Msvm ElementSettingData

Associa um elemento gerenciado a seus dados de configuração. Alguns dos aplicativos mais notáveis dessa associação são o seu uso na vinculação de uma máquina virtual e dos dispositivos lógicos que foram atribuídos a esse sistema com suas informações de configuração de instantâneo. As informações de configuração atuais são associadas à máquina virtual e seus dispositivos por meio da Associação [**Msvm \_ SettingsDefineState**](msvm-settingsdefinestate.md) .

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementSettingData : CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault = 0;
  uint16                 IsCurrent = 0;
  uint16                 IsNext = 0;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ ElementSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ElementSettingData** tem essas propriedades.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica que a configuração referenciada está sendo usada no momento na operação do elemento ou que essas informações são desconhecidas. Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata). O valor padrão é 0 (desconhecido).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Está atual** (1)
</dt> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Não é atual** (2)
</dt> </dl>

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica que a configuração referenciada é uma configuração padrão para o elemento ou que essas informações são desconhecidas. Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata). O valor padrão é 0 (desconhecido).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**É padrão** (1)
</dt> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Não é o padrão** (2)
</dt> </dl>

</dd> <dt>

**Isnext**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a configuração referenciada é a próxima configuração a ser aplicada. Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata). O valor padrão é 0 (desconhecido).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**É próximo** (1)
</dt> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Não é próximo** (2)
</dt> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**É o próximo para uso único** (3)
</dt> </dl>

</dd> <dt>

**Managedelement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência à máquina virtual ou dispositivo virtual. Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência às configurações de instantâneo para a máquina virtual ou dispositivo virtual. Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ ElementSettingData** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemplos

Consulte [consultando objetos de rede](querying-networking-objects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ELEMENTSETTINGDATA CIM**](cim-elementsettingdata.md)
</dt> <dt>

[**\_ELEMENTSETTINGDATA CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)
</dt> <dt>

[Classes de gerenciamento do sistema virtual](virtual-system-management-classes.md)
</dt> </dl>

 

