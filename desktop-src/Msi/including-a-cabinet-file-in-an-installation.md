---
description: Esta seção descreve como incluir arquivos de gabinete em instalações do. Para obter mais informações, consulte usando gabinetes e fontes compactadas.
ms.assetid: 17ea7f76-90b2-48fb-8187-64dc6d294443
title: Incluindo um arquivo de gabinete em uma instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098e660de3f7ec7097ab02613d75219ac0a0d624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752645"
---
# <a name="including-a-cabinet-file-in-an-installation"></a>Incluindo um arquivo de gabinete em uma instalação

Esta seção descreve como incluir arquivos de gabinete em instalações do. Para obter mais informações, consulte [usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).

**Para incluir um arquivo de gabinete em um pacote de instalação**

1.  Use uma ferramenta de criação de gabinete para compactar os arquivos de origem em um arquivo de gabinete. Consulte [arquivos de gabinete](cabinet-files.md).
2.  O arquivo de gabinete deve estar localizado em um fluxo de dados dentro do arquivo. msi ou em um arquivo de gabinete separado localizado na raiz da árvore de origem especificada pela [tabela de diretórios](directory-table.md).
3.  Determine se a origem deve ser um tipo compactado ou misto que tenha arquivos compactados e descompactados. Consulte [fontes compactadas e descompactadas](compressed-and-uncompressed-sources.md). Dependendo do tipo de imagem de origem, defina os bits de sinalizador compactado ou descompactado da propriedade de [**Resumo contagem de palavras**](word-count-summary.md) .
4.  Adicione um registro à [tabela de arquivos](file-table.md) para cada um dos arquivos no gabinete. Insira uma chave de arquivo na coluna arquivo que corresponda exatamente à chave de arquivo do arquivo no gabinete. As chaves de arquivo diferenciam maiúsculas de minúsculas. A sequência de instalação de arquivo na tabela de arquivos e o gabinete também devem ser iguais. A sequência de arquivos é especificada pelo número de sequência na coluna sequência. Para chegar ao número de sequência do primeiro arquivo no gabinete, faça o seguinte. Localize o registro existente na [tabela de mídia](media-table.md) que tem o maior valor na coluna DiskId. O campo LastSequence desse registro fornece o último número de sequência de arquivo usado na mídia. Na tabela de arquivos, atribua o primeiro arquivo do novo gabinete um número de sequência maior que este. Atribua números de sequência a todos os arquivos restantes na mesma ordem que no arquivo de gabinete. Para obter uma descrição dos campos de registro restantes, consulte [tabela de arquivos](file-table.md).
5.  Adicione um registro à [tabela de mídia](media-table.md) para o gabinete. Especifique um valor no campo DiskId desse novo registro que seja maior do que o maior valor de DiskId já existente na tabela. Coloque o nome do gabinete no campo de gabinete. Esse nome deve estar na forma de um tipo de dados de [gabinete](cabinet.md) . Prefixe o nome com um sinal numérico " \# " se o gabinete for um fluxo de dados armazenado no arquivo. msi. Observe que, se o gabinete for um fluxo de dados, o nome do gabinete diferenciará maiúsculas de minúsculas. Se o gabinete for um arquivo separado, o nome do arquivo não diferenciará maiúsculas de minúsculas.
6.  Determine o maior número de sequência de arquivo no novo gabinete, verificando a coluna de sequência da tabela de arquivos atualizada. Insira um valor que seja maior que este no campo LastSequence do novo registro da tabela de mídia. Para obter uma descrição dos campos de registro restantes, consulte [tabela de mídia](media-table.md).
7.  Você pode armazenar o arquivo de gabinete no pacote de instalação usando uma ferramenta como Msidb.exe ou usando as [funções de banco de dados](database-functions.md)do instalador. As quatro etapas a seguir explicam como adicionar o gabinete de um programa usando as funções de banco de dados.
8.  Para adicionar o gabinete ao pacote de instalação de um programa, abra uma exibição na [ \_ tabela fluxos](-streams-table.md) do banco de dados usando [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa).
9.  Use [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) para definir a coluna de nome da \_ tabela de fluxos como o nome que aparece na coluna de gabinete da [tabela de mídia](media-table.md). Omita o sinal numérico: \# .
10. Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para definir a coluna de dados da \_ tabela de fluxos para os dados do gabinete.
11. Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para atualizar o registro na \_ tabela de fluxos.
12. Para usar Msidb.exe para adicionar o arquivo de gabinete Mycab.cab ao pacote de instalação denominado Mydatabase.msi, use a seguinte linha de comando: Msidb.exe-d mydatabase.msi-a mycab.cab. Nesse caso, a coluna de gabinete da tabela de mídia deve conter a cadeia de caracteres: \#mycab.cab.

 

 



