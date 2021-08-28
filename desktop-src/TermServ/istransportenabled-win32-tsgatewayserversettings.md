---
title: Método IsTransportEnabled da classe Win32_TSGatewayServerSettings
description: Determina se o transporte especificado está habilitado.
ms.assetid: 3f08a206-5800-4088-a113-bb3f0cc826f2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsTransportEnabled
- Método IsTransportEnabled Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método IsTransportEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsTransportEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7960748228e11f3749cd86daa2a323ca32ab9b05e1c17f98261ad4ae62b0fc9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515076"
---
# <a name="istransportenabled-method-of-the-win32_tsgatewayserversettings-class"></a>Método IsTransportEnabled da classe Win32 \_ TSGatewayServerSettings

Determina se o transporte especificado está habilitado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsTransportEnabled(
  [in]  uint16  TransportType,
  [out] boolean Enabled
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

*Habilitado* \[ fora\]
</dt> <dd>

Um valor **booliano** que indica se o transporte está habilitado.

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

 

 





