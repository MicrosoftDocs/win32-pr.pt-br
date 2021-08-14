---
description: Um conjunto de backup é uma lista de todos os arquivos a serem armazenados em backup, seus locais e como fazer backup deles.
ms.assetid: 34a66a9c-c1bc-437d-b034-59dc0c88228c
title: Gerando um conjunto de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120643c827afdabfbb9a2c347fa16290e03969f0e87f913b0c5d9fdb682f2619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122102"
---
# <a name="generating-a-backup-set"></a>Gerando um conjunto de backup

Um conjunto de backup é uma lista de todos os arquivos a serem armazenados em backup, seus locais e como fazer backup deles.

Um solicitante deve usar os arquivos contidos nos volumes copiados em sombra depois que [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) retornar com êxito para gerar a lista completa de arquivos a serem copiados em backup.

Além disso, um solicitante deve lidar com a possibilidade de que alguns arquivos [*tenham*](vssgloss-a.md) caminhos alternativos e que alguns arquivos tenham sido excluídos.

Um algoritmo para selecionar arquivos para [](vssgloss-w.md) fazer backup deve ir em uma instância de writer por instância de writer, componente por componente (como será o caso durante a restauração; consulte [Gerando](generating-a-restore-set.md)um conjunto de restauração ) e pode continuar fazendo o seguinte:

1.  Determinando os volumes que contêm os arquivos do autor e os objetos de dispositivo correspondentes
2.  Usando [](vssgloss-f.md) as informações do conjunto de arquivos (contidas em [**objetos IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) retornados por [**IVssExamineWriterMetadata::GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)) para criar uma lista dos arquivos explicitamente excluídos, se necessário usando **FindFileFirst,** **FindFileFirstEx** e **FindNextFile**.
3.  Iterando em todos os componentes de um autor, usando [**IVssExamineWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Se um componente selecionável for selecionado, [*use*](vssgloss-l.md) o caminho lógico para obter esses componentes não selecionáveis associados a ele em um conjunto de componentes. (Consulte [Trabalhando com selecionabilidade e caminhos lógicos](working-with-selectability-and-logical-paths.md).)
4.  Obter os conjuntos [*de arquivos*](vssgloss-f.md) contidos em cada componente selecionado usando a interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) correspondente a cada componente que ele contém.
5.  Gerando uma lista de arquivos das especificações – se necessário usando **FindFileFirst,** **FindFileFirstEx** e **FindNextFile**.
6.  Verificando cada arquivo na lista gerada a partir de informações de componente em relação à lista de arquivos excluídos gerados acima. Isso deve ser feito usando o caminho padrão para o arquivo (retornado por [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), não pelo caminho alternativo retornado por [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)). Se o arquivo corresponde à lista excluída, ele não será feito backup.
7.  Escolhendo o local real do qual fazer o back-up (usando o caminho alternativo se ele tiver sido definido)
8.  Neste ponto, uma lista completa de arquivos e seus locais está disponível e um backup pode começar.

Depois que um conjunto de backup inicial tiver sido gerado para todos os autores presentes no sistema, o solicitante verificará a seguinte chave do Registro:

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToBackup**

O solicitante usa as sub-chaves nesta chave da seguinte forma:

-   Se um autor estiver presente no sistema e houver uma sub-chave cujo nome corresponde ao nome do autor, essa sub-chave deverá ser ignorada.
-   Se um autor estava presente no sistema, mas está ausente no momento do conjunto de backup e há uma sub-chave correspondente, todos os arquivos especificados nos dados da sub-chave são excluídos e devem ser removidos do conjunto de backup.
-   O aplicativo de backup adiciona arquivos aos dados de sub-chave criando um valor MULTI SZ que contém uma lista de especificações de arquivo para os arquivos que não devem \_ ser armazenados em backup. Cada cadeia de caracteres no valor de MULTI \_ SZ deve conter uma especificação de arquivo.
-   As especificações de arquivo podem conter o ? e \* caracteres curinga. Uma especificação pode ser recursiva ao fazer a adoção de /s até o final. Por exemplo, especificar "%TEMP% /s" faz com que todos os arquivos no diretório %TEMP% e todos os seus subdireários não sejam \\ \* armazenados em backup.

 

 



