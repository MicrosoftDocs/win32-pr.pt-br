---
title: Método DisableClipboard da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade ClipboardDisabled. Se a propriedade DeviceRedirectionType tiver um valor de \ 0034; 2 \ 0034;, a propriedade ClipboardDisabled controlará o redirecionamento da área de transferência para sessões que são estabelecidas por meio do servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: c53fc802-958b-452d-9af9-0ce89ed46079
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DisableClipboard
- Método DisableClipboard Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método DisableClipboard
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
ms.openlocfilehash: 23ae2070a35fa31f1c9d9ad31e9e632e31c0193f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779280"
---
# <a name="disableclipboard-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método DisableClipboard da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy

Define a propriedade **ClipboardDisabled** . Se a propriedade **DeviceRedirectionType** tiver um valor de "2", a propriedade **ClipboardDisabled** controlará o redirecionamento da área de transferência para sessões que são estabelecidas por meio do servidor gateway de área de trabalho remota (gateway de área de trabalho remota).

## <a name="syntax"></a>Sintaxe


```mof
uint32 DisableClipboard(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Desabilitado* \[ no\]
</dt> <dd>

Novo valor para a propriedade **ClipboardDisabled** .

</dd> </dl>

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

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

