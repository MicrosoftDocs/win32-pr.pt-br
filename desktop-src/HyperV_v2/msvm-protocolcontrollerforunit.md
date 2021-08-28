---
description: Essa associação indica que uma subclasse de dispositivo lógico (por exemplo, um volume de armazenamento) está conectada por meio de um controlador de protocolo específico.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Msvm_ProtocolControllerForUnit classe
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
ms.openlocfilehash: 73b8478e561d53212e0439219622595751ad954e13d0d086fabdbf57a483039d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086626"
---
# <a name="msvm_protocolcontrollerforunit-class"></a>Classe \_ ProtocolControllerForUnit Msvm

Essa associação indica que uma subclasse de dispositivo lógico (por exemplo, um volume de armazenamento) está conectada por meio de um controlador de protocolo específico. Em muitas situações (por exemplo, mascaramento de LUN de armazenamento), pode haver muitas dessas associações usadas para se relacionar a objetos diferentes. Portanto, as subclasses foram definidas para otimizar a enumeração das associações.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

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

A **classe \_ ProtocolControllerForUnit Msvm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ ProtocolControllerForUnit Msvm** tem essas propriedades.

<dl> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A prioridade dada aos acessos do dispositivo por meio desse controlador. O caminho de prioridade mais alta terá o valor mais baixo para esse parâmetro. Essa classe é herdada de **Cim \_ ProtocolControllerForDevice**.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o controlador está ordenando ativamente ou acessando o dispositivo (2) ou não (3). Além disso, o valor 0 (Desconhecido) pode ser definido. Essas informações são necessárias quando um dispositivo lógico pode ser comandoado por vários controladores de protocolo ou acessados por meio de vários controladores de protocolo. Essa classe é herdada de **Cim \_ ProtocolControllerForDevice**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Ativo** (2)
</dt> <dt>

<span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inativo** (3 )
</dt> </dl>

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Protocolo \_ CIMController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O controlador de protocolo. Essa classe é herdada da [**\_ Dependência CIM.**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Cim \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O dispositivo controlado. Essa classe é herdada da [**\_ Dependência CIM.**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> <dt>

**DeviceAccess**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os direitos de acesso concedidos ao dispositivo por meio desse controlador. Essa classe é herdada de **CIM \_ ProtocolControllerForUnit**.



| Valor                                                                               | Significado                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>        | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>        | Leitura/Gravação<br/>      |
| <dl> <dt>3</dt> </dl>        | Somente leitura<br/>       |
| <dl> <dt>4</dt> </dl>        | Sem acesso.<br/>      |
| <dl> <dt>5..15999</dt> </dl> | DMTF Reservado<br/>   |
| <dl> <dt>16000..</dt> </dl>  | Fornecedor reservado<br/> |



 

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço do dispositivo associado no contexto do controlador antecessor. Essa classe é herdada de **Cim \_ ProtocolControllerForDevice**.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe \_ ProtocolControllerForUnit do Msvm** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**Protocolo \_ CIMControllerForUnit**](cim-protocolcontrollerforunit.md)
</dt> <dt>

[**Protocolo \_ CIMControllerForUnit**](/previous-versions//cc150672(v=vs.85))
</dt> <dt>

[Armazenamento Classes](storage-classes.md)
</dt> </dl>

 

