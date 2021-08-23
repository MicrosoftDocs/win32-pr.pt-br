---
title: Interface IMsRdpClient10
description: Fornece os métodos e as propriedades necessários para configurar e usar o controle de cliente. Deriva da interface IMsRdpClient9.
ms.assetid: 601f70aa-85f1-4180-921b-9f1bb31d4def
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10
- Serviços de Área de Trabalho Remota da interface IMsRdpClient10, descrita
topic_type:
- apiref
api_name:
- IMsRdpClient10
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561541f170fbe6dc5342b359e5deae69d0c92469ad2d692ee4ea3b9d59904885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737236"
---
# <a name="imsrdpclient10-interface"></a>Interface IMsRdpClient10

Fornece os métodos e as propriedades necessários para configurar e usar o controle de cliente. Deriva da interface [**IMsRdpClient9**](imsrdpclient9.md) .

## <a name="members"></a>Membros

A interface **IMsRdpClient10** herda de [**IMsRdpClient9**](imsrdpclient9.md). **IMsRdpClient10** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IMsRdpClient10** tem esses métodos.



| Método                                                                             | Descrição                                                                         |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**attachEvent**](imsrdpclient9-attachevent.md)                                   | Anexa um evento.<br/>                                                       |
| [**detachEvent**](imsrdpclient9-detachevent.md)                                   | Desanexa um evento.<br/>                                                       |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                   | Recupera a descrição do erro para os eventos de desconexão de sessão.<br/>       |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                               | Recupera o texto de status do código de status especificado.<br/>                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)          | Recupera as opções definidas para um canal virtual.<br/>                         |
| [**Reconectar**](imsrdpclient8-reconnect.md)                                       | Reconecta-se à sessão remota com a nova largura e altura da área de trabalho.<br/>  |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | solicita um desligamento normal do controle de ActiveX de Área de Trabalho Remota.<br/>      |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                         | Faz com que uma ação seja executada na sessão remota.<br/>                  |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)          | define as opções de canal virtual para o controle de ActiveX de Área de Trabalho Remota.<br/> |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)     | Sincroniza as configurações de exibição da sessão.<br/>                                   |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | Atualiza as configurações de exibição da sessão.<br/>                                        |



 

### <a name="properties"></a>Propriedades

A interface **IMsRdpClient10** tem essas propriedades.



| Propriedade                                                                             | Tipo de acesso           | Descrição                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Somente leitura<br/>  | Recupera um ponteiro para a interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) . A interface pode ser usada para definir configurações avançadas para o controle de cliente.<br/> |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Somente leitura<br/>  | Recupera um ponteiro para a interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) . A interface pode ser usada para definir configurações avançadas para o controle de cliente.<br/>         |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Somente leitura<br/>  | Recupera um ponteiro para a interface [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .<br/>                                                                                    |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | Somente leitura<br/>  | Recupera um ponteiro para uma interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .<br/>                                                                                     |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | Somente leitura<br/>  | Recupera a interface [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .<br/>                                                                                                 |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | Somente leitura<br/>  | Recupera a interface [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) .<br/>                                                                                                 |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | Somente leitura<br/>  | Recupera um objeto que dá suporte à interface [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .<br/>                                                                         |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | Somente leitura<br/>  | Contém um objeto que dá suporte à interface [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) .<br/>                                                                          |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Leitura/gravação<br/> | A profundidade de cor (em bits por pixel) para a conexão do controle.<br/>                                                                                                                               |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Leitura/gravação<br/> | Contém o texto que é exibido na área do cliente do controle enquanto o controle está no estado conectado.<br/>                                                                              |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Somente leitura<br/>  | Contém informações estendidas sobre o motivo do controle para desconexão.<br/>                                                                                                                     |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Leitura/gravação<br/> | Determina se o controle de cliente está no modo de tela inteira.<br/>                                                                                                                                   |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>                | Somente leitura<br/>  | Recupera a interface de configuração de cliente programável [**IMsRdpClientShell**](imsrdpclientshell.md).<br/>                                                                                               |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>                      | Somente leitura<br/>  | Recupera um objeto que dá suporte à interface [**ITSRemoteProgram**](itsremoteprogram.md) .<br/>                                                                                                   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Somente leitura<br/>  | Recupera um objeto que dá suporte à interface [**ITSRemoteProgram2**](itsremoteprogram2.md) .<br/>                                                                                                 |
| [**RemoteProgram3**](imsrdpclient10-remoteprogram3.md)<br/>                   | Somente leitura<br/>  | Um objeto que dá suporte à interface [**ITSRemoteProgram3**](itsremoteprogram3.md) .<br/>                                                                                                           |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Somente leitura<br/>  | Recupera um ponteiro para a interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) . Essa interface pode ser usada para definir configurações protegidas para o controle de cliente.<br/>   |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | Somente leitura<br/>  | Recupera um objeto que dá suporte à interface [**IMsRdpClientSecuredSettings2.**](imsrdpclientsecuredsettings2.md)<br/>                                                                           |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Somente leitura<br/>  | Recupera o que foi passado por meio de um script para a interface [**IMsRdpClientTransportSettings.**](imsrdpclienttransportsettings.md)<br/>                                                             |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Somente leitura<br/>  | Recupera a interface [**IMsRdpClientTransportSettings2.**](imsrdpclienttransportsettings2.md)<br/>                                                                                               |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | Somente leitura<br/>  | Recupera um objeto que dá suporte à interface [**IMsRdpClientTransportSettings3.**](imsrdpclienttransportsettings3.md)<br/>                                                                       |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | Somente leitura<br/>  | Recupera um objeto que dá suporte à interface [**IMsRdpClientTransportSettings4.**](imsrdpclienttransportsettings4.md)<br/>                                                                       |



 

## <a name="remarks"></a>Comentários

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                                                                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                                                                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 é definido como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting é definido como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> |
| IID<br/>                      | IID \_ IMsRdpClient10 é definido como 7ED92C39-EB38-4927-A70A-708AC5A59321<br/>                                                                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**Imsrdpclient**](imsrdpclient-interface.md)
</dt> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> <dt>

[Conexão Web de Área de Trabalho Remota referência](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

