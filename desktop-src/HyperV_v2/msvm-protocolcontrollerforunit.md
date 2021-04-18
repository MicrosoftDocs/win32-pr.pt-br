---
description: Essa associação indica que uma subclasse de dispositivo lógico (por exemplo, um volume de armazenamento) é conectada por meio de um controlador de protocolo específico.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Classe Msvm_ProtocolControllerForUnit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1470192fc4f10e60bdfef013146483b47cbfa7f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761710"
---
# <a name="msvm_protocolcontrollerforunit-class"></a>\_Classe Msvm ProtocolControllerForUnit

Essa associação indica que uma subclasse de dispositivo lógico (por exemplo, um volume de armazenamento) é conectada por meio de um controlador de protocolo específico. Em muitas situações (por exemplo, mascaramento de LUN de armazenamento), pode haver muitas dessas associações usadas para se relacionar a objetos diferentes. Portanto, as subclasses foram definidas para otimizar a enumeração das associações.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ ProtocolControllerForUnit** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ProtocolControllerForUnit** tem essas propriedades.

<dl> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A prioridade fornecida para acessar o dispositivo por meio desse controlador. O caminho de prioridade mais alta terá o valor mais baixo para esse parâmetro. Essa classe é herdada do **CIM \_ ProtocolControllerForDevice**.

</dd> <dt>

**Accessstate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o controlador está ativando ou acessando ativamente o dispositivo (2) ou não (3). Além disso, o valor, 0 (desconhecido), pode ser definido. Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores de protocolo. Essa classe é herdada do **CIM \_ ProtocolControllerForDevice**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Ativo** (2)
</dt> <dt>

<span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inativo** (3)
</dt> </dl>

</dd> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O controlador de protocolo. Essa classe é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O dispositivo controlado. Essa classe é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**DeviceAccess**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os direitos de acesso concedidos ao dispositivo por meio desse controlador. Essa classe é herdada do **CIM \_ ProtocolControllerForUnit**.



| Valor                                                                               | Significado                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>        | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>        | Leitura/Gravação<br/>      |
| <dl> <dt>3</dt> </dl>        | Somente leitura<br/>       |
| <dl> <dt>4</dt> </dl>        | Sem acesso.<br/>      |
| <dl> <dt>5.. 15999</dt> </dl> | DMTF reservado<br/>   |
| <dl> <dt>16000..</dt> </dl>  | Fornecedor reservado<br/> |



 

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço do dispositivo associado no contexto do controlador Antecedent. Essa classe é herdada do **CIM \_ ProtocolControllerForDevice**.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ ProtocolControllerForUnit** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_PROTOCOLCONTROLLERFORUNIT CIM**](cim-protocolcontrollerforunit.md)
</dt> <dt>

[**\_PROTOCOLCONTROLLERFORUNIT CIM**](/previous-versions//cc150672(v=vs.85))
</dt> <dt>

[Classes de armazenamento](storage-classes.md)
</dt> </dl>

 

