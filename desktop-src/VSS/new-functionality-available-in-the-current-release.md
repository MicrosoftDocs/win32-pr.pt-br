---
description: 'A versão 2003 do Windows Server do Serviço de Cópias de Sombra de Volume contém a seguinte nova funcionalidade:'
ms.assetid: 3dcfcc01-3e3c-43e9-a933-5c72f331da9a
title: Nova funcionalidade disponível no Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5782ef6b24f208f69e50cdb992e12ba3212c47f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091434"
---
# <a name="new-functionality-available-in-windows-server-2003"></a>Nova funcionalidade disponível no Windows Server 2003

A versão 2003 do Windows Server do Serviço de Cópias de Sombra de Volume contém a seguinte nova funcionalidade:

-   Suporte para a [*seleção de restauração*](vssgloss-s.md) , além de e em uma base igual à [*seleção de backup*](vssgloss-s.md) (anteriormente conhecida como seleção). Consulte [trabalhando com a seleção e caminhos lógicos](working-with-selectability-and-logical-paths.md) para obter mais informações.
-   Introdução de um evento [*BackupShutdown*](vssgloss-b.md) que indica que um aplicativo de backup compatível com VSS (solicitante) foi desligado, se a tentativa de backup foi concluída corretamente ou não. Consulte [manipulando eventos BackupShutdown](handling-backupshutdown-events.md) para obter mais informações.
-   Suporte para dependências explícitas de componente de gravador. Um meio para descrever e dar suporte às situações em que um componente (e o conjunto de componentes definido por ele) gerenciado por um gravador não pode ser copiado ou restaurado independentemente dos componentes gerenciados por outros gravadores. Consulte [dependências entre os componentes gerenciados por diferentes gravadores](dependencies-between-components-managed-by-different-writers.md) para obter mais informações.
-   Suporte completo para operações de [*arquivos parciais*](vssgloss-p.md) . O backup e a restauração de segmentos de arquivos por gravadores e solicitantes agora têm suporte total. Consulte [trabalhando com arquivos parciais](working-with-partial-files.md) para obter mais informações sobre operações de arquivo parcial.
-   Introdução de [*arquivos diferenciados*](vssgloss-d.md) para dar suporte a operações incrementais de backup e restauração. Consulte [backups incrementais e diferenciais](incremental-and-differential-backups.md) para obter mais informações.
-   Introdução de esquemas de backup como um conceito que indica o nível de suporte do gravador para tipos de operações de backup. Consulte [**\_ \_ esquema de backup do VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) para obter mais informações.
-   Suporte para a especificação do solicitante de novos destinos de restauração de arquivo ([*novos locais de destino*](vssgloss-n.md)) durante as operações de restauração. Consulte [trabalhando com novos destinos durante a restauração](working-with-new-targets-during-restore.md) para obter mais informações.
-   Suporte para restauração condicional no momento da reinicialização. Consulte VSS \_ RME \_ Restore \_ na \_ reinicialização \_ se \_ não for possível \_ substituir ([**VSE \_ RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)) para obter mais informações.
-   Definição de um estado de restauração e tipo de restauração. Consulte [**\_ \_ tipo de restauração do VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) e estado de restauração do [VSS](vss-restore-state.md) para obter mais informações.
-   Suporte para consultas de gravador sobre o estado da cópia de sombra. Consulte [**CVssWriter:: GetContext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext) e [**CVssWriter:: GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename) para obter mais informações.
-   Suporte para cópias de sombra transportáveis no Windows Server 2003, Enterprise Edition e Windows Server 2003, Datacenter Edition. Para obter mais informações, consulte [importando volumes copiados de sombra transportável](importing-transportable-shadow-copied-volumes.md).

 

 



