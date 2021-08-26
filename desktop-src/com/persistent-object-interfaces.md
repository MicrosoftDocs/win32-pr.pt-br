---
title: INTERFACES de objeto persistente (COM)
description: Um objeto persistente implementa uma ou mais interfaces de objeto persistentes.
ms.assetid: 8c8e44e4-f564-4af5-9a8a-ac6883862cae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ee1062c80a5c40d139965e0e3bebf96cbda534062322e218e2f5a7da586ff0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120406"
---
# <a name="persistent-object-interfaces"></a>Interfaces de objeto persistente

Um objeto persistente implementa uma ou mais *interfaces de objeto persistentes*. Os clientes usam interfaces de objeto persistentes para dizer a esses objetos quando e onde armazenar seu estado. Todas as interfaces de objeto persistente são derivadas de [**IPersist,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist)portanto, qualquer objeto que implementa qualquer interface de objeto persistente também implementa **IPersist**.

As seguintes interfaces de objeto persistente estão definidas atualmente:

-   [**Ipersiststream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)
-   [**Ipersiststreaminit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)
-   [**Ipersiststorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)
-   [**Ipersistfile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)
-   [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))
-   [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))
-   [Ipersistpropertybag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))

Os implementadores escolhem quais interfaces de objeto persistente um objeto dá suporte, dependendo de como o objeto deve ser usado. Ao não dar suporte a nenhuma interface de objeto persistente, o implementador está efetivamente dizendo: "O estado desse objeto não pode ser armazenado persistentemente". Ao dar suporte a uma ou mais interfaces de objeto persistentes, o implementador está efetivamente dizendo: "O estado desse objeto pode ser armazenado persistentemente em uma ou mais mídias de armazenamento de dados".

Por exemplo, a tabela a seguir lista vários tipos de objeto que permitem suporte para diferentes interfaces de objeto persistente.



| Categoria                            | Interfaces de objeto persistente normalmente têm suporte                                                                                                                                                         |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Monikers<br/>                 | [**Ipersiststream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)<br/>                                                                                                                                                      |
| Objetos inbeddáveis OLE<br/>   | [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |
| Controles ActiveX<br/>         | [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)IPersistMemory, IPersistPropertyBag, [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/> |
| ActiveX objetos de documento<br/> | [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |



 

Os implementadores de cliente também podem escolher quais interfaces de objeto persistentes o cliente pode usar. As interfaces que um cliente usa geralmente são determinadas por onde o cliente pode armazenar seus próprios dados. Um cliente que pode armazenar seus dados somente em um arquivo simples provavelmente usará apenas [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))e IPersistPropertyBag. (**IPersistStreamInit** pode substituir [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) na maioria dos aplicativos, porque ele contém essa definição e adiciona um método de inicialização.) Um cliente que pode salvar seus dados em um arquivo de armazenamento estruturado usará, além disso, [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inicializando objetos persistentes](initializing-persistent-objects.md)
</dt> </dl>

 

