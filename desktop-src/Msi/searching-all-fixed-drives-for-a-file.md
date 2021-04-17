---
description: Durante uma instalação de Windows Installer, o instalador pode pesquisar por um arquivo em todas as unidades fixas.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Pesquisando todas as unidades fixas de um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b79c7f2999d4ee7937790dc68470210f1d4b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758765"
---
# <a name="searching-all-fixed-drives-for-a-file"></a>Pesquisando todas as unidades fixas de um arquivo

**Para pesquisar todas as unidades fixas de um arquivo**

1.  Insira a assinatura e o nome do arquivo na [tabela de assinatura](signature-table.md). Os campos restantes nesse registro podem ser nulos para pesquisar qualquer versão do MyApp.exe.

    [Tabela de assinatura](signature-table.md) (parcial)

    

    | Assinatura          | Nome do Arquivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Insira a propriedade que o instalador deve definir se MyApp.exe estiver instalado.

    [Tabela AppSearch](appsearch-table.md)

    

    | Propriedade         | Assinatura          |
    |------------------|--------------------|
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  Use a [tabela DrLocator](drlocator-table.md). Deixe os campos pai e caminho vazios para pesquisar todas as unidades fixas do sistema de usuário. Especifique na coluna profundidade o número de níveis de subdiretório a serem pesquisados. Por exemplo, a definição de profundidade como 0 detecta c: \\MyApp.exe, mas não detecta o arquivo em uma profundidade de 2, por exemplo: c: \\ arquivos de programas \\ myapps \\MyApp.exe.

    [Tabela DrLocator](drlocator-table.md)

    

    | Assinatura          | Pai | Caminho | Profundidade        |
    |--------------------|--------|------|--------------|
    | AppFile<br/> |        |      | 3<br/> |

    

     

4.  Inclua a ação AppSearch na sequência de ação. Se MyApp.exe estiver instalado, o instalador definirá a propriedade MYAPP para o local do arquivo. Se o arquivo estiver instalado, MYAPP será avaliado como true em uma expressão condicional.

 

 




