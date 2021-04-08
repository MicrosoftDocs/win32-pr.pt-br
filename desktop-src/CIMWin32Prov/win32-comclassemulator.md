---
description: A \_ classe WMI de associação ComClassEmulator do Win32 relaciona duas versões de uma classe com (Component Object Model).
ms.assetid: 33899c1e-911d-49ad-be25-355dcdb8f0c7
ms.tgt_platform: multiple
title: Classe Win32_ComClassEmulator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassEmulator
- Win32_ComClassEmulator.NewVersion
- Win32_ComClassEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9966ed85b0e0b4eeb25073e13ad679759f1d460b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088974"
---
# <a name="win32_comclassemulator-class"></a>\_Classe Win32 ComClassEmulator

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ ComClassEmulator do Win32** relaciona duas versões de uma classe com (Component Object Model).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5C-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ ComClassEmulator** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ ComClassEmulator** tem essas propriedades.

<dl> <dt>

**NewVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Referência à instância que representa o componente COM que contém interfaces que emulam a versão mais antiga do componente.

</dd> <dt>

**OldVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Referência à instância que representa o componente com com interfaces que podem ser emuladas pela nova versão do componente.

</dd> </dl>

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

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

