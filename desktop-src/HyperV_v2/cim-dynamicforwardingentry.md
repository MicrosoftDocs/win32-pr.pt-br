---
description: Representa uma entrada no banco de dados de encaminhamento associado à \_ classe CIM TransparentBridgingService.
ms.assetid: 4c3afe7c-f7e5-4a83-8ba1-f0b1909cee52
title: Classe CIM_DynamicForwardingEntry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DynamicForwardingEntry
- CIM_DynamicForwardingEntry.SystemCreationClassName
- CIM_DynamicForwardingEntry.SystemName
- CIM_DynamicForwardingEntry.ServiceCreationClassName
- CIM_DynamicForwardingEntry.ServiceName
- CIM_DynamicForwardingEntry.CreationClassName
- CIM_DynamicForwardingEntry.MACAddress
- CIM_DynamicForwardingEntry.DynamicStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65cf4f1bc5e678089d54dd99a09a6d3b7aeb3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759252"
---
# <a name="cim_dynamicforwardingentry-class"></a>\_Classe CIM DynamicForwardingEntry

Representa uma entrada no banco de dados de encaminhamento associado à classe [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) .

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_DynamicForwardingEntry : CIM_LogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string ServiceCreationClassName;
  string ServiceName;
  string CreationClassName;
  string MACAddress;
  uint16 DynamicStatus;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ DynamicForwardingEntry** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ DynamicForwardingEntry** tem essas propriedades.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

O nome da classe ou da subclasse usada para criar a instância. Quando usado com as outras propriedades de chave dessa classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

</dd> <dt>

**DynamicStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpFdbStatus ")
</dt> </dl>

O status da entrada.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>

**Inválido** (2)


</dt> <dd></dd> <dt>

<span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>

**Aprendido** (3)


</dt> <dd></dd> <dt>

<span id="Self"></span><span id="self"></span><span id="SELF"></span>

Por **conta própria** (4)


</dt> <dd></dd> <dt>

<span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>

**Gerenciamento** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpFdbAddress ")
</dt> </dl>

O endereço MAC unicast para o qual o serviço de ponte filtra informações. O endereço MAC é formatado como doze dígitos hexadecimais, como 010203040506, com cada par que representa um dos seis octetos do endereço MAC na ordem de bits canônica de acordo com a RFC 2469.

</dd> <dt>

**ServiceCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ serviço CIM**](cim-service.md).**CreationClassName**")
</dt> </dl>

O valor de **CreationClassName** do objeto de serviço de escopo.

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ serviço CIM**](cim-service.md).**Nome**")
</dt> </dl>

O nome do serviço de escopo.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**")
</dt> </dl>

O valor de **CreationClassName** do objeto do sistema de escopo.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Nome**")
</dt> </dl>

O nome do sistema de escopo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> </dl>

 

