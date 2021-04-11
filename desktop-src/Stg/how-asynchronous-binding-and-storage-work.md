---
title: Como funciona a associação assíncrona e o armazenamento
description: O armazenamento assíncrono aprimora a especificação de armazenamento estruturado COM para dar suporte ao download de objetos de armazenamento em redes de alta latência e de link lento, como a Internet.
ms.assetid: 891152c3-5abd-45e4-a7bb-0aac23262b03
keywords:
- Como funciona a associação assíncrona e o armazenamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626e8c7a55b667e158de42b3c88a17315b5e41ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366184"
---
# <a name="how-asynchronous-binding-and-storage-work"></a>Como funciona a associação assíncrona e o armazenamento

O armazenamento assíncrono aprimora a especificação de armazenamento estruturado COM para dar suporte ao download de objetos de armazenamento em redes de alta latência e de link lento, como a Internet. O armazenamento assíncrono funciona junto com monikers assíncronos para fornecer comportamento de ligação assíncrona completo.

## <a name="document-object-embedded-in-a-web-page"></a>Objeto de documento inserido em uma página da Web

Quando um usuário clica em um link que representa um documento inserido em uma página da Web, ocorrem os seguintes eventos:

1.  O navegador chama a função [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) , passando a URL do link.
2.  O [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) analisa a URL, cria um moniker assíncrono correspondente e retorna um ponteiro para a interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) do moniker.
3.  O navegador chama [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) para determinar se o moniker é assíncrono, cria um contexto de associação, registra a interface [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) com o contexto de associação, somente se o moniker for assíncrono e chama [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject), passando o contexto de ligação.
4.  O moniker é associado ao objeto e o consulta para a interface [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , que indica se o objeto dá suporte à associação assíncrona e ao armazenamento. Se o objeto retornar um ponteiro para **IPersistMoniker**:

    1.  O moniker da URL chama [**IPersistMoniker:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)), passando seu próprio ponteiro [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) para o objeto.
    2.  O objeto modifica o contexto de associação, escolhe se ele deseja um armazenamento de bloqueio ou de não bloqueio, registra seu próprio [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) e chama [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) no ponteiro recebido por meio de [**IPersistMoniker:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)).
    3.  O moniker cria um armazenamento assíncrono, mantém uma referência à interface [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) do objeto wrapper, registra a interface [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) no armazenamento raiz e chama [**IPersistStorage:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load), passando o ponteiro [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) do armazenamento assíncrono. À medida que os dados chegam (em um thread em segundo plano), o moniker chama **IFillLockBytes** para preencher o [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) no arquivo temporário.
    4.  O objeto lê dados do armazenamento e retorna de [**IPersistMoniker:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)) quando recebeu dados suficientes para se considerar inicializados. Se o objeto tentar ler dados que ainda não foram baixados, o Downloader receberá uma notificação em [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). Dentro do método [**IProgressNotify:: OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) , o thread de download bloqueia em um loop de mensagem modal ou faz com que o armazenamento assíncrono retorne E \_ pendente, dependendo se o objeto solicitou um armazenamento de bloqueio ou de não bloqueio.

5.  Se o objeto não implementar [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)), o moniker consultará por [**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), o que indica que o estado persistente do objeto será armazenado em um objeto de armazenamento. Se o objeto retornar um ponteiro para **IPersistStorage**:

    1.  O moniker chama [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) em si, solicitando um [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) de bloqueio (porque o objeto não reconhece assíncrona), cria um armazenamento assíncrono, mantém uma referência à interface [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) do objeto wrapper, registra a interface [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) no armazenamento raiz e chama [**IPersistStorage:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load), passando o ponteiro **IStorage** do armazenamento assíncrono. À medida que os dados chegam (em um thread em segundo plano), o moniker chama [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) para preencher o [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) no arquivo temporário.
    2.  O objeto lê dados do armazenamento e retorna de [**IPersistStorage:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) quando recebeu dados suficientes para se considerar inicializados. Se o objeto tentar ler dados que ainda não foram baixados, ele receberá uma notificação em [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). Dentro do método [**IProgressNotify:: OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) , o thread de download sempre é bloqueado em um loop de mensagem modal.

6.  Independentemente de o download ser síncrono ou assíncrono, o moniker retorna de [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject)e o navegador recebe o objeto inicializado solicitado.
7.  O navegador consulta o [**IOleObject**](/windows/win32/api/oleidl/nn-oleidl-ioleobject) e hospeda o objeto como um objeto de documento. (Neste ponto, o objeto pode não ser inicializado completamente, mas o suficiente para exibir algo útil; nesse caso, o download continua em segundo plano.)

 

 