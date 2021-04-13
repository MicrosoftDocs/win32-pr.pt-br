---
title: Método MoveUp da classe Win32_TSGatewayRADIUSServer
description: Move esse servidor de serviço RADIUS (RADIUS) uma posição para cima na ordem de prioridade.
ms.assetid: 060bb90d-72c0-4364-a44f-c6368434b174
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método MoveUp
- Método MoveUp Serviços de Área de Trabalho Remota, classe Win32_TSGatewayRADIUSServer
- Classe Win32_TSGatewayRADIUSServer Serviços de Área de Trabalho Remota, método MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca93eee44abd147576c6e678dce871ae4d49d921
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499758"
---
# <a name="moveup-method-of-the-win32_tsgatewayradiusserver-class"></a>Método MoveUp da classe Win32 \_ TSGatewayRADIUSServer

Move esse servidor de serviço RADIUS (RADIUS) uma posição para cima na ordem de prioridade. Esse método diminui a propriedade **Priority** do servidor RADIUS atual e incrementa a propriedade **Priority** do servidor RADIUS que precede o servidor RADIUS atual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 MoveUp();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

