---
title: Classe MsRdpClient5
description: Controle de cliente RDP da Microsoft (redistribuível) – versão 6.
ms.assetid: 30DC49A8-A9B1-4F74-B578-5761FA0C1315
ms.tgt_platform: multiple
keywords:
- Classe MsRdpClient5 Serviços de Área de Trabalho Remota
- Classe MsRdpClient5 Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- MsRdpClient5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca53765f137e524f1605cdc0bbcabadbc12e89da
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473372"
---
# <a name="msrdpclient5-class"></a>Classe MsRdpClient5

Controle de cliente RDP da Microsoft (redistribuível) – versão 6

Essa classe implementa as interfaces a seguir.

-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**Imsrdpclient**](imsrdpclientshell2.md)
-   [**Imstscax**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**Imstscaxevents**](imstscaxevents-interface.md)
-   [**Imstscnonscriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)

**MsRdpClient5** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe MsRdpClient5** tem esses métodos.



| Método                                                                                      | Descrição                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectar**](imstscax-connect.md)                                                         | Inicia uma conexão usando as propriedades atualmente definidas no controle .<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Cria um objeto de canal virtual do lado do cliente para cada nome de canal virtual especificado.<br/>                                                                                                                                                                                              |
| [**Desconectar**](imstscax-disconnect.md)                                                   | Desconecta a conexão ativa.<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | Recupera os códigos de erro e as mensagens de erro.<br/>                                                                                                                                                                                                                                      |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Recupera as opções definidas para um canal virtual.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Notifica o módulo de redirecionamento de dispositivo do Área de Trabalho Remota ActiveX controle de que ocorreu uma alteração de dispositivo no sistema. Esse método passa [**notificações \_ WM DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) para o controle .<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | Chamado depois que um ActiveX exibe uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo de erro do certificado).<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | Chamado antes que um ActiveX exibia uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo de erro do certificado).<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Chamado quando o controle de cliente é reconectado automaticamente a uma sessão remota.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Chamado quando um cliente está no processo de reconectar automaticamente uma sessão com um Host da Sessão RD servidor.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Chamado quando um cliente está no processo de reconectar automaticamente uma sessão com um Host da Sessão RD servidor.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Chamado quando o cliente recebe dados em um canal virtual que pode ser roteável.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Chamado quando o cliente chama o [**método IMsRdpClient::RequestClose.**](imsrdpclient-requestclose.md)<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | Chamado quando o controle de cliente está no processo de estabelecer uma conexão com um Host da Sessão RD servidor.<br/>                                                                                                                                                                       |
| [**OnConnecting**](imstscaxevents-onconnecting.md)                                         | Chamado quando o controle de cliente começa a se conectar a um servidor em resposta a uma chamada para [**IMsTscAx::Conexão**](imstscax-connect.md).<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Chamado quando o usuário foi arrastado para baixo na barra de conexão.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Chamado quando o botão dispositivos na barra de conexão foi pressionado.<br/>                                                                                                                                                                                                             |
| [**OnDisconnected**](imstscaxevents-ondisconnected.md)                                     | Chamado quando o controle de cliente foi desconectado do servidor Host da Sessão RD servidor.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Chamado quando o cliente entra no modo de tela inteira. Por exemplo, esse evento é chamado quando o usuário pressiona a combinação de teclas de atalho do modo de tela [inteira](terminal-services-shortcut-keys.md) (CTRL+ALT+BREAK).<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Chamado quando o controle do cliente encontra um erro fatal.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Chamado quando a combinação de teclas de foco de versão é pressionada. Por exemplo, esse evento é chamado quando o usuário pressiona a tecla CTRL+ALT+SETA PARA A ESQUERDA ou a combinação de teclas CTRL+ALT+SETA PARA A DIREITA.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Chamado quando não há nenhuma entrada de mouse ou teclado pelo usuário durante o período definido pelo método [**IMsRdpClientAdvancedSettings::p ut \_ MinutesToIdleTimeout.**](imsrdpclientadvancedsettings-minutestoidletimeout.md)<br/>                                                |
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
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Solicita um desligamento normalmente do controle de cliente.<br/>                                                                                                                                                                                                                                |
| [**Resetpassword**](imstscnonscriptable-resetpassword.md)                                  | Redefine todos os estados de senha no controle .<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Envia uma série de teclas de teclas para o controle . Os teclas de tecla estão no formulário de código de verificação, que são os dados de teclado das chaves físicas reais.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Envia dados para o Host da Sessão RD por um canal virtual criado anteriormente usando o [**método IMsTscAx::CreateVirtualChannels.**](imstscax-createvirtualchannels.md)<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Define as opções de canal virtual para o controle de cliente.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Propriedades

A **classe MsRdpClient5** tem essas propriedades.




| Propriedade | Tipo de acesso | Descrição | 
|----------|-------------|-------------|
| <a href="imstscax-advancedsettings.md"><strong>AdvancedSettings</strong></a><br /> | Somente leitura<br /> | Um ponteiro de interface <a href="imstscadvancedsettings-interface.md"><strong>IMsTscAdvancedSettings.</strong></a><br /> | 
| <a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a><br /> | Somente leitura<br /> | Ponteiro para a interface <a href="imsrdpclientadvancedsettings-interface.md"><strong>IMsRdpClientAdvancedSettings,</strong></a> usada para definir configurações avançadas para o controle do cliente.<br /> | 
| <a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a><br /> | Somente leitura<br /> | Ponteiro para a interface <a href="imsrdpclientadvancedsettings2.md"><strong>IMsRdpClientAdvancedSettings2,</strong></a> usada para definir configurações avançadas para o controle do cliente.<br /> | 
| <a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a><br /> | Somente leitura<br /> | Ponteiro para a interface <a href="imsrdpclientadvancedsettings3.md"><strong>IMsRdpClientAdvancedSettings3,</strong></a> usada para definir configurações avançadas para o controle do cliente.<br /> | 
| <a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a><br /> | Somente leitura<br /> | Um ponteiro de interface <a href="imsrdpclientadvancedsettings4.md"><strong>IMsRdpClientAdvancedSettings4.</strong></a><br /> | 
| <a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a><br /> | Somente leitura<br /> | A interface para <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5</strong></a>.<br /> | 
| <a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a><br /> | Leitura/gravação<br /> | Não há suporte a esta propriedade.<br /> | 
| <a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a><br /> | Leitura/gravação<br /> | Não há suporte a esta propriedade.<br /> | 
| <a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a><br /> | Somente leitura<br /> | A intensidade máxima de criptografia do controle atual.<br /> | 
| <a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a><br /> | Somente gravação<br /> | O Área de Trabalho Remota ActiveX controle de senha, em formato de texto não criptografado.<br /> | 
| <a href="imsrdpclient-colordepth.md"><strong>Colordepth</strong></a><br /> | Leitura/gravação<br /> | Profundidade de cor do controle atual.<br /> | 
| <a href="imstscax-connected.md"><strong>Conectado</strong></a><br /> | Somente leitura<br /> | O estado de conexão do controle atual.<br /> | 
| <a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a><br /> | Leitura/gravação<br /> | Texto exibido na área do cliente do controle enquanto o controle está no estado conectado.<br /> | 
| <a href="imstscax-connectingtext.md"><strong>ConnectingText</strong></a><br /> | Leitura/gravação<br /> | O texto que aparece centralizado no controle enquanto o controle está se conectando.<br /> | 
| <a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br /> | Leitura/gravação<br /> | A cadeia de caracteres de texto a ser exibida para a barra de conexão.<br /> | 
| <a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a><br /> | Leitura/gravação<br /> | A altura do controle atual, em pixels, na área de trabalho remota inicial.<br /> | 
| <a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a><br /> | Leitura/gravação<br /> | A largura do controle atual, em pixels, na área de trabalho remota inicial.<br /> | 
| <a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br /> | Somente leitura<br /> | A coleção de dispositivos PnP que estão disponíveis para redirecionamento.<br /> | 
| <a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a><br /> | Leitura/gravação<br /> | O texto que aparece centralizado no controle antes de uma conexão ser encerrada.<br /> | 
| <a href="imstscax-domain.md"><strong>Domínio</strong></a><br /> | Leitura/gravação<br /> | O domínio no qual o usuário atual faz o login.<br /> | 
| <a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br /> | Somente leitura<br /> | A coleção de unidades de disco que está disponível para redirecionamento.<br /> | 
| <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br /> | Leitura/gravação<br /> | Especifica se CredSSP está habilitado para essa conexão.<br /> | 
| <a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a><br /> | Somente leitura<br /> | Informações estendidas sobre o motivo da desconexão do controle do cliente.<br /> | 
| <a href="imsrdpclient-fullscreen.md"><strong>FullScreen</strong></a><br /> | Leitura/gravação<br /> | Indica se o controle está no modo de tela inteira.<br /> | 
| <a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a><br /> | Somente gravação<br /> | O título da janela exibido quando o controle está no modo de tela inteira.<br /> | 
| <a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a><br /> | Somente leitura<br /> | Indica se o controle exibiu uma barra de rolagem horizontal.<br /> | 
| <a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a><br /> | Somente leitura<br /> | As configurações do cliente para o iniciador do portal da Web.<br /> | 
| <a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br /> | Leitura/gravação<br /> | Especifica se a configuração NegotiateSecurityLayer tem suporte para essa conexão.<br /><blockquote>[!Note]<br />Quando o <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> está habilitado e presente no cliente, ou quando protocolo SSL (SSL) é habilitado com a autenticação do usuário, NegotiateSecurityLayer é ignorado.</blockquote><br /> | 
| <a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a><br /> | Leitura/gravação<br /> | Não há suporte a esta propriedade.<br /> | 
| <a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a><br /> | Leitura/gravação<br /> | Não há suporte a esta propriedade.<br /> | 
| <a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br /> | Leitura/gravação<br /> | Especifica se a caixa de diálogo solicitar credenciais deve ser mostrada.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br /> | Leitura/gravação<br /> | Especifica se dispositivos PnP dinamicamente anexados que são enumerados enquanto estão em uma sessão estão disponíveis para redirecionamento.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br /> | Leitura/gravação<br /> | Especifica se as unidades PnP conectadas dinamicamente que são enumeradas enquanto estiverem em uma sessão estão disponíveis para redirecionamento.<br /> | 
| <a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a><br /> | Somente leitura<br /> | A configuração do RemoteApp do cliente.<br /> | 
| <a href="imstscax-securedsettings.md"><strong>SecuredSettings</strong></a><br /> | Somente leitura<br /> | Um ponteiro de interface <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a> .<br /> | 
| <a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br /> | Somente leitura<br /> | Ponteiro para a interface <a href="imsrdpclientsecuredsettings-interface.md"><strong>IMsRdpClientSecuredSettings</strong></a> , usado para definir configurações protegidas para o controle de cliente.<br /> | 
| <a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a><br /> | Somente leitura<br /> | Indica se a interface <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a> está disponível.<br /> | 
| <a href="imstscax-server.md"><strong>Servidor</strong></a><br /> | Leitura/gravação<br /> | O nome do servidor ao qual o controle atual está conectado.<br /> | 
| <a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br /> | Leitura/gravação<br /> | Especifica se a caixa de diálogo de aviso de segurança de redirecionamento deve ser mostrada antes de iniciar uma sessão.<br /> | 
| <a href="imstscax-startconnected.md"><strong>StartConnected</strong></a><br /> | Leitura/gravação<br /> | Indica se o controle irá estabelecer a conexão do Host da Sessão RD Server imediatamente após a inicialização.<br /> | 
| <a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br /> | Somente leitura<br /> | A configuração do gateway RD do cliente.<br /> | 
| <a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a><br /> | Leitura/gravação<br /> | O identificador de janela para ser a janela pai do controle. Isso permite que qualquer janela exibida pelo controle seja devidamente modal com relação a todas as janelas exibidas pelo aplicativo pai.<br /> | 
| <a href="imstscax-username.md"><strong>Usu</strong></a><br /> | Leitura/gravação<br /> | A credencial de logon do nome de usuário.<br /> | 
| <a href="imstscax-version.md"><strong>Versão</strong></a><br /> | Somente leitura<br /> | O número de versão do controle atual.<br /> | 
| <a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a><br /> | Somente leitura<br /> | Indica se o controle exibe uma barra de rolagem vertical.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br /> | Leitura/gravação<br /> | Especifica se a caixa de diálogo de aviso de segurança deve incluir um aviso sobre o redirecionamento da área de transferência antes de iniciar uma sessão.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br /> | Leitura/gravação<br /> | Especifica se o aviso de segurança deve incluir um aviso sobre o envio de credenciais ao servidor remoto antes de iniciar uma sessão.<br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ MsRdpClient5 é definido como 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Área de Trabalho Remota ActiveX classes de controle](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

