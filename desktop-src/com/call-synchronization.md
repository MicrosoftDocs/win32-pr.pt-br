---
title: Sincronização de chamada
description: Sincronização de chamada
ms.assetid: e74407ef-f500-4d13-aef4-ca6bb37d5858
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9969c968294a3dfdbfbc4cb78d40e64ad65c17392bf3b9fd09fc7a5f99b9049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048734"
---
# <a name="call-synchronization"></a>Sincronização de chamada

Os aplicativos COM devem ser capazes de lidar corretamente com a entrada do usuário durante o processamento de uma ou mais chamadas do COM ou do sistema operacional. O COM fornece sincronização de chamada apenas para apartments de thread único. Os apartments multithread (que contêm threads de thread livre) não recebem chamadas ao fazer chamadas (no mesmo thread). Os apartments multithread não podem fazer chamadas sincronizadas de entrada. Chamadas assíncronas são convertidas em chamadas síncronas em apartments multithreaded. O filtro de mensagem não é chamado para nenhum thread em um apartment multithreaded. Para obter mais informações sobre problemas de threading, consulte [Processos, threads e apartments.](processes--threads--and-apartments.md)

As chamadas COM entre processos se enquadram em três categorias, da seguinte forma:

<dl> <dt>

<span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*Chamadas síncronas*
</dt> <dd>

A maior parte da comunicação que ocorre no COM é síncrona. Ao fazer chamadas síncronas, o chamador aguarda a resposta antes de continuar e pode receber mensagens de entrada enquanto aguarda. COM inser um loop modal para aguardar a resposta, recebendo e expedindo outras mensagens de maneira controlada.

</dd> <dt>

<span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*Notificações assíncronas*
</dt> <dd>

Ao enviar notificações assíncronas, o chamador não aguarda a resposta. O COM [**usa eventos PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) ou de alto nível para enviar notificações assíncronas, dependendo da plataforma. COM define cinco métodos assíncronos de [**IAdviseSink:**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)

-   [**Ondatachange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)
-   [**Onviewchange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)
-   [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)
-   [**Onsave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)
-   [**Onclose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)

> [!Note]  
> Enquanto COM estiver izando uma chamada assíncrona, chamadas síncronas não podem ser feitas. Por exemplo, a implementação de [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) de um aplicativo de contêiner não pode conter uma chamada para [**IPersistStorage::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save). Essas chamadas são as únicas chamadas assíncronas com suporte pelo COM. Não há nenhuma maneira de criar uma interface personalizada que seja assíncrona no momento.

 

</dd> <dt>

<span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*Chamadas sincronizadas de entrada*
</dt> <dd>

Ao fazer chamadas sincronizadas de entrada, o objeto chamado deve concluir a chamada antes de gerar controle. Isso ajuda a garantir que o gerenciamento de foco funcione corretamente e que os dados inseridos pelo usuário são processados adequadamente. Essas chamadas são feitas por COM por meio da [**função SendMessage,**](/windows/win32/api/winuser/nf-winuser-sendmessage) sem inserir um loop modal. Durante o processamento de uma chamada sincronizada de entrada, o objeto chamado não deve chamar nenhuma função ou método (incluindo métodos síncronos) que possa gerar controle. Os métodos a seguir são sincronizados de entrada

-   [**IOleWindow::GetWindow**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-getwindow)
-   [**IOleInPlaceActiveObject::OnFrameWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate)
-   [**IOleInPlaceActiveObject::OnDocWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate)
-   [**IOleInPlaceActiveObject::ResizeBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-resizeborder)
-   [**IOleInPlaceUIWindow::GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)
-   [**IOleInPlaceUIWindow::RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)
-   [**IOleInPlaceUIWindow::SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)
-   [**IOleInPlaceFrame::SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)
-   [**IOleInPlaceFrame::SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)
-   [**IOleInPlaceObject::SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects)

</dd> </dl>

Para minimizar problemas que podem surgir do processamento assíncrono de mensagens, a maioria das chamadas de método COM é síncrona. Com a comunicação síncrona, não há necessidade de código especial para expedir e manipular mensagens de entrada. Quando um aplicativo faz uma chamada de método síncrono, o COM entra em um loop de espera modal que trata as respostas necessárias e envia mensagens de entrada para aplicativos capazes de processá-las.

O COM gerencia chamadas de método atribuindo um identificador chamado *ID de thread lógico*. Um novo é atribuído quando um usuário seleciona um comando de menu ou quando o aplicativo inicia uma nova operação COM. As chamadas subsequentes relacionadas à chamada COM inicial são atribuídas à mesma ID de thread lógico que a chamada inicial.

 

 