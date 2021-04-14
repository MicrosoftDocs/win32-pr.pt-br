---
title: Criando objetos dinâmicos
description: Especifique a classe auxiliar DynamicObject como um valor para o atributo objectClass no momento da instanciação de um objeto.
ms.assetid: d2d961c5-6420-446f-bbb2-54984410e04e
ms.tgt_platform: multiple
keywords:
- Criando o AD de objetos dinâmicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f41ee98d002fa6004503ff83049fb07ff52b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453520"
---
# <a name="creating-dynamic-objects"></a>Criando objetos dinâmicos

Especifique a classe auxiliar **DynamicObject** como um valor para o atributo **objectClass** no momento da instanciação de um objeto. Nesse caso, a classe auxiliar especial aparecerá na lista de classes que é o valor do atributo **objectClass** para o objeto. Se um valor para o atributo **entryTTL** não for fornecido no momento da adição da classe auxiliar especial, um valor padrão, conforme especificado posteriormente, será fornecido por Active Directory Domain Services.

Para obter mais informações sobre como adicionar uma classe auxiliar a um objeto, consulte [classes auxiliares dinâmicas](dynamic-auxiliary-classes.md).

 

 




