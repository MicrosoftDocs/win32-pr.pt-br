---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44279c0e-17f4-4109-bc12-af9064cd321e
title: P (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f018a19c1d00ff3c6530e7c45fbca2350df8fec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501731"
---
# <a name="p-volume-shadow-copy-service"></a>P (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**suporte a arquivos parciais**
</dt> <dd>

A capacidade de implementar operações de backup modificando subseções dos arquivos envolvidos, em vez de trabalhar com os arquivos inteiros. Consulte também [*direcionamento direcionado*](vssgloss-d.md).

</dd> <dt>

<span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**cópia de sombra persistente**
</dt> <dd>

Uma cópia de sombra que não é excluída automaticamente quando o solicitante libera um objeto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ou quando o computador é reiniciado. Consulte também [*cópia de sombra de lançamento automático*](vssgloss-a.md), [*cópia de sombra*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plexos**
</dt> <dd>

Um tipo especial de volume de cópia de sombra que representa totalmente e completamente um volume de cópia de sombra sem a necessidade de qualquer volume original. Isso também é conhecido como espelho dividido, mas esta documentação usa o termo Plex.

</dd> <dt>

<span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**Evento de restauração**
</dt> <dd>

Um evento do VSS que indica que uma restauração do VSS foi concluída.

</dd> <dt>

<span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**Evento de pós-instantâneo**
</dt> <dd>

Um evento do VSS que indica que uma cópia de sombra foi concluída. Consulte também [*cópia de sombra*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**Evento PrepareForBackup**
</dt> <dd>

Um evento do VSS que indica que uma operação de backup está prestes a ocorrer.

</dd> <dt>

<span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**Evento PrepareForSnapshot**
</dt> <dd>

Um evento do VSS que indica que os gravadores devem tomar medidas para se preparar para uma operação de cópia de sombra futura. Consulte também [*cópia de sombra*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**Evento de prerestore**
</dt> <dd>

Um evento do VSS que indica que uma operação de restauração está prestes a ocorrer.

</dd> <dt>

<span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**operador**
</dt> <dd>

Um objeto do sistema operacional que intercepta e gerencia solicitações de e/s para criar e representar cópias de sombra de volume para o sistema de arquivos. Consulte também [*provedor de hardware*](vssgloss-h.md), [*provedor de software*](vssgloss-s.md).

</dd> </dl>

 

 



