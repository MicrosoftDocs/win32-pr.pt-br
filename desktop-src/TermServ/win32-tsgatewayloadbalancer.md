---
title: Classe Win32_TSGatewayLoadBalancer
description: Descreve um conjunto de servidores de balanceamento de carga de gateway de Área de Trabalho Remota (gateway de área de trabalho remota). Eles são usados para balancear a carga de conexões de gateway de área de trabalho remota em vários servidores.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayLoadBalancer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayLoadBalancer classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4956ed4dc9536ff6f7e3263071a2a477cb0f515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644587"
---
# <a name="win32_tsgatewayloadbalancer-class"></a>\_Classe Win32 TSGatewayLoadBalancer

Descreve um conjunto de servidores de balanceamento de carga de gateway de Área de Trabalho Remota (gateway de área de trabalho remota). Eles são usados para balancear a carga de conexões de gateway de área de trabalho remota em vários servidores.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSGatewayLoadBalancer** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSGatewayLoadBalancer** tem esses métodos.



| Método                                                                             | Descrição                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**Addservers**](addservers-win32-tsgatewayloadbalancer.md)                       | Adiciona servidores à propriedade **servidores** .<br/>                                                             |
| [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md)           | Exclui todos os servidores de balanceamento de carga do gateway de área de trabalho remota que participam do farm de balanceamento de carga.<br/>               |
| [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)                 | Exclui servidores da propriedade **servidores** .<br/>                                                        |
| [**IsLoadBalancingServer**](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | Determina se o servidor pode executar o balanceamento de carga.<br/>                                             |
| [**Setservers**](setservers-win32-tsgatewayloadbalancer.md)                       | Define a propriedade **Servers** com a lista separada por ponto e vírgula dos servidores de balanceamento de carga do gateway de área de trabalho remota.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSGatewayLoadBalancer** tem essas propriedades.

<dl> <dt>

**Servidores**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Lista separada por ponto e vírgula dos servidores de balanceamento de carga do gateway de área de trabalho remota. Essa propriedade pode ser alterada com os métodos [**Setservers**](setservers-win32-tsgatewayloadbalancer.md), [**addservers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)e [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para usar essa classe.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

