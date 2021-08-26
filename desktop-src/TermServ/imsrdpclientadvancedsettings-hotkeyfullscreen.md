---
title: Propriedade IMsRdpClientAdvancedSettings HotKeyFullScreen
description: Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para alternar para o modo de tela inteira.
ms.assetid: 75fda212-ec68-4b68-b7db-2bfcdee7a7de
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade HotKeyFullScreen
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyFullScreen
- IMsRdpClientAdvancedSettings.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.put_HotKeyFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3276551c826c09b60c94a637194358093dafe7ce67094af085093f65d91e1668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870996"
---
# <a name="imsrdpclientadvancedsettingshotkeyfullscreen-property"></a>Propriedade IMsRdpClientAdvancedSettings:: HotKeyFullScreen

Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para alternar para o modo de tela inteira.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HotKeyFullScreen(
  [in]  LONG hotKeyFullScreen
);

HRESULT get_HotKeyFullScreen(
  [out] LONG *photKeyFullScreen
);
```



## <a name="property-value"></a>Valor da propriedade

O novo código de chave virtual. **VK \_ CANCEL** é o valor padrão.

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

 

 





