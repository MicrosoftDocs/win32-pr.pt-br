---
title: Criar método da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Cria uma política Área de Trabalho Remota de autorização de recursos (RD \ 160; VIOLA).
ms.assetid: 3301a543-cdf9-4528-a29e-691054ef81c9
ms.tgt_platform: multiple
keywords:
- Criar método Serviços de Área de Trabalho Remota
- Criar método Serviços de Área de Trabalho Remota classe Win32_TSGatewayResourceAuthorizationPolicy ,
- Win32_TSGatewayResourceAuthorizationPolicy classe Serviços de Área de Trabalho Remota , criar método
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a85055ed9c8930a47e9a9949693457456fd8f261e1cb458e1092eb570532231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131180"
---
# <a name="create-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Criar método da classe \_ Win32 TSGatewayResourceAuthorizationPolicy

Cria uma política Área de Trabalho Remota de autorização de recurso (RD VIOLA).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Create(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupType,
  [in] string  ResourceGroupName,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ Em\]
</dt> <dd>

Nome do RD VIOLA.

</dd> <dt>

*Descrição* \[ Em\]
</dt> <dd>

Descrição do RD VIOLA.

</dd> <dt>

*Habilitado* \[ Em\]
</dt> <dd>

Indica se o RD VIOLA deve ser habilitado.

</dd> <dt>

*ResourceGroupType* \[ Em\]
</dt> <dd>

Tipo de grupo de recursos.

<dt>

"RG"
</dt> <dd>

Grupo de recursos.

</dd> <dt>

"CG"
</dt> <dd>

Grupo de computadores, conforme armazenado em Active Directory Domain Services.

</dd> <dt>

"ALL"
</dt> <dd>

Todos os recursos.

</dd> </dl> </dd> <dt>

*ResourceGroupName* \[ Em\]
</dt> <dd>

Nome do grupo de recursos.

</dd> <dt>

*UserGroupNames* \[ Em\]
</dt> <dd>

Lista separada por ponto e vírgula de nomes de grupo de usuários. Se o usuário pertencer a qualquer um desses grupos de usuários, o acesso será permitido. Os nomes de grupo de usuários devem estar no formato *Domain \\ UserGroupName*.

</dd> <dt>

*ProtocolNames* \[ Em\]
</dt> <dd>

Lista separada por ponto e vírgula de nomes de protocolo habilitados para essa política. Os nomes devem corresponder ao retorno [**do método GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) da classe [**\_ Win32 TSGatewayServerSettings.**](win32-tsgatewayserversettings.md)

</dd> <dt>

*PortNumbers* \[ Em\]
</dt> <dd>

Lista separada por ponto e vírgula de números de porta habilitados para essa política. Para permitir qualquer número de porta, de definir " \* ".

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

