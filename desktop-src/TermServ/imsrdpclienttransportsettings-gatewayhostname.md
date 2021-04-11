---
title: Propriedade IMsRdpClientTransportSettings GatewayHostname
description: Especifica o nome do host do servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 34c4b3b7-3768-4d98-b1e8-7fcb8f9c758d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayHostname
- Propriedade GatewayHostname Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings, Propriedade GatewayHostname
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
ms.openlocfilehash: 03835faf48fa8aba557f82da158fdba827a84831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294773"
---
# <a name="imsrdpclienttransportsettingsgatewayhostname-property"></a>Propriedade IMsRdpClientTransportSettings:: GatewayHostname

Especifica o nome do host do servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).

Esta propriedade é de leitura/gravação.

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

Uma cadeia de caracteres que contém o nome do host do servidor de gateway RD.

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

 

 





