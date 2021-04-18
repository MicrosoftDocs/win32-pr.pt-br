---
description: A instalação e a remoção de cada arquivo são determinadas pelo componente de Windows Installer que controla o arquivo.
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: Especificando arquivos e atributos de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719dacbc434d47b4074a183e67edb02a88cb3c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759373"
---
# <a name="specifying-files-and-file-attributes"></a>Especificando arquivos e atributos de arquivo

A instalação e a remoção de cada arquivo são determinadas pelo [componente de Windows Installer](windows-installer-components.md) que controla o arquivo. Depois que o agrupamento de recursos em componentes for especificado, as informações de atributo de arquivo poderão ser adicionadas ao banco de dados de instalação. Nesta seção, você adiciona informações de arquivo ao banco de dados de instalação do exemplo do bloco de notas. Consulte o [grupo tabelas de arquivos](file-tables-group.md).

Os arquivos no exemplo do bloco de notas são descompactados. Consulte [fontes compactadas e descompactadas](compressed-and-uncompressed-sources.md) para obter informações sobre como adicionar arquivos de gabinete a pacotes. Este exemplo não contém informações de controle de versão de arquivo. Para obter mais informações sobre o controle de versão de arquivo, consulte [regras de controle de versão de arquivo](file-versioning-rules.md) e controle de versão de [arquivo padrão](default-file-versioning.md).

Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela de arquivos vazia.

[File Table](file-table.md)



| Arquivo         | Componente\_ | FileName     | FileSize | Versão | Idioma | Atributos | Sequência |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Beisebol    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Concerto     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Dance       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Comemorar    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Ajuda        | Help.txt     | 1000     |         |          | 0          | 1        |
| January.txt  | Janeiro     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Bloco de notas     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Bloco de notas     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Continuar](specifying-source-media.md)

 

 



