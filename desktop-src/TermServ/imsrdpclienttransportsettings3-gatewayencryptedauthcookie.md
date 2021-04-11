---
title: Propriedade IMsRdpClientTransportSettings3 GatewayEncryptedAuthCookie
description: O cookie de autenticação criptografado.
ms.assetid: c9ab6667-327c-44f8-a10e-b048ea91980c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayEncryptedAuthCookie
- Propriedade GatewayEncryptedAuthCookie Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings3, Propriedade GatewayEncryptedAuthCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3949d36f25f2029d7b134943b4e57d8a13db798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295785"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookie-property"></a>Propriedade IMsRdpClientTransportSettings3:: GatewayEncryptedAuthCookie

O cookie de autenticação criptografado. O tamanho da propriedade é especificado pela propriedade [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) .

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayEncryptedAuthCookie(
  [in]          BSTR bstrEncryptedAuthCookie
);

HRESULT get_GatewayEncryptedAuthCookie(
  [out, retval] BSTR *pbstrEncryptedAuthCookie
);
```



## <a name="property-value"></a>Valor da propriedade

O novo cookie de autenticação criptografado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)
</dt> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





