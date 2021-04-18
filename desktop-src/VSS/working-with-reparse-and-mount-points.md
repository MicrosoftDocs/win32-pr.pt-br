---
description: O processamento de um dos conjuntos de arquivos de um componente pode exigir que um solicitante Percorra uma árvore de diretório recursivamente, o que pode exigir que o solicitante manipule pastas montadas e pontos de nova análise (como links) que apontam para dados que não estão no volume atual.
ms.assetid: d0e08598-a8a2-489b-9cb2-e989bed1ce53
title: Trabalhando com pastas montadas e pontos de nova análise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a7aa88f39361f788f9aac882b4f9d337fd6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781484"
---
# <a name="working-with-mounted-folders-and-reparse-points"></a>Trabalhando com pastas montadas e pontos de nova análise

O processamento de um dos conjuntos de arquivos de um componente pode exigir que um solicitante Percorra uma árvore de diretório recursivamente, o que pode exigir que o solicitante manipule pastas montadas e pontos de nova análise (como links) que apontam para dados que não estão no volume atual.

Os solicitantes devem seguir as pastas montadas e os pontos de nova análise ao atravessar uma árvore de diretórios, e o VSS tem diretrizes bem definidas para tratá-las para operações de backup e restauração.

Para ilustrar essas diretrizes, considere o seguinte exemplo:

-   O volume \\ \\ ? \\ O volume {GUID \_ 1} tem a letra da unidade C: \\ .
-   Um conjunto de arquivos tem um caminho de C: \\ WriterData.
-   Um arquivo Specification \* . dat é usado pelo conjunto de arquivos.
-   A recursão do conjunto de arquivos é definida como **true**.
-   O diretório C: \\ WriterData está localizado no volume \\ \\ ? \\ Volume {GUID \_ 1}.
-   O diretório C: \\ WriterData \\ arquivo morto é uma pasta montada.
-   O volume \\ \\ ? \\ O volume {GUID \_ 2} está associado ao arquivo C: WriterData da pasta montada \\ \\ .

## <a name="handling-mounted-folders-and-reparse-points-during-backup"></a>Manipulando pastas montadas e pontos de nova análise durante o backup

As regras básicas para lidar com pastas montadas e pontos de nova análise no VSS ao executar um backup recursivo podem ser resumidas da seguinte maneira:

-   Os caminhos são seguidos entre pastas montadas e pontos de nova análise.
-   Se um ponto de reanálise ou pasta montada apontar para um volume, esse volume deverá ser copiado em sombra.
-   Se um volume contiver pastas montadas ou pontos de nova análise, eles serão exibidos na cópia de sombra do volume.
-   Os dados que estão sob a pasta montada ou o ponto de nova análise são capturados na cópia de sombra do volume para o qual a pasta montada ou o ponto de nova análise aponta.

Para ilustrar o uso do exemplo acima, como o sinalizador recursivo está definido, o solicitante deve examinar todos os dados em C: \\ WriterData \\ arquivo morto e abaixo.

O solicitante deve adicionar o volume com a letra da unidade C: \\ ( \\ \\ ? \\ Volume {GUID \_ 1}) e o volume associado à pasta montada C: \\ WriterData \\ ( \\ \\ ? \\ Volume {GUID \_ 2}) para o conjunto de cópias de sombra usando [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

A pasta montada C: \\ WriterData \\ arquivo morto aparece na cópia de sombra do volume \\ \\ ? \\ Volume {GUID \_ 1}, que tem um objeto de dispositivo chamado deviceObject1.

No entanto, o VSS não copiará nenhum dado nessa pasta montada (dados em \\ \\ ? \\ Volume {GUID \_ 2}) para a cópia de sombra referenciada por deviceObject1. Em vez disso, esses dados são capturados na cópia de sombra de \\ \\ ? \\ Volume {GUID \_ 2}, que tem um objeto de dispositivo chamado deviceObject2.

Portanto, um solicitante que está fazendo backup dos arquivos de sombra copiados em C: \\ WriterData usará um caminho de deviceObject1 \\ WriterData para pesquisar arquivos que correspondem a C: \\ WriterData \\ \* . dat.

Para fazer backup de arquivos de sombra copiados no arquivo C: \\ WriterData \\ , o solicitante usará um caminho de deviceObject2 (porque o diretório raiz de \\ \\ ? \\ O volume {GUID \_ 2} foi associado à pasta montada c: \\ Writer \\ Archive) para pesquisar arquivos que correspondem a c: \\ WriterData \\ Archive \\ \* . dat.

Observe que um ponto de nova análise é tratado da mesma maneira que uma pasta montada. O ponto de nova análise aparece na cópia de sombra do primeiro volume. Os dados sob o ponto de nova análise aparecem na cópia de sombra do segundo volume.

Durante o backup, os solicitantes devem armazenar informações sobre pastas montadas e os volumes associados a eles, bem como pontos de nova análise e seus destinos para garantir que todos os dados sejam armazenados em backup e restaurados corretamente.

## <a name="handling-mount-and-reparse-points-during-restore"></a>Manipulando pontos de montagem e de nova análise durante a restauração

Ao restaurar arquivos, o solicitante deve seguir as diretrizes um pouco diferentes daqueles que foram usados durante o backup (ignorando problemas, como o [*mapeamento de local alternativo*](vssgloss-a.md) e o [*novo local de destino*](vssgloss-n.md)):

-   Como antes, se a recursão for necessária, os caminhos serão seguidos entre as pastas montadas e os pontos de nova análise.
-   As pastas montadas devem ser restauradas.
-   Os locais de restauração de pastas montadas e pontos de nova análise são aqueles determinados pelos seus caminhos originais.

Se os nomes de volume persistirem entre backup e restauração, ou seja, você não recriar os volumes, as pastas montadas restauradas e os pontos de nova análise devem apontar para os volumes corretos.

Portanto, no exemplo discutido acima, se a pasta montada C: \\ WriterData \\ arquivo morto foi restaurada para ( \\ \\ ? \\ Volume {GUID \_ 1}) e o volume associado anteriormente a ele foi restaurado para ( \\ \\ ? \\ Volume {GUID \_ 2}), os arquivos restaurados e a estrutura de arquivos seriam corretos e consistentes.

Pode acontecer que os dados sejam restaurados para um sistema no qual os nomes de volume foram alterados. Isso pode ser devido a falhas de disco, em que talvez seja necessário executar uma recuperação manual do sistema e recriar volumes. Nesse tipo de situação, as pastas montadas e os pontos de nova análise não serão mais válidos após a restauração. Para recriar os arquivos e a estrutura de arquivos no volume restaurado, será necessário excluir as pastas montadas e os pontos de nova análise restaurados e recriá-los no disco. Cabe ao aplicativo de backup decidir se isso é apropriado.

Observe que é possível que o destino de restauração de uma pasta montada já esteja ocupado. Por exemplo, C: \\ WriterData \\ arquivo morto pode já conter alguns arquivos. Cabe ao aplicativo de backup decidir como lidar com essa situação.

 

 



