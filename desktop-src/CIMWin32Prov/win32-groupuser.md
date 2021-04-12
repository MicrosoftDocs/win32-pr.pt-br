---
description: A \_ classe WMI de associação GroupUser do Win32 relaciona um grupo e uma conta que é membro desse grupo.
ms.assetid: 46dd65f0-b729-4b23-8a00-bc33d1a4868b
ms.tgt_platform: multiple
title: Classe Win32_GroupUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_GroupUser
- Win32_GroupUser.GroupComponent
- Win32_GroupUser.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 79035ff3c56331a240704cf6605fdf72efa4e81c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457119"
---
# <a name="win32_groupuser-class"></a>\_Classe Win32 GroupUser

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ GroupUser do Win32** relaciona um grupo e uma conta que é membro desse grupo.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C508-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_GroupUser : CIM_Component
{
  Win32_Group   REF GroupComponent;
  Win32_Account REF PartComponent;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ GroupUser** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ GroupUser** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ grupo Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| grupo WMI Win32 \_ ")
</dt> </dl>

Referência à instância que representa o grupo do qual a conta é membro.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ conta Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| conta WMI Win32 \_ ")
</dt> </dl>

Referência à instância que representa a conta de usuário ou sistema que faz parte de um grupo de contas.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ GroupUser** é derivada do [**\_ componente CIM**](cim-component.md).

## <a name="examples"></a>Exemplos

Para obter um exemplo do PowerShell de \_ como usar o Win32 GroupUser para recuperar uma lista de membros do grupo local, consulte o [exemplo listar membros do grupo local em um computador remoto usando o WMI e o PowerShell](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) na galeria do TechNet.

O exemplo de código VBScript do [recuperador de informações do WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) na galeria do TechNet usa a classe **Win32 \_ GroupUser** para recuperar informações do usuário de vários computadores remotos.

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

 

