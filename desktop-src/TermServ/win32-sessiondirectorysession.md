---
title: Win32_SessionDirectorySession classe
description: Fornece propriedades para exibir as propriedades de uma sessão Conexão de Área de Trabalho Remota Broker (Agente de Conexão de Área de Trabalho Remota).
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectorySession classe Serviços de Área de Trabalho Remota
- Win32_SessionDirectorySession classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a7d883d3b356713f2f9c3d2b1f9de76676e845020b211ee8a600604a674c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118848190"
---
# <a name="win32_sessiondirectorysession-class"></a>Classe \_ SessionDirectorySession do Win32

Fornece propriedades para exibir as propriedades de uma sessão Conexão de Área de Trabalho Remota Broker (Agente de Conexão de Área de Trabalho Remota).

> [!Note]  
> No Windows Server 2008 R2, o nome do Agente de Sessão dos Serviços de Terminal (Agente de Sessão TS) foi alterado para Agente de Conexão de Área de Trabalho Remoto. Essas propriedades se aplicam a todos os sistemas operacionais com suporte, a menos que seja notado de outra forma.

 

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a>Membros

A **classe \_ SessionDirectorySession do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ SessionDirectorySession do Win32** tem essas propriedades.

<dl> <dt>

**ApplicationType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Aplicativo iniciado com esta sessão. Isso é o mesmo que a **propriedade StartProgram** de [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).

</dd> <dt>

**Colordepth**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Profundidade de cor da sessão, medida em bits por pixel.

</dd> <dt>

**CreateTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data e hora em que a sessão foi criada. Esse valor não é redefinido quando uma sessão é desconectada e reconectada.

</dd> <dt>

**DisconnectTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data e hora em que a sessão foi desconectada (se aplicável).

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome de domínio do usuário conectado a esta sessão.

</dd> <dt>

**ResolutionHeight**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Altura da sessão, em pixels, para esta sessão.

</dd> <dt>

**ResolutionWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Largura da sessão, em pixels, para esta sessão.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereço IP do servidor do Agente de Conexão de RD para esta sessão.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome do servidor do Agente de Conexão de RD para esta sessão.

</dd> <dt>

**Sessionid**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

ID da sessão para esta sessão.

</dd> <dt>

**Sessionstate**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Estado desta sessão.

<dt>

0
</dt> <dd>

A sessão está ativa.

</dd> <dt>

1
</dt> <dd>

A sessão está desconectada.

</dd> </dl>

</dd> <dt>

**TSProtocol**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Protocolo para esta sessão.

<dt>

0
</dt> <dd>

Esta sessão está em execução em um console físico.

</dd> <dt>

1
</dt> <dd>

Um protocolo proprietário de terceiros é usado para esta sessão.

</dd> <dt>

2
</dt> <dd>

protocolo RDP (RDP) é usado para esta sessão.

</dd> </dl>

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome de usuário do usuário conectado a esta sessão.

</dd> </dl>

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ SessionDirectoryCluster**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**\_SessionDirectoryServer Win32**](win32-sessiondirectoryserver.md)
</dt> </dl>

 

