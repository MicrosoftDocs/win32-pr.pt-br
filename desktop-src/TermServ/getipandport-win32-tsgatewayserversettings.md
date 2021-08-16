---
title: Método GetIPAndPort da classe Win32_TSGatewayServerSettings
description: Obtém o endereço IP de escuta e o número da porta para o transporte especificado.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetIPAndPort
- Método GetIPAndPort Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método GetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf1cb1d4f597e734ac66456cd515193afed5ad31b7b6543d4e52c09717346a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353847"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Método GetIPAndPort da classe Win32 \_ TSGatewayServerSettings

Obtém o endereço IP de escuta e o número da porta para o transporte especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Transportetype* \[ no\]
</dt> <dd>

Especifica o tipo de transporte. Deve ser um dos valores a seguir.

<dt>

0
</dt> <dd>

RPC sobre transporte HTTP.

</dd> <dt>

1
</dt> <dd>

Transporte HTTP.

</dd> <dt>

2
</dt> <dd>

Transporte UDP.

</dd> </dl> </dd> <dt>

*IPAddress* \[ fora\]
</dt> <dd>

Uma cadeia de caracteres que recebe o endereço IP de escuta, em formato de octeto (por exemplo, "192.168.1.1").

</dd> <dt>

*Porta* \[ do fora\]
</dt> <dd>

Especifica o número da porta de escuta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





