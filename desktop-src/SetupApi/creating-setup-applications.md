---
description: Depois de criar um arquivo INF, você normalmente escreverá o código-fonte do seu aplicativo de instalação. Você chama as funções de instalação do seu aplicativo de instalação para executar muitas operações de instalação.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Criando aplicativos de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aaca2b1d509795f625e67c18c13131d7e502b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754493"
---
# <a name="creating-setup-applications"></a>Criando aplicativos de instalação

Depois de criar um arquivo INF, você normalmente escreverá o código-fonte do seu aplicativo de instalação. Você chama as funções de instalação do seu aplicativo de instalação para executar muitas operações de instalação.

As etapas a seguir abrangem uma maneira de usar as funções de instalação para criar um aplicativo de instalação. Você pode usar este exemplo como um ponto de partida ou desenvolver seu próprio algoritmo de instalação.

**Initialization**

-   [Abra o INF e, se apropriado, acrescente outros arquivos INF.](opening-the-inf-file.md)
-   [Extraia informações de arquivo do arquivo INF.](extracting-file-information-from-the-inf-file.md)
-   [Coletar informações de instalação do usuário.](gathering-setup-information-from-the-user.md)
-   [Crie uma fila.](creating-a-queue-and-queuing-file-operations.md)

**Arquivos de instalação**

-   [Confirme a fila, especificando uma rotina de retorno de chamada.](committing-the-queue.md)
-   [Atualizar informações do registro.](updating-registry-information.md)

**Limpeza**

-   [Feche a fila de arquivos e o INF.](closing-the-file-queue-and-inf-file.md)
-   [Libere outros recursos do sistema e encerre o programa.](releasing-other-system-resources.md)

 

 



