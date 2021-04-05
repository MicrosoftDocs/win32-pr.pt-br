---
description: Um objeto consiste em um cabeçalho padrão e atributos específicos de objeto. Como todos os objetos têm a mesma estrutura, há um Gerenciador de objetos único no Windows que mantém todos os objetos.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Gerenciador de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a74581650828a77c6423825d3c557a13075a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922224"
---
# <a name="object-manager"></a>Gerenciador de objetos

Um objeto consiste em um cabeçalho padrão e atributos específicos de objeto. Como todos os objetos têm a mesma estrutura, há um Gerenciador de objetos único no Windows que mantém todos os objetos.

O cabeçalho do objeto inclui itens como o nome do objeto, para que outros processos possam referenciar o objeto por nome e um descritor de segurança, para que o Gerenciador de objetos possa controlar quais processos acessam o recurso do sistema.

As tarefas que o Gerenciador de objetos executa incluem o seguinte:

-   Criando objetos
-   Verificando se um processo tem o direito de usar o objeto
-   Criando identificadores de objeto e retornando-os para o chamador
-   Mantendo cotas de recursos
-   Criando identificadores duplicados
-   Identificadores de fechamento para objetos

 

 



