---
description: Em geral, a forma como uma cópia de sombra é criada depende do tipo de cópia de sombra a ser criado, seu contexto e da função com o acordeão dos gravadores na operação de cópia de sombra.
ms.assetid: eab3b39b-dfa7-43ea-adba-cd0b495c373f
title: Detalhes da criação da cópia de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d8f506ef8d5c7acff86cb6a2fa890b3773423fddf339ea4911a0299963224
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998126"
---
# <a name="shadow-copy-creation-details"></a>Detalhes da criação da cópia de sombra

Em geral, a forma como uma cópia de sombra é criada depende do tipo de cópia de sombra a ser criado, seu contexto e da função com o acordeão dos gravadores na operação de cópia de sombra. (Consulte [configurações de contexto de cópia de sombra](shadow-copy-context-configurations.md) para obter mais informações.)

O contexto de cópia de sombra é definido chamando o método [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) . Antes de chamar o método [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) para criar uma cópia de sombra, os solicitantes devem chamar os métodos [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) na ordem especificada nas seções a seguir.

## <a name="prerequisites-for-all-shadow-copies"></a>Pré-requisitos para todas as cópias de sombra

Independentemente do nível de participação no gravador, a criação de qualquer cópia de sombra sempre exigirá que o solicitante seja inicializado com chamadas para [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) e [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset).

Se essa chamada não for feita, o método [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) retornará um erro.

## <a name="shadow-copies-with-writer-participation"></a>Cópias de sombra com participação no gravador

Se o contexto de cópia de sombra especificar a participação do gravador (ou seja, [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) é chamado com o **\_ \_ backup do VSS CTX** ou **\_ \_ \_ reversão do aplicativo CTX VSS**):

-   Os solicitantes devem sempre chamar [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) quando o contexto da cópia de sombra dá suporte à participação no gravador. Se o contexto de cópia de sombra oferecer suporte à participação de gravador e **IVssBackupComponents:: GatherWriterMetadata** não for chamado antes do [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), um erro será retornado.
-   Se um solicitante quiser selecionar componentes específicos do gravador, ele deverá chamar [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) antes de chamar [**StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) para criar o conjunto de cópias de sombra.
-   [**StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) deve ser chamado para criar o conjunto de cópias de sombra.
-   Os solicitantes podem adicionar um ou mais volumes ao conjunto de cópias de sombra chamando [**AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset). Alguns componentes do gravador podem não especificar nenhum volume afetado. Nesse caso, é aceitável que um conjunto de instantâneos esteja vazio (ou seja, não contenha nenhum volume).
-   Para garantir a consistência dos metadados do gravador, um solicitante sempre deve chamar [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) mesmo que nenhum componente esteja selecionado. Isso faz com que o VSS gere um evento **PrepareForBackup** , no qual o VSS chama o método [**CVssWriter:: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) para cada gravador participante.
-   O VSS irá gerar eventos [*PrepareForSnapshot*](vssgloss-p.md) e [*Freeze*](vssgloss-f.md) antes de criar a cópia de sombra em resposta a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Os gravadores tratarão os eventos com [**CVssWriter:: OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot) e [**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze).
-   O VSS gerará eventos [*descongelar*](vssgloss-t.md) e eventos de [*instantâneo*](vssgloss-p.md) após a criação de uma cópia de sombra em resposta a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Os gravadores tratarão os eventos com [**CVssWriter:: descongelar**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) e [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot).

## <a name="shadow-copies-without-writer-participation"></a>Cópias de sombra sem participação no gravador

A criação de cópias de sombra sem a participação do gravador é desencorajada para aplicativos de backup padrão (consulte [backups sem participação no gravador](backups-without-writer-participation.md)).

Há usos, como backups rápidos de um disco para fornecer uma rede de segurança contra corrupção acidental de arquivos, que pode ser realizado sem a participação explícita do gravador. Essa cópia de sombra teria um contexto de backup de **\_ compartilhamento de \_ arquivos \_ \_ VSS CTX** ou **de \_ \_ \_ reversão de nas CTX do VSS**.

Para esse tipo de cópia de sombra, observe o seguinte:

-   Os solicitantes ainda devem chamar os métodos necessários listados em [pré-requisitos para todas as cópias de sombra](#prerequisites-for-all-shadow-copies).
-   Os solicitantes podem chamar [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), mas isso não é necessário.
-   Se os solicitantes chamarem [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent), [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)ou [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete), um erro será retornado.
-   Os provedores não gerarão eventos [*PrepareForSnapshot*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*descongelar*](vssgloss-t.md)ou [*upsnapshot*](vssgloss-p.md) para esse tipo de cópia de sombra.

 

 



