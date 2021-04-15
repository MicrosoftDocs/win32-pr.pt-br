---
title: Método Create da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Cria uma política de autorização de recursos de Área de Trabalho Remota (RD \ 160; RAP).
ms.assetid: 3301a543-cdf9-4528-a29e-691054ef81c9
ms.tgt_platform: multiple
keywords:
- Criar Serviços de Área de Trabalho Remota do método
- Criar método Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota, método Create
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
ms.openlocfilehash: d6372706a294902b03f22807049db9a954de4f7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369326"
---
# <a name="create-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método Create da classe Win32 \_ TSGatewayResourceAuthorizationPolicy

Cria uma RD RAP (política de autorização de recursos) Área de Trabalho Remota.

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

*Nome* \[ do no\]
</dt> <dd>

Nome da RD RAP.

</dd> <dt>

*Descrição* \[ do no\]
</dt> <dd>

Descrição da RD RAP.

</dd> <dt>

*Habilitado* \[ no\]
</dt> <dd>

Indica se a RD RAP deve ser habilitada.

</dd> <dt>

*ResourceGroupType* \[ no\]
</dt> <dd>

Tipo de grupo de recursos.

<dt>

RT
</dt> <dd>

Grupo de recursos.

</dd> <dt>

CG
</dt> <dd>

Grupo de computadores, conforme armazenado em Active Directory Domain Services.

</dd> <dt>

OS
</dt> <dd>

Todos os recursos.

</dd> </dl> </dd> <dt>

*ResourceGroupName* \[ no\]
</dt> <dd>

Nome do grupo de recursos.

</dd> <dt>

*Usergroupnames* \[ no\]
</dt> <dd>

Lista de nomes de grupos de usuários separados por ponto e vírgula. Se o usuário pertencer a qualquer um desses grupos de usuários, o acesso será permitido. Os nomes de grupos de usuários devem ter o formato *domínio \\ userGroupName*.

</dd> <dt>

De *protocolo* \[ no\]
</dt> <dd>

Lista separada por ponto e vírgula de nomes de protocolo que estão habilitados para esta política. Os nomes devem corresponder ao retorno do método [**Getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) da classe [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .

</dd> <dt>

*Portnumbers* \[ no\]
</dt> <dd>

Lista separada por ponto e vírgula de números de porta que estão habilitados para esta política. Para permitir qualquer número de porta, defina " \* ".

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

