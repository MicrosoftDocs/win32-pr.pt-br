---
description: Um conjunto de backup é uma lista de todos os arquivos cujo backup será feito, suas localizações e como fazer backup deles.
ms.assetid: 34a66a9c-c1bc-437d-b034-59dc0c88228c
title: Gerando um conjunto de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827d9ecb90ac376aa9818b61e8dab65550ff8c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810613"
---
# <a name="generating-a-backup-set"></a>Gerando um conjunto de backup

Um conjunto de backup é uma lista de todos os arquivos cujo backup será feito, suas localizações e como fazer backup deles.

Um solicitante deve fazer uso dos arquivos contidos nos volumes copiados por sombra após o [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) retorna com êxito para gerar a lista completa de arquivos cujo backup será feito.

Além disso, um solicitante deve lidar com a possibilidade de que alguns arquivos tenham [*caminhos alternativos*](vssgloss-a.md) e que alguns arquivos tenham sido excluídos.

Um algoritmo para selecionar arquivos para fazer backup deve ir em uma [*instância de gravador*](vssgloss-w.md) por instância de gravador, base componente a componente (como será o caso durante a restauração; consulte [gerando um conjunto de restauração](generating-a-restore-set.md)) e pode continuar fazendo o seguinte:

1.  Determinando os volumes que contêm os arquivos do gravador e os objetos de dispositivo correspondentes
2.  Usando as informações de [*conjunto de arquivos*](vssgloss-f.md) (contidas em objetos [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) retornados por [**IVssExamineWriterMetadata::**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)getdelete) para criar uma lista dos arquivos explicitamente excluídos, se necessário, usando **FindFileFirst**, **FindFileFirstEx** e **FindNextFile**.
3.  Iterando em todos os componentes de um gravador, usando [**IVssExamineWriterMetadata:: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Se um componente selecionável for selecionado, use o [*caminho lógico*](vssgloss-l.md) para obter esses componentes não selecionáveis associados a ele em um conjunto de componentes. (Consulte [trabalhando com a seleção e os caminhos lógicos](working-with-selectability-and-logical-paths.md).)
4.  Obter os [*conjuntos de arquivos*](vssgloss-f.md) contidos em cada componente selecionado usando a interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) correspondente a cada componente que ele contém.
5.  Gerando uma lista de arquivos a partir das especificações — se necessário, usando **FindFileFirst**, **FindFileFirstEx** e **FindNextFile**.
6.  Verificando cada arquivo na lista gerada a partir de informações de componente em relação à lista de arquivos excluídos gerados acima. Isso deve ser feito usando o caminho padrão para o arquivo (retornado por [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), não pelo caminho alternativo retornado por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)). Se o arquivo corresponder à lista excluída, não será feito backup dele.
7.  Escolhendo o local real do qual fazer backup (usando o caminho alternativo se ele foi definido)
8.  Neste ponto, uma lista completa de arquivos e seus locais estão disponíveis e um backup pode começar.

Depois que um conjunto de backup inicial tiver sido gerado para todos os gravadores presentes no sistema, o solicitante verificará a seguinte chave do registro:

**HKEY \_ local \_ Machine \\ sistema \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToBackup**

O solicitante usa as subchaves sob esta tecla da seguinte maneira:

-   Se um gravador estiver presente no sistema e houver uma subchave cujo nome corresponda ao nome do gravador, essa subchave deverá ser ignorada.
-   Se um gravador estava presente no sistema, mas estiver ausente atualmente no conjunto de backup e houver uma subchave correspondente, todos os arquivos especificados nos dados da subchave serão excluídos e deverão ser removidos do conjunto de backup.
-   O aplicativo de backup adiciona arquivos aos dados da subchave criando um \_ valor de vários sz contendo uma lista de especificações de arquivo para os arquivos cujo backup não deve ser feito. Cada cadeia de caracteres no \_ valor de vários sz deve conter uma especificação de arquivo.
-   As especificações de arquivo podem conter o? e \* caracteres curinga. Uma especificação pode ser tornada recursiva acrescentando/s ao final. Por exemplo, especificar "% TEMP% \\ \* /s" faz com que todos os arquivos no diretório% temp% e todos os seus subdiretórios não sejam submetidos a backup.

 

 



