---
title: Classe Win32_VirtualDesktopSession
description: Gerencia uma sessão de área de trabalho virtual.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Classe de Win32_VirtualDesktopSession Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_VirtualDesktopSession classe, descrita
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f343c1dc022dcb4759f813de956ade27e1aff213
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454724"
---
# <a name="win32_virtualdesktopsession-class"></a>\_Classe Win32 VirtualDesktopSession

Gerencia uma sessão de área de trabalho virtual.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ VirtualDesktopSession** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ VirtualDesktopSession** tem esses métodos.



| Método                                                         | Descrição                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**Desconectar**](disconnect-win32-virtualdesktopsession.md)   | Desconecta a sessão de área de trabalho virtual.<br/>                        |
| [**Verbos**](logoff-win32-virtualdesktopsession.md)           | Faz logoff do usuário da sessão de área de trabalho virtual.<br/>             |
| [**SendMessage**](sendmessage-win32-virtualdesktopsession.md) | Envie uma mensagem para o usuário por meio da sessão de área de trabalho virtual.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ VirtualDesktopSession** tem essas propriedades.

<dl> <dt>

**ClientMachineName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o nome do computador cliente que está conectado à sessão.

</dd> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o nome da coleção de áreas de trabalho virtuais que hospeda a máquina virtual.

</dd> <dt>

**Connectstate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o estado da conexão com a sessão.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o nome de domínio do usuário.

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém a ID da sessão de área de trabalho virtual.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o nome da conta de usuário que é atribuída à sessão.

</dd> <dt>

**VMHostName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém o nome do servidor host de virtualização Área de Trabalho Remota que hospeda a máquina virtual.

</dd> <dt>

**VMName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o nome da máquina virtual que é atribuída à sessão.

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

 

