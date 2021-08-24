---
description: A classe WMI de associação Win32 ClassicCOMApplicationClasses relaciona um aplicativo COM e um \_ componente COM agrupados sob ele.
ms.assetid: 77f24461-9ca0-4fc3-8728-4a4b9a1edbc3
ms.tgt_platform: multiple
title: Win32_ClassicCOMApplicationClasses classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMApplicationClasses
- Win32_ClassicCOMApplicationClasses.PartComponent
- Win32_ClassicCOMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24bc2871afa5916644a3bcdb3ddb4ad2f653e7aa1cd0522c52782ef17bb2352c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751385"
---
# <a name="win32_classiccomapplicationclasses-class"></a>Classe Win32 \_ ClassicCOMApplicationClasses

A classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **Win32 \_ ClassicCOMApplicationClasses** relaciona um aplicativo COM e um componente COM agrupados sob ele.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED54-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMApplicationClasses : Win32_COMApplicationClasses
{
  Win32_ClassicCOMClass REF PartComponent;
  Win32_DCOMApplication REF GroupComponent;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ ClassicCOMApplicationClasses** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ ClassicCOMApplicationClasses** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Win32 DCOMApplication**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")
</dt> </dl>

Um [**\_ DCOMApplication Win32 que**](win32-dcomapplication.md) representa um aplicativo DCOM que contém ou usa o componente COM.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Um [**Win32 \_ ClassicCOMClass**](win32-classiccomclass.md) que representa o componente COM existente no ou usado pelo aplicativo DCOM.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe Win32 \_ ClassicCOMApplicationClasses** é derivada de [**Win32 \_ COMApplicationClasses**](win32-comapplicationclasses.md).

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

[**Win32 \_ COMApplicationClasses**](win32-comapplicationclasses.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

