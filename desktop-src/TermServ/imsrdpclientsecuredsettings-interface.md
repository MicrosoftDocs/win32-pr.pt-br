---
title: Interface IMsRdpClientSecuredSettings
description: inclui métodos para recuperar e definir propriedades do controle de ActiveX de Área de Trabalho Remota que são restritos a zonas de segurança de URL específicas do Internet Explorer. | Interface IMsRdpClientSecuredSettings
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings
- Serviços de Área de Trabalho Remota da interface IMsRdpClientSecuredSettings, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a1b834d42c957998ad2a8eda5cd3790dd16f40dfd82a8e463bc34e510cd742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129786"
---
# <a name="imsrdpclientsecuredsettings-interface"></a>Interface IMsRdpClientSecuredSettings

inclui métodos para recuperar e definir propriedades do controle de ActiveX de Área de Trabalho Remota que são restritos a zonas de segurança de URL específicas do Internet Explorer.

## <a name="members"></a>Membros

A interface **IMsRdpClientSecuredSettings** herda de [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md). **IMsRdpClientSecuredSettings** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientSecuredSettings** tem essas propriedades.



| Propriedade                                                                                   | Tipo de acesso           | Descrição                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | Leitura/gravação<br/> | As configurações de redirecionamento de áudio.<br/>    |
| [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | Leitura/gravação<br/> | As configurações de redirecionamento de teclado.<br/> |



 

## <a name="remarks"></a>Comentários

Essas propriedades não podem ser definidas quando o controle está conectado.

Consulte [fornecer para o RDP Client Security](providing-for-rdp-client-security.md) para obter mais informações sobre os métodos dessa interface.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings é definido como 605befcf-39c1-45CC-a811-068fb7be346d<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





