---
description: Um objeto consiste em um cabeçalho padrão e atributos específicos de objeto. como todos os objetos têm a mesma estrutura, há um único gerenciador de objetos no Windows que mantém todos os objetos.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Gerenciador de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b87b239d685d53b29243212e06ba2fd5af20e1249794355ed2169278c7f46c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885344"
---
# <a name="object-manager"></a>Gerenciador de objetos

Um objeto consiste em um cabeçalho padrão e atributos específicos de objeto. como todos os objetos têm a mesma estrutura, há um único gerenciador de objetos no Windows que mantém todos os objetos.

O cabeçalho do objeto inclui itens como o nome do objeto, para que outros processos possam referenciar o objeto por nome e um descritor de segurança, para que o Gerenciador de objetos possa controlar quais processos acessam o recurso do sistema.

As tarefas que o Gerenciador de objetos executa incluem o seguinte:

-   Criando objetos
-   Verificando se um processo tem o direito de usar o objeto
-   Criando identificadores de objeto e retornando-os para o chamador
-   Mantendo cotas de recursos
-   Criando identificadores duplicados
-   Identificadores de fechamento para objetos

 

 



