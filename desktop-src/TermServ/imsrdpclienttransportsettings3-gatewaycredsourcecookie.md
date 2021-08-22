---
title: Propriedade IMsRdpClientTransportSettings3 GatewayCredSourceCookie
description: Especifica se a origem da credencial é baseada em cookie.
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- Propriedade GatewayCredSourceCookie Serviços de Área de Trabalho Remota
- Propriedade GatewayCredSourceCookie Serviços de Área de Trabalho Remota , interface IMsRdpClientTransportSettings3
- Interface IMsRdpClientTransportSettings3 Serviços de Área de Trabalho Remota , propriedade GatewayCredSourceCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fae89a3b7694d1ab73c076464b7ac62e6b18bcac6b4877d6156731135ee47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606941"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a>Propriedade IMsRdpClientTransportSettings3::GatewayCredSourceCookie

Especifica se a origem da credencial é baseada em cookie. Conterá um se a origem da credencial for baseada em cookie ou zero, caso contrário.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a>Valor da propriedade

Um **valor ULONG** que especifica se a origem da credencial é baseada em cookie.

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

 

 





