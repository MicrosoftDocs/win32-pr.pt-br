---
description: Durante uma Windows do instalador, o instalador pode pesquisar um arquivo e criar uma propriedade que contém o caminho do arquivo.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Pesquisando um arquivo e criando uma propriedade que mantém o caminho do arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d1315616c6d2ea24052ddad85c005d53716f8b130f4aa2d23d69754c946416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041136"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a>Pesquisando um arquivo e criando uma propriedade que mantém o caminho do arquivo

**Para pesquisar um arquivo e criar uma propriedade que mantenha o caminho desse arquivo**

1.  Primeiro, pesquise o arquivo listando a assinatura e o nome do arquivo na [Tabela de Assinatura](signature-table.md).

    Os campos restantes desse registro podem ser deixados vazios para especificar uma pesquisa para qualquer versão do MyApp.exe.

    [Tabela de Assinatura](signature-table.md) (parcial)

    

    | Assinatura          | Nome do arquivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Em seguida, especifique o caminho do arquivo que está sendo pesquisado na [Tabela DrLocator](drlocator-table.md).

    Como AppFolder não está listado na Tabela [de Assinatura,](signature-table.md)o Instalador determina que AppFolder é uma pasta em vez de um arquivo.

    [Tabela DrLocator](drlocator-table.md)

    

    | Assinatura            | Pai             | Caminho | Profundidade |
    |----------------------|--------------------|------|-------|
    | AppFile<br/>   |                    |      |       |
    | AppFolder<br/> | AppFile<br/> |      |       |

    

     

3.  Por fim, preencha a [Tabela appSearch](appsearch-table.md) para que [a Ação do AppSearch](appsearch-action.md) retorne o caminho de AppFolder.

    Depois que o Instalador executar a ação AppSearch, o valor de MYFOLDER será o caminho completo de AppFolder.

    [Tabela AppSearch](appsearch-table.md) (parcial)

    

    | Propriedade            | Assinatura            |
    |---------------------|----------------------|
    | Myfolder<br/> | AppFolder<br/> |

    

     

 

 




