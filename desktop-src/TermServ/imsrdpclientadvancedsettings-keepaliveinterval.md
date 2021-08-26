---
title: Propriedade IMsRdpClientAdvancedSettings keepAliveInterval
description: Especifica um intervalo, em milissegundos, no qual o cliente envia mensagens keep alive para o servidor.
ms.assetid: 0d1b7d8f-f81c-4591-bb08-adab307e87fe
ms.tgt_platform: multiple
keywords:
- propriedade keepAliveInterval Serviços de Área de Trabalho Remota
- propriedade keepAliveInterval Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings
- Interface IMsRdpClientAdvancedSettings Serviços de Área de Trabalho Remota , propriedade keepAliveInterval
- propriedade keepAliveInterval Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings2
- Interface IMsRdpClientAdvancedSettings2 Serviços de Área de Trabalho Remota , propriedade keepAliveInterval
- propriedade keepAliveInterval Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings3
- Interface IMsRdpClientAdvancedSettings3 Serviços de Área de Trabalho Remota , propriedade keepAliveInterval
- propriedade keepAliveInterval Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings4
- Interface IMsRdpClientAdvancedSettings4 Serviços de Área de Trabalho Remota , propriedade keepAliveInterval
- propriedade keepAliveInterval Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings5
- Interface IMsRdpClientAdvancedSettings5 Serviços de Área de Trabalho Remota , propriedade keepAliveInterval
- A propriedade keepAliveInterval Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings6
- Interface IMsRdpClientAdvancedSettings6 Serviços de Área de Trabalho Remota , propriedade keepAliveInterval
- a propriedade keepAliveInterval Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings7
- Interface IMsRdpClientAdvancedSettings7 Serviços de Área de Trabalho Remota , propriedade keepAliveInterval
- propriedade keepAliveInterval Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings8
- Interface IMsRdpClientAdvancedSettings8 Serviços de Área de Trabalho Remota , propriedade keepAliveInterval
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.keepAliveInterval
- IMsRdpClientAdvancedSettings.get_keepAliveInterval
- IMsRdpClientAdvancedSettings.put_keepAliveInterval
- IMsRdpClientAdvancedSettings2.keepAliveInterval
- IMsRdpClientAdvancedSettings2.get_keepAliveInterval
- IMsRdpClientAdvancedSettings2.put_keepAliveInterval
- IMsRdpClientAdvancedSettings3.keepAliveInterval
- IMsRdpClientAdvancedSettings3.get_keepAliveInterval
- IMsRdpClientAdvancedSettings3.put_keepAliveInterval
- IMsRdpClientAdvancedSettings4.keepAliveInterval
- IMsRdpClientAdvancedSettings4.get_keepAliveInterval
- IMsRdpClientAdvancedSettings4.put_keepAliveInterval
- IMsRdpClientAdvancedSettings5.keepAliveInterval
- IMsRdpClientAdvancedSettings5.get_keepAliveInterval
- IMsRdpClientAdvancedSettings5.put_keepAliveInterval
- IMsRdpClientAdvancedSettings6.keepAliveInterval
- IMsRdpClientAdvancedSettings6.get_keepAliveInterval
- IMsRdpClientAdvancedSettings6.put_keepAliveInterval
- IMsRdpClientAdvancedSettings7.keepAliveInterval
- IMsRdpClientAdvancedSettings7.get_keepAliveInterval
- IMsRdpClientAdvancedSettings7.put_keepAliveInterval
- IMsRdpClientAdvancedSettings8.keepAliveInterval
- IMsRdpClientAdvancedSettings8.get_keepAliveInterval
- IMsRdpClientAdvancedSettings8.put_keepAliveInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dad34455d1203fb353672b8ef3797866b8ad2aa8b5686f71f769eccc5f3c9ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033296"
---
# <a name="imsrdpclientadvancedsettingskeepaliveinterval-property"></a>Propriedade IMsRdpClientAdvancedSettings::keepAliveInterval

Especifica um intervalo, em milissegundos, no qual o cliente envia mensagens keep alive para o servidor.

Uma configuração de política de grupo que especifica se as conexões de cliente persistentes com o servidor são permitidas podem substituir essa configuração de propriedade.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_keepAliveInterval(
  [in]  LONG keepAliveInterval
);

HRESULT get_keepAliveInterval(
  [out] LONG *pkeepAliveInterval
);
```



## <a name="property-value"></a>Valor da propriedade

O novo intervalo, em milissegundos. O valor padrão da propriedade é zero, que desabilita mensagens keep alive. O valor mínimo válido dessa propriedade é 10.000, que representa 10 segundos.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

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

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





