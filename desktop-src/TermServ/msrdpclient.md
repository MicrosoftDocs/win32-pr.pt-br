---
title: Classe MsRdpClient
description: Controle de cliente RDP da Microsoft (redistribuível) – versão 2.
ms.assetid: 58A779AF-4946-4D3B-B640-5675092A641D
ms.tgt_platform: multiple
keywords:
- Classe MsRdpClient Serviços de Área de Trabalho Remota
- Classe MsRdpClient Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- MsRdpClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f08494ccde9b0a25d7f862580c3ff1d828b7502c902fc101f16e0960d322163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870186"
---
# <a name="msrdpclient-class"></a>Classe MsRdpClient

Controle de cliente RDP da Microsoft (redistribuível) – versão 2

Essa classe implementa as interfaces a seguir.

-   [**Imsrdpclient**](imsrdpclientshell2.md)
-   [**Imstscax**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**Imstscaxevents**](imstscaxevents-interface.md)
-   [**Imstscnonscriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)

**MsRdpClient** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe MsRdpClient** tem esses métodos.



| Método                                                                                      | Descrição                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectar**](imstscax-connect.md)                                                         | Inicia uma conexão usando as propriedades atualmente definidas no controle .<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Cria um objeto de canal virtual do lado do cliente para cada nome de canal virtual especificado.<br/>                                                                                                                                                                                              |
| [**Desconectar**](imstscax-disconnect.md)                                                   | Desconecta a conexão ativa.<br/>                                                                                                                                                                                                                                                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Recupera as opções definidas para um canal virtual.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Notifica o módulo de redirecionamento de dispositivo do Área de Trabalho Remota ActiveX controle de que ocorreu uma alteração de dispositivo no sistema. Esse método passa [**notificações \_ WM DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) para o controle .<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | Chamado depois que um controle ActiveX exibe uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo de erro do certificado).<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | Chamado antes que um controle ActiveX exibia uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo de erro do certificado).<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Chamado quando o controle de cliente é reconectado automaticamente a uma sessão remota.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Chamado quando um cliente está no processo de reconectar automaticamente uma sessão com um Host da Sessão RD servidor.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Chamado quando um cliente está no processo de reconectar automaticamente uma sessão com um Host da Sessão RD servidor.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Chamado quando o cliente recebe dados em um canal virtual que pode ser roteável.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Chamado quando o cliente chama o [**método IMsRdpClient::RequestClose.**](imsrdpclient-requestclose.md)<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | Chamado quando o controle de cliente está no processo de estabelecer uma conexão com um Host da Sessão RD servidor.<br/>                                                                                                                                                                       |
| [**OnConnecting**](imstscaxevents-onconnecting.md)                                         | Chamado quando o controle de cliente começa a se conectar a um servidor em resposta a uma chamada para [**IMsTscAx::Conexão**](imstscax-connect.md).<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Chamado quando o usuário foi arrastado para baixo na barra de conexão.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Chamado quando o botão dispositivos na barra de conexão foi pressionado.<br/>                                                                                                                                                                                                             |
| [**OnDisconnected**](imstscaxevents-ondisconnected.md)                                     | Chamado quando o controle de cliente foi desconectado do Host da Sessão RD servidor.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Chamado quando o cliente entra no modo de tela inteira. Por exemplo, esse evento é chamado quando o usuário pressiona a combinação de teclas de atalho do modo de tela [inteira](terminal-services-shortcut-keys.md) (CTRL+ALT+BREAK).<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Chamado quando o controle do cliente encontra um erro fatal.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Chamado quando a combinação de teclas de foco de versão é pressionada. Por exemplo, esse evento é chamado quando o usuário pressiona a tecla CTRL+ALT+SETA PARA A ESQUERDA ou a combinação de teclas CTRL+ALT+SETA PARA A DIREITA.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Chamado quando não houve nenhuma entrada de mouse ou teclado pelo usuário durante o período definido pelo método [**IMsRdpClientAdvancedSettings::p ut \_ MinutesToIdleTimeout.**](imsrdpclientadvancedsettings-minutestoidletimeout.md)<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | Chamado quando o cliente sai do modo de tela inteira. Por exemplo, esse evento é chamado quando o usuário pressiona a combinação de teclas de atalho do modo de tela [inteira](terminal-services-shortcut-keys.md) (CTRL+ALT+BREAK).<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | Chamado quando o controle de cliente fez logon com êxito em um servidor Host da Sessão RD, seguindo a exibição da caixa de diálogo Windows Logon.<br/>                                                                                                                                      |
| [**OnLogonError**](imstscaxevents-onlogonerror.md)                                         | Chamado quando ocorre um erro de logon ou outro evento de logon.<br/>                                                                                                                                                                                                                             |
| [**OnMouseInputModeChanged**](imstscaxevents-onmouseinputmodechanged.md)                   | Chamado quando o modo de entrada do mouse foi alterado.<br/>                                                                                                                                                                                                                                      |
| [**OnNetworkStatusChanged**](imstscaxevents-onnetworkstatuschanged.md)                     | Chamado quando o status da rede foi alterado.<br/>                                                                                                                                                                                                                                        |
| [**OnReceivedTSPublicKey**](imstscaxevents-onreceivedtspublickey.md)                       | Chamado durante a sequência de conexão quando o cliente recupera a chave pública do servidor. Esse evento só será chamado se a **propriedade NotifyTSPublicKey** for **VARIANT \_ TRUE.**<br/>                                                                                              |
| [**OnRemoteDesktopSizeChange**](imstscaxevents-onremotedesktopsizechange.md)               | Chamado para indicar que o tamanho do controle de cliente na área de trabalho remota foi alterado em resposta a uma operação de controle de cliente.<br/>                                                                                                                                                |
| [**OnRemoteProgramDisplayed**](imstscaxevents-onremoteprogramdisplayed.md)                 | Chamado quando um programa RemoteApp é exibido.<br/>                                                                                                                                                                                                                                      |
| [**OnRemoteProgramResult**](imstscaxevents-onremoteprogramresult.md)                       | Chamado quando um programa RemoteApp retorna um resultado para o controle de cliente.<br/>                                                                                                                                                                                                            |
| [**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)                   | Chamado quando uma janela do RemoteApp é exibida.<br/>                                                                                                                                                                                                                                       |
| [**OnRequestContainerMinimize**](imstscaxevents-onrequestcontainerminimize.md)             | Chamado quando o usuário pressiona o **botão Minimizar** na barra de conexão no modo de tela inteira. O acionamento desse evento é uma solicitação que o aplicativo de contêiner se minimiza.<br/>                                                                                              |
| [**OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md)                       | Chamado quando o cliente solicita alternar para o modo de tela inteira e o método [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) é chamado para definir a **propriedade ContainerHandledFullScreen** como um valor diferente de zero.<br/> |
| [**OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md)                 | Chamado quando o cliente solicita para sair do modo de tela inteira e a propriedade [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) foi definida como um valor diferente de zero.<br/>                                                   |
| [**OnServiceMessageReceived**](imstscaxevents-onservicemessagereceived.md)                 | Chamado quando o cliente recebe uma mensagem do sistema.<br/>                                                                                                                                                                                                                                  |
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | Chamado quando o nome de usuário foi adquirido pelo controle .<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Chamado quando o controle do cliente encontra uma condição de erro que não é fatal.<br/>                                                                                                                                                                                                    |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Solicita um desligamento normal do controle de cliente.<br/>                                                                                                                                                                                                                                |
| [**ResetPassword**](imstscnonscriptable-resetpassword.md)                                  | Redefine todos os Estados de senha no controle.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Envia uma série de pressionamentos de teclas para o controle. Os pressionamentos de tecla estão no formato de código de digitalização, que são os dados de teclado das chaves físicas reais.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Envia dados para o servidor de Host da Sessão RD por meio de um canal virtual que foi criado anteriormente usando o método [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md) .<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Define as opções de canal virtual para o controle de cliente.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Propriedades

A classe **MsRdpClient** tem essas propriedades.



| Propriedade                                                                             | Tipo de acesso           | Descrição                                                                                                                                                               |
|:-------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                     | Somente leitura<br/>  | Um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .<br/>                                                                       |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Somente leitura<br/>  | Ponteiro para a interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) , usado para definir configurações avançadas para o controle de cliente.<br/> |
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>              | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                                                                                                                |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>                      | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                                                                                                                |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | Somente leitura<br/>  | A intensidade máxima de criptografia do controle atual.<br/>                                                                                                        |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/>        | Somente gravação<br/> | o Área de Trabalho Remota ActiveX a senha de controle, em formato de texto sem formatação.<br/>                                                                                              |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Leitura/gravação<br/> | Profundidade de cor do controle atual.<br/>                                                                                                                            |
| [**Conectado**](imstscax-connected.md)<br/>                                   | Somente leitura<br/>  | O estado de conexão do controle atual.<br/>                                                                                                                   |
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
| [**Usu**](imstscax-username.md)<br/>                                     | Leitura/gravação<br/> | A credencial de logon do nome de usuário.<br/>                                                                                                                                |
| [**Versão**](imstscax-version.md)<br/>                                       | Somente leitura<br/>  | O número de versão do controle atual.<br/>                                                                                                                     |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | Somente leitura<br/>  | Indica se o controle exibe uma barra de rolagem vertical.<br/>                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ MsRdpClient é definido como 791fa017-2de3-492e-acc5-53c67a2b94d0<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Área de Trabalho Remota ActiveX classes de controle](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

