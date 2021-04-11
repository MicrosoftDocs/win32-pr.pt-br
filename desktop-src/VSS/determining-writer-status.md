---
description: Um solicitante precisa ter um entendimento bem definido sobre o status do gravador que participa dele durante a criação da cópia de sombra e durante as operações de backup e restauração.
ms.assetid: 676d5cff-bd28-43f0-a402-d184c96f0061
title: Determinando o status do gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719322a18808748e92d412c48c7b7628fdac9d51
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172603"
---
# <a name="determining-writer-status"></a>Determinando o status do gravador

Um solicitante precisa ter um entendimento bem definido sobre o status do gravador que participa dele durante a criação da cópia de sombra e durante as operações de backup e restauração. Para fazer isso, é recomendável:

-   Os solicitantes usam [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents:: GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount)e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).
-   Conforme descrito em [visão geral do processamento de um backup no VSS](overview-of-processing-a-backup-under-vss.md) e [visão geral do processamento de uma restauração no VSS](overview-of-processing-a-restore-under-vss.md), esses métodos são mais úteis quando chamados em uma sequência de backup ou restauração bem definida. Normalmente, isso significa que os gravadores devem ser consultados depois que um solicitante tiver concluído uma de suas tarefas e gerado um evento do VSS.

    Ao processar um backup, um solicitante deve consultar um gravador após a conclusão dos métodos a seguir. Os solicitantes devem chamar [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) depois de chamar [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) para fazer com que a sessão de gravador seja definida como um estado concluído.

    > [!Note]  
    > Isso só é necessário no Windows Server 2008 com Service Pack 2 (SP2) e versões anteriores.

     

    <dl> <dt>

[**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)
</dt> <dt>

[**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
</dt> <dt>

[**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
</dt> </dl>

Durante as operações de restauração, um solicitante deve consultar um gravador após a conclusão desses métodos:
<dl> <dt>

[**IVssBackupComponents: rerestaurar:P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
</dt> <dt>

[**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
</dt> </dl>

-   Chamadas para [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) que não fazem parte de uma sequência de backup ou restauração bem definida não fornecem uma imagem confiável do status do gravador, pois elas podem refletir condições que não indicam falha na operação atual, como:
    -   Uma falha de uma criação de cópia de sombra anterior
    -   Um erro em uma operação de backup ou restauração inicial
    -   Um gravador sem resposta que está processando um evento

Portanto, os desenvolvedores não devem contar com o status do gravador retornado por outros processos em seguida, o solicitante ou a tentativa de monitorar o progresso de uma instância da interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) com outra (possivelmente em um thread separado).

Observe que para operações de backup, em que é necessário examinar documentos de metadados do gravador de gravadores, não há necessidade de uma chamada de solicitante para [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) após a geração e manipulação do evento de [*identificação*](vssgloss-i.md) causado por [**IVssBackupComponents:: GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

[**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) relata apenas o status dos gravadores cujos metadados foram fornecidos ao VSS pelos gravadores ' [*identificar*](vssgloss-i.md) manipuladores de eventos, [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (e retornados ao solicitante por [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).

Se a implementação de um gravador de [**CVssWriter:: Onidentification**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) falhar, os metadados do gravador não serão parte da lista de documentos de metadados do gravador fornecidos ao VSS, nenhuma informação de status estará disponível e a chamada será redundante.

Para operações de restauração, em que o solicitante não precisa examinar os documentos de metadados do gravador dos gravadores em execução, chamar [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) pode ser uma maneira mais eficiente de determinar quais gravadores estão em execução.

 

 



