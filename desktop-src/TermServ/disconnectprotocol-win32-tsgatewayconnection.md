---
title: Método DisconnectProtocol da classe Win32_TSGatewayConnection
description: Desconecta todas as conexões do protocolo especificado do servidor gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 0ca3f478-dfdc-404e-ac17-43b6873b7256
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DisconnectProtocol
- Método DisconnectProtocol Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnection
- Classe Win32_TSGatewayConnection Serviços de Área de Trabalho Remota, método DisconnectProtocol
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectProtocol
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a37050cbd622c6fea14b8b4e5dc6a414eaad85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295813"
---
# <a name="disconnectprotocol-method-of-the-win32_tsgatewayconnection-class"></a>Método DisconnectProtocol da classe Win32 \_ TSGatewayConnection

Desconecta todas as conexões do protocolo especificado do servidor gateway de Área de Trabalho Remota (gateway de área de trabalho remota).

## <a name="syntax"></a>Sintaxe


```mof
uint32 DisconnectProtocol(
  [in] string ProtocolName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtocolName* \[ no\]
</dt> <dd>

O nome do protocolo para uma conexão específica. Isso pode ser recuperado da propriedade **ProtocolName** da classe **Win32 \_ TSGatewayConnection** .

<dt>

CALs
</dt> <dd>

O protocolo para o servidor de gateway de área de trabalho remota.

</dd> </dl> </dd> </dl>

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

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> </dl>

 

