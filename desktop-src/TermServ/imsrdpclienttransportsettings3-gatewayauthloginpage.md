---
title: Propriedade IMsRdpClientTransportSettings3 GatewayAuthLoginPage
description: O endereço da página da Web de logon a ser usada para autenticar um usuário.
ms.assetid: d7a5e0d8-353e-416d-a9e0-11ef5072f9ff
ms.tgt_platform: multiple
keywords:
- Propriedade GatewayAuthLoginPage Serviços de Área de Trabalho Remota
- A propriedade GatewayAuthLoginPage Serviços de Área de Trabalho Remota , interface IMsRdpClientTransportSettings3
- Interface IMsRdpClientTransportSettings3 Serviços de Área de Trabalho Remota , propriedade GatewayAuthLoginPage
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.get_GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.put_GatewayAuthLoginPage
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672fc929e2fccf6934a2703684e467c75fd8afb725107a73bf0f6bb311c09bfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000925"
---
# <a name="imsrdpclienttransportsettings3gatewayauthloginpage-property"></a>Propriedade IMsRdpClientTransportSettings3::GatewayAuthLoginPage

O endereço da página da Web de logon a ser usada para autenticar um usuário.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayAuthLoginPage(
  [in]          BSTR bstrProxyAuthLoginPage
);

HRESULT get_GatewayAuthLoginPage(
  [out, retval] BSTR *pbstrProxyAuthLoginPage
);
```



## <a name="property-value"></a>Valor da propriedade

O novo endereço da página da Web de logon.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





