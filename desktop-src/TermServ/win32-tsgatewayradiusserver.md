---
title: Classe Win32_TSGatewayRADIUSServer
description: Descreve um servidor serviço RADIUS (RADIUS), que tem um conjunto de Serviços de Área de Trabalho Remota políticas de autorização de conexão (RD \ 160; CAPs).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayRADIUSServer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayRADIUSServer classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9997494f9e93980ac4d6e4b1dcb9c95b0d7665a70226f77d1cd4c7ca3ad751d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769836"
---
# <a name="win32_tsgatewayradiusserver-class"></a>\_Classe Win32 TSGatewayRADIUSServer

Descreve um servidor serviço RADIUS (RADIUS), que tem um conjunto de Serviços de Área de Trabalho Remota RD CAPs (políticas de autorização de conexão).

O RADIUS é um protocolo padrão da indústria que é usado para transmitir informações de autenticação, autorização e configuração entre um computador servidor e um servidor de autenticação, chamado de servidor RADIUS, com um banco de dados que armazena informações do usuário. Para obter mais informações, consulte [protocolo RADIUS](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSGatewayRADIUSServer** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSGatewayRADIUSServer** tem esses métodos.



| Método                                                                 | Descrição                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Agrega**](win32-tsgatewayradiusserver-add.md)                         | Adiciona um novo servidor RADIUS.<br/>                                         |
| [**MoveDown**](movedown-win32-tsgatewayradiusserver.md)               | Move esse servidor RADIUS uma posição para baixo na ordem de prioridade.<br/> |
| [**MoveUp**](moveup-win32-tsgatewayradiusserver.md)                   | Move este servidor RADIUS uma posição para cima na ordem de prioridade.<br/>   |
| [**Remover**](win32-tsgatewayradiusserver-remove.md)                   | Remove o servidor RADIUS atual.<br/>                                |
| [**SetName**](setname-win32-tsgatewayradiusserver.md)                 | Define a propriedade **Name** para este servidor RADIUS.<br/>                |
| [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) | Define a propriedade **SharedSecret** para esse servidor RADIUS.<br/>        |
| [**Atualizar**](update-win32-tsgatewayradiusserver.md)                   | Atualiza o servidor RADIUS atual.<br/>                                |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSGatewayRADIUSServer** tem essas propriedades.

<dl> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome do servidor RADIUS. Essa propriedade pode ser alterada com o método [**SetName**](setname-win32-tsgatewayradiusserver.md) .

</dd> <dt>

**Prioridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Prioridade do servidor RADIUS. O servidor de gateway de área de trabalho remota procura RD CAPs em servidores RADIUS com base na prioridade. Essa propriedade pode ser alterada com os métodos [**moveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md)e [**Remove**](win32-tsgatewayradiusserver-remove.md) .

</dd> <dt>

**SharedSecret**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Segredo compartilhado para o servidor RADIUS. Essa propriedade pode ser alterada com o método [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para usar essa classe.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

