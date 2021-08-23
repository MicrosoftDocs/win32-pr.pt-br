---
title: Inicializando objetos persistentes
description: Inicializando objetos persistentes
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee98b01c6c9eab28f8f96f98ea1a2980c9eb5d10988c2efbe495a920c98c51e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756176"
---
# <a name="initializing-persistent-objects"></a>Inicializando objetos persistentes

Várias das interfaces de objeto persistente, [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))e [IPersistPropertyBag,](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)permitem que os clientes inicializem objetos para um estado "novo" ou "padrão". Esse estado inicial é diferente de um objeto recém-criado, que não tem nenhum estado.

Inicializar o estado de um objeto, mesmo para o estado padrão, pode ser uma operação de computação intensiva ou de uso intensivo de recursos. Ao separar a criação da inicialização, a inicialização pode ser executada somente quando ela é realmente necessária e os clientes podem evitar inicializar objetos para o estado padrão apenas para carregar imediatamente os dados armazenados anteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces de objeto persistente](persistent-object-interfaces.md)
</dt> </dl>

 

 