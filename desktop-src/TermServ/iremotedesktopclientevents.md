---
title: Interface IRemoteDesktopClientEvents
description: Fornece métodos que recebem informações do servidor que estão relacionados a eventos de controle de cliente.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota da interface IRemoteDesktopClientEvents, descrita
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009371"
---
# <a name="iremotedesktopclientevents-interface"></a>Interface IRemoteDesktopClientEvents

Fornece métodos que recebem informações do servidor que estão relacionados a eventos de controle de cliente. Os eventos incluem conexão e desconexão, solicitações de modo de tela inteira, logon bem-sucedido e condições de erro.

## <a name="members"></a>Membros

A interface **IRemoteDesktopClientEvents** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRemoteDesktopClientEvents** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IRemoteDesktopClientEvents** tem esses métodos.



| Método                                                                                      | Descrição                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Chamado quando o controle de cliente recebe uma mensagem administrativa. <br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Chamado quando o controle de cliente é reconectado automaticamente a uma sessão remota. <br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Chamado quando o controle de cliente tenta restabelecer automaticamente uma conexão com uma sessão remota. <br/>                                                  |
| [**Onconnected**](iremotedesktopclientevents-onconnected.md)                               | Chamado quando o controle de cliente se conectou a uma sessão remota.<br/>                                                                                        |
| [**Desconectando**](iremotedesktopclientevents-onconnecting.md)                             | Chamado quando o controle de cliente tenta estabelecer uma conexão com uma sessão remota. <br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | Chamado depois que uma caixa de diálogo exibida pelo controle de cliente é ignorada. <br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Chamado antes de o controle exibir uma caixa de diálogo. <br/>                                                                                                        |
| [**Desconectado**](iremotedesktopclientevents-ondisconnected.md)                         | Chamado quando o controle de cliente foi desconectado de uma sessão remota. <br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Chamado quando as combinações de teclas especiais são pressionadas na sessão remota. <br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | Chamado quando o controle de cliente faz logon com êxito em uma sessão remota. <br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Chamado quando o status da rede é alterado. <br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Chamado quando o tamanho da área de trabalho remota é alterado. <br/>                                                                                                        |
| [**Onstatuschanged**](iremotedesktopclientevents-onstatuschanged.md)                       | Chamado quando o controle de cliente atualizou seu status. <br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Chamado quando o cursor do ponteiro de toque foi movido e a propriedade [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) está definida como true. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| CLSID<br/>                    | CLSID \_ RemoteDesktopClient é definido como EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/>       |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Área de Trabalho Remota referência de controle ActiveX](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

