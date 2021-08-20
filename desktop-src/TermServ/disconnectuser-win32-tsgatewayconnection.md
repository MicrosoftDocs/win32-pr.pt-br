---
title: Método DisconnectUser da classe Win32_TSGatewayConnection (Tsgauthenticationengine.h)
description: Desconecta todas as conexões do usuário especificado do servidor Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- Método DisconnectUser Serviços de Área de Trabalho Remota
- Método DisconnectUser Serviços de Área de Trabalho Remota , Win32_TSGatewayConnection classe
- Win32_TSGatewayConnection classe Serviços de Área de Trabalho Remota , método DisconnectUser
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
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a>Método DisconnectUser da classe \_ Win32 TSGatewayConnection

Desconecta todas as conexões do usuário especificado do servidor Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UserName* \[ Em\]
</dt> <dd>

O nome de usuário, no formato #Domain* **\\** _UserName,_ cujas conexões devem ser desconectadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                       |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                             |
| Cabeçalho<br/>                   | <dl> <dt>Tsgauthenticationengine.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl>             |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> </dl>

 

