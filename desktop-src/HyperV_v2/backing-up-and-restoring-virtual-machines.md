---
description: O Hyper-V usa o VSS (Serviço de Cópias de Sombra de Volume) para fazer backup e restaurar máquinas virtuais.
ms.assetid: 94C67F22-658D-49DD-9588-6BB4FCF7ADA9
title: Fazer o back-up e restaurar máquinas virtuais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf5a0db5bf6956557c22445d5745dbaede03389cf6ead7467b32b65e76c59b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914036"
---
# <a name="backing-up-and-restoring-virtual-machines"></a>Fazer o back-up e restaurar máquinas virtuais

O Hyper-V usa o VSS (Serviço de Cópias de Sombra de Volume) para fazer backup e restaurar máquinas virtuais. Se os serviços de integração de backup (instantâneo de volume) estão instalados no sistema operacional convidado, um solicitante VSS é instalado que permitirá que os autores vsS no sistema operacional convidado participem do backup da máquina virtual. Para obter detalhes, consulte as seguintes seções:

-   [Fazer o back-up das máquinas virtuais](#backing-up-the-virtual-machines)
-   [Restaurando as máquinas virtuais](#restoring-the-virtual-machines)
-   [Clustering de failover e VSS do Hyper-V](#failover-clustering-and-hyper-v-vss)
-   [Detalhes sobre o VsS Writer do Hyper-V](#details-on-the-hyper-v-vss-writer)
-   [Tópicos relacionados](#related-topics)

## <a name="backing-up-the-virtual-machines"></a>Fazer o back-up das máquinas virtuais

O Hyper-V usa um dos dois mecanismos para fazer o back-up de cada máquina virtual. O mecanismo de backup padrão é chamado de método "Estado Salvo", em que a máquina virtual é colocada em um estado salvo durante o processamento do evento PrepareForSnapshot, os instantâneos são tirados dos volumes apropriados e a máquina virtual é retornada ao estado anterior durante o processamento do evento PostSnapshot.

O outro mecanismo de backup é chamado de método "Instantâneo de VM filho", que usa VSS dentro da máquina virtual filho para participar do backup. Para que o método "Instantâneo de VM filho" seja suportado, todas as seguintes condições devem ser atendidas:

-   O Serviço de Integração de Backup (instantâneo de volume) está instalado e em execução na máquina virtual filho. O nome do serviço é "Solicitante de Cópia de Sombra de Volume do Hyper-V".
-   A máquina virtual filho deve estar no estado de execução.
-   O Local do Arquivo de Instantâneo para a máquina virtual está definido como sendo o mesmo volume no sistema operacional host que os arquivos VHD para a máquina virtual.
-   Todos os volumes na máquina virtual filho são discos básicos e não há discos dinâmicos.
-   Todos os discos na máquina virtual filho devem usar um sistema de arquivos que dá suporte a instantâneos (por exemplo, NTFS).

Em geral, o processo para fazer backup de máquinas virtuais é o mesmo descrito em Visão geral do processamento de [um backup no VSS.](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss) O comportamento exclusivo ocorre quando o autor VSS do Hyper-V (parte do serviço "Gerenciamento de Máquinas Virtuais do Hyper-V") processa o evento PrepareForSnapshot. Se o backup tiver sido feito usando o método "Instantâneo de VM filho", haverá processamento adicional feito, mas ele não será visível para a máquina virtual filho.

O procedimento a seguir descreve como fazer o back-up de máquinas virtuais.

**Para fazer o back-up de máquinas virtuais**

1.  Para cada máquina virtual nos metadados do autor, se o método "Estado Salvo" for usado, a máquina virtual será colocada em um estado salvo. Para máquinas virtuais que usam o método "Instantâneo de VM filho", o Serviço solicitante de cópia de sombra de volume do Hyper-V na máquina virtual filho processa o backup conforme detalhado em Visão geral do processamento de um backup no [VSS.](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss) Todos os eventos VSS na máquina virtual filho ocorrem durante o processamento do sistema operacional host do evento PrepareForSnapshot.
2.  Depois que todas as máquinas virtuais foram colocadas no estado salvo ou tiveram instantâneos tirados, o autor vss do Hyper-V retorna do evento PrepareForSnapshot. Nenhum processamento é feito pelo autor vss do Hyper-V durante os eventos de congelamento e descongelamento.
3.  Quando o autor vss do Hyper-V processa o evento PostSnapshot, as máquinas virtuais que tiveram o backup feito usando o método "Estado Salvo" e foram colocadas em um estado salvo pelo autor vsS do Hyper-V são retornadas para o estado em que estavam antes do início do backup. Para as máquinas virtuais que tiveram o backup feito usando o método "Instantâneo de VM filho", a imagem de host dos arquivos VHD que tiveram os instantâneos tirados é relembolsada para o instantâneo tirado durante o processamento do evento PrepareForSnapshot. Esse processamento é feito independentemente dos autores vss nas máquinas virtuais filho, de modo que os instantâneos tirados devem ser recuperáveis automaticamente. (**VSS \_ VOLSNAP \_ ATTR \_ NO \_ AUTORECOVERY** não está definido no contexto.)

Não há suporte para backups parciais. Se qualquer máquina virtual não conseguir criar um instantâneo, nenhuma máquina virtual terá o backup feito.

> [!Note]  
> Os discos de passagem e iSCSI não são visíveis para o sistema operacional do host e, portanto, não têm backup feito pelo autor vss do Hyper-V. Os backups desses volumes devem ser feitos inteiramente na máquina virtual.

 

## <a name="restoring-the-virtual-machines"></a>Restaurando as máquinas virtuais

A restauração das máquinas virtuais é feita inteiramente pelo sistema operacional host; os autores VSS nas máquinas virtuais filho não estão envolvidos.

O procedimento a seguir descreve como restaurar máquinas virtuais.

**Para restaurar máquinas virtuais**

1.  Durante o processamento do evento PreRestore, o autor vss do Hyper-V desliga e exclui todas as máquinas virtuais que estão prestes a ser restauradas.
2.  Depois que todos os autores vss processam o evento PreRestore, os arquivos são restaurados.
3.  Durante o processamento do evento PostRestore, o autor vss do Hyper-V chama o método [**IVssComponent::GetFileRestoreStatus.**](/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus) Se o retorno não for **VSS \_ RS \_ ALL,** o autor vss do Hyper-V chamará o método [**SetWriterFailure**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure) e retornará **False** do [**método OnPostRestore.**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore)
4.  Para cada máquina virtual restaurada, o autor vss do Hyper-V registra a máquina virtual com o serviço de gerenciamento do Hyper-V. Se a máquina virtual for restaurada para um local não padrão, um link simbólico será criado no local padrão, vinculando-se a esse local.
5.  Para cada VHD que foi restaurado, o local é comparado com o especificado para essa máquina virtual. Se o local for diferente, a configuração será atualizada com o local apropriado.
6.  A configuração de rede é atualizada. Se as opções virtuais às que a máquina virtual foi conectada quando foi feito backup ainda sairão, novas portas serão criadas e conectadas à máquina virtual.

## <a name="failover-clustering-and-hyper-v-vss"></a>Clustering de failover e VSS do Hyper-V

O autor vss do Hyper-V não considera as máquinas virtuais que fazem parte de um cluster de failover. Durante os backups do método "Estado Salvo" e todas as restaurações, a máquina virtual seria colocada no estado salvo ou excluída inteiramente. Isso seria visto como uma falha pelo serviço de clustering e faria com que os aplicativos nesses nós falhassem em outros nós. Para evitar isso durante backups de "Estado Salvo", o estado da máquina virtual deve ser salvo usando o serviço de clustering. Para evitar isso durante uma restauração, os recursos na máquina virtual precisariam ser offline.

## <a name="details-on-the-hyper-v-vss-writer"></a>Detalhes sobre o VsS Writer do Hyper-V

Nome do autor: Microsoft Hyper-V vss writer

ID do autor: 66841cd4-6ded-4f4b-8f17-fd23f8ddc3de

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do processamento de um backup no VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)
</dt> <dt>

[Visão geral do processamento de uma restauração no VSS](/windows/desktop/VSS/overview-of-processing-a-restore-under-vss)
</dt> </dl>

 

 
