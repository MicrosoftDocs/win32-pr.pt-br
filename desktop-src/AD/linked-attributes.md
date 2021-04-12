---
title: Atributos vinculados (AD DS)
description: Atributos vinculados são pares de atributos nos quais o sistema calcula os valores de um atributo (o link voltar) com base nos valores definidos no outro atributo (o link para frente) em toda a floresta.
ms.assetid: 31b7e8f5-e46d-4aff-9b17-c8dec7f19bae
ms.tgt_platform: multiple
keywords:
- AD de atributos vinculados
- Atributos de AD, vinculados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0e3f6706c797497fb1bb25ea82805385f9897e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104365820"
---
# <a name="linked-attributes-ad-ds"></a>Atributos vinculados (AD DS)

Atributos vinculados são pares de atributos nos quais o sistema calcula os valores de um atributo (o link voltar) com base nos valores definidos no outro atributo (o link para frente) em toda a floresta. Um valor de vínculo de back-link em qualquer instância de objeto consiste no DNs de todos os objetos que têm o DN do objeto definido no link de encaminhamento correspondente. Por exemplo, "gerente" e "relatórios" são um par de atributos vinculados, em que gerente é o link de encaminhamento e os relatórios são o link voltar. Agora suponha que Bill seja gerente de Joe. Se você armazenar o DN do objeto de usuário de Bill no atributo "Manager" do objeto de usuário de Joe, o DN do objeto de usuário de Joe será exibido no atributo "Reports" do objeto de usuário da lista.

Um par link para frente/link de fundo é identificado pelos valores de [**LinkId**](/windows/desktop/ADSchema/a-linkid) de duas definições de [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . A **LinkId** do link de encaminhamento é um valor par, positivo, diferente de zero e a **LinkId** do link regressivo associado é o **LinkId** posterior mais um. Por exemplo, **LinkId** para "Manager" é 42 e **LinkId** para "Reports" é 43.

Veja a seguir uma lista de diretrizes para definir um novo par de atributos vinculados:

-   Os valores de [**LinkId**](/windows/desktop/ADSchema/a-linkid) devem ser exclusivos entre todos os objetos [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Para evitar conflitos, você deve gerar automaticamente o **LinkId** seguindo as instruções no tópico [obtendo uma ID de link](obtaining-a-link-id.md).
-   Um vínculo regressivo deve ter um link de encaminhamento correspondente, ou seja, o link de encaminhamento deve existir antes que um atributo back link correspondente possa ser criado.
-   Um vínculo regressivo sempre é um atributo com valores múltiplos. Um link de encaminhamento pode ter valor único ou com vários valores. Use um link de encaminhamento com vários valores quando houver uma relação muitos para muitos.
-   O valor de [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de um link de encaminhamento deve ser 2.5.5.1, 2.5.5.7 ou 2.5.5.14. Esses valores correspondem a sintaxes que contêm um nome distinto, como a sintaxe do [**objeto (DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn) .
-   O valor de [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de um vínculo regressivo deve ser 2.5.5.1, que é a sintaxe do [**objeto (DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn) .
-   Por convenção, os atributos de vínculos posteriores são adicionados ao valor [**mayContain**](/windows/desktop/ADSchema/a-maycontain) da classe abstrata [**Top**](/windows/desktop/ADSchema/c-top) . Isso permite que o atributo back link seja lido a partir de objetos de qualquer classe, pois eles não são realmente armazenados com o objeto, mas são calculados com base nos valores do link de encaminhamento.

 

 