---
description: Descreve as restrições nas propriedades de um objeto CIM \_ EnabledLogicalElement associado.
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: CIM_EnabledLogicalElementCapabilities classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElementCapabilities
- CIM_EnabledLogicalElementCapabilities.ElementNameEditSupported
- CIM_EnabledLogicalElementCapabilities.MaxElementNameLen
- CIM_EnabledLogicalElementCapabilities.RequestedStatesSupported
- CIM_EnabledLogicalElementCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbec7b52d735b6dcff4da4c211da1db8b36d18adf20798fdcaa3932e1761119a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695906"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a>Classe CIM \_ EnabledLogicalElementCapabilities

Descreve as restrições nas propriedades de um objeto [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md) associado.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_EnabledLogicalElementCapabilities : CIM_Capabilities
{
  boolean ElementNameEditSupported;
  uint16  MaxElementNameLen;
  uint16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ EnabledLogicalElementCapabilities** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ EnabledLogicalElementCapabilities** tem essas propriedades.

<dl> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI. INCITS-T11 \| SWAPI \_ UNIT \_ CONFIG CAPS T \_ \_ \| EditName"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedElement**](cim-managedelement.md).**ElementName**")
</dt> </dl>

**true** se a **propriedade ElementName** do elemento lógico habilitado puder ser modificada; caso contrário, **false.**

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElementCapabilities**.**MaxElementNameLen**")
</dt> </dl>

Uma expressão regular que indica as restrições na **propriedade ElementName** do elemento lógico enable. Consulte *ABNF padrão DMTF com o Guia de Uso* da Especificação do Perfil de Gerenciamento , apêndice C para ver a sintaxe permitida.

> [!Note]  
> Se essa propriedade e **a propriedade ElementNameMask** do elemento lógico enable descreverem o comprimento máximo de **ElementName**, o valor menor será usado.

 

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI. INCITS-T11 \| SWAPI \_ UNIT \_ CONFIG CAPS T \_ \_ \| MaxNameChars"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ FCSwitchCapabilities.ElementNameEditSupported", "**CIM \_ EnabledLogicalElementCapabilities**.**ElementNameMask**")
</dt> </dl>

O comprimento máximo com suporte da propriedade **ElementName** do elemento lógico habilitado.

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")
</dt> </dl>

Os possíveis estados que podem ser solicitados no elemento lógico habilitado pelo [**método RequestStateChange.**](cim-enabledlogicalelement-requeststatechange.md)

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Desligar** (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Teste** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**Adiar** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Quiesce** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Reinicializar** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Redefinir** (11)


</dt> <dd></dd> </dl>

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

[**Funcionalidades cim \_**](cim-capabilities.md)
</dt> </dl>

 

