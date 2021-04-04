---
description: 'Durante uma operação de backup, o solicitante usa IVssBackupComponents:: setbackupstate para definir o tipo de operação em andamento.'
ms.assetid: 43dcdac7-ed8e-4150-83eb-585e0e92f13c
title: Estado de backup do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aa9250139aee9f48f9880fd4a657fa7c6c4991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647166"
---
# <a name="vss-backup-state"></a>Estado de backup do VSS

Durante uma operação de backup, o solicitante usa [**IVssBackupComponents:: Setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) para definir o tipo de operação em andamento.

Essas informações não são incluídas em um formulário facilmente recuperável no documento de componentes de backup, por isso os desenvolvedores de solicitantes devem armazenar essas informações independentemente em qualquer mídia de backup.

O estado de backup contém o seguinte:

<dl> <dt>

<span id="Backup_Type"></span><span id="backup_type"></span><span id="BACKUP_TYPE"></span>Tipo de backup
</dt> <dd>

O tipo de backup especifica critérios para identificar os arquivos cujo backup será feito. A avaliação desses critérios deve ser feita usando a API do VSS.

Ao decidir sobre o tipo de backup a ser buscado e com quais gravadores trabalhar, os solicitantes devem examinar os tipos (ou esquemas — consulte [suporte ao esquema de backup do gravador](writer-backup-schema-support.md)) de operações de backup com suporte de cada um dos gravadores do sistema. Os backups em VSS podem ser os seguintes tipos:

-   Completo (VSS \_ BT \_ completa) — será feito backup dos arquivos, independentemente da data do último backup. O histórico de backup de cada arquivo será atualizado e esse tipo de backup poderá ser usado como a base de um backup incremental ou diferencial. A restauração de um backup completo requer apenas uma única imagem de backup.
-   Copiar backup (cópia do VSS \_ BT \_ ) — como o \_ tipo de backup completo de BT do VSS \_ , será feito backup dos arquivos, independentemente da data do último backup. No entanto, o histórico de backup de cada arquivo não será atualizado e esse tipo de backup não poderá ser usado como a base de um backup incremental ou diferencial.
-   Incremental (VSS \_ BT \_ incremental) – a API do VSS é usada para garantir que apenas os arquivos que foram alterados ou adicionados desde o último backup completo ou incremental sejam copiados para um meio de armazenamento. A restauração de um backup incremental requer a imagem de backup original e todas as imagens de backup incremental feitas desde o backup inicial.
-   Diferencial ( \_ diferencial do VSS BT \_ ) – a API do VSS é usada para garantir que apenas os arquivos que foram alterados ou adicionados desde o último backup completo sejam copiados para uma mídia de armazenamento; todas as informações de backup intermediários são ignoradas. A restauração de um backup diferencial requer a imagem de backup original e a imagem de backup diferencial mais recente feita desde o último backup completo.
-   Arquivo de log ( \_ log de BT VSS \_ ) — somente os arquivos de log de um gravador (arquivos adicionados a um componente com o método [**IVssCreateWriterMetadata:: AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) e recuperados por uma chamada para [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)) serão submetidos a backup. Esse tipo de backup é específico do VSS.

É possível que os solicitantes implementem esses backups usando informações e métodos fora do VSS. Somente quando um solicitante implementa um backup usando a API do VSS, deve-se dizer que ele tem um dos tipos de backup listados. Por exemplo, um solicitante participará de um \_ \_ tipo de log de BT VSS do backup somente se ele usou as informações retornadas por [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) para identificar os arquivos de log. Da mesma forma, \_ os \_ tipos diferenciais VSS BT incremental e VSS \_ BT \_ se aplicam somente a operações incrementais ou diferenciais, conforme descrito em [backups incrementais e diferenciais](incremental-and-differential-backups.md).

</dd> <dt>

<span id="Specification_about_Selectability"></span><span id="specification_about_selectability"></span><span id="SPECIFICATION_ABOUT_SELECTABILITY"></span>Especificação sobre a seleção
</dt> <dd>

Um backup do VSS pode optar por respeitar noções do VSS de seleção de componentes – isso é chamado de execução no [*modo de componente*](vssgloss-c.md)— ou de ignorá-los.

Um exemplo de não execução no modo de componente seria executar um backup de imagem do sistema, em que o aplicativo de backup precisaria de uma cooperação de gravador para garantir a estabilidade dos dados, mas onde a seleção de componentes seria irrelevante.

</dd> <dt>

<span id="Saving_Bootable_State"></span><span id="saving_bootable_state"></span><span id="SAVING_BOOTABLE_STATE"></span>Salvando estado inicializável
</dt> <dd>

O VSS dá suporte à gravação do estado do sistema em execução em uma configuração totalmente inicializável. No entanto, isso nem sempre é necessário, e a preparação do gravador para salvar um estado inicializável pode, às vezes, prejudicar o desempenho em tempo real de um sistema em execução.

Portanto, os solicitantes indicam se um backup incluirá um estado de sistema inicializável como um argumento para [**IVssBackupComponents:: Setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Os gravadores determinam se precisam dar suporte ao salvamento do estado do sistema inicializável chamando [**CVssWriter:: IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup).

Mesmo se o estado do sistema inicializável não estiver selecionado, as cópias de sombra dos arquivos do sistema serão feitas e o backup dos arquivos poderá ser feito.

No entanto, deve-se ter muito cuidado ao restaurar arquivos do sistema se o backup não tiver salvo o estado do sistema inicializável (consulte [fazendo backup e restaurando o estado do sistema no Windows server 2003 R2 e no Windows server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)).

Não é possível recuperar essas informações de um documento de componentes de backup recuperado, portanto, os autores do solicitante devem armazenar se o backup do sistema foi feito com um estado de sistema inicializável ou não.

</dd> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Suporte a arquivos parciais
</dt> <dd>

Alguns gravadores dão suporte à restauração de arquivos por meio da substituição de partes dos arquivos que eles gerenciam. Um solicitante pode ser projetado para tirar proveito disso e, se for, ele indicará isso definindo as informações em [**IVssBackupComponents:: Setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

 

 



