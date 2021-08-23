---
title: Propriedade IMsRdpClientAdvancedSettings SmartSizing
description: Especifica se a exibição deve ser dimensionada para se ajustar à área do cliente do controle. Observe que as barras de rolagem não aparecem quando a propriedade SmartSizing está habilitada.
ms.assetid: d0b93129-5f84-49c5-bf8c-048075ac1481
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade SmartSizing
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmartSizing
- IMsRdpClientAdvancedSettings.get_SmartSizing
- IMsRdpClientAdvancedSettings.put_SmartSizing
- IMsRdpClientAdvancedSettings2.SmartSizing
- IMsRdpClientAdvancedSettings2.get_SmartSizing
- IMsRdpClientAdvancedSettings2.put_SmartSizing
- IMsRdpClientAdvancedSettings3.SmartSizing
- IMsRdpClientAdvancedSettings3.get_SmartSizing
- IMsRdpClientAdvancedSettings3.put_SmartSizing
- IMsRdpClientAdvancedSettings4.SmartSizing
- IMsRdpClientAdvancedSettings4.get_SmartSizing
- IMsRdpClientAdvancedSettings4.put_SmartSizing
- IMsRdpClientAdvancedSettings5.SmartSizing
- IMsRdpClientAdvancedSettings5.get_SmartSizing
- IMsRdpClientAdvancedSettings5.put_SmartSizing
- IMsRdpClientAdvancedSettings6.SmartSizing
- IMsRdpClientAdvancedSettings6.get_SmartSizing
- IMsRdpClientAdvancedSettings6.put_SmartSizing
- IMsRdpClientAdvancedSettings7.SmartSizing
- IMsRdpClientAdvancedSettings7.get_SmartSizing
- IMsRdpClientAdvancedSettings7.put_SmartSizing
- IMsRdpClientAdvancedSettings8.SmartSizing
- IMsRdpClientAdvancedSettings8.get_SmartSizing
- IMsRdpClientAdvancedSettings8.put_SmartSizing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b944dcb5d03e579817b2789e2bbefd5a3da8e20dd86c5a85ca7394201f6d36b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118855352"
---
# <a name="imsrdpclientadvancedsettingssmartsizing-property"></a>Propriedade IMsRdpClientAdvancedSettings:: SmartSizing

Especifica se a exibição deve ser dimensionada para se ajustar à área do cliente do controle. Observe que as barras de rolagem não aparecem quando a propriedade **SmartSizing** está habilitada.

Ao contrário da maioria das outras propriedades, essa propriedade pode ser definida quando o controle é conectado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SmartSizing(
  [in]  VARIANT_BOOL fSmartSizing
);

HRESULT get_SmartSizing(
  [out] VARIANT_BOOL *pfSmartSizing
);
```



## <a name="property-value"></a>Valor da propriedade

Defina esse parâmetro como **Variant \_ false** para desabilitar o recurso ou a **variante \_ true** para habilitar o recurso.

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
</dt> </dl>

 

 





