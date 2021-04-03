---
description: Durante uma instalação de Windows Installer, o instalador pode pesquisar um arquivo e criar uma propriedade que contém o caminho do arquivo.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Procurando um arquivo e criando uma propriedade que contém o caminho do arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed742ee874c2e4b76137e9f17e90fbf54e9729f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828862"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a>Procurando um arquivo e criando uma propriedade que contém o caminho do arquivo

**Para pesquisar um arquivo e criar uma propriedade que contém o caminho do arquivo**

1.  Primeiro, faça uma pesquisa para o arquivo, listando a assinatura e o nome do arquivo na [tabela de assinatura](signature-table.md).

    Os campos restantes desse registro podem ser deixados em branco para especificar uma pesquisa de qualquer versão do MyApp.exe.

    [Tabela de assinatura](signature-table.md) (parcial)

    

    | Assinatura          | Nome do arquivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Em seguida, especifique o caminho do arquivo que está sendo pesquisado na [tabela DrLocator](drlocator-table.md).

    Como AppFolder não está listado na [tabela de assinatura](signature-table.md), o instalador determina que AppFolder é uma pasta em vez de um arquivo.

    [Tabela DrLocator](drlocator-table.md)

    

    | Assinatura            | Pai             | Caminho | Profundidade |
    |----------------------|--------------------|------|-------|
    | AppFile<br/>   |                    |      |       |
    | AppFolder<br/> | AppFile<br/> |      |       |

    

     

3.  Por fim, preencha a [tabela AppSearch](appsearch-table.md) para que a [ação AppSearch](appsearch-action.md) retorne o caminho de AppFolder.

    Depois que o instalador executar a ação AppSearch, o valor de MyFolder será o caminho completo de AppFolder.

    [Tabela AppSearch](appsearch-table.md) (parcial)

    

    | Propriedade            | Assinatura            |
    |---------------------|----------------------|
    | MYFOLDER<br/> | AppFolder<br/> |

    

     

 

 




