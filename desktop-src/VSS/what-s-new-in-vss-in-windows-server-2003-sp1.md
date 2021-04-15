---
description: 'A lista a seguir indica as adições e alterações na interface Serviço de Cópias de Sombra de Volume no Windows Server 2003 com Service Pack 1 (SP1):'
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: O que há de novo no VSS no Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559b51d5b019d9d57aa154c4728ef5c8f4bb19d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461134"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a>O que há de novo no VSS no Windows Server 2003 SP1

A lista a seguir indica as adições e alterações na interface Serviço de Cópias de Sombra de Volume no Windows Server 2003 com Service Pack 1 (SP1):

## <a name="auto-recovery"></a>Recuperação automática

A [*recuperação automática*](vssgloss-a.md) permite aos gravadores um tempo para atualizar os componentes em uma cópia de sombra antes que a cópia de sombra seja alterada permanentemente para somente leitura. Por exemplo, um banco de dados pode precisar reverter todas as transações incompletas para todas as cópias de sombra (o gravador de banco de dados definiria o sinalizador de **\_ recuperação de \_ backup \_ do CF VSS** para os componentes do banco de dados). A recuperação automática iniciada pelo solicitante permite uma restauração refinada (por exemplo, restaurar uma tabela em um banco de dados ou uma pasta em um servidor de email), ou a reversão para dar suporte a Data Mining para executar a análise que seria muito lenta para um servidor de produção (o solicitante adicionaria a **\_ \_ \_ \_ recuperação de reversão do atributo** de cópia de sombra do VSS.) A recuperação automática não é compatível com cópias de sombra transportáveis, mas há suporte para a mesma funcionalidade usando a [recuperação rápida usando volumes copiados de sombra transportável](fast-recovery-using-transportable-shadow-copied-volumes.md).

Os seguintes elementos de programação têm alterações para dar suporte à recuperação automática:

Métodos de classe

-   [**CVssWriter::GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

Enumerações

-   [**\_sinalizadores de componente do VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [**\_\_atributos de \_ instantâneo de volume do VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

Métodos de interface

-   [**IVssProviderCreateSnapshotSet::P reFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [**IVssProviderCreateSnapshotSet::P ostFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a>Suporte completo para cópias de sombra transportáveis

As cópias de sombra transportáveis têm suporte em todas as edições do Windows Server 2003 com SP1. Para obter mais informações, consulte [importando volumes copiados de sombra transportável](importing-transportable-shadow-copied-volumes.md).

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Recuperação rápida usando volumes copiados de sombra transportável

[Recuperação rápida usando volumes copiados de sombra transportável](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a>Gerenciamento de área de armazenamento de cópias de sombra

[**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



