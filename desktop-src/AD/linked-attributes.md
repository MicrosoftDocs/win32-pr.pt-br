---
title: Atributos vinculados (AD DS)
description: Atributos vinculados são pares de atributos nos quais o sistema calcula os valores de um atributo (o link voltar) com base nos valores definidos no outro atributo (o link de encaminhamento) em toda a floresta.
ms.assetid: 31b7e8f5-e46d-4aff-9b17-c8dec7f19bae
ms.tgt_platform: multiple
keywords:
- AD de atributos vinculados
- Atributos do AD , vinculados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2167169d6a9d2f8eabe69323054767ae66823d8e1fe954a232ed63fd31a9b845
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186989"
---
# <a name="linked-attributes-ad-ds"></a>Atributos vinculados (AD DS)

Atributos vinculados são pares de atributos nos quais o sistema calcula os valores de um atributo (o link voltar) com base nos valores definidos no outro atributo (o link de encaminhamento) em toda a floresta. Um valor de back-link em qualquer instância de objeto consiste nos DNs de todos os objetos que têm o DN do objeto definido no link de encaminhamento correspondente. Por exemplo, "Manager" e "Reports" são um par de atributos vinculados, em que Manager é o link de encaminhamento e Relatórios é o link de retorno. Agora, suponha que Bill seja o gerente de Joe. Se você armazenar o DN do objeto de usuário de Bill no atributo "Manager" do objeto de usuário de Joe, o DN do objeto de usuário de Joe será aparecer no atributo "Relatórios" do objeto de usuário de Bill.

Um par de link/link de retorno é identificado pelos valores [**linkID**](/windows/desktop/ADSchema/a-linkid) de duas [**definições de attributeSchema.**](/windows/desktop/ADSchema/c-attributeschema) A **linkID** do link de encaminhamento é um valor even, positive, nonzero e a **linkID** do link back associado é o **linkID** de encaminhamento mais um. Por exemplo, o **linkID** para "Manager" é 42 e o **linkID** para "Relatórios" é 43.

Veja a seguir uma lista de diretrizes para definir um novo par de atributos vinculados:

-   Os [**valores de linkID**](/windows/desktop/ADSchema/a-linkid) devem ser exclusivos entre todos [**os objetos attributeSchema.**](/windows/desktop/ADSchema/c-attributeschema) Para evitar conflitos, você deve gerar automaticamente a **linkID** seguindo as instruções no tópico [Obtendo uma ID de link](obtaining-a-link-id.md).
-   Um link voltar deve ter um link de encaminhamento correspondente, ou seja, o link de encaminhamento deve existir antes que um atributo de link de retorno correspondente possa ser criado.
-   Um link voltar é sempre um atributo com vários valores. Um link de encaminhamento pode ser de valor único ou de vários valores. Use um link de encaminhamento com vários valores quando houver uma relação muitos para muitos.
-   O [**valor attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de um link de encaminhamento deve ser 2.5.5.1, 2.5.5.7 ou 2.5.5.14. Esses valores correspondem a sintaxes que contêm um nome diferenciado, como a [**sintaxe Object(DS-DN).**](/windows/desktop/ADSchema/s-object-ds-dn)
-   O [**valor attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de um link de retorno deve ser 2.5.5.1, que é a sintaxe [**Object(DS-DN).**](/windows/desktop/ADSchema/s-object-ds-dn)
-   Por convenção, os atributos de link de fundo são adicionados ao [**valor mayContain**](/windows/desktop/ADSchema/a-maycontain) da [**classe abstrata**](/windows/desktop/ADSchema/c-top) superior. Isso permite que o atributo de link de fundo seja lido de objetos de qualquer classe porque eles não são realmente armazenados com o objeto , mas são calculados com base nos valores de link de encaminhamento.

 

 