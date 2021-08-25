---
title: Método MoveUp da classe Win32_TSGatewayConnectionAuthorizationPolicy dados
description: Move a política de Área de Trabalho Remota de conexão atual (RD \ 160; CAP) uma posição para cima na ordem em que RD \ 160; Os CAPs são avaliados.
ms.assetid: 5c9ff18d-e019-4a52-af0b-75fa61d77b7a
ms.tgt_platform: multiple
keywords:
- Método MoveUp Serviços de Área de Trabalho Remota
- Método MoveUp Serviços de Área de Trabalho Remota , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Serviços de Área de Trabalho Remota , método MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc5be4f15cee03097abcb52c50e3206d51872c8886970a49dbd20628f4b7beae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866366"
---
# <a name="moveup-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método MoveUp da classe \_ Win32 TSGatewayConnectionAuthorizationPolicy

Move a atual Área de Trabalho Remota política de autorização de conexão (RD CAP) uma posição para cima na ordem em que os CAPs de Área de TrabalhoRd são avaliados. Esse método diminui a propriedade **Order** do RD CAP atual e incrementa a propriedade **Order** do RD CAP que precedeu a RD CAP.

## <a name="syntax"></a>Sintaxe


```mof
uint32 MoveUp();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI.](terminal-services-wmi-provider-error-codes.md)

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Movedown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

