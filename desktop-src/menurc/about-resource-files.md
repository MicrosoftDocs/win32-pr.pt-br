---
title: Sobre arquivos de recurso
description: Descreve como incluir recursos em seu aplicativo baseado em Windows com RC.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f351592c57cb628204ad6528a48bfa1a10507f5e7aad90a524ea2f6034f304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034464"
---
# <a name="about-resource-files"></a>Sobre arquivos de recurso

Para incluir recursos em seu Windows baseado em recursos com RC, faça o seguinte:

1.  Crie arquivos individuais para seus cursores, ícones, bitmaps, caixas de diálogo e fontes.
2.  Crie um script de definição de recurso (arquivo .rc) que descreve os recursos usados pelo seu aplicativo.
3.  Compile o script com RC. Para obter mais informações, [consulte Usando RC (a linha de comando RC)](using-rc-the-rc-command-line-.md).
4.  Vincule o arquivo de recurso compilado (.res) ao arquivo executável do aplicativo com o seu linker.

Um arquivo de recurso é um arquivo de texto com a extensão .rc. O arquivo pode usar caracteres Unicode, de byte único, de byte duplo. A sintaxe e a semântica do pré-processador RC são semelhantes às do compilador C/C++ da Microsoft. No entanto, o RC dá suporte a um subconjunto das diretivas de pré-processador, defines e pragmas em um script.

O arquivo de script define recursos. Para um recurso que existe em um arquivo separado, como um ícone ou cursor, o script especifica o recurso e o arquivo que o contém. Para alguns recursos, como um menu, toda a definição do recurso existe dentro do script.

Os tópicos a seguir descrevem as informações que um arquivo de script pode conter:

-   [Comentários](comments.md), que são observações a serem ignoradas pelo RC.
-   [Macros predefinidos](predefined-macros.md), que não têm argumentos e não podem ser redefinidas.
-   [Diretivas de pré-processador](preprocessor-directives.md), que instruem o RC a executar ações no script antes de compilá-lo.
-   [Operadores de pré-processador](preprocessor-operators.md), que são usados com a **\# diretiva define.**
-   [Diretivas pragma](pragma-directives.md)
-   [Instruções de definição de recurso](resource-definition-statements.md), que nomeam e descrevem recursos.

 

 




