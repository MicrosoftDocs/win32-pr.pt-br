---
description: O desenvolvimento de um aplicativo COM+ bem-sucedido requer o design de arquitetura de aplicativo inicial.
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: Criando o aplicativo COM+ usando UML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48526623df5bc929daa4d8ce9cbe4d7592d6b30c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370415"
---
# <a name="designing-the-com-application-using-uml"></a>Criando o aplicativo COM+ usando UML

O desenvolvimento de um aplicativo COM+ bem-sucedido requer o design de arquitetura de aplicativo inicial. O Unified Modeling Language (UML) é fundamental para esse desenvolvimento de design. O UML é uma notação de modelagem para dados e processos de aplicativos que combina as práticas recomendadas do setor de software. Como o UML divide o aplicativo em três exibições que refletem o aplicativo, bem como seu empacotamento e implementação, a notação de modelagem se estende bem para dar suporte à modelagem empresarial.

O UML aborda três exibições do aplicativo, da seguinte maneira:

-   A exibição estática, que é modelada por informações obtidas de cenários de usuário e diagramas de classe.
-   A exibição dinâmica, que é modelada usando diagramas de sequência, colaboração e transição de estado.
-   A exibição funcional, que é a narrativa descritiva mais tradicional usando o pseudocódigo e as especificações.

As informações para essas exibições podem ser coletadas seguindo três etapas de design que funcionam bem com o UML. Antes de escrever uma única linha de código, você precisa criar os seguintes modelos:

<dl> <dt>

<span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Modelo conceitual
</dt> <dd>

Decida quais componentes e serviços são necessários.

</dd> <dt>

<span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Modelo lógico
</dt> <dd>

Determine em qual camada de design lógico ele pertence.

</dd> <dt>

<span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Modelo físico
</dt> <dd>

Determine onde os componentes residem fisicamente e como eles devem ser codificados.

</dd> </dl>

Esses modelos podem ser usados com ferramentas de caso baseado em UML. Para obter mais informações sobre esses três modelos de design, consulte os seguintes tópicos nesta seção:

-   [O modelo conceitual: requisitos de aplicativo](the-conceptual-model--application-requirements.md)
-   [O modelo lógico: definição e planejamento de aplicativos](the-logical-model--application-definition-and-planning.md)
-   [O modelo físico: arquitetura de aplicativo](the-physical-model--application-architecture.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Princípios e pressuposições de design de COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Dicas de design gerais para usar o COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Otimizando interações com a camada de lógica de negócios do COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Outras ferramentas da Microsoft para a criação de aplicativos distribuídos](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



