---
title: Sincronização de chamadas
description: Sincronização de chamadas
ms.assetid: e74407ef-f500-4d13-aef4-ca6bb37d5858
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9254aceaaa8a6fa26d56d4a86987cc955b90dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008431"
---
# <a name="call-synchronization"></a>Sincronização de chamadas

Os aplicativos COM devem ser capazes de lidar corretamente com a entrada do usuário durante o processamento de uma ou mais chamadas de COM ou do sistema operacional. O COM fornece sincronização de chamadas somente para Apartments de thread único. O Apartments multithread (que contém threads de thread livre) não recebe chamadas ao fazer chamadas (no mesmo thread). O Apartments multithread não pode fazer chamadas sincronizadas de entrada. As chamadas assíncronas são convertidas em chamadas síncronas em Apartments multithread. O filtro de mensagem não é chamado para nenhum thread em um apartamento multithread. Para obter mais informações sobre problemas de Threading, consulte [processos, threads e Apartments](processes--threads--and-apartments.md).

As chamadas COM entre os processos se enquadram em três categorias, da seguinte maneira:

<dl> <dt>

<span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*Chamadas síncronas*
</dt> <dd>

A maioria das comunicações que ocorrem no COM é síncrona. Ao fazer chamadas síncronas, o chamador aguarda a resposta antes de continuar e pode receber mensagens de entrada enquanto aguarda. COM entra em um loop modal para aguardar a resposta, receber e despachar outras mensagens de maneira controlada.

</dd> <dt>

<span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*Notificações assíncronas*
</dt> <dd>

Ao enviar notificações assíncronas, o chamador não aguarda a resposta. O COM usa eventos de alto nível ou de uma [**mensagem**](/windows/win32/api/winuser/nf-winuser-postmessagea) para enviar notificações assíncronas, dependendo da plataforma. COM define cinco métodos assíncronos de [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink):

-   [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)
-   [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)
-   [**Renomear**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)
-   [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)
-   [**Fechamento**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)

> [!Note]  
> Embora o COM esteja processando uma chamada assíncrona, não é possível fazer chamadas síncronas. Por exemplo, a implementação de um aplicativo de contêiner de [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) não pode conter uma chamada para [**IPersistStorage:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save). Essas chamadas são as únicas chamadas assíncronas com suporte do COM. Não é possível criar uma interface personalizada que seja assíncrona no momento.

 

</dd> <dt>

<span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*Chamadas de entrada sincronizadas*
</dt> <dd>

Ao fazer chamadas sincronizadas de entrada, o objeto chamado deve concluir a chamada antes de produzir o controle. Isso ajuda a garantir que o gerenciamento de foco funcione corretamente e que os dados inseridos pelo usuário sejam processados adequadamente. Essas chamadas são feitas por COM por meio da função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) , sem entrar em um loop modal. Ao processar uma chamada de entrada sincronizada, o objeto chamado não deve chamar nenhuma função ou método (incluindo métodos síncronos) que pode gerar controle. Os métodos a seguir são de entrada sincronizada

-   [**IOleWindow:: GetWindow**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-getwindow)
-   [**IOleInPlaceActiveObject::OnFrameWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate)
-   [**IOleInPlaceActiveObject::OnDocWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate)
-   [**IOleInPlaceActiveObject::ResizeBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-resizeborder)
-   [**IOleInPlaceUIWindow:: GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)
-   [**IOleInPlaceUIWindow::RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)
-   [**IOleInPlaceUIWindow::SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)
-   [**IOleInPlaceFrame:: SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)
-   [**IOleInPlaceFrame::SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)
-   [**IOleInPlaceObject::SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects)

</dd> </dl>

Para minimizar os problemas que podem surgir no processamento assíncrono de mensagens, a maioria das chamadas de método COM é síncrona. Com a comunicação síncrona, não há necessidade de código especial para enviar e tratar mensagens de entrada. Quando um aplicativo faz uma chamada de método síncrona, COM entra em um loop de espera modal que manipula as respostas necessárias e envia mensagens de entrada para aplicativos capazes de processá-las.

O COM gerencia chamadas de método atribuindo um identificador chamado *ID de thread lógico*. Um novo é atribuído quando um usuário seleciona um comando de menu ou quando o aplicativo inicia uma nova operação COM. As chamadas subsequentes relacionadas à chamada COM inicial recebem a mesma ID de thread lógico que a chamada inicial.

 

 