---
title: Classe MsRdpClient5NotSafeForScripting
description: Controle de cliente RDP da Microsoft – versão 6.
ms.assetid: 0DC46910-D77E-47CF-92C3-4019D79C783C
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota classe MsRdpClient5NotSafeForScripting
- Serviços de Área de Trabalho Remota classe MsRdpClient5NotSafeForScripting, descrita
topic_type:
- apiref
api_name:
- MsRdpClient5NotSafeForScripting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23c525a779429eef31204c7f54fa9b4a15aa67f2a84c3f65f5a3cc0f8816d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605336"
---
# <a name="msrdpclient5notsafeforscripting-class"></a>Classe MsRdpClient5NotSafeForScripting

Controle de cliente RDP da Microsoft – versão 6

Essa classe implementa as interfaces a seguir.

-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient**](imsrdpclientshell2.md)
-   [**IMsTscAx**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**IMsTscAxEvents**](imstscaxevents-interface.md)
-   [**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)

**MsRdpClient5NotSafeForScripting** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MsRdpClient5NotSafeForScripting** tem esses métodos.



| Método                                                                                      | Descrição                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectar**](imstscax-connect.md)                                                         | Inicia uma conexão usando as propriedades atualmente definidas no controle.<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Cria um objeto de canal virtual do lado do cliente para cada nome de canal virtual especificado.<br/>                                                                                                                                                                                              |
| [**Desconectar**](imstscax-disconnect.md)                                                   | Desconecta a conexão ativa.<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | Recupera os códigos de erro e as mensagens de erro.<br/>                                                                                                                                                                                                                                      |
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
| [**OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md)                 | Chamado quando o cliente solicita para sair do modo de tela inteira e a propriedade [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) foi definida como um valor diferente de zero.<br/>                                                   |
| [**OnServiceMessageReceived**](imstscaxevents-onservicemessagereceived.md)                 | Chamado quando o cliente recebe uma mensagem do sistema.<br/>                                                                                                                                                                                                                                  |
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | Chamado quando o nome de usuário foi adquirido pelo controle .<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Chamado quando o controle do cliente encontra uma condição de erro que não é fatal.<br/>                                                                                                                                                                                                    |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Solicita um desligamento normalmente do controle de cliente.<br/>                                                                                                                                                                                                                                |
| [**Resetpassword**](imstscnonscriptable-resetpassword.md)                                  | Redefine todos os estados de senha no controle .<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Envia uma série de teclas de teclas para o controle . Os teclas de tecla estão no formulário de código de verificação, que são os dados de teclado das chaves físicas reais.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Envia dados para o servidor Host da Sessão RD por um canal virtual criado anteriormente usando o [**método IMsTscAx::CreateVirtualChannels.**](imstscax-createvirtualchannels.md)<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Define as opções de canal virtual para o controle de cliente.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Propriedades

A **classe MsRdpClient5NotSafeForScripting** tem essas propriedades.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propriedade</th>
<th style="text-align: left;">Tipo de acesso</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-advancedsettings.md"><strong>AdvancedSettings</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Um ponteiro de interface <a href="imstscadvancedsettings-interface.md"><strong>IMsTscAdvancedSettings.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Ponteiro para a interface <a href="imsrdpclientadvancedsettings-interface.md"><strong>IMsRdpClientAdvancedSettings,</strong></a> usada para definir configurações avançadas para o controle do cliente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Ponteiro para a interface <a href="imsrdpclientadvancedsettings2.md"><strong>IMsRdpClientAdvancedSettings2,</strong></a> usada para definir configurações avançadas para o controle do cliente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Ponteiro para a interface <a href="imsrdpclientadvancedsettings3.md"><strong>IMsRdpClientAdvancedSettings3,</strong></a> usada para definir configurações avançadas para o controle do cliente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Um ponteiro de interface <a href="imsrdpclientadvancedsettings4.md"><strong>IMsRdpClientAdvancedSettings4.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">A interface para <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Não há suporte a esta propriedade.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Não há suporte a esta propriedade.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">A intensidade máxima de criptografia do controle atual.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a><br/></td>
<td style="text-align: left;">Somente gravação<br/></td>
<td style="text-align: left;">O Área de Trabalho Remota ActiveX senha de controle, em formato de texto não criptografado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient-colordepth.md"><strong>Colordepth</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Profundidade de cor do controle atual.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-connected.md"><strong>Conectado</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">O estado de conexão do controle atual.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Texto exibido na área do cliente do controle enquanto o controle está no estado conectado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-connectingtext.md"><strong>ConnectingText</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">O texto que aparece centralizado no controle enquanto o controle está se conectando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">A cadeia de caracteres de texto a ser exibida para a barra de conexão.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">A altura do controle atual, em pixels, na área de trabalho remota inicial.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">A largura do controle atual, em pixels, na área de trabalho remota inicial.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">A coleção de dispositivos PnP que estão disponíveis para redirecionamento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">O texto que aparece centralizado no controle antes de uma conexão ser encerrada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-domain.md"><strong>Domínio</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">O domínio no qual o usuário atual faz o login.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">A coleção de unidades de disco que está disponível para redirecionamento.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se CredSSP está habilitado para essa conexão.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Informações estendidas sobre o motivo da desconexão do controle do cliente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-fullscreen.md"><strong>FullScreen</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Indica se o controle está no modo de tela inteira.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a><br/></td>
<td style="text-align: left;">Somente gravação<br/></td>
<td style="text-align: left;">O título da janela exibido quando o controle está no modo de tela inteira.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Indica se o controle exibiu uma barra de rolagem horizontal.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">As configurações do cliente para o launcher do portal da Web.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se a configuração NegotiateSecurityLayer tem suporte para essa conexão.<br/>
<blockquote>
[!Note]<br />
Quando <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> está habilitado e presente no cliente ou quando protocolo SSL (SSL) está habilitado com autenticação de usuário, NegotiateSecurityLayer é ignorado.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Não há suporte a esta propriedade.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Não há suporte a esta propriedade.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se a caixa de diálogo solicitar credenciais deve ser mostrada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se os dispositivos PnP anexados dinamicamente que são enumerados em uma sessão estão disponíveis para redirecionamento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se as unidades PnP anexadas dinamicamente que são enumeradas em uma sessão estão disponíveis para redirecionamento.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">A configuração remoteapp do cliente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-securedsettings.md"><strong>SecuredSettings</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Um ponteiro de interface <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Ponteiro para a interface <a href="imsrdpclientsecuredsettings-interface.md"><strong>IMsRdpClientSecuredSettings,</strong></a> usada para definir configurações protegidas para o controle do cliente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Indica se a interface <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a> está disponível.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-server.md"><strong>Servidor</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">O nome do servidor ao qual o controle atual está conectado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se a caixa de diálogo de aviso de segurança de redirecionamento deve ser mostrada antes de iniciar uma sessão.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-startconnected.md"><strong>StartConnected</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Indica se o controle estabelecerá a conexão de Host da Sessão RD servidor imediatamente após a inicialização.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">A configuração do Gateway de RD do cliente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">O alça de janela para ser a janela pai do controle. Isso permite que todas as janelas exibidas pelo controle sejam modais corretamente em relação a todas as janelas exibidas pelo aplicativo pai.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-username.md"><strong>Username</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">A credencial de logon de nome de usuário.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-version.md"><strong>Versão</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">O número de versão do controle atual.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Indica se o controle exibe uma barra de rolagem vertical.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se a caixa de diálogo de aviso de segurança deve incluir um aviso sobre o redirecionamento da área de transferência antes de iniciar uma sessão.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se o aviso de segurança deve incluir um aviso sobre como enviar credenciais para o servidor remoto antes de iniciar uma sessão.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| CLSID<br/>                    | CLSID \_ MsRdpClient5NotSafeForScripting é definido como 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Área de Trabalho Remota ActiveX classes de controle](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

