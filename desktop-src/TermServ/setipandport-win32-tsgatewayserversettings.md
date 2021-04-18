---
title: Método SetIPAndPort da classe Win32_TSGatewayServerSettings
description: Define o endereço IP de escuta e o número da porta para o transporte especificado.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetIPAndPort
- Método SetIPAndPort Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método SetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88870cce628a94ca34b38ccf315edc87a1a734b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499344"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Método SetIPAndPort da classe Win32 \_ TSGatewayServerSettings

Define o endereço IP de escuta e o número da porta para o transporte especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
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

*IPAddress* \[ no\]
</dt> <dd>

Especifica o endereço IP de escuta, em formato de octeto (por exemplo, "192.168.1.1").

</dd> <dt>

*Porta* \[ do no\]
</dt> <dd>

Especifica o número da porta de escuta.

</dd> <dt>

*OverrideExisting* \[ no\]
</dt> <dd>

Indica se a associação de IP/porta existente deve ser substituída para HTTP. Esse parâmetro só será usado se o parâmetro *TransportType* contiver 0 (RPC sobre http) ou 1 (http).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 





