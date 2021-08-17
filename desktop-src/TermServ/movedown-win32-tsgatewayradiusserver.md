---
title: Método MoveDown da classe Win32_TSGatewayRADIUSServer
description: Move esse servidor de serviço RADIUS (RADIUS) uma posição para baixo na ordem de prioridade.
ms.assetid: 1b12d2a0-1463-4bd7-9b92-5df2ba799a8a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método MoveDown
- Método MoveDown Serviços de Área de Trabalho Remota, classe Win32_TSGatewayRADIUSServer
- Classe Win32_TSGatewayRADIUSServer Serviços de Área de Trabalho Remota, método MoveDown
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acee402af28ed62c5f4627972b083d1fd5c3ed7f49b02a058fb4f2562ffbd681
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138159"
---
# <a name="movedown-method-of-the-win32_tsgatewayradiusserver-class"></a>Método MoveDown da classe Win32 \_ TSGatewayRADIUSServer

Move esse servidor de serviço RADIUS (RADIUS) uma posição para baixo na ordem de prioridade. Esse método incrementa a propriedade **Priority** do servidor RADIUS atual e decrementa a propriedade **Priority** do servidor RADIUS que segue o servidor RADIUS atual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 MoveDown();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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

 

