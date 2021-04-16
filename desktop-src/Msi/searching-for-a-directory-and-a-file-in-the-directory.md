---
description: Durante uma instalação de Windows Installer, o instalador pode pesquisar um diretório e um arquivo nesse diretório.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Procurando um diretório e um arquivo no diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768460"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a>Procurando um diretório e um arquivo no diretório

**Para procurar um diretório e, em seguida, um arquivo nesse diretório**

1.  Primeiro, procure o diretório.

    AppDir deve ser definido como a assinatura válida do diretório. Se AppDir não estiver definido como uma assinatura válida, AppSearch não terá um local para localizar o arquivo, por exemplo, se a pesquisa for para c: \\ MyDir \\MyApp.exe, appdir deverá ser definido como c: \\ mydir. AppDir pode ser definido por meio da inclusão de um registro na [tabela DrLocator](drlocator-table.md)ou por algum outro método. Nenhum registro está incluído na [tabela de assinatura](signature-table.md) para a pesquisa de diretório. Para a pesquisa de arquivos, liste a assinatura e o nome do arquivo na tabela de assinatura. Os campos restantes nesse registro podem ser nulos para pesquisar qualquer versão do MyApp.exe.

    [Tabela de assinatura](signature-table.md) (parcial)

    

    | Assinatura          | Nome do Arquivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Use a [tabela AppSearch](appsearch-table.md).

    Insira a propriedade que o instalador deve definir se o diretório com a assinatura AppDir estiver instalado. Se o instalador encontrar esse diretório estiver instalado, ele definirá MYDIR como o caminho do diretório. Insira a propriedade que o instalador deve definir se MyApp.exe estiver instalado.

    [Tabela AppSearch](appsearch-table.md) (parcial)

    

    | Propriedade         | Assinatura          |
    |------------------|--------------------|
    | MYDIR<br/> | AppDir<br/>  |
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  Use a [tabela DrLocator](drlocator-table.md).

    Insira na coluna pai a assinatura, AppDir, que é definida como o caminho do diretório. Especifique na coluna profundidade o número de níveis de subdiretório para Pesquisar nesse diretório. AppDir deve ser definido como a assinatura de diretório. AppDir pode ser definido por meio da inclusão de um registro, como mostrado aqui ou por outro método.

    [Tabela DrLocator](drlocator-table.md)

    

    | Assinatura | Pai | Caminho      | Profundidade |
    |-----------|--------|-----------|-------|
    | AppDir    |        | C: \\ mydir | 0     |
    | AppFile   | AppDir |           | 0     |

    

     

4.  Inclua a ação AppSearch na sequência de ação.

    Se MyApp.exe for encontrado para ser instalado em AppDir, o instalador definirá a propriedade MYAPP como o local do arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisando aplicativos, arquivos, entradas de registro ou entradas de arquivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




