---
title: Método Update da classe Win32_TSGatewayRADIUSServer
description: Atualiza o servidor atual de serviço RADIUS (RADIUS).
ms.assetid: 38a15768-66eb-40d6-a079-16555f2bf96a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de atualização
- Método Update Serviços de Área de Trabalho Remota, classe Win32_TSGatewayRADIUSServer
- Serviços de Área de Trabalho Remota de classe Win32_TSGatewayRADIUSServer, método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9129ae0cba782d2c0ac81e2acdeddac5fd27906b1e4dabd18c6a6cc4cce6b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423976"
---
# <a name="update-method-of-the-win32_tsgatewayradiusserver-class"></a>Método Update da classe Win32 \_ TSGatewayRADIUSServer

Atualiza o servidor atual de serviço RADIUS (RADIUS).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Update(
  [in] string Name,
  [in] string SharedSecret
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ do no\]
</dt> <dd>

Nome do servidor RADIUS.

</dd> <dt>

*SharedSecret* \[ no\]
</dt> <dd>

Segredo compartilhado para o servidor RADIUS.

</dd> </dl>

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

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

