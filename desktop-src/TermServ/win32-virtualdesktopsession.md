---
title: Win32_VirtualDesktopSession classe
description: Gerencia uma sessão da área de trabalho virtual.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Win32_VirtualDesktopSession classe Serviços de Área de Trabalho Remota
- Win32_VirtualDesktopSession classe Serviços de Área de Trabalho Remota , descrito
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
ms.openlocfilehash: 01e039df658ded4534e3e2582f08ba4e5f5a04530d810349fff5633730a84332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137419"
---
# <a name="win32_virtualdesktopsession-class"></a>Classe Win32 \_ VirtualDesktopSession

Gerencia uma sessão da área de trabalho virtual.

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

A **classe Win32 \_ VirtualDesktopSession** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe Win32 \_ VirtualDesktopSession** tem esses métodos.



| Método                                                         | Descrição                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**Desconectar**](disconnect-win32-virtualdesktopsession.md)   | Desconecta a sessão da área de trabalho virtual.<br/>                        |
| [**Logoff**](logoff-win32-virtualdesktopsession.md)           | Faz o logs do usuário da sessão da área de trabalho virtual.<br/>             |
| [**SendMessage**](sendmessage-win32-virtualdesktopsession.md) | Envie uma mensagem ao usuário por meio da sessão da área de trabalho virtual.<br/> |



 

### <a name="properties"></a>Propriedades

A **classe Win32 \_ VirtualDesktopSession** tem essas propriedades.

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

**ConnectState**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
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

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém a ID da sessão da área de trabalho virtual.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o nome da conta de usuário atribuída à sessão.

</dd> <dt>

**VMHostName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém o nome do servidor Área de Trabalho Remota host de virtualização que hospeda a máquina virtual.

</dd> <dt>

**VMName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o nome da máquina virtual atribuída à sessão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Raiz \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Área de Trabalho Remota de Serviços de Gerenciamento do Área de Trabalho Remota](rdms-api-reference.md)
</dt> </dl>

 

