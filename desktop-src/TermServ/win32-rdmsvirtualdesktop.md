---
title: Classe Win32_RDMSVirtualDesktop
description: Representa uma área de trabalho virtual.
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSVirtualDesktop Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSVirtualDesktop classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787574"
---
# <a name="win32_rdmsvirtualdesktop-class"></a>\_Classe Win32 RDMSVirtualDesktop

Representa uma área de trabalho virtual.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ RDMSVirtualDesktop** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ RDMSVirtualDesktop** tem esses métodos.



| Método                                                                                              | Descrição                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**GetUserAssignment**](getuserassignment-win32-rdmsvirtualdesktop.md)                             | Recupera o nome de usuário e o domínio que é atribuído à área de trabalho virtual.<br/> |
| [**GetVirtualDesktopAssignedToUser**](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | Recupera a área de trabalho virtual que é atribuída ao usuário especificado.<br/>                       |
| [**GetVirtualDesktopDetails**](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | Recupera as informações adicionais sobre a área de trabalho virtual.<br/>                             |
| [**GetVirtualDesktopState**](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | Recupera o estado da área de trabalho virtual.<br/>                                                 |
| [**RemoveUserAssignment**](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | Remove a atribuição de usuário da área de trabalho virtual.<br/>                                       |
| [**SetUserAssignment**](setuserassignment-win32-rdmsvirtualdesktop.md)                             | Atribui uma área de trabalho virtual a um usuário.<br/>                                                        |
| [**SetVirtualDesktopState**](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | Atualiza o estado da área de trabalho virtual.<br/>                                                   |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ RDMSVirtualDesktop** tem essas propriedades.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém o alias para a coleção de áreas de trabalho virtuais que gerencia a máquina virtual.

</dd> <dt>

**HostName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o nome do computador que hospeda a máquina virtual.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém o nome da máquina virtual.

</dd> <dt>

**SessionState**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém o estado da sessão de área de trabalho virtual.

</dd> <dt>

**SessionUserName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém o nome de usuário que está conectado à sessão de área de trabalho virtual.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o status da máquina virtual.

</dd> <dt>

**UserDomain**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém o nome de domínio do usuário atribuído à área de trabalho virtual.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém o nome do usuário atribuído à área de trabalho virtual.

</dd> <dt>

**VMState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o estado da área de trabalho virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs cimv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Provedor de serviços de gerenciamento de Área de Trabalho Remota](rdms-api-reference.md)
</dt> </dl>

 

