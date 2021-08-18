---
title: Classes auxiliares vinculadas dinamicamente
description: Uma classe auxiliar vinculada dinamicamente é uma classe anexada a um objeto individual, em vez de a uma classe de objeto.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- AD de classes auxiliares vinculadas dinamicamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5fc73ef64e1ed4af0dd73879dc1cd7ed8b2d82ac1d397db001c1487680b13b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695369"
---
# <a name="dynamically-linked-auxiliary-classes"></a>Classes auxiliares vinculadas dinamicamente

Uma classe auxiliar vinculada dinamicamente é uma classe anexada a um objeto individual, em vez de a uma classe de objeto. A vinculação dinâmica permite que você armazene atributos adicionais com um objeto individual sem o impacto em toda a floresta de estender a definição de esquema para uma classe inteira. Por exemplo, uma empresa pode usar a vinculação dinâmica para anexar uma classe auxiliar específica de vendas aos objetos de usuário de suas pessoas de vendas e outras classes auxiliares específicas do departamento aos objetos de usuário de funcionários em outros departamentos.

A vinculação dinâmica não é complexa: adicione o nome da classe auxiliar aos valores do atributo **objectClass de um** objeto. Se a classe auxiliar tiver atributos obrigatórios (**mustHave** ou **systemMustHave**), você deverá defini-los ao mesmo tempo. Para obter mais informações e um exemplo de código, consulte [Adicionando uma classe auxiliar a uma instância de objeto](adding-an-auxiliary-class-to-an-object-instance.md).

Para remover uma classe auxiliar vinculada dinamicamente, limpe os valores de todos os atributos da classe auxiliar e remova o nome da classe auxiliar do atributo **objectClass** do objeto .

Se você adicionar dinamicamente uma classe auxiliar que seja uma subclasse de outra classe auxiliar, ambas as classes auxiliares serão adicionadas ao objeto de destino. No entanto, remover a classe auxiliar filho não remove seu pai; cada classe deve ser removida explicitamente.

 

 




