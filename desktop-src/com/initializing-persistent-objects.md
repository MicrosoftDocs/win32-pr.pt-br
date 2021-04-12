---
title: Inicializando objetos persistentes
description: Inicializando objetos persistentes
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211d9d89b7a8f36ab06d9930e45f365e0fb5d4dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366755"
---
# <a name="initializing-persistent-objects"></a>Inicializando objetos persistentes

Várias das interfaces de objeto persistente, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))e [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), permitem que os clientes inicializem objetos para um estado "novo" ou "padrão". Esse estado inicial é diferente do de um objeto recém-criado, que não tem estado.

Inicializar o estado de um objeto, mesmo para o estado padrão, pode ser uma operação de computação intensiva ou com uso intensivo de recursos. Ao separar a criação da inicialização, a inicialização pode ser executada somente quando é realmente necessária e os clientes podem evitar a inicialização de objetos para o estado padrão somente para carregar imediatamente os dados armazenados anteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces de objeto persistentes](persistent-object-interfaces.md)
</dt> </dl>

 

 