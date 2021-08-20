---
description: Representa uma associação entre um sistema de computador e seu instantâneo de sistema virtual aplicado mais recentemente.
ms.assetid: 722491a3-1c46-4d37-8bd6-7c7d6648a806
title: Classe CIM_LastAppliedSnapshot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSnapshot
- CIM_LastAppliedSnapshot.Antecedent
- CIM_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d5b9cbc34d1f2fa8e5daf83012783898feb7973894d9dd7a5f667adc8524bef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812192"
---
# <a name="cim_lastappliedsnapshot-class"></a>\_Classe CIM LastAppliedSnapshot

Representa uma associação entre um sistema de computador e seu instantâneo de sistema virtual aplicado mais recentemente.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_LastAppliedSnapshot : CIM_Dependency
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ LastAppliedSnapshot** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ LastAppliedSnapshot** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

O instantâneo do sistema virtual que foi aplicado pela última vez no sistema de computador.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sistema de ComputerSystem CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

O sistema do computador.

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

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

