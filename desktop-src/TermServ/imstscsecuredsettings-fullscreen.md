---
title: Propriedade IMsTscSecuredSettings fullscreen
description: Especifica o estado de tela inteira do controle de cliente.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade fullscreen
- Serviços de Área de Trabalho Remota da propriedade fullscreen, interface IMsTscSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsTscSecuredSettings, Propriedade fullscreen
- Serviços de Área de Trabalho Remota da propriedade fullscreen, interface IMsRdpClientSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings, Propriedade fullscreen
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811909"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a>Propriedade IMsTscSecuredSettings:: fullscreen

Especifica o estado de tela inteira do controle de cliente.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a>Valor da propriedade

Defina esse parâmetro como **true** se o controle deve usar o modo de tela inteira e **false** caso contrário.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre esse método, consulte [fornecendo para o RDP Client Security](providing-for-rdp-client-security.md).

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

Observe que, embora o uso dessa propriedade seja restrito às zonas de segurança de URL do Internet Explorer permitidas, um usuário sempre poderá mudar para o modo de tela inteira depois que a conexão for estabelecida pressionando a combinação de [teclas de atalho](terminal-services-shortcut-keys.md) no modo de tela inteira (Ctrl + Alt + Break).

Esse método pode ser chamado enquanto a conexão do cliente é estabelecida.

Você deve chamar o método [**IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) antes de chamar o método **IMsTscSecuredSettings::p UT \_ fullscreen** ou o método [**IMsRdpClient::p UT \_ fullscreen**](imsrdpclient-fullscreen.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsTscSecuredSettings é definido como c9d65442-a0f9-45b2-8f73-d61d2db8cbb6<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





