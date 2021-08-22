---
description: Durante uma Windows instalador, o instalador pode pesquisar todas as unidades fixas para um arquivo.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Pesquisando todas as unidades fixas para um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d460cd55fe54a98c6a02e23e49af9ea9838c7651262fa03f868bdb76acc2d506
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041246"
---
# <a name="searching-all-fixed-drives-for-a-file"></a>Pesquisando todas as unidades fixas para um arquivo

**Para pesquisar todas as unidades fixas para um arquivo**

1.  Insira a assinatura de arquivo e o nome na [Tabela de Assinatura](signature-table.md). Os campos restantes nesse registro podem ser nulos para pesquisar qualquer versão do MyApp.exe.

    [Tabela de Assinatura](signature-table.md) (parcial)

    

    | Assinatura          | Nome do Arquivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Insira a propriedade que o Instalador deve definir se MyApp.exe estiver instalado.

    [Tabela AppSearch](appsearch-table.md)

    

    | Propriedade         | Assinatura          |
    |------------------|--------------------|
    | Myapp<br/> | AppFile<br/> |

    

     

3.  Use a [tabela DrLocator](drlocator-table.md). Deixe os campos Pai e Caminho vazios para pesquisar todas as unidades fixas do sistema de usuário. Especifique na coluna Profundidade o número de níveis de subdiretório a ser pesquisado. Por exemplo, definir Profundidade como 0 detecta c:MyApp.exe, mas não detecta o arquivo em uma profundidade de 2, por exemplo: c: Arquivos de Programas \\ \\ \\ MyApps \\MyApp.exe.

    [Tabela DrLocator](drlocator-table.md)

    

    | Assinatura          | Pai | Caminho | Profundidade        |
    |--------------------|--------|------|--------------|
    | AppFile<br/> |        |      | 3<br/> |

    

     

4.  Inclua a ação AppSearch na sequência de ação. Se MyApp.exe estiver instalado, o Instalador define a propriedade MYAPP como o local do arquivo. Se o arquivo estiver instalado, MYAPP será avaliada como True em uma expressão condicional.

 

 




