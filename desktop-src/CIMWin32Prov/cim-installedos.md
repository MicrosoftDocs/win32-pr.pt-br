---
description: A \_ classe de associação CIM InstalledOS representa um link entre o sistema de computador e o sistema operacional instalado.
ms.assetid: 6db5b5a2-91b6-4540-83b8-bb9c86c7f94e
ms.tgt_platform: multiple
title: Classe CIM_InstalledOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledOS
- CIM_InstalledOS.PartComponent
- CIM_InstalledOS.GroupComponent
- CIM_InstalledOS.PrimaryOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a60bbd71993557eac238d6facd75d99b967b993a075cad726ccdef4625d6dce5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923406"
---
# <a name="cim_installedos-class"></a>\_Classe CIM InstalledOS

A classe de associação **CIM \_ InstalledOS** representa um link entre o sistema de computador e o sistema operacional instalado. Um sistema operacional é instalado quando está na extensão de armazenamento de um sistema de computador (por exemplo, copiado para uma unidade de disco ou baixado para memória).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8502C575-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_InstalledOS : CIM_SystemComponent
{
  CIM_OperatingSystem REF PartComponent;
  CIM_ComputerSystem  REF GroupComponent;
  boolean                 PrimaryOS;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ InstalledOS** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ InstalledOS** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sistema de ComputerSystem CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Um sistema de computadores [**CIM \_**](cim-computersystem.md) que descreve o computador.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: sistema **\_ operacional CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Um [**\_ OperatingSystem CIM**](cim-operatingsystem.md) que descreve o sistema operacional instalado no sistema de computador.

</dd> <dt>

**PrimaryOS**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sistema operacional DMTF \| 1,4 ")
</dt> </dl>

Se for **true**, o sistema operacional instalado será o sistema operacional padrão do sistema de computador.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ InstalledOS** é derivada de [**\_ Systemcomponent CIM**](cim-systemcomponent.md).

O WMI não implementa essa classe. Para classes derivadas do **CIM \_ InstalledOS**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> </dl>

 

