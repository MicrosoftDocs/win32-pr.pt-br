---
description: A \_ classe WMI de associação abstrata COMApplicationClasses do Win32 relaciona um componente com (Component Object Model) e o aplicativo com onde ele reside.
ms.assetid: 7c188199-86fb-45ba-b318-9d9529b831b8
ms.tgt_platform: multiple
title: Classe Win32_COMApplicationClasses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationClasses
- Win32_COMApplicationClasses.PartComponent
- Win32_COMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01413128f7457049a4383c1148938e2136645337
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089470"
---
# <a name="win32_comapplicationclasses-class"></a>\_Classe Win32 COMApplicationClasses

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação abstrata **\_ COMApplicationClasses do Win32** relaciona um componente com (Component Object Model) e o aplicativo com onde ele reside.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract, UUID("{0F73ED51-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationClasses : CIM_Component
{
  Win32_COMClass       REF PartComponent;
  Win32_COMApplication REF GroupComponent;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ COMApplicationClasses** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ COMApplicationClasses** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ aplicativo Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| aplicativo WMI Win32 \_ ")
</dt> </dl>

Um [**\_ aplicativo do Win32**](win32-comapplication.md) que representa o aplicativo com que contém o componente com.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ COMClass**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ COMClass")
</dt> </dl>

Um [**\_ COMClass do Win32**](win32-comclass.md) que representa o componente com agrupado sob o aplicativo com.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ COMApplicationClasses** é derivada do [**\_ componente CIM**](cim-component.md).

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

[**\_Componente CIM**](cim-component.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

