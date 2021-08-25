---
title: Método SetSmartcardAllowed da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade SmartcardAllowed, que habilita ou desabilita o suporte para usar um cartão inteligente para se conectar ao servidor de gateway de área de trabalho de Área de Trabalho Remota (Gateway RD).
ms.assetid: 9fe1c7a9-2bab-439f-8dc2-421ed876fcf7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSmartcardAllowed
- Método SetSmartcardAllowed Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método SetSmartcardAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSmartcardAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54ea5618bd974c2051a588f532cac9fa741563f6d96be312c50fd9923497d9ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870066"
---
# <a name="setsmartcardallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método SetSmartcardAllowed da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy

Define a propriedade **SmartcardAllowed** , que habilita ou desabilita o suporte para usar um cartão inteligente para se conectar ao servidor de gateway de área de trabalho de área de trabalho remota (Gateway RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSmartcardAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Permitido* \[ no\]
</dt> <dd>

Novo valor de **SmartcardAllowed** .

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

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

