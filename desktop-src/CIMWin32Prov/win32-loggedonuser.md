---
description: A classe WMI de associação Win32 \_ LoggedOnUser relaciona uma sessão e uma conta de usuário.
ms.assetid: b1233f90-4898-4ced-84d2-0858027e935a
ms.tgt_platform: multiple
title: Win32_LoggedOnUser classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoggedOnUser
- Win32_LoggedOnUser.Dependent
- Win32_LoggedOnUser.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73cb34246f7b31393527aef053c0cb8cbd12702217dd7113d5714ac022bc3716
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973441"
---
# <a name="win32_loggedonuser-class"></a>Classe Win32 \_ LoggedOnUser

A classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **Win32 \_ LoggedOnUser** relaciona uma sessão e uma conta de usuário.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8BB5B3EC-E1F7-4b39-942A-605D5F55789A}"), AMENDMENT]
class Win32_LoggedOnUser : CIM_Dependency
{
  Win32_LogonSession REF Dependent;
  Win32_Account      REF Antecedent;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ LoggedOnUser** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ LoggedOnUser** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Conta win32 \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Uma [**conta do Win32 \_**](win32-account.md) que descreve a conta usada no início desta sessão. A conta pode ser uma conta de usuário ou uma conta do sistema.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ LogonSession do Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependente), [**chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Uma [**\_ LogonSession do Win32**](win32-logonsessionmappeddisk.md) que descreve a sessão que a conta está usando no momento.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe Win32 \_ LoggedOnUser** é derivada da [**\_ Dependência CIM.**](cim-dependency.md)

## <a name="examples"></a>Exemplos

O [exemplo de função get-loggedonuser](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) do PowerShell obtém os usuários conectados em um computador local ou remoto, com informações de sessão.

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

[**Dependência cim \_**](cim-dependency.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

