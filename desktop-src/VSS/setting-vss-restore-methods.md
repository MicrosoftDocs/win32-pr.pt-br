---
description: A configuração das operações de restauração realmente começa durante o backup de dados, quando os autores especificam, em seus Documentos de Metadados do Writer, como seus dados devem ser restaurados.
ms.assetid: b1f948cd-d3b0-4637-b76d-b54a74bb5948
title: Definição de métodos de restauração do VSS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f7b0d138555b1e10dba55483c694c08a649e97e59cb66ed65c1a276187d3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751705"
---
# <a name="setting-vss-restore-methods"></a>Definição de métodos de restauração do VSS

A configuração das operações de restauração realmente começa durante o backup de dados, quando os autores especificam, em seus Documentos de Metadados do Writer, como seus dados devem ser restaurados.

Essas especificações, conhecidas como métodos de restauração ou [*destinos*](vssgloss-r.md) de restauração originais, podem ser modificadas durante a restauração por autores definindo novos destinos de restauração ou por solicitantes restaurando para novos locais (consulte Locais de [backup](non-default-backup-and-restore-locations.md)e restauração não padrão). [](vssgloss-r.md)

Ao chamar [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod), um autor indica qual método de restauração deve ser usado em seu Documento de Metadados do Writer. O método de restauração é definido como todo o writer e aplicado a todos os arquivos em todos os componentes que um autor gerencia.

Um solicitante obtém (e deve respeitar) essas informações chamando [**IVssExamineWriterMetadata::GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

O método de restauração é definido por uma enumeração [**\_ \_ ENUM RESTOREMETHOD do VSS,**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) que é passada para [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) e retornada de [**IVssExamineWriterMetadata::GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

O Documento de Metadados do Writer dá suporte aos seguintes métodos de restauração válidos (um método de restauração do VSS \_ RME \_ UNDEFINED indica um erro de autor). As figuras resumem como os vários métodos de restauração com suporte e definidos devem ser implementados (VSS RME CUSTOM não tem nenhuma figura associada a ele, porque, por definição, ele é específico para o autor e deve seguir as APIs e a documentação específicas do \_ \_ autor):

-   VSS \_ RME \_ RESTORE SE NÃO ESTIVER \_ \_ \_ LÁ. Restaure os arquivos de componente no disco se nenhum dos arquivos já estiver no disco. O status do arquivo de destino deve ser verificado após um [**evento PreRestore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
    ![Diagrama que mostra uma árvore de solução de problemas para VSS_RME_RESTORE_IF_NOT_THERE.](images/rint.png)
-   VSS \_ RME \_ RESTORE SE \_ PUDER \_ \_ SUBSTITUIR. Restaure arquivos em disco se todos os arquivos puderem ser substituídos. O status do arquivo de destino deve ser verificado após um [**evento PreRestore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
    ![Diagrama que mostra uma árvore de solução de problemas para VSS_RME_RESTORE_IF_CAN_REPLACE.](images/ricr.png)
-   VSS \_ RME \_ STOP \_ RESTORE \_ START. Um serviço será interrompido antes de restaurar os arquivos.
    ![Diagrama que mostra uma árvore de solução de problemas para VSS_RME_STOP_RESTORE_START.](images/srr.png)
-   VSS \_ RME \_ RESTORE PARA \_ LOCAL \_ \_ ALTERNATIVO. Restaure arquivos em disco em um local alternativo. Os mapeamentos de localização alternativos são especificados no Documento de Metadados do Writer.
    ![Diagrama que mostra uma árvore de solução de problemas para VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.](images/rtal.png)
-   RESTAURAÇÃO \_ DO VSS RME \_ \_ NA \_ REINICIALIZAÇÃO. Fazer com que os arquivos sejam restaurados (substituídos) quando o computador for reinicializado.
    ![Diagrama que mostra uma árvore de solução de problemas para VSS_RME_RESTORE_AT_REBOOT.](images/rar.png)
-   VSS \_ RME \_ RESTORE \_ AT \_ REBOOT \_ IF \_ CANNOT \_ REPLACE. Se um arquivo não puder ser restaurado no disco em um sistema em execução, ele será restaurado (substituído) quando o computador for reinicializado.
    ![Diagrama que mostra uma árvore de solução de forVSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE. ](images/raricr.png)
-   VSS \_ RME \_ CUSTOM. Nenhum dos métodos predefinidos funcionará; O aplicativo de backup deve usar APIs especializadas para executar a operação de restauração. Para esse método de backup, o solicitante deve entender completamente o autor em questão. Consulte [Casos de uso especiais do VSS](special-vss-usage-cases.md) para instâncias com suporte no momento.

 

 



