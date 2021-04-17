---
description: O Hyper-V usa o Serviço de Cópias de Sombra de Volume (VSS) para fazer backup e restaurar máquinas virtuais.
ms.assetid: 94C67F22-658D-49DD-9588-6BB4FCF7ADA9
title: Fazendo backup e restaurando máquinas virtuais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9cf6d5b80a4c7392fb38e893a4fafad3f90435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759886"
---
# <a name="backing-up-and-restoring-virtual-machines"></a>Fazendo backup e restaurando máquinas virtuais

O Hyper-V usa o Serviço de Cópias de Sombra de Volume (VSS) para fazer backup e restaurar máquinas virtuais. Se os serviços de integração de backup (instantâneo de volume) estiverem instalados no sistema operacional convidado, um solicitante VSS será instalado que permitirá que gravadores VSS no sistema operacional convidado participem do backup da máquina virtual. Para obter detalhes, consulte as seguintes seções:

-   [Fazendo backup das máquinas virtuais](#backing-up-the-virtual-machines)
-   [Restaurando as máquinas virtuais](#restoring-the-virtual-machines)
-   [Clustering de failover e VSS do Hyper-V](#failover-clustering-and-hyper-v-vss)
-   [Detalhes sobre o gravador VSS do Hyper-V](#details-on-the-hyper-v-vss-writer)
-   [Tópicos relacionados](#related-topics)

## <a name="backing-up-the-virtual-machines"></a>Fazendo backup das máquinas virtuais

O Hyper-V usa um dos dois mecanismos para fazer backup de cada máquina virtual. O mecanismo de backup padrão é chamado de método "estado salvo", em que a máquina virtual é colocada em um estado salvo durante o processamento do evento PrepareForSnapshot, os instantâneos são tirados dos volumes apropriados e a máquina virtual é retornada ao estado anterior durante o processamento do evento de instantâneo.

O outro mecanismo de backup é chamado de "instantâneo de VM filho", que usa o VSS dentro da máquina virtual filho para participar do backup. Para que o método "instantâneo de VM filho" tenha suporte, todas as condições a seguir devem ser atendidas:

-   O serviço de integração de backup (instantâneo de volume) está instalado e em execução na máquina virtual filho. O nome do serviço é "solicitante de cópia de sombra de volume do Hyper-V".
-   A máquina virtual filho deve estar no estado executando.
-   O local do arquivo de instantâneo para a máquina virtual é definido para ser o mesmo volume no sistema operacional do host que os arquivos VHD da máquina virtual.
-   Todos os volumes na máquina virtual filho são discos básicos e não há discos dinâmicos.
-   Todos os discos na máquina virtual filho devem usar um sistema de arquivos que ofereça suporte a instantâneos (por exemplo, NTFS).

Em geral, o processo de backup de máquinas virtuais é o mesmo descrito em [visão geral do processamento de um backup no VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss). O comportamento exclusivo ocorre quando o gravador VSS do Hyper-V (parte do serviço de gerenciamento de máquinas virtuais do Hyper-V) processa o evento PrepareForSnapshot. Se o backup foi feito usando o método "instantâneo de VM filho", há processamento adicional feito, mas não é visível para a máquina virtual filho.

O procedimento a seguir descreve como fazer backup de máquinas virtuais.

**Para fazer backup de máquinas virtuais**

1.  Para cada máquina virtual nos metadados do gravador, se o método "estado salvo" for usado, a máquina virtual será colocada em um estado salvo. Para máquinas virtuais usando o método "instantâneo de VM filho", o serviço do solicitante de cópias de sombra de volume do Hyper-V na máquina virtual filho processa o backup conforme detalhado em [visão geral do processamento de um backup no VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss). Todos os eventos do VSS na máquina virtual filho ocorrem durante o processamento do sistema operacional do host do evento PrepareForSnapshot.
2.  Depois que todas as máquinas virtuais tiverem sido colocadas no estado salvo ou tiverem instantâneos tirados, o gravador VSS do Hyper-V retornará do evento PrepareForSnapshot. Nenhum processamento é feito pelo gravador VSS do Hyper-V durante os eventos Freeze e descongelar.
3.  Quando o gravador VSS do Hyper-V processa o evento de pós-instantâneo, as máquinas virtuais cujo backup foi feito usando o método "estado salvo" e foram colocadas em um estado salvo pelo gravador VSS do Hyper-V são retornadas para o estado em que estavam antes do início do backup. Para as máquinas virtuais cujo backup foi feito usando o método "instantâneo de VM filho", a imagem de host dos arquivos VHD que tiveram os instantâneos obtidos é revertida para o instantâneo obtido durante o processamento do evento PrepareForSnapshot. Esse processamento é feito independentemente dos gravadores VSS nas máquinas virtuais filhas, de modo que os instantâneos tirados devem ser recuperáveis automaticamente. (Não é possível definir a **\_ \_ \_ \_ AutoRecuperação do atributo de VOLSNAP do VSS** no contexto.)

Não há suporte para backups parciais. Se alguma máquina virtual falhar ao criar um instantâneo, não será feito backup de máquinas virtuais.

> [!Note]  
> Os discos de passagem e iSCSI não são visíveis para o sistema operacional do host e, portanto, não são submetidos a backup pelo gravador VSS do Hyper-V. Os backups desses volumes devem ser inteiramente executados na máquina virtual.

 

## <a name="restoring-the-virtual-machines"></a>Restaurando as máquinas virtuais

A restauração das máquinas virtuais é feita inteiramente pelo sistema operacional do host; os gravadores VSS nas máquinas virtuais filhas não estão envolvidos.

O procedimento a seguir descreve como restaurar máquinas virtuais.

**Para restaurar máquinas virtuais**

1.  Durante o processamento do evento de prerestore, o gravador VSS do Hyper-V desliga e exclui todas as máquinas virtuais que estão prestes a ser restauradas.
2.  Depois que todos os gravadores VSS tiverem processado o evento prerestore, os arquivos serão restaurados.
3.  Durante o processamento do evento de restauração, o gravador VSS do Hyper-V chama o método [**IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus) . Se o retorno não for **VSS \_ RS \_**, o gravador VSS do Hyper-V chamará o método [**SetWriterFailure**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure) e retornará **false** do método [**OnPostRestore**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore) .
4.  Para cada máquina virtual que foi restaurada, o gravador VSS do Hyper-V registra a máquina virtual com o serviço de gerenciamento do Hyper-V. Se a máquina virtual for restaurada para um local não padrão, um link simbólico será criado no local padrão vinculando a esse local.
5.  Para cada VHD que foi restaurado, o local é comparado com aquele especificado para essa máquina virtual. Se o local for diferente, a configuração será atualizada com o local apropriado.
6.  A configuração de rede está atualizada. Se os comutadores virtuais aos quais a máquina virtual estava conectada quando foi feito o backup ainda forem encerrados, novas portas serão criadas e conectadas à máquina virtual.

## <a name="failover-clustering-and-hyper-v-vss"></a>Clustering de failover e VSS do Hyper-V

O gravador VSS do Hyper-V não dá nenhuma consideração às máquinas virtuais que fazem parte de um cluster de failover. Durante os backups do método "estado salvo" e todas as restaurações, a máquina virtual seria colocada no estado salvo ou totalmente excluída. Isso seria visto como uma falha pelo serviço de clustering e faz com que os aplicativos nesses nós fossem failover para outros nós. Para evitar isso durante os backups de "estado salvo", o estado da máquina virtual deve ser salvo usando o serviço de clustering. Para evitar isso durante uma restauração, os recursos na máquina virtual precisariam ser colocados offline.

## <a name="details-on-the-hyper-v-vss-writer"></a>Detalhes sobre o gravador VSS do Hyper-V

Nome do gravador: gravador VSS do Microsoft Hyper-V

ID do gravador: 66841cd4-6ded-4f4b-8f17-fd23f8ddc3de

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do processamento de um backup no VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)
</dt> <dt>

[Visão geral do processamento de uma restauração no VSS](/windows/desktop/VSS/overview-of-processing-a-restore-under-vss)
</dt> </dl>

 

 
