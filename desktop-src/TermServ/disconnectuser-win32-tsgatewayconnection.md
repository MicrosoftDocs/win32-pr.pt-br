---
title: Método DisconnectUser da classe Win32_TSGatewayConnection (Tsgauthenticationengine. h)
description: Desconecta todas as conexões do usuário especificado do servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DisconnectUser
- Método DisconnectUser Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnection
- Classe Win32_TSGatewayConnection Serviços de Área de Trabalho Remota, método DisconnectUser
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d31c7c89d285aed576024c551b07766a7387938762d60c252dec43e491037e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130991"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a>Método DisconnectUser da classe Win32 \_ TSGatewayConnection

Desconecta todas as conexões do usuário especificado do servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).

## <a name="syntax"></a>Sintaxe


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome de usuário* \[ no\]
</dt> <dd>

O nome de usuário, no formato * DOMAIN * **\\** _username_ , cujas conexões devem ser desconectadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                       |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                             |
| parâmetro<br/>                   | <dl> <dt>Tsgauthenticationengine. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl>             |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> </dl>

 

