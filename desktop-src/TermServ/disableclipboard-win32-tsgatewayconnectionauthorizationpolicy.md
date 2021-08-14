---
title: Método DisableClipboard da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade ClipboardDisabled. Se a propriedade DeviceRedirectionType tiver um valor de \ 0034;2 \ 0034;, a propriedade ClipboardDisabled controlará o redirecionamento da área de transferência para sessões estabelecidas por meio do servidor do Gateway de Área de Trabalho Área de Trabalho Remota (Gateway de Área de Trabalho Remoto).
ms.assetid: c53fc802-958b-452d-9af9-0ce89ed46079
ms.tgt_platform: multiple
keywords:
- Método DisableClipboard Serviços de Área de Trabalho Remota
- O método DisableClipboard Serviços de Área de Trabalho Remota classe Win32_TSGatewayConnectionAuthorizationPolicy ,
- Win32_TSGatewayConnectionAuthorizationPolicy classe Serviços de Área de Trabalho Remota , método DisableClipboard
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableClipboard
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01b5e8d2449bae2ee7f344c78b54850eb9ae300f4233c36b6eb2d84ad0b6132f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609611"
---
# <a name="disableclipboard-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método DisableClipboard da classe \_ Win32 TSGatewayConnectionAuthorizationPolicy

Define a **propriedade ClipboardDisabled.** Se a **propriedade DeviceRedirectionType** tiver um valor de "2", a propriedade **ClipboardDisabled** controlará o redirecionamento da área de transferência para sessões estabelecidas por meio do servidor do Gateway de Área de Trabalho Área de Trabalho Remota (Gateway de Área de Trabalho Remoto).

## <a name="syntax"></a>Sintaxe


```mof
uint32 DisableClipboard(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Desabilitado* \[ Em\]
</dt> <dd>

Novo valor para a **propriedade ClipboardDisabled.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Managed Object Format arquivos (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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
</dt> </dl>

 

