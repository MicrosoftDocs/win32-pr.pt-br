---
description: Associa dados de configurações a um elemento gerenciado.
ms.assetid: 3fdf111b-3ec1-4559-94ce-27d6a8cd0080
title: Classe CIM_SettingsDefineState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineState
- CIM_SettingsDefineState.ManagedElement
- CIM_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4278043511348f3df5f72886f0c96bf18a34158a61b31a4590f880c7a1c0f150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647264"
---
# <a name="cim_settingsdefinestate-class"></a>\_Classe CIM SettingsDefineState

Associa dados de configurações a um elemento gerenciado.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Settings")]
class CIM_SettingsDefineState
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ SettingsDefineState** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ SettingsDefineState** tem essas propriedades.

<dl> <dt>

**Managedelement**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ managedelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O elemento gerenciado na associação.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ SettingData**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Os dados de configurações na associação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

