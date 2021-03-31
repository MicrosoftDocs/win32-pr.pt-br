---
title: Método EnableAllowOnlySDRServers da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Usado para alternar a propriedade AllowOnlySDRServers.
ms.assetid: ec7f22bc-4e80-4ece-9567-5f405207480e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnableAllowOnlySDRServers
- Método EnableAllowOnlySDRServers Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método EnableAllowOnlySDRServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.EnableAllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f031cff46e0fafdce80a995d2d4778875c1d56f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644588"
---
# <a name="enableallowonlysdrservers-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método EnableAllowOnlySDRServers da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy

Usado para alternar a propriedade **AllowOnlySDRServers** .

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableAllowOnlySDRServers(
  [in] boolean AllowOnlySDRServers
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AllowOnlySDRServers* \[ no\]
</dt> <dd>

Se definido como **true**, as conexões serão permitidas somente para proteger os servidores RDS do redirecionamento de dispositivo (SDR). Se definido como **false**, as conexões serão permitidas a servidores RDS mais antigos também

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | \\TerminalServices da cimv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

 





