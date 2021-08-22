---
title: Classe MsRdpClient3a
description: Controle de cliente RDP da Microsoft (redistribuível) – versão 4a.
ms.assetid: F2E3D49F-B3F9-40EF-9B93-C87F55DB0352
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota classe MsRdpClient3a
- Serviços de Área de Trabalho Remota classe MsRdpClient3a, descrita
topic_type:
- apiref
api_name:
- MsRdpClient3a
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46699f5cd070c8a302305479f9eade7ba1191ae07e272af7409623f3d01960ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058634"
---
# <a name="msrdpclient3a-class"></a>Classe MsRdpClient3a

Controle de cliente RDP da Microsoft (redistribuível) – versão 4a

Essa classe implementa as interfaces a seguir.

-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient**](imsrdpclientshell2.md)
-   [**IMsTscAx**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**IMsTscAxEvents**](imstscaxevents-interface.md)
-   [**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)

**MsRdpClient3a** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MsRdpClient3a** tem esses métodos.



| Método                                                                                      | Descrição                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectar**](imstscax-connect.md)                                                         | Inicia uma conexão usando as propriedades atualmente definidas no controle.<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Cria um objeto de canal virtual do lado do cliente para cada nome de canal virtual especificado.<br/>                                                                                                                                                                                              |
| [**Desconectar**](imstscax-disconnect.md)                                                   | Desconecta a conexão ativa.<br/>                                                                                                                                                                                                                                                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Recupera as opções definidas para um canal virtual.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | notifica o módulo de redirecionamento de dispositivo do Área de Trabalho Remota ActiveX controle de que uma alteração de dispositivo ocorreu no sistema. Esse método passa notificações do [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) para o controle.<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | chamado depois que um controle de ActiveX exibe uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo de erro de certificado).<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | chamado antes de um controle de ActiveX exibir uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo de erro de certificado).<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Chamado quando o controle de cliente é reconectado automaticamente a uma sessão remota.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Chamado quando um cliente está no processo de reconexão automática de uma sessão com um servidor Host da Sessão RD.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Chamado quando um cliente está no processo de reconexão automática de uma sessão com um servidor Host da Sessão RD.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Chamado quando o cliente recebe dados em um canal virtual programável.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Chamado quando o cliente chama o método [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) .<br/>                                                                                                                                                                           |
| [**Onconnected**](imstscaxevents-onconnected.md)                                           | Chamado quando o controle de cliente está no processo de estabelecer uma conexão com um servidor Host da Sessão RD.<br/>                                                                                                                                                                       |
| [**Desconectando**](imstscaxevents-onconnecting.md)                                         | chamado quando o controle de cliente começa a se conectar a um servidor em resposta a uma chamada para [**IMsTscAx:: Conexão**](imstscax-connect.md).<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Chamado quando o usuário arrasta para baixo na barra de conexão.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Chamado quando o botão dispositivos na barra de conexão é pressionado.<br/>                                                                                                                                                                                                             |
| [**Desconectado**](imstscaxevents-ondisconnected.md)                                     | Chamado quando o controle de cliente foi desconectado do servidor de Host da Sessão RD.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Chamado quando o cliente entra no modo de tela inteira. Por exemplo, esse evento é chamado quando o usuário pressiona a combinação de [teclas de atalho](terminal-services-shortcut-keys.md) no modo de tela inteira (Ctrl + Alt + Break).<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Chamado quando o controle de cliente encontra um erro fatal.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Chamado quando a combinação de teclas de foco da versão é pressionada. Por exemplo, esse evento é chamado quando o usuário pressiona as teclas CTRL + ALT + seta para a esquerda ou CTRL + ALT + seta para a direita.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Chamado quando não há entrada de mouse ou de teclado pelo usuário durante o período definido pelo método [**IMsRdpClientAdvancedSettings::p UT \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | Chamado quando o cliente deixa o modo de tela inteira. Por exemplo, esse evento é chamado quando o usuário pressiona a combinação de [teclas de atalho](terminal-services-shortcut-keys.md) no modo de tela inteira (Ctrl + Alt + Break).<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | chamado quando o controle de cliente tiver feito logon com êxito em um servidor de Host da Sessão RD, seguindo a exibição da caixa de diálogo de Logon de Windows.<br/>                                                                                                                                      |
| [**OnLogonError**](imstscaxevents-onlogonerror.md)                                         | Chamado quando ocorre um erro de logon ou outro evento de logon.<br/>                                                                                                                                                                                                                             |
| [**OnMouseInputModeChanged**](imstscaxevents-onmouseinputmodechanged.md)                   | Chamado quando o modo de entrada do mouse é alterado.<br/>                                                                                                                                                                                                                                      |
| [**OnNetworkStatusChanged**](imstscaxevents-onnetworkstatuschanged.md)                     | Chamado quando o status da rede é alterado.<br/>                                                                                                                                                                                                                                        |
| [**OnReceivedTSPublicKey**](imstscaxevents-onreceivedtspublickey.md)                       | Chamado durante a sequência de conexão quando o cliente recupera a chave pública do servidor. Esse evento só será chamado se a propriedade **NotifyTSPublicKey** for **Variant \_ true**.<br/>                                                                                              |
| [**OnRemoteDesktopSizeChange**](imstscaxevents-onremotedesktopsizechange.md)               | Chamado para indicar que o tamanho do controle de cliente na área de trabalho remota foi alterado em resposta a uma operação de controle de cliente.<br/>                                                                                                                                                |
| [**OnRemoteProgramDisplayed**](imstscaxevents-onremoteprogramdisplayed.md)                 | Chamado quando um programa do RemoteApp é exibido.<br/>                                                                                                                                                                                                                                      |
| [**OnRemoteProgramResult**](imstscaxevents-onremoteprogramresult.md)                       | Chamado quando um programa do RemoteApp retorna um resultado para o controle de cliente.<br/>                                                                                                                                                                                                            |
| [**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)                   | Chamado quando uma janela do RemoteApp é exibida.<br/>                                                                                                                                                                                                                                       |
| [**OnRequestContainerMinimize**](imstscaxevents-onrequestcontainerminimize.md)             | Chamado quando o usuário pressiona o botão **minimizar** na barra de conexão no modo de tela inteira. O acionamento desse evento é uma solicitação que o aplicativo de contêiner minimiza em si mesmo.<br/>                                                                                              |
| [**OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md)                       | Chamado quando o cliente solicita para alternar para o modo de tela inteira e o método [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) é chamado para definir a propriedade **ContainerHandledFullScreen** como um valor diferente de zero.<br/> |
| [**OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md)                 | Chamado quando o cliente solicita a saída do modo de tela inteira e a propriedade [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) foi definida como um valor diferente de zero.<br/>                                                   |
| [**OnServiceMessageReceived**](imstscaxevents-onservicemessagereceived.md)                 | Chamado quando o cliente recebe uma mensagem do sistema.<br/>                                                                                                                                                                                                                                  |
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | Chamado quando o nome de usuário foi adquirido pelo controle.<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Chamado quando o controle de cliente encontra uma condição de erro que não é fatal.<br/>                                                                                                                                                                                                    |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Solicita um desligamento normal do controle de cliente.<br/>                                                                                                                                                                                                                                |
| [**ResetPassword**](imstscnonscriptable-resetpassword.md)                                  | Redefine todos os Estados de senha no controle.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Envia uma série de pressionamentos de teclas para o controle. Os pressionamentos de tecla estão no formato de código de digitalização, que são os dados de teclado das chaves físicas reais.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Envia dados para o servidor de Host da Sessão RD por meio de um canal virtual que foi criado anteriormente usando o método [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md) .<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Define as opções de canal virtual para o controle de cliente.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Propriedades

A classe **MsRdpClient3a** tem essas propriedades.



| Propriedade                                                                             | Tipo de acesso           | Descrição                                                                                                                                                               |
|:-------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                     | Somente leitura<br/>  | Um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .<br/>                                                                       |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Somente leitura<br/>  | Ponteiro para a interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) , usado para definir configurações avançadas para o controle de cliente.<br/> |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Somente leitura<br/>  | Ponteiro para a interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) , usado para definir configurações avançadas para o controle de cliente.<br/>         |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Somente leitura<br/>  | Ponteiro para a interface [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) , usado para definir configurações avançadas para o controle de cliente.<br/>         |
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>              | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                                                                                                                |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>                      | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                                                                                                                |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | Somente leitura<br/>  | A intensidade máxima de criptografia do controle atual.<br/>                                                                                                        |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/>        | Somente gravação<br/> | o Área de Trabalho Remota ActiveX a senha de controle, em formato de texto sem formatação.<br/>                                                                                              |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Leitura/gravação<br/> | Profundidade de cor do controle atual.<br/>                                                                                                                            |
| [**Conectado**](imstscax-connected.md)<br/>                                   | Somente leitura<br/>  | O estado de conexão do controle atual.<br/>                                                                                                                   |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Leitura/gravação<br/> | Texto que é exibido na área do cliente do controle enquanto o controle está no estado conectado.<br/>                                                          |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                         | Leitura/gravação<br/> | O texto que aparece centralizado no controle enquanto o controle está se conectando.<br/>                                                                                 |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | Leitura/gravação<br/> | A altura do controle atual, em pixels, na área de trabalho remota inicial.<br/>                                                                                        |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | Leitura/gravação<br/> | A largura do controle atual, em pixels, na área de trabalho remota inicial.<br/>                                                                                         |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                     | Leitura/gravação<br/> | O texto que aparece centralizado no controle antes que uma conexão seja encerrada.<br/>                                                                               |
| [**Domínio**](imstscax-domain.md)<br/>                                         | Leitura/gravação<br/> | O domínio no qual o usuário atual faz logon.<br/>                                                                                                                  |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Somente leitura<br/>  | Informações estendidas sobre o motivo do controle de cliente para desconexão.<br/>                                                                                      |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Leitura/gravação<br/> | Indica se o controle está no modo de tela inteira.<br/>                                                                                                          |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                       | Somente gravação<br/> | O título da janela exibido quando o controle está no modo de tela inteira.<br/>                                                                                            |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/> | Somente leitura<br/>  | Indica se o controle exibiu uma barra de rolagem horizontal.<br/>                                                                                           |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>          | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                                                                                                                |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>                  | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                                                                                                                |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                       | Somente leitura<br/>  | Um ponteiro de interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .<br/>                                                                          |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Somente leitura<br/>  | Ponteiro para a interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , usado para definir configurações protegidas para o controle de cliente.<br/>    |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>         | Somente leitura<br/>  | Indica se a interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) está disponível.<br/>                                                 |
| [**Servidor**](imstscax-server.md)<br/>                                         | Leitura/gravação<br/> | O nome do servidor ao qual o controle atual está conectado.<br/>                                                                                              |
| [**StartConnected**](imstscax-startconnected.md)<br/>                         | Leitura/gravação<br/> | Indica se o controle irá estabelecer a conexão do Host da Sessão RD Server imediatamente após a inicialização.<br/>                                                   |
| [**Usu**](imstscax-username.md)<br/>                                     | Leitura/gravação<br/> | A credencial de logon de nome de usuário.<br/>                                                                                                                                |
| [**Versão**](imstscax-version.md)<br/>                                       | Somente leitura<br/>  | O número de versão do controle atual.<br/>                                                                                                                     |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | Somente leitura<br/>  | Indica se o controle exibe uma barra de rolagem vertical.<br/>                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ MsRdpClient3a é definido como 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Área de Trabalho Remota ActiveX classes de controle](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

