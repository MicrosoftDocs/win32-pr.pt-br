---
title: Propriedade IMsRdpClientAdvancedSettings overallConnectionTimeout
description: Especifica o período total de tempo, em segundos, que o controle de cliente aguarda até que uma conexão seja concluída.
ms.assetid: 02fb24e1-b5e4-4d8e-a1c2-a9bd62a69bed
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade overallConnectionTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.overallConnectionTimeout
- IMsRdpClientAdvancedSettings.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_overallConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de6687d3d5cbccb3f7fdab94eca5ba4f2331c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753329"
---
# <a name="imsrdpclientadvancedsettingsoverallconnectiontimeout-property"></a>Propriedade IMsRdpClientAdvancedSettings:: overallConnectionTimeout

Especifica o período total de tempo, em segundos, que o controle de cliente aguarda até que uma conexão seja concluída.

Se o tempo especificado tiver decorrido antes de a conexão ser concluída, o controle desconectará e chamará o método [**IMsTscAxEvents:: OnDisconnect**](imstscaxevents-ondisconnected.md) .

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_overallConnectionTimeout(
  [in]  LONG overallConnectionTimeout
);

HRESULT get_overallConnectionTimeout(
  [out] LONG *poverallConnectionTimeout
);
```



## <a name="property-value"></a>Valor da propriedade

O novo horário, em segundos. O valor máximo é 600, que representa 10 minutos.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                  |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**singleConnectionTimeout**](imsrdpclientadvancedsettings-singleconnectiontimeout.md)
</dt> </dl>

 

 





