---
title: Propriedade TransportType IMsRdpClientAdvancedSettings
description: Especifica o tipo de transporte usado pelo cliente.
ms.assetid: 752f5fbc-eb5a-48eb-8750-fc25c8a2f024
ms.tgt_platform: multiple
keywords:
- Propriedade TransportType Serviços de Área de Trabalho Remota
- A propriedade TransportType Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings
- Interface IMsRdpClientAdvancedSettings Serviços de Área de Trabalho Remota , propriedade TransportType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.TransportType
- IMsRdpClientAdvancedSettings.get_TransportType
- IMsRdpClientAdvancedSettings.put_TransportType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7829e39db819cf43e58856e4ea7ecd8d76621a78b9d45544a85034703e6ba9b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352970"
---
# <a name="imsrdpclientadvancedsettingstransporttype-property"></a>Propriedade IMsRdpClientAdvancedSettings::TransportType

Especifica o tipo de transporte usado pelo cliente. Essa propriedade não é usada pelo controle Área de Trabalho Remota ActiveX dados.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_TransportType(
  [in]  LONG transportType
);

HRESULT get_TransportType(
  [out] LONG *ptransportType
);
```



## <a name="property-value"></a>Valor da propriedade

Define o tipo de transporte. Esse método pode ser bem-sucedido, mas o conjunto de valores nunca é usado pelo Área de Trabalho Remota ActiveX controle.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                  |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | \_IMs IIDRdpClientAdvancedSettings é definido como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





