---
description: A tabela de arquivos contém uma lista completa de todos os arquivos de origem para a instalação.
ms.assetid: 481fdc45-82db-4128-93de-388562f636e9
title: Ordenando números de sequência de arquivos em um gabinete, tabela de arquivos e tabelas de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f64558a570c7184da36feba8aeea6d2a7dc32c0d8add4c6963dece131c4849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327862"
---
# <a name="ordering-file-sequence-numbers-in-a-cabinet-file-table-and-media-table"></a>Ordenando números de sequência de arquivos em um gabinete, tabela de arquivos e tabelas de mídia

A [tabela de arquivos](file-table.md) contém uma lista completa de todos os arquivos de origem para a instalação. Os arquivos podem ser armazenados na mídia de origem como arquivos individuais ou compactados em [arquivos de gabinete](cabinet-files.md). Os números de sequência na coluna sequência da tabela de arquivos, juntamente com o campo LastSequence da [tabela de mídia](media-table.md), especificam a ordem de instalação dos arquivos e a mídia de origem na qual cada arquivo está localizado. Cada registro na tabela de mídia identifica o disco de origem que contém todos os arquivos com números de sequência menores ou iguais ao valor mostrado na coluna LastSequence e maior que o valor de LastSequence do disco anterior.

Por exemplo, suponha que um arquivo tenha um número de sequência de 92 inserido na coluna sequência da tabela de arquivos. Para determinar em qual disco de origem esse arquivo reside, o instalador verifica o registro da tabela de mídia para a entrada com o menor valor de LastSequence maior que 92. A coluna DiskId é a chave primária para a tabela de mídia e esse campo identifica exclusivamente o disco na tabela.

o limite máximo do número de arquivos que podem ser listados na tabela de arquivos de um pacote de Windows Installer é 32767 arquivos. para criar um pacote de Windows Installer que contém mais arquivos, consulte [criando um pacote grande](authoring-a-large-package.md).

Os autores de pacotes podem reduzir o tamanho de seus pacotes de instalação compactando os arquivos de origem e incluindo-os em arquivos de gabinete. A imagem do arquivo de origem pode ser compactada, descompactada ou uma mistura de ambos os tipos. Para obter mais informações sobre fontes compactadas e não compactadas [, consulte fontes compactadas e descompactadas](compressed-and-uncompressed-sources.md). Os arquivos de origem compactados devem ser armazenados dentro de um arquivo de gabinete. Os arquivos compactados dentro de um gabinete têm seus próprios números de sequência internos. Os valores desses números de sequência interna não precisam corresponder ao valor dos números de sequência dentro da tabela de arquivos. No entanto, a sequência dos arquivos especificados na tabela de arquivos deve ser idêntica à sequência real dos arquivos dentro dos gabinetes. Os números de sequência de arquivos descompactados não precisam ser exclusivos. Por exemplo, se todos os arquivos forem descompactados e residirem em um disco, todos os arquivos poderão ter o mesmo número de sequência na tabela de arquivos.

A tabela de mídia descreve o conjunto de discos que compõem a mídia de origem para a instalação do. A primeira entrada na tabela de mídia sempre deve ter um 1 no campo DiskId. Os arquivos devem ser organizados na mídia de origem de modo que todos os arquivos no disco 1 tenham números de sequência de tabela de arquivos menores do que os números de sequência de arquivos no disco 2, e todos os números de sequência no disco 2 devem ser menores do que no disco 3 e assim por diante. Esse requisito também se aplica a um disco que contém fontes compactadas e descompactadas. Por exemplo, se as fontes de mídia para a instalação estiverem localizadas em dois discos de origem, e se o disco 1 contiver arquivos descompactados e um arquivo de gabinete, ambos os arquivos descompactados e os arquivos no gabinete deverão ter números de sequência menores do que o menor número de sequência de arquivo de qualquer arquivo armazenado no disco 2. Se todos os arquivos no disco 1 forem compactados em um arquivo de gabinete, a tabela de mídia poderá ser criada, conforme mostrado na tabela a seguir.

[Tabela de mídia](media-table.md) (parcial)



| DiskId | LastSequence | DiskPrompt | Gabinete   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          | mycab.cab | Disco 1      |
| 2      | 10           | 2          |           | Disco 2      |



 

Se alguns arquivos no disco 1 forem compactados em um gabinete e alguns estiverem descompactados, a tabela de mídia poderá ser criada da seguinte maneira.

[Tabela de mídia](media-table.md) (parcial)



| DiskId | LastSequence | DiskPrompt | Gabinete   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Disco 1      |
| 2      | 10           | 1          | mycab.cab | Disco 1      |
| 3      | 15           | 2          |           | Disco 2      |



 

Observe que a criação na tabela de mídia a seguir está incorreta porque ela especifica alguns números de sequência de arquivos no disco 2 que são menores do que alguns arquivos dentro do gabinete no disco 1.

[Tabela de mídia](media-table.md)



| DiskId | LastSequence | DiskPrompt | Gabinete   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Disco 1      |
| 2      | 10           | 2          |           | Disco 2      |
| 3      | 15           | 1          | mycab.cab | Disco 1      |



 

Arquivos grandes podem ser divididos entre dois ou mais arquivos de gabinete. Não pode haver mais de 15 arquivos em um arquivo de gabinete que abranja o próximo arquivo de gabinete. Por exemplo, se você tiver três arquivos de gabinete, o primeiro gabinete poderá ter 15 arquivos que se estendem ao segundo arquivo de gabinete, e o segundo gabinete pode ter 15 arquivos que abrangem o terceiro arquivo de gabinete. Quando você adiciona um registro à tabela de arquivos para um arquivo de vários gabinetes, use a primeira parte do arquivo para especificar o número de sequência de arquivo que você inserir na coluna sequência.

As tabelas de arquivo e mídia podem ser criadas da seguinte maneira se houver três arquivos, dois gabinetes e dois discos. Neste exemplo, c1.cab reside em DISK1 e c2.cab reside em disco 2. O arquivo F2 abrange ambos os gabinetes. O c1.cab gabinete contém o arquivo F1 inteiro e a primeira parte do arquivo F2. O c2.cab gabinete contém a segunda parte de F2 e todo o arquivo F3.

[Tabela de mídia](media-table.md) (parcial)



| DiskId | LastSequence | DiskPrompt | Gabinete | VolumeLabel |
|--------|--------------|------------|---------|-------------|
| 1      | 5            | 1          | c1.cab  | Disco 1      |
| 2      | 10           | 2          | c2.cab  | Disco 2      |



 

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo | Sequência |
|------|----------|
| F1   | 1        |
| F2   | 2        |
| tecla   | 6        |



 

 

 



