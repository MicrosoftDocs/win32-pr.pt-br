---
title: Método TSGRemoveAdminMsg da classe Win32_TSGatewayServerSettings
description: Remove a mensagem administrativa para o servidor de gateway. | Método TSGRemoveAdminMsg da Win32_TSGatewayServerSettings classe
ms.assetid: 36b157de-80ee-46f8-9803-5012cf1d6f5f
ms.tgt_platform: multiple
keywords:
- Método TSGRemoveAdminMsg Serviços de Área de Trabalho Remota
- Método TSGRemoveAdminMsg Serviços de Área de Trabalho Remota classe Win32_TSGatewayServerSettings ,
- Win32_TSGatewayServerSettings classe Serviços de Área de Trabalho Remota , método TSGRemoveAdminMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGRemoveAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc70fc302ea261a7777b3fbcd3c7773139b92bec48ea611960dfd6f1017b93af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869036"
---
# <a name="tsgremoveadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a>Método TSGRemoveAdminMsg da classe \_ Win32 TSGatewayServerSettings

Remove a mensagem administrativa para o servidor de gateway.

## <a name="syntax"></a>Sintaxe


```mof
uint32 TSGRemoveAdminMsg();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

