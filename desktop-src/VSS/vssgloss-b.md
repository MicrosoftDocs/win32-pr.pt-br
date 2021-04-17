---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: B (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20cabdfa5260f65d1176f6f1d12ac1d805b9dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296363"
---
# <a name="b-volume-shadow-copy-service"></a>B (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**aplicativos de nível de back-end**
</dt> <dd>

Indica o ponto em que um gravador é notificado de um congelamento pelo VSS. Gravadores que são inicializados como aplicativos de nível back-end são notificados depois que os gravadores são inicializados como aplicativos de nível front-end e antes daqueles inicializados como aplicativos de nível de sistema. Consulte também [*nível de aplicativo*](vssgloss-a.md), [*aplicativos de nível front-end*](vssgloss-f.md), [*aplicativos de nível de sistema*](vssgloss-s.md), [*gravador*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**Evento BackupComplete**
</dt> <dd>

Um evento do VSS que indica que um backup do VSS foi concluído. Esse evento deve ser seguido por um evento BackupShutdown em operação normal. Consulte também *evento BackupShutdown*.

</dd> <dt>

<span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Documento de componentes de backup**
</dt> <dd>

Um documento XML criado por um solicitante (usando a interface **IVssBackupComponents** ) no decorrer da configuração de uma operação de restauração ou backup. O Documento de Componentes de Backup contém uma lista dos componentes explicitamente incluídos, de um ou mais gravadores, que participam de uma operação de backup ou restauração. Ele não contém informações de componentes implicitamente incluídos. Por outro lado, um Documento de Metadados do Gravador contém somente os componentes do gravador que podem participar de um backup.

Um documento de componentes de backup pode ser salvo em disco. Consulte também [*inclusão de componente explícita*](vssgloss-e.md), [*inclusão de componente implícita*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**conjunto de backup**
</dt> <dd>

Os arquivos cujo backup será feito. Ele inclui os arquivos selecionados pela inclusão em um componente, aqueles indicados por instruções include no nível do gravador, menos os arquivos que foram explicitamente incluídos.

</dd> <dt>

<span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**Evento BackupShutdown**
</dt> <dd>

Um evento do VSS que indica que um aplicativo de backup em conformidade foi desligado. Normalmente, isso é precedido por um evento BackupComplete. No entanto, se um backup for encerrado inesperadamente, esse evento poderá ser gerado sem um evento BackupComplete anterior. Consulte também *evento BackupComplete*.

</dd> <dt>

<span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**carimbo de backup**
</dt> <dd>

Uma cadeia de caracteres que contém informações sobre quando um backup ocorreu. O VSS não coloca nenhuma restrição no formato dessa cadeia de caracteres, exceto que ele é inteligível para todas as instâncias de gravador de uma determinada classe. Ele pode conter informações de data e hora, números de sequência lógica ou qualquer outra informação que permitirá que um escritor da mesma classe determine quando o último backup ocorre.

</dd> </dl>

 

 



