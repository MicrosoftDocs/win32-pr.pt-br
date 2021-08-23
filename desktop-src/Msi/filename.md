---
description: O tipo de dados filename é uma cadeia de caracteres de texto que contém um nome de arquivo ou pasta.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Nome de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d125a1151520fb4d3b885bd815b0a5bf58d2b00ec61581fc7773f1da1bd29e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636200"
---
# <a name="filename"></a>Nome de arquivo

O tipo de dados filename é uma cadeia de caracteres de texto que contém um nome de arquivo ou pasta. Por padrão, o nome do arquivo é considerado para usar a sintaxe de nome de arquivo curto; ou seja, nome de oito caracteres, ponto final (.) e extensão de 3 caracteres. Um nome de arquivo curto sempre deve ser fornecido porque a propriedade [**SHORTFILENAMES**](shortfilenames.md) pode ser definida ou o volume de destino para a instalação pode dar suporte apenas a nomes de arquivo curtos.

Para incluir um nome de arquivo longo com o nome de arquivo curto, separe-o do nome de arquivo curto com uma barra vertical ( \| ).

Por exemplo, as duas cadeias de caracteres a seguir são válidas:

-   status.txt
-   proje ~1.txt\| Project Status.txt

Nomes de arquivo curtos e longos não devem conter os seguintes caracteres:

-   barra (/) ou ( \\ )
-   ponto de interrogação (?)
-   barra vertical ( \| )
-   colchete angular direito (>)
-   colchete angular esquerdo (<)
-   dois pontos (:)
-   asterisco ( \* )
-   aspas (")

Além disso, nomes de arquivo curtos não devem conter os seguintes caracteres:

-   sinal de mais (+)
-   vírgula (,)
-   ponto e vírgula (;)
-   sinal de igual (=)
-   colchete esquerdo ( \[ )
-   colchete direito ( \] )

Nenhum espaço é permitido antes do separador de barra vertical ( \| ) para a sintaxe de nome de arquivo curto/arquivo longo. Nomes de arquivo curtos não podem incluir um espaço, embora um nome de arquivo longo possa. Um espaço pode existir após o separador somente se o nome de arquivo longo do nome do arquivo começar com o espaço. Nenhuma sintaxe de caminho completo é permitida.

> [!Note]  
> O formato da coluna FileName da tabela [MsiEmbeddedUI](msiembeddedui-table.md) é como o tipo de dados Format FileName, exceto que o separador da barra vertical ( \| ) para a sintaxe nome curto do arquivo/nome de arquivo longo não está disponível.

 

 

 



