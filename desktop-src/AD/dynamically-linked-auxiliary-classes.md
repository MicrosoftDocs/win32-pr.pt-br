---
title: Classes auxiliares vinculadas dinamicamente
description: Uma classe auxiliar vinculada dinamicamente é uma classe que é anexada a um objeto individual, em vez de uma classe de objeto.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- AD de classes auxiliares vinculadas dinamicamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0cacb09d3aef05bcaf0ef729411c2e023469be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159329"
---
# <a name="dynamically-linked-auxiliary-classes"></a>Classes auxiliares vinculadas dinamicamente

Uma classe auxiliar vinculada dinamicamente é uma classe que é anexada a um objeto individual, em vez de uma classe de objeto. A vinculação dinâmica permite que você armazene atributos adicionais com um objeto individual sem o impacto em toda a floresta de estender a definição de esquema para uma classe inteira. Por exemplo, uma empresa poderia usar a vinculação dinâmica para anexar uma classe auxiliar específica de vendas aos objetos de usuário de suas pessoas de vendas e outras classes auxiliares específicas de departamento aos objetos de usuário de funcionários de outros departamentos.

A vinculação dinâmica não é complexa: Adicione o nome da classe auxiliar aos valores do atributo **objectClass** de um objeto. Se a classe auxiliar tiver atributos obrigatórios (**mustHave** ou **systemMustHave**), você deverá defini-los ao mesmo tempo. Para obter mais informações e um exemplo de código, consulte [adicionando uma classe auxiliar a uma instância de objeto](adding-an-auxiliary-class-to-an-object-instance.md).

Para remover uma classe auxiliar dinamicamente vinculada, limpe os valores de todos os atributos da classe auxiliar e, em seguida, remova o nome da classe auxiliar do atributo **objectClass** do objeto.

Se você adicionar dinamicamente uma classe auxiliar que é uma subclasse de outra classe auxiliar, ambas as classes auxiliares serão adicionadas ao objeto de destino. No entanto, remover a classe auxiliar filho não remove seu pai; cada classe deve ser explicitamente removida.

 

 




