---
title: Interface IMsRdpClient9
description: Fornece os métodos e propriedades necessários para configurar e usar o controle de cliente. Deriva da interface IMsRdpClient8.
ms.assetid: 353f0328-d8a3-4466-bf23-c6d6b8a47e5d
ms.tgt_platform: multiple
keywords:
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- IMsRdpClient9
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a84530c401398f373d9ae7e2f02619f9b3abeaa9f1d51a9f550afe55a7347e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609277"
---
# <a name="imsrdpclient9-interface"></a>Interface IMsRdpClient9

Fornece os métodos e propriedades necessários para configurar e usar o controle de cliente. Deriva da interface [**IMsRdpClient8.**](imsrdpclient8.md)

## <a name="members"></a>Membros

A interface **IMsRdpClient9** herda de [**IMsRdpClient8.**](imsrdpclient8.md) **IMsRdpClient9** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IMsRdpClient9** tem esses métodos.



| Método                                                                             | Descrição                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](imsrdpclient9-attachevent.md)                                   | Anexa um evento .<br/>                                                                                                                                                               |
| [**Conexão**](imstscax-connect.md)                                                | Inicia uma conexão usando as propriedades atualmente definidas no controle .<br/>                                                                                                        |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                    | Cria um objeto de canal virtual do lado do cliente para cada nome de canal virtual especificado.<br/>                                                                                            |
| [**detachEvent**](imsrdpclient9-detachevent.md)                                   | Desconecta um evento.<br/>                                                                                                                                                               |
| [**Desconectar**](imstscax-disconnect.md)                                          | Desconecta a conexão ativa.<br/>                                                                                                                                               |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                   | Recupera a descrição do erro para os eventos de desconexão da sessão.<br/>                                                                                                               |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                               | Recupera o texto de status para o código de status especificado.<br/>                                                                                                                         |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)          | Recupera as opções definidas para um canal virtual.<br/>                                                                                                                                 |
| [**Reconectar**](imsrdpclient8-reconnect.md)                                       | Reconecta-se à sessão remota com a nova largura e altura da área de trabalho.<br/>                                                                                                          |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | Solicita um desligamento normalmente do controle Área de Trabalho Remota ActiveX controle.<br/>                                                                                                              |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                      | Envia dados para o servidor Host da Sessão RD por um canal virtual criado anteriormente usando o [**método CreateVirtualChannels.**](imstscax-createvirtualchannels.md)<br/> |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                         | Faz com que uma ação seja executada na sessão remota.<br/>                                                                                                                          |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)          | Define as opções de canal virtual para o Área de Trabalho Remota ActiveX controle.<br/>                                                                                                         |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)     | Sincroniza as configurações de exibição da sessão.<br/>                                                                                                                                           |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | Atualiza as configurações de exibição da sessão.<br/>                                                                                                                                                |



 

### <a name="properties"></a>Propriedades

A interface **IMsRdpClient9** tem essas propriedades.



| Propriedade                                                                             | Tipo de acesso           | Descrição                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                     | Somente leitura<br/>  | Recupera um ponteiro de interface [**IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md)<br/>                                                                                                                                          |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Somente leitura<br/>  | Recupera um ponteiro para a interface [**IMsRdpClientAdvancedSettings.**](imsrdpclientadvancedsettings-interface.md) A interface pode ser usada para definir configurações avançadas para o controle do cliente.<br/>                                             |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Somente leitura<br/>  | Recupera um ponteiro para a interface [**IMsRdpClientAdvancedSettings2.**](imsrdpclientadvancedsettings2.md) A interface pode ser usada para definir configurações avançadas para o controle do cliente.<br/>                                                     |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Somente leitura<br/>  | Recupera um ponteiro para a interface [**IMsRdpClientAdvancedSettings3.**](imsrdpclientadvancedsettings3.md)<br/>                                                                                                                                |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | Somente leitura<br/>  | Recupera um ponteiro para uma interface [**IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md)<br/>                                                                                                                                 |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | Somente leitura<br/>  | Recupera a interface [**IMsRdpClientAdvancedSettings5.**](imsrdpclientadvancedsettings5.md)<br/>                                                                                                                                             |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | Somente leitura<br/>  | Recupera a interface [**IMsRdpClientAdvancedSettings6.**](imsrdpclientadvancedsettings5.md)<br/>                                                                                                                                             |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | Somente leitura<br/>  | Recupera um objeto que dá suporte à interface [**IMsRdpClientAdvancedSettings7.**](imsrdpclientadvancedsettings7.md)<br/>                                                                                                                     |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | Somente leitura<br/>  | Contém um objeto que dá suporte à interface [**IMsRdpClientAdvancedSettings8.**](imsrdpclientadvancedsettings8.md)<br/>                                                                                                                      |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | Somente leitura<br/>  | Recupera a intensidade máxima de criptografia do controle atual.<br/>                                                                                                                                                                           |
| [**Colordepth**](imsrdpclient-colordepth.md)<br/>                             | Leitura/gravação<br/> | A profundidade da cor (em bits por pixel) para a conexão do controle.<br/>                                                                                                                                                                           |
| [**Conectado**](imstscax-connected.md)<br/>                                   | Somente leitura<br/>  | Recupera o estado de conexão do controle atual.<br/>                                                                                                                                                                                      |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Leitura/gravação<br/> | Contém o texto exibido na área de cliente do controle enquanto o controle está no estado conectado.<br/>                                                                                                                          |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                         | Leitura/gravação<br/> | Especifica o texto que aparece centralizado no controle enquanto o controle está se conectando.<br/>                                                                                                                                                    |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | Leitura/gravação<br/> | Especifica a altura do controle atual, em pixels, na área de trabalho remota inicial.<br/>                                                                                                                                                           |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | Leitura/gravação<br/> | Especifica a largura do controle atual, em pixels, na área de trabalho remota inicial.<br/>                                                                                                                                                            |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                     | Leitura/gravação<br/> | Especifica o texto que aparece centralizado no controle antes que uma conexão seja encerrada.<br/>                                                                                                                                                  |
| [**Domínio**](imstscax-domain.md)<br/>                                         | Leitura/gravação<br/> | Especifica o domínio no qual o usuário atual faz logon.<br/>                                                                                                                                                                                     |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Somente leitura<br/>  | Contém informações estendidas sobre o motivo do controle para desconexão.<br/>                                                                                                                                                                 |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Leitura/gravação<br/> | Determina se o controle de cliente está no modo de tela inteira.<br/>                                                                                                                                                                               |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                       | Somente gravação<br/> | Especifica o título da janela exibido quando o controle está no modo de tela inteira.<br/>                                                                                                                                                               |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/> | Somente leitura<br/>  | Indica se o controle exibiu uma barra de rolagem horizontal.<br/>                                                                                                                                                                        |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>                | Somente leitura<br/>  | Recupera a interface de configuração de cliente programável [**IMsRdpClientShell**](imsrdpclientshell.md).<br/>                                                                                                                                           |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>                      | Somente leitura<br/>  | Recupera um objeto que dá suporte à interface [**ITSRemoteProgram**](itsremoteprogram.md) .<br/>                                                                                                                                               |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Somente leitura<br/>  | Recupera um objeto que dá suporte à interface [**ITSRemoteProgram2**](itsremoteprogram2.md) .<br/>                                                                                                                                             |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                       | Somente leitura<br/>  | Recupera um ponteiro de interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .<br/>                                                                                                                                            |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Somente leitura<br/>  | Recupera um ponteiro para a interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) . Essa interface pode ser usada para definir configurações protegidas para o controle de cliente.<br/>                                               |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | Somente leitura<br/>  | Recupera um objeto que dá suporte à interface [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .<br/>                                                                                                                       |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>         | Somente leitura<br/>  | Indica se a interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) está disponível. Ou seja, se a página da Web que contém o controle está atualmente em uma das zonas de segurança de URL permitidas do Internet Explorer.<br/> |
| [**Servidor**](imstscax-server.md)<br/>                                         | Leitura/gravação<br/> | Especifica o nome do servidor ao qual o controle atual está conectado.<br/>                                                                                                                                                                 |
| [**StartConnected**](imstscax-startconnected.md)<br/>                         | Leitura/gravação<br/> | Indica se o controle irá estabelecer a conexão do Host da Sessão RD Server imediatamente após a inicialização.<br/>                                                                                                                                |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Somente leitura<br/>  | Recupera o que passou por um script para a interface [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) .<br/>                                                                                                         |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Somente leitura<br/>  | Recupera a interface [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .<br/>                                                                                                                                           |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | Somente leitura<br/>  | Recupera um objeto que dá suporte à interface [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .<br/>                                                                                                                   |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | Somente leitura<br/>  | Recupera um objeto que dá suporte à interface [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .<br/>                                                                                                                   |
| [**Usu**](imstscax-username.md)<br/>                                     | Leitura/gravação<br/> | Especifica a credencial de logon do nome de usuário.<br/>                                                                                                                                                                                                   |
| [**Versão**](imstscax-version.md)<br/>                                       | Somente leitura<br/>  | Especifica o número de versão do controle atual.<br/>                                                                                                                                                                                        |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | Somente leitura<br/>  | Indica se o controle exibe uma barra de rolagem vertical.<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentários

A interface **IMsRdpClient9** foi estendida pelas seguintes interfaces, com cada nova interface herdando todos os métodos e propriedades das interfaces anteriores:

-   [**IMsRdpClient10**](imsrdpclient10.md)

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                                                                                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                                                                                                                                                                                                                                                                                               |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                          |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 é definido como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting é definido como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient9 é definido como 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient9 é definido como 28904001-04B6-436C-A55B-0AF1A0883DC9<br/>                                                                                                                                                                                                                                                                                                |



## <a name="see-also"></a>Confira também

<dl> <dt>

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

 

