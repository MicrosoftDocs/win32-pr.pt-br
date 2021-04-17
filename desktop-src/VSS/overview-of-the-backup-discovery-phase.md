---
description: 'Depois de chamar IVssBackupComponents:: GatherWriterMetadata, um solicitante usa a instância da interface IVssAsync retornada dessa chamada para determinar quando todos os gravadores no sistema acabaram de construir seus documentos de metadados do gravador.'
ms.assetid: 04658d50-04f0-4189-8b88-ff152f1bf482
title: Visão geral da fase de descoberta de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d2a2d05220ecf3e25c77c18cc62b07726964f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759773"
---
# <a name="overview-of-the-backup-discovery-phase"></a>Visão geral da fase de descoberta de backup

Depois de chamar [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), um solicitante usa a instância da interface [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) retornada dessa chamada para determinar quando todos os gravadores no sistema acabaram de construir seus documentos de metadados do gravador. Para obter mais informações, consulte [visão geral do processamento de um backup em VSS](overview-of-processing-a-backup-under-vss.md).

Neste ponto, o solicitante pode iniciar uma fase de descoberta, examinando os metadados para determinar quais aplicativos estão em execução e quais volumes devem ser copiados em sombra para obter um backup completo. A tabela a seguir mostra a sequência de ações e eventos que são necessários para a fase de descoberta de backup.



| Ação do solicitante                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Evento | Ação do gravador                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|-----------------------------------------------------------------------------------|
| Recuperar documentos de metadados do gravador (consulte [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata), [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)).                                                                                                                                                                                                                                                                                                                                                 | Nenhum  | Durante esse período, os gravadores podem continuar com suas operações normais. |
| Use a lista de componentes e seus [*conjuntos de arquivos*](vssgloss-f.md), bem como arquivos excluídos, para obter uma lista de volumes e arquivos envolvidos no backup (consulte [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent), [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)).                                                                                                                                                                                                                                                                      | Nenhum  | Nenhum                                                                              |
| Escolha os componentes no documento de metadados do gravador do gravador para fazer backup. Chame o [**componente IVssBackupComponents::**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) Addpara cada componente para adicioná-lo ao documento de componentes de backup. (Consulte [trabalhando com a seleção para fazer backup](working-with-selectability-for-backup.md) e [trabalhar com o documento de componentes de backup](working-with-the-backup-components-document.md).)                                                                                                                      | Nenhum  | Nenhum                                                                              |
| Inicialize o conjunto de cópias de sombra, o contexto e a verificação de volumes com suporte (consulte [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset), [**IVssBackupComponents:: IsVolumeSupported**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported)).                                                                                                                                                                                                                                                                                   | Nenhum  | Nenhum                                                                              |
| Se estiver executando um backup que não seja de componente, adicione os volumes de destino desejados do documento de metadados do gravador ao conjunto de cópias de sombra chamando [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) para cada volume. Caso contrário, para os componentes no documento de metadados do gravador que já foram adicionados ao documento de componentes de backup (chamando [**addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)), o solicitante também deve chamar **IVssBackupComponents:: AddToSnapshotSet** para cada volume afetado. | Nenhum  | Nenhum                                                                              |



 

## <a name="writer-actions-during-the-discovery-phase"></a>Ações do gravador durante a fase de descoberta

Como a fase de descoberta de um backup consiste principalmente em um solicitante processando as informações que ele recuperou dos documentos de metadados do gravador, há alguns requisitos em um gravador.

Teoricamente, um escritor pode continuar a ser executado normalmente neste ponto. No entanto, pode ser desejável que os autores comecem a preparações para as operações de cópia de sombra e backup.

## <a name="requester-actions-during-the-discovery-phase"></a>Ações do solicitante durante a fase de descoberta

Um solicitante usa os objetos [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) obtidos por meio de [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para iterar em todos os metadados dos gravadores e selecionar os gravadores cujos dados pretendem fazer backup.

Neste ponto, o solicitante precisará gerar uma lista inicial de candidatos de backup de cada gravador Iterando os componentes do gravador usando [**IVssExamineWriterMetadata:: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Isso fornece o solicitante com objetos [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) , do qual você pode obter as especificações para os arquivos cujo backup será feito usando [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent:: getdatabasefile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)e [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile).

Como o objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) pode usar caracteres curinga para armazenar informações de local de arquivo, pode ser necessário usar funções como [**findfirstfilefile**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/win32/api/fileapi/nf-fileapi-findfirstfileexa)e [**FindNextFile**](/windows/win32/api/fileapi/nf-fileapi-findnextfilea).

Até que a cópia de sombra tenha sido concluída, ainda é possível que os gravadores adicionem ou removam arquivos do disco no curso normal de seu trabalho, de modo que você não deve gerar a lista real de arquivos cujo backup será feito neste momento.

Em vez disso, a lista inicial de arquivos e volumes dos quais será feito backup é encontrada neste ponto, fazendo o seguinte:

1.  Examinando tudo selecionável para backup e componentes não selecionáveis no documento de metadados do gravador de cada gravador (usando [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)) e organizá-los em [*conjuntos de componentes*](vssgloss-c.md) usar [*caminho lógico*](vssgloss-l.md) (consulte [trabalhando com a seleção e caminhos lógicos](working-with-selectability-and-logical-paths.md))
2.  [*Incluindo explicitamente*](vssgloss-e.md) todos os componentes necessários (não selecionáveis para componentes de backup sem selecionáveis para os ancestrais de backup) no documento de componentes de backup usando [ **IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)
3.  Optando por incluir explicitamente opcional selecionável para componentes de backup que não definem um conjunto de componentes (usando [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent))
4.  Seleção [*de conjuntos de componentes*](vssgloss-c.md) para participação em um backup adicionando explicitamente seus definindo selecionáveis para o componente de backup (usando [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)), que [*implicitamente inclui*](vssgloss-i.md) os [*Subcomponentes*](vssgloss-s.md)do conjunto de componentes.
5.  Usando as informações do [*conjunto de arquivos*](vssgloss-f.md) no documento de metadados do gravador selecionado e nas funções de gerenciamento de volume, um solicitante determina os caminhos dos arquivos dos quais será feito backup e os volumes que precisarão ser copiados em sombra

Observe que apenas os componentes explicitamente incluídos (usando [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)) no backup e no documento de componentes de backup terão instâncias da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) adicionadas a esse documento. Essas instâncias serão usadas para examinar e modificar as configurações de componente para os componentes explicitamente incluídos e qualquer um de seus subcomponentes incluídos implicitamente (consulte [a seleção e trabalhando com propriedades de componente](selectability-and-working-with-component-properties.md)).

Se um gravador incluir um dos componentes do gravador, ele deverá adicionar todos os seus componentes necessários. No entanto, um solicitante também é gratuito para ignorar completamente todos os conjuntos de componentes de um gravador. Se nenhum dos componentes do gravador estiver explicitamente selecionado, o gravador não será selecionado e o VSS inibirá o gravador de participar do restante da operação de backup.

O solicitante inicia o conjunto de cópias de sombra que conterá os volumes selecionados chamando [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset).

Se o volume puder participar de uma cópia de sombra (que pode ser verificada com [**IVssBackupComponents:: IsVolumeSupported**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported)), o solicitante poderá adicionar esse volume ao conjunto de cópias de sombra usando [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Embora não seja geralmente útil, um solicitante às vezes também pode escolher qual [*provedor*](vssgloss-p.md) manterá a cópia de sombra para um determinado volume (consulte [selecionando provedores](selecting-providers.md) para obter detalhes).

Deve-se ter cuidado ao lidar com um volume que contenha pastas montadas ou pontos de nova análise. Uma pasta montada ou um ponto de nova análise pode aparecer em uma cópia de sombra e pode ser feito backup. No entanto, uma pasta montada ou um ponto de nova análise não pode ser atravessado no volume de sombra copiado (consulte [trabalhando com pastas montadas e pontos de nova análise](working-with-reparse-and-mount-points.md)).

Neste ponto do backup, o documento de componentes de backup é inicializado e preenchido. Em operações futuras, os escritores e solicitantes podem usar a interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) para se comunicar entre si.

Os gravadores recebem acesso à interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ao manipular os eventos [*PrepareForBackup*](vssgloss-p.md), [*pós-instantâneo*](vssgloss-p.md)e [*BackupComplete*](vssgloss-b.md) .

 

 
