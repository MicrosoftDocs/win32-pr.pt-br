---
title: Interfaces de objeto persistentes (COM)
description: Um objeto persistente implementa uma ou mais interfaces de objeto persistentes.
ms.assetid: 8c8e44e4-f564-4af5-9a8a-ac6883862cae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df8920f1242d077044654d1090adcc0e3f3f05c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917735"
---
# <a name="persistent-object-interfaces"></a>Interfaces de objeto persistentes

Um objeto persistente implementa uma ou mais *interfaces de objeto persistentes*. Os clientes usam interfaces de objeto persistentes para informar a esses objetos quando e onde armazenar seu estado. Todas as interfaces de objeto persistentes são derivadas de [**IPersist**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist), portanto, qualquer objeto que implemente qualquer interface de objeto persistente também implementa **IPersist**.

As seguintes interfaces de objeto persistentes estão definidas no momento:

-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)
-   [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)
-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)
-   [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))
-   [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))
-   [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))

Os implementadores escolhem as interfaces de objeto persistentes com suporte de um objeto, dependendo de como o objeto deve ser usado. Ao não dar suporte a nenhuma interface de objeto persistente, o implementador está dizendo efetivamente "o estado deste objeto não pode ser armazenado de forma persistente". Ao dar suporte a uma ou mais interfaces de objeto persistentes, o implementador está dizendo efetivamente "o estado desse objeto pode ser armazenado de forma persistente em um ou mais meios de armazenamento de dados".

Por exemplo, a tabela a seguir lista vários tipos de objeto que permitem suporte para diferentes interfaces de objeto persistente.



| Categoria                            | Interfaces de objeto persistentes geralmente suportadas                                                                                                                                                         |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Monikers<br/>                 | [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)<br/>                                                                                                                                                      |
| Objetos de inserção OLE<br/>   | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |
| Controles ActiveX<br/>         | [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), IPersistMemory, IPersistPropertyBag, [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/> |
| Objetos de documento ActiveX<br/> | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |



 

Os implementadores de cliente também podem escolher quais interfaces de objeto persistente o cliente pode usar. As interfaces que um cliente usa geralmente são determinadas por onde o cliente pode armazenar seus próprios dados. Um cliente que pode armazenar seus dados somente em um arquivo simples provavelmente usará apenas [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))e IPersistPropertyBag. (**IPersistStreamInit** pode substituir [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) na maioria dos aplicativos, pois contém essa definição e adiciona um método de inicialização.) Um cliente que pode salvar seus dados em um arquivo de armazenamento estruturado irá, além disso, usar [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inicializando objetos persistentes](initializing-persistent-objects.md)
</dt> </dl>

 

