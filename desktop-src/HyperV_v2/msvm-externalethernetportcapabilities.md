---
description: Descreve os recursos do ExternalEthernetPort Msvm associado \_ .
ms.assetid: 63731b62-b1c7-4dd9-b906-03225bbc3154
title: Classe Msvm_ExternalEthernetPortCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPortCapabilities
- Msvm_ExternalEthernetPortCapabilities.InstanceID
- Msvm_ExternalEthernetPortCapabilities.Caption
- Msvm_ExternalEthernetPortCapabilities.Description
- Msvm_ExternalEthernetPortCapabilities.ElementName
- Msvm_ExternalEthernetPortCapabilities.IOVSupport
- Msvm_ExternalEthernetPortCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 748b207151fb1d11b013af7c736de52bbe5bec8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827302"
---
# <a name="msvm_externalethernetportcapabilities-class"></a>\_Classe Msvm ExternalEthernetPortCapabilities

Descreve os recursos do [**\_ ExternalEthernetPort Msvm**](msvm-externalethernetport.md)associado.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPortCapabilities : CIM_Capabilities
{
  string  InstanceID;
  string  Caption = "Ethernet Port Capabilities";
  string  Description = "Describes the capabilities of the Microsoft External Ethernet Port";
  string  ElementName = "Ethernet Port Capabilities";
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ ExternalEthernetPortCapabilities** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ExternalEthernetPortCapabilities** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "capacidades de porta Ethernet".

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "descreve os recursos da porta Ethernet externa da Microsoft".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "capacidades de porta Ethernet".

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

**IOVSupport**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um valor booliano que indica se o adaptador de rede oferece suporte a virtualização de e/s (IOV). Se o valor for **true**, a IOV será suportada pelo adaptador de rede e a propriedade **IOVSupportReasons** estará vazia. Caso contrário, a propriedade **IOVSupportReasons** terá os motivos pelos quais a IOV não tem suporte.

</dd> <dt>

**IOVSupportReasons**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de cadeias de caracteres que indica as possíveis razões pelas quais a IOV não tem suporte. Se o valor de **IOVSupport** for **true**, essa matriz estará vazia.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

