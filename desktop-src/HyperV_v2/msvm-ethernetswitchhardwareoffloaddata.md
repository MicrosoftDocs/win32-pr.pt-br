---
description: Representa o status de descarregamento de hardware do comutador.
ms.assetid: 77a34df7-e3c4-4d91-af5a-91a03dd8246d
title: Classe Msvm_EthernetSwitchHardwareOffloadData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadData
- Msvm_EthernetSwitchHardwareOffloadData.InstanceID
- Msvm_EthernetSwitchHardwareOffloadData.Caption
- Msvm_EthernetSwitchHardwareOffloadData.Description
- Msvm_EthernetSwitchHardwareOffloadData.ElementName
- Msvm_EthernetSwitchHardwareOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.SystemName
- Msvm_EthernetSwitchHardwareOffloadData.CreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.Name
- Msvm_EthernetSwitchHardwareOffloadData.IovVfCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovVfUsage
- Msvm_EthernetSwitchHardwareOffloadData.VmqCapacity
- Msvm_EthernetSwitchHardwareOffloadData.VmqUsage
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSACapacity
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSAUsage
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchHardwareOffloadData.PacketDirectInUse
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssMinQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b64762b824cea7d3b064636e7f7f87777e053daf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750844"
---
# <a name="msvm_ethernetswitchhardwareoffloaddata-class"></a>\_Classe Msvm EthernetSwitchHardwareOffloadData

Representa o status de descarregamento de hardware do comutador.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1C37E01C-0CD6-496F-9076-90C131033DC2"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Offload Resource Status"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadData : Msvm_EthernetSwitchData
{
  string  InstanceID;
  string  Caption = Ethernet Switch Offload Resource Status;
  string  Description = Represents the switch hardware offload status.;
  string  ElementName = Ethernet Switch Offload Resource Status;
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  CreationClassName = "Msvm_EthernetSwitchHardwareOffloadData";
  string  Name;
  uint32  IovVfCapacity = 0;
  uint32  IovVfUsage = 0;
  uint32  VmqCapacity = 0;
  uint32  VmqUsage = 0;
  uint32  IPsecSACapacity = 0;
  uint32  IPsecSAUsage = 0;
  uint32  IovQueuePairCapacity = 0;
  uint32  IovQueuePairUsage = 0;
  boolean PacketDirectInUse = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 0;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 0;
  uint32  DefaultQueueVrssMinQueuePairs = 0;
  boolean DefaultQueueVmmqEnabled = FALSE;
  boolean DefaultQueueVrssEnabled = FALSE;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ EthernetSwitchHardwareOffloadData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ EthernetSwitchHardwareOffloadData** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**, **maxlen** (256)
</dt> </dl>

O nome da classe ou subclasse usada na criação dessa instância. Esta propriedade é herdada de [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).

</dd> <dt>

**DefaultQueueVmmqEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

A configuração de VMMQ atual para a fila padrão

> [!Note]  
> Propriedade adicionada no Windows 10, versão 1703.

 

</dd> <dt>

**DefaultQueueVmmqQueuePairs**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

O número atual de filas alocadas para a fila padrão

> [!Note]  
> Propriedade adicionada no Windows 10, versão 1703.

 

</dd> <dt>

**DefaultQueueVrssEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

A configuração de VRss atual para a fila padrão

> [!Note]  
> Propriedade adicionada no Windows 10, versão 1703.

 

</dd> <dt>

**DefaultQueueVrssExcludePrimaryProcessor**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Indica se a CPU de VMQ primária foi excluída da tabela de indireção VRSS/VMMQ.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**DefaultQueueVrssIndependentHostSpreading**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Indica se a difusão do VRSS deve ser sempre feita para a fila padrão, independentemente do estado de RSS do vPort externo.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**DefaultQueueVrssMinQueuePairs**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Indica o número mínimo de filas usadas para VRSS/VMMQ.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**DefaultQueueVrssQueueSchedulingMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Indica como as filas VRSS/VMMQ são direcionadas para processadores de host diferentes.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**IovQueuePairCapacity**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O número máximo de pares de fila com suporte no comutador.

</dd> <dt>

**IovQueuePairUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O número atual de pares de fila que estão sendo usados pelo comutador.

</dd> <dt>

**IovVfCapacity**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O número máximo de funções virtuais com suporte no comutador.

</dd> <dt>

**IovVfUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O número atual de funções virtuais que estão sendo usadas pelo comutador.

</dd> <dt>

**IPsecSACapacity**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O número máximo de descarregamentos de associação de segurança IPsec com suporte no comutador.

</dd> <dt>

**IPsecSAUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O número atual de descarregamentos de associação de segurança IPsec que estão sendo usados pelo comutador.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**, **substituição**, **maxlen** (256)
</dt> </dl>

O nome exclusivo do recurso. Esta propriedade é herdada de [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).

</dd> <dt>

**PacketDirectInUse**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica se o pacote direto está sendo usado pelo comutador

> [!Note]  
> Propriedade adicionada no Windows 10.

 

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**, **maxlen** (256)
</dt> </dl>

O nome da classe de criação do sistema de hospedagem. Esta propriedade é herdada de [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**, **maxlen** (256)
</dt> </dl>

O nome do comutador virtual ao qual a instância de recurso associada está associada. Esta propriedade é herdada de [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).

</dd> <dt>

**VmqCapacity**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O número máximo de descarregamentos de fila de máquina virtual com suporte no comutador.

</dd> <dt>

**VmqUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O número atual de descarregamentos de fila de máquina virtual que estão sendo usados pelo comutador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

