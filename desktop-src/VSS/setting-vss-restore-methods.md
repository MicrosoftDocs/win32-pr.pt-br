---
description: A configuração das operações de restauração é realmente iniciada durante o backup de dados, quando os gravadores especificam, em seus documentos de metadados do gravador, como seus dados devem ser restaurados.
ms.assetid: b1f948cd-d3b0-4637-b76d-b54a74bb5948
title: Definição de métodos de restauração do VSS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412cb699fb791a973e280f63fec03bd2854ccd1d
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104172399"
---
# <a name="setting-vss-restore-methods"></a>Definição de métodos de restauração do VSS

A configuração das operações de restauração é realmente iniciada durante o backup de dados, quando os gravadores especificam, em seus documentos de metadados do gravador, como seus dados devem ser restaurados.

Essas especificações, conhecidas como métodos de [*restauração*](vssgloss-r.md) ou destinos de [*restauração*](vssgloss-r.md)originais, podem ser modificadas durante a restauração por gravadores definindo novos destinos de restauração ou por solicitantes restaurando para novos locais (consulte [locais de backup e restauração não padrão](non-default-backup-and-restore-locations.md)).

Chamando [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod), um gravador indica qual método de restauração deve ser usado em seu documento de metadados do gravador. O método Restore é definido para todo o gravador e aplicado a todos os arquivos em todos os componentes gerenciados por um gravador.

Um solicitante Obtém (e deve respeitar) essas informações chamando [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

O método Restore é definido por uma enumeração de [**\_ \_ Enumeração RESTOREMETHOD do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) , que é passada para [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) e retornada de [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

O documento de metadados do gravador dá suporte aos seguintes métodos de restauração válidos (um método Restore do VSS \_ RME \_ indefinido indica um erro do gravador). As figuras resumem como os vários métodos de restauração com suporte e definidos devem ser implementados (VSS \_ RME \_ Custom não tem nenhuma figura associada a ele, porque por definição ele é específico para o gravador e deve seguir as APIs e a documentação do gravador específicas):

-   restauração do VSS \_ RME \_ \_ se \_ não \_ existir. Restaure os arquivos de componente para o disco se nenhum dos arquivos já estiver no disco. O status do arquivo de destino deve ser verificado após um evento de [**Prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .
    ![Diagrama que mostra uma árvore de solução de problemas para VSS_RME_RESTORE_IF_NOT_THERE.](images/rint.png)
-   a \_ restauração do VSS RME \_ se o \_ \_ puder ser \_ substituído. Restaure os arquivos no disco se todos os arquivos puderem ser substituídos. O status do arquivo de destino deve ser verificado após um evento de [**Prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .
    ![Diagrama que mostra uma árvore de solução de problemas para VSS_RME_RESTORE_IF_CAN_REPLACE.](images/ricr.png)
-   início da restauração de interrupção do VSS \_ RME \_ \_ \_ . Um serviço será interrompido antes da restauração dos arquivos.
    ![Diagrama que mostra uma árvore de solução de problemas para VSS_RME_STOP_RESTORE_START.](images/srr.png)
-   restauração do VSS \_ RME \_ para o \_ \_ \_ local alternativo. Restaurar arquivos em disco em um local alternativo. Os mapeamentos de local alternativos são especificados no documento de metadados do gravador.
    ![Diagrama que mostra uma árvore de solução de problemas para VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.](images/rtal.png)
-   restauração do VSS \_ RME \_ \_ na \_ reinicialização. Faz com que os arquivos sejam restaurados (substituídos) quando o computador é reinicializado.
    ![Diagrama que mostra uma árvore de solução de problemas para VSS_RME_RESTORE_AT_REBOOT.](images/rar.png)
-   restauração do VSS \_ RME \_ \_ na \_ reinicialização \_ se \_ não puder \_ substituir. Se um arquivo não puder ser restaurado no disco em um sistema em execução, ele será restaurado (substituído) quando o computador for reinicializado.
    ![Diagrama que mostra uma forVSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE de árvore de solução de problemas. ](images/raricr.png)
-   VSS \_ RME \_ personalizado. Nenhum dos métodos predefinidos funcionará; o aplicativo de backup deve usar APIs especializadas para executar a operação de restauração. Para esse método de backup, o solicitante deve entender completamente o gravador em questão. Consulte [casos de uso do VSS especiais](special-vss-usage-cases.md) para instâncias com suporte no momento.

 

 



