---
description: Durante uma operação de backup, o solicitante usa IVssBackupComponents::SetBackupState para definir o tipo de operação em andamento.
ms.assetid: 43dcdac7-ed8e-4150-83eb-585e0e92f13c
title: Estado de backup do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35701e1b576d9ea2e5464516589ae419dc73b74898768af06e974da05afffa8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056214"
---
# <a name="vss-backup-state"></a>Estado de backup do VSS

Durante uma operação de backup, o solicitante usa [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) para definir o tipo de operação em andamento.

Essas informações não são incluídas em um formato facilmente recuperável no Documento de Componentes de Backup, portanto, os desenvolvedores solicitantes devem armazenar essas informações independentemente em qualquer mídia de backup.

O estado de backup contém o seguinte:

<dl> <dt>

<span id="Backup_Type"></span><span id="backup_type"></span><span id="BACKUP_TYPE"></span>Tipo de backup
</dt> <dd>

O tipo de backup especifica critérios para identificar arquivos a serem armazenados em backup. A avaliação desses critérios deve ser feita usando a API do VSS.

Ao decidir sobre o tipo de backup a ser buscado e com quais autores trabalhar, os solicitantes devem examinar os tipos (ou esquemas — consulte Suporte a esquemas de [backup](writer-backup-schema-support.md)de writer ) de operações de backup compatíveis com cada um dos autores do sistema. Os backups no VSS podem ser os seguintes tipos:

-   Completo (VSS \_ BT \_ FULL)— os arquivos serão armazenados em backup independentemente da data do último backup. O histórico de backup de cada arquivo será atualizado e esse tipo de backup pode ser usado como base de um backup incremental ou diferencial. A restauração de um backup completo requer apenas uma única imagem de backup.
-   Backup de cópia (VSS BT COPY) – como o tipo de \_ \_ backup \_ VSS BT FULL, os arquivos serão copiados em backup independentemente da data do \_ último backup. No entanto, o histórico de backup de cada arquivo não será atualizado e esse tipo de backup não pode ser usado como base de um backup incremental ou diferencial.
-   Incremental (VSS \_ BT INCREMENTAL)— a API do VSS é usada para garantir que somente os arquivos que foram alterados ou adicionados desde o último backup completo ou incremental sejam copiados para uma mídia de \_ armazenamento. A restauração de um backup incremental requer a imagem de backup original e todas as imagens de backup incrementais feitas desde o backup inicial.
-   Diferencial (VSS \_ BT DIFFERENTIAL)— a API do VSS é usada para garantir que somente os arquivos que foram alterados ou adicionados desde o último backup completo sejam copiados para uma mídia de armazenamento; todas as informações de backup intermediárias são \_ ignoradas. A restauração de um backup diferencial requer a imagem de backup original e a imagem de backup diferencial mais recente feita desde o último backup completo.
-   Arquivo de Log (VSS BT LOG) – somente os arquivos de log de um autor (arquivos adicionados a um componente com o método \_ \_ [**IVssCreateWriterMetadata::AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) e recuperados por uma chamada para [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)) serão backups. Esse tipo de backup é específico do VSS.

É possível que os solicitantes implementem esses backups usando informações e métodos fora do VSS. Somente quando um solicitante implementa um backup usando a API do VSS, deve-se dizer que ele tem um dos tipos de backup listados. Por exemplo, um solicitante participa de um tipo de backup LOG BT do VSS somente se ele usou as informações retornadas por \_ \_ [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) para identificar arquivos de log. Da mesma forma, os tipos INCREMENTAL e DIFERENCIAL BT DO VSS se aplicam somente a operações incrementais ou diferenciais, conforme descrito em Backups incrementais \_ \_ e \_ \_ [diferenciais.](incremental-and-differential-backups.md)

</dd> <dt>

<span id="Specification_about_Selectability"></span><span id="specification_about_selectability"></span><span id="SPECIFICATION_ABOUT_SELECTABILITY"></span>Especificação sobre selecionável
</dt> <dd>

Um backup do VSS pode optar por respeitar as noções vss de selecionabilidade de componente — isso é conhecido como em execução no modo de componente [*—*](vssgloss-c.md)ou ignorá-las.

Um exemplo de não execução no modo de componente seria executar um backup de imagem do sistema, em que o aplicativo de backup precisaria de cooperação do autor para garantir a estabilidade dos dados, mas onde a seleção de componentes seria irrelevante.

</dd> <dt>

<span id="Saving_Bootable_State"></span><span id="saving_bootable_state"></span><span id="SAVING_BOOTABLE_STATE"></span>Salvando o estado inicializável
</dt> <dd>

O VSS dá suporte ao salvar o estado do sistema em execução em uma configuração totalmente inicializável. No entanto, isso nem sempre é necessário e a preparação do autor para salvar um estado inicializável pode, às vezes, prejudicar o desempenho em tempo real de um sistema em execução.

Portanto, os solicitantes indicam se um backup incluirá um estado inicializável do sistema como um argumento [**para IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Os autores determinam se precisam dar suporte ao salvar o estado inicializável do sistema chamando [**CVssWriter::IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup).

Mesmo que o estado do sistema inicializável não seja selecionado, cópias de sombra dos arquivos do sistema serão feitas e os arquivos poderão ser copiados em backup.

No entanto, é necessário ter muito cuidado ao restaurar arquivos do sistema se o backup não salvou o estado inicializável do sistema (consulte Backup e restauração do estado do sistema no [Windows Server 2003 R2 e Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)).

Não é possível recuperar essas informações de um Documento de Componentes de Backup recuperado, portanto, os autores do solicitante devem armazenar se o sistema foi feito backup com um estado do sistema inicializável ou não.

</dd> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Suporte parcial a arquivos
</dt> <dd>

Alguns autores suportam a restauração de arquivos por meio da substituição de partes dos arquivos que eles gerenciam. Um solicitante pode ser projetado para tirar proveito disso e, nesse caso, ele indica isso definindo as informações em [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

 

 



