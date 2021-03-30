---
title: Sobre arquivos de recurso
description: Descreve como incluir recursos em seu aplicativo baseado no Windows com o RC.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c43e9df59cf0b6507b6c6a53c42299b8792634f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005523"
---
# <a name="about-resource-files"></a>Sobre arquivos de recurso

Para incluir recursos em seu aplicativo baseado no Windows com o RC, faça o seguinte:

1.  Crie arquivos individuais para seus cursores, ícones, bitmaps, caixas de diálogo e fontes.
2.  Crie um script de definição de recurso (arquivo. rc) que descreve os recursos usados pelo seu aplicativo.
3.  Compile o script com o RC. Para obter mais informações, consulte [usando o RC (a linha de comando RC)](using-rc-the-rc-command-line-.md).
4.  Vincule o arquivo de recurso compilado (. res) no arquivo executável do aplicativo com o vinculador.

Um arquivo de recurso é um arquivo de texto com a extensão. rc. O arquivo pode usar caracteres de byte único, dois bytes ou Unicode. A sintaxe e a semântica do pré-processador do RC são semelhantes às do compilador do Microsoft C/C++. No entanto, o RC dá suporte a um subconjunto de diretivas de pré-processador, define e pragmas em um script.

O arquivo de script define os recursos. Para um recurso que existe em um arquivo separado, como um ícone ou cursor, o script especifica o recurso e o arquivo que o contém. Para alguns recursos, como um menu, toda a definição do recurso existe no script.

Os tópicos a seguir descrevem as informações que um arquivo de script pode conter:

-   [Comentários](comments.md), que são observações a serem ignoradas pelo RC.
-   [Macros predefinidas](predefined-macros.md), que não usam argumentos e não podem ser redefinidas.
-   [Diretivas](preprocessor-directives.md)de pré-processador, que instruem o RC a executar ações no script antes de compilá-lo.
-   [Operadores de pré-processador](preprocessor-operators.md), que são usados com a diretiva **\# define** .
-   [Diretivas pragma](pragma-directives.md)
-   [Instruções de definição de recurso](resource-definition-statements.md), que nome e descrevem recursos.

 

 




