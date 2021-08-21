---
description: 'A lista a seguir indica adições e alterações na interface Serviço de Cópias de Sombra de Volume no Windows Server 2003 com Service Pack 1 (SP1):'
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Novidades no VSS no Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baed6cde05eb1aabe1bc43f48aa035146e020f23d215e7902d3544414619b4e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344189"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a>Novidades no VSS no Windows Server 2003 SP1

A lista a seguir indica adições e alterações na interface Serviço de Cópias de Sombra de Volume no Windows Server 2003 com Service Pack 1 (SP1):

## <a name="auto-recovery"></a>Recuperação automática

[*A recuperação automática*](vssgloss-a.md) permite que os autores atualizem os componentes em uma cópia de sombra antes que a cópia de sombra seja alterada permanentemente para somente leitura. Por exemplo, um banco de dados pode precisar reverter quaisquer transações incompletas para todas as cópias de sombra (o autor do banco de dados definiria o sinalizador **\_ VSS CF \_ BACKUP \_ RECOVERY** para os componentes do banco de dados). A recuperação automática iniciada pelo solicitante permite a restauração fina (por exemplo, restaurar uma tabela em um banco de dados ou uma pasta em um servidor de email) ou a redução para dar suporte à mineração de dados para executar uma análise que seria muito lenta para um servidor de produção (o solicitante adicionaria **\_ VSS VOLSNAP \_ ATTR \_ ROLLBACK \_ RECOVERY** ao contexto de cópia de sombra.) A recuperação automática não é compatível com cópias de sombra transportáveis, mas há suporte para a mesma funcionalidade usando a Recuperação Rápida usando volumes copiados de sombra [transportáveis.](fast-recovery-using-transportable-shadow-copied-volumes.md)

Os seguintes elementos de programação têm alterações para dar suporte à recuperação automática:

Métodos de classe

-   [**CVssWriter::GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

Enumerações

-   [**SINALIZADORES \_ DE COMPONENTE DO \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [**\_ATRIBUTOS DE \_ INSTANTÂNEO DE VOLUME \_ \_ DO VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

Métodos de interface

-   [**IVssProviderCreateSnapshotSet::P reFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [**IVssProviderCreateSnapshotSet::P ostFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a>Suporte completo para cópias de sombra transportáveis

Cópias de sombra transportáveis têm suporte em todas as edições do Windows Server 2003 com SP1. Para obter mais informações, consulte [Importando volumes copiados de sombra transportáveis.](importing-transportable-shadow-copied-volumes.md)

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Recuperação rápida usando volumes copiados de sombra transportáveis

[Recuperação rápida usando volumes copiados de sombra transportáveis](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a>Gerenciamento de área de armazenamento de cópia de sombra

[**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



