---
title: Win32_TSGatewayLoadBalancer classe
description: Descreve um conjunto de servidores de balanceamento de carga Área de Trabalho Remota Gateway de RD (Gateway de RD). Eles são usados para balancear a carga de conexões do Gateway de Área de Trabalho Trabalho Em vários servidores.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayLoadBalancer classe Serviços de Área de Trabalho Remota
- Win32_TSGatewayLoadBalancer classe Serviços de Área de Trabalho Remota , descrito
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
ms.openlocfilehash: 584077911faf8593e7c26aadd36ca17a0a11d82b18d1d6ade20be1f1444fedf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769866"
---
# <a name="win32_tsgatewayloadbalancer-class"></a>Classe Win32 \_ TSGatewayLoadBalancer

Descreve um conjunto de servidores de balanceamento de carga Área de Trabalho Remota Gateway de RD (Gateway de RD). Eles são usados para balancear a carga de conexões do Gateway de Área de Trabalho Trabalho Em vários servidores.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ TSGatewayLoadBalancer** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe Win32 \_ TSGatewayLoadBalancer** tem esses métodos.



| Método                                                                             | Descrição                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**AddServers**](addservers-win32-tsgatewayloadbalancer.md)                       | Adiciona servidores à **propriedade Servers.**<br/>                                                             |
| [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md)           | Exclui todos os servidores de balanceamento de carga do Gateway de Área de Trabalho Local que participam do farm de balanceamento de carga.<br/>               |
| [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)                 | Exclui servidores da **propriedade Servers.**<br/>                                                        |
| [**IsLoadBalancingServer**](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | Determina se o servidor pode executar o balanceamento de carga.<br/>                                             |
| [**SetServers**](setservers-win32-tsgatewayloadbalancer.md)                       | Define a **propriedade Servers** com a lista separada por ponto e vírgula de servidores de balanceamento de carga do Gateway de RD.<br/> |



 

### <a name="properties"></a>Propriedades

A **classe Win32 \_ TSGatewayLoadBalancer** tem essas propriedades.

<dl> <dt>

**Servidores**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Lista separada por ponto e vírgula de servidores de balanceamento de carga do Gateway de RD. Essa propriedade pode ser alterada com os métodos [**SetServers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers,**](addservers-win32-tsgatewayloadbalancer.md) [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)e [**DeleteAllServers.**](deleteallservers-win32-tsgatewayloadbalancer.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para usar essa classe.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

