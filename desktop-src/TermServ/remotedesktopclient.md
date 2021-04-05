---
title: Classe RemoteDesktopClient
description: Implementa o aplicativo da Microsoft Windows Store Área de Trabalho Remota controle de cliente-versão 1.
ms.assetid: 0910883A-BD49-4908-8423-1FC280E0FE0C
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota classe RemoteDesktopClient
- Serviços de Área de Trabalho Remota classe RemoteDesktopClient, descrita
topic_type:
- apiref
api_name:
- RemoteDesktopClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb10b23f52f53e2d89fd5a81449818a8fe374116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918183"
---
# <a name="remotedesktopclient-class"></a>Classe RemoteDesktopClient

Implementa o aplicativo da Microsoft Windows Store Área de Trabalho Remota controle de cliente-versão 1

Essa classe implementa as interfaces a seguir.

-   [**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
-   [**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)

**RemoteDesktopClient** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **RemoteDesktopClient** tem esses métodos.



| Método                                                                                      | Descrição                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-attachevent)                                     | Anexa um manipulador de eventos a um evento.<br/>                                                                                                                  |
| [**Connect**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-connect)                                             | Inicia uma conexão usando as propriedades atualmente definidas no controle de cliente do contêiner de aplicativo protocolo RDP (RDP).<br/>                         |
| [**DeleteSavedCredentials**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-deletesavedcredentials)               | Exclui as credenciais salvas para o computador remoto especificado.<br/>                                                                                            |
| [**detachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-detachevent)                                     | Desanexa um manipulador de eventos de um evento.<br/>                                                                                                                |
| [**Desconectar**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-disconnect)                                       | Desconecta a conexão ativa.<br/>                                                                                                                      |
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Chamado quando o controle de cliente recebe uma mensagem administrativa.<br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Chamado quando o controle de cliente é reconectado automaticamente a uma sessão remota.<br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Chamado quando o controle de cliente tenta restabelecer automaticamente uma conexão com uma sessão remota.<br/>                                                  |
| [**Onconnected**](iremotedesktopclientevents-onconnected.md)                               | Chamado quando o controle de cliente se conectou a uma sessão remota.<br/>                                                                                       |
| [**Desconectando**](iremotedesktopclientevents-onconnecting.md)                             | Chamado quando o controle de cliente tenta estabelecer uma conexão com uma sessão remota.<br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | Chamado depois que uma caixa de diálogo exibida pelo controle de cliente é ignorada.<br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Chamado antes de o controle exibir uma caixa de diálogo.<br/>                                                                                                        |
| [**Desconectado**](iremotedesktopclientevents-ondisconnected.md)                         | Chamado quando o controle de cliente foi desconectado de uma sessão remota.<br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Chamado quando as combinações de teclas especiais são pressionadas na sessão remota.<br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | Chamado quando o controle de cliente faz logon com êxito em uma sessão remota.<br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Chamado quando o status da rede é alterado.<br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Chamado quando o tamanho da área de trabalho remota é alterado.<br/>                                                                                                        |
| [**Onstatuschanged**](iremotedesktopclientevents-onstatuschanged.md)                       | Chamado quando o controle de cliente atualizou seu status.<br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Chamado quando o cursor do ponteiro de toque foi movido e a propriedade [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) está definida como true.<br/> |
| [**Reconectar**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-reconnect)                                         | Inicia uma reconexão automática do controle de cliente do contêiner de aplicativo protocolo RDP (RDP) para ajustar a sessão à nova largura e altura.<br/>   |
| [**UpdateSessionDisplaySettings**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-updatesessiondisplaysettings)   | Atualiza as configurações de largura e altura para o controle de cliente do contêiner de aplicativo protocolo RDP (RDP).<br/>                                               |



 

### <a name="properties"></a>Propriedades

A classe **RemoteDesktopClient** tem essas propriedades.



| Propriedade                                                             | Tipo de acesso          | Descrição                                                                                                                                                            |
|:---------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ações**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_actions)<br/>           | Somente leitura<br/> | Recupera o objeto Actions para o cliente de contêiner de aplicativo protocolo RDP (RDP).<br/>                                                                    |
| [**Configurações**](iremotedesktopclient-settings.md)<br/>         | Somente leitura<br/> | Recupera o objeto de configurações para o cliente de contêiner de aplicativo protocolo RDP (RDP).<br/>                                                                   |
| [**TouchPointer**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_touchpointer)<br/> | Somente leitura<br/> | Contém o objeto [**RemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer) para o cliente de contêiner de aplicativo protocolo RDP (RDP).<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| CLSID<br/>                    | CLSID \_ RemoteDesktopClient é definido como EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Área de Trabalho Remota classes de controle ActiveX](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

