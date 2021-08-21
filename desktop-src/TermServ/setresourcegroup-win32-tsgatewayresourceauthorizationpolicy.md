---
title: Método fileresource da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Define o tipo e o nome do grupo de recursos.
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- Método fileresource Serviços de Área de Trabalho Remota
- Método fileresource Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota, método setresourceobject
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c29c4ca301a26fb3199891f3d25141f69402ecfe55bc46a2f3581c31e99b9445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058444"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método fileresource da \_ classe Win32 TSGatewayResourceAuthorizationPolicy

Define o tipo e o nome do grupo de recursos.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ResourceGroupName* \[ no\]
</dt> <dd>

Nome do grupo de recursos. Esse valor substitui a propriedade **ResourceGroupName** existente.

</dd> <dt>

*ResourceGroupType* \[ no\]
</dt> <dd>

Identifica o tipo do grupo de recursos. Esse valor substitui a propriedade **ResourceGroupType** existente.

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

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

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

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

