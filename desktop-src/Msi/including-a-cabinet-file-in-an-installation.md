---
description: Esta seção descreve a inclusão de arquivos de gabinete em instalações. Para obter mais informações, consulte Usando gabinetes e fontes compactadas.
ms.assetid: 17ea7f76-90b2-48fb-8187-64dc6d294443
title: Incluindo um arquivo de gabinete em uma instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0970d87b8b219e1558c6b3f1daf78a6a01100a7bc41f9ae1dad51a25048b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787336"
---
# <a name="including-a-cabinet-file-in-an-installation"></a>Incluindo um arquivo de gabinete em uma instalação

Esta seção descreve a inclusão de arquivos de gabinete em instalações. Para obter mais informações, consulte [Usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).

**Para incluir um arquivo de gabinete em um pacote de instalação**

1.  Use uma ferramenta de criação de gabinete para compactar os arquivos de origem em um arquivo de gabinete. Consulte [Arquivos de gabinete](cabinet-files.md).
2.  O arquivo de gabinete deve estar localizado em um fluxo de dados dentro do arquivo .msi ou em um arquivo de gabinete separado localizado na raiz da árvore de origem especificada pela Tabela [de Diretórios](directory-table.md).
3.  Determine se a origem deve ser um tipo compactado ou um tipo misto que tenha arquivos descompactados e compactados. Consulte [Fontes compactadas e descompactados.](compressed-and-uncompressed-sources.md) Dependendo do tipo de imagem de origem, de definir os bits de sinalizador compactados ou descompactados da propriedade [**Resumo de Contagem de**](word-count-summary.md) Palavras.
4.  Adicione um registro à [tabela Arquivo](file-table.md) para cada um dos arquivos no gabinete. Insira uma chave de arquivo na coluna Arquivo que corresponde exatamente à chave de arquivo do arquivo no gabinete. As chaves de arquivo são sensíveis a minúsculas. A sequência de instalação do arquivo na tabela Arquivo e no gabinete também deve ser a mesma. A sequência de arquivos é especificada pelo número de sequência na coluna Sequência. Para chegar ao número de sequência do primeiro arquivo no gabinete, faça o seguinte. Localize o registro existente na tabela [Mídia com](media-table.md) o maior valor na coluna DiskID. O campo LastSequence desse registro fornece o último número de sequência de arquivos usado na mídia. Na tabela Arquivo, atribua ao primeiro arquivo do novo gabinete um número de sequência maior que este. Atribua números de sequência a todos os arquivos restantes na mesma ordem que no arquivo de gabinete. Para ver uma descrição dos campos de registro restantes, consulte [Tabela de arquivos](file-table.md).
5.  Adicione um registro à tabela [Mídia](media-table.md) para o gabinete. Especifique um valor no campo DiskID desse novo registro maior que o maior valor DiskID já existente na tabela. Coloque o nome do gabinete no campo Gabinete. Esse nome deve estar na forma de um tipo [de dados De gabinete.](cabinet.md) Prefixe o nome com um sinal de número " " se o gabinete for um fluxo \# de dados armazenado no .msi arquivo. Observe que, se o gabinete for um fluxo de dados, o nome do gabinete será sensível a minúsculas. Se o gabinete for um arquivo separado, o nome do arquivo não será sensível a minúsculas.
6.  Determine o maior número de sequência de arquivos no novo gabinete verificando a coluna Sequência da tabela Arquivo atualizada. Insira um valor maior que este no campo LastSequence do novo registro da tabela Mídia. Para ver uma descrição dos campos de registro restantes, consulte [Tabela de mídia](media-table.md).
7.  Você pode armazenar o arquivo de gabinete no pacote de instalação usando uma ferramenta como Msidb.exe ou usando funções de banco de dados [do instalador.](database-functions.md) As quatro etapas a seguir explicam como adicionar o gabinete de um programa usando as funções de banco de dados.
8.  Para adicionar o gabinete ao pacote de instalação [ \_](-streams-table.md) de um programa, abra uma exibição na Fluxos do banco de dados usando [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa).
9.  Use [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) para definir a coluna Nome da tabela Fluxos para o nome que aparece na coluna Gabinete da tabela \_ [Mídia](media-table.md). Omita o sinal de número: \# .
10. Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para definir a coluna Dados \_ da tabela Fluxos para os dados do gabinete.
11. Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para atualizar o registro na \_ tabela Fluxos dados.
12. Para usar Msidb.exe adicionar o arquivo de gabinete Mycab.cab ao pacote de instalação chamado Mydatabase.msi, use a seguinte linha de comando: Msidb.exe -d mydatabase.msi -a mycab.cab. Nesse caso, a coluna Gabinete da tabela Mídia deve conter a cadeia de caracteres: \#mycab.cab.

 

 



