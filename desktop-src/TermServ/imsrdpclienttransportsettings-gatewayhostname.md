---
title: Propriedade GatewayHostname de IMsRdpClientTransportSettings
description: Especifica o nome do host do servidor Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).
ms.assetid: 34c4b3b7-3768-4d98-b1e8-7fcb8f9c758d
ms.tgt_platform: multiple
keywords:
- Propriedade GatewayHostname Serviços de Área de Trabalho Remota
- A propriedade GatewayHostname Serviços de Área de Trabalho Remota , interface IMsRdpClientTransportSettings
- Interface IMsRdpClientTransportSettings Serviços de Área de Trabalho Remota , propriedade GatewayHostname
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayHostname
- IMsRdpClientTransportSettings.get_GatewayHostname
- IMsRdpClientTransportSettings.put_GatewayHostname
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de618d31f4d0989ebce319260f0afe4548d658e3c28891a9d26dad0580d62452
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870836"
---
# <a name="imsrdpclienttransportsettingsgatewayhostname-property"></a>Propriedade IMsRdpClientTransportSettings::GatewayHostname

Especifica o nome do host do servidor Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayHostname(
  [in]  BSTR newVal
);

HRESULT get_GatewayHostname(
  [out] BSTR *pProxyHostname
);
```



## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres que contém o nome do host do servidor do Gateway de RD.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings é definido como 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





