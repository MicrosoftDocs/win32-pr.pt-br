---
description: A instalação e a remoção de cada arquivo são determinadas pelo componente Windows Instalador que controla o arquivo.
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: Especificando arquivos e atributos de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdb63bf2779ddc5730013bad06b382c168a62bab5e897d5d621f7a65644e445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893726"
---
# <a name="specifying-files-and-file-attributes"></a>Especificando arquivos e atributos de arquivo

A instalação e a remoção de cada arquivo são determinadas [pelo componente Windows Instalador que](windows-installer-components.md) controla o arquivo. Depois que o grupo de recursos em componentes for especificado, as informações de atributo de arquivo poderão ser adicionadas ao banco de dados de instalação. Nesta seção, você adicionará informações de arquivo ao banco de dados de instalação para o Bloco de notas exemplo. Consulte o [Grupo tabelas de arquivos](file-tables-group.md).

Os arquivos na amostra Bloco de notas são descompactados. Consulte [Fontes compactadas e descompactados para](compressed-and-uncompressed-sources.md) obter informações sobre como adicionar arquivos de gabinete a pacotes. Este exemplo não contém informações de versão de arquivo. Para obter mais informações sobre o versionamento de arquivo, consulte [Regras de versão de arquivo](file-versioning-rules.md) e Versão de arquivo [padrão.](default-file-versioning.md)

Use o editor de banco de dados para MNP2000.msi e insira os dados a seguir na tabela Arquivo vazia.

[File Table](file-table.md)



| Arquivo         | Componente\_ | FileName     | FileSize | Versão | Idioma | Atributos | Sequência |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Beisebol    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Concerto     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Dança       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Futebol    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Ajuda        | Help.txt     | 1000     |         |          | 0          | 1        |
| January.txt  | Janeiro     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Bloco de notas     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Bloco de notas     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Continuar](specifying-source-media.md)

 

 



