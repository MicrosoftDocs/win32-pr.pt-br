---
description: A classe WMI de associação Win32 ComClassAutoEmulator relaciona uma classe COM (Component Object Model) e outra classe COM que \_ ela emula automaticamente.
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Win32_ComClassAutoEmulator classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassAutoEmulator
- Win32_ComClassAutoEmulator.NewVersion
- Win32_ComClassAutoEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba849eed744ff342cfde10d0f31072d4e898cf52cf4e6966760f780236c56df4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986376"
---
# <a name="win32_comclassautoemulator-class"></a>Classe Win32 \_ ComClassAutoEmulator

A classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ Win32 ComClassAutoEmulator** relaciona uma classe COM (Component Object Model) e outra classe COM que ela emula automaticamente.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5D-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassAutoEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a>Membros

A **classe \_ ComClassAutoEmulator do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ ComClassAutoEmulator do Win32** tem essas propriedades.

<dl> <dt>

**NewVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Referência à instância que representa o componente COM que pode emular automaticamente o componente COM associado. Essas informações são obtidas por meio da entrada do Registro AutoTreatAs.

</dd> <dt>

**OldVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Referência à instância que representa o componente COM que é emulado automaticamente por outro componente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

