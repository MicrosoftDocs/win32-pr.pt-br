---
title: Considerações sobre programação (Agendador de Tarefas)
description: Ao desenvolver aplicativos que usam o Agendador de Tarefas 1,0, tenha em mente os seguintes problemas de programação. Seu aplicativo deve garantir que o serviço de Agendador de Tarefas esteja em execução antes de tentar fazer qualquer chamada usando a API Agendador de Tarefas. Ao recuperar cadeias de caracteres, certifique-se de chamar CoTaskMemFree para liberar cada cadeia de caracteres depois que ela não for mais necessária. Ao recuperar matrizes de cadeias de caracteres, certifique-se de primeiro lançar cada cadeia de caracteres na matriz e, em seguida, liberar a própria matriz. Ao criar ou modificar um item de trabalho, incluindo gatilhos associados a um item de trabalho, certifique-se de chamar IPersistFile Save para salvar o item de trabalho em disco. Depois de usar qualquer uma das interfaces fornecidas pela API de Agendador de Tarefas, certifique-se de chamar a versão IUnknown para liberar a interface. Há suporte para IUnknown em cada objeto de Agendador de Tarefas.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- Iniciando Agendador de Tarefas
- considerações sobre programação Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105780582"
---
# <a name="programming-considerations-task-scheduler"></a>Considerações sobre programação (Agendador de Tarefas)

Ao desenvolver aplicativos que usam o Agendador de Tarefas 1,0, tenha em mente os seguintes problemas de programação.

-   Seu aplicativo deve garantir que o serviço de Agendador de Tarefas esteja em execução antes de tentar fazer qualquer chamada usando a API Agendador de Tarefas.
-   Ao recuperar cadeias de caracteres, certifique-se de chamar [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar cada cadeia de caracteres depois que ela não for mais necessária. Ao recuperar matrizes de cadeias de caracteres, certifique-se de primeiro lançar cada cadeia de caracteres na matriz e, em seguida, liberar a própria matriz.
-   Ao criar ou modificar um item de trabalho, incluindo gatilhos associados a um item de trabalho, certifique-se de chamar [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para salvar o item de trabalho em disco.
-   Depois de usar qualquer uma das interfaces fornecidas pela API de Agendador de Tarefas, certifique-se de chamar [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar a interface. Há suporte para [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) em cada objeto de Agendador de tarefas.

A seção usando da documentação do Agendador de Tarefas fornece inúmeros exemplos que seguem essas diretrizes. A tabela a seguir fornece saltos para alguns desses exemplos.

| Para um exemplo de         | Consulte                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| Liberando cadeias de caracteres         | [Recuperando exemplos de propriedade de item de trabalho](retrieving-work-item-property-examples.md)       |
| Salvando itens de trabalho em disco | [Definindo exemplos de propriedade de item de trabalho](setting-work-item-property-examples.md)             |
| Liberando interfaces      | [Criando uma tarefa usando o exemplo NewWorkItem](creating-a-task-using-newworkitem-example.md) |



 

 

 
