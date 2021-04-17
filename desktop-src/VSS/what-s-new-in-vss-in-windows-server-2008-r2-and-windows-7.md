---
description: O Windows Server 2008 R2 e o Windows 7 apresentam as seguintes alterações na Serviço de Cópias de Sombra de Volume.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'O que há de novo: VSS no Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3677f89517a770a4519369ae11f2eed7e7985414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811378"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a>O que há de novo: VSS no Windows Server 2008 R2 & Windows 7

O Windows Server 2008 R2 e o Windows 7 apresentam as seguintes alterações na Serviço de Cópias de Sombra de Volume.

## <a name="new-vss-interfaces"></a>Novas interfaces VSS

<dl>

[**IVssBackupComponentsEx3**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[**IVssComponentEx2**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[**IVssCreateExpressWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[**IVssExpressWriter**](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a>Novas classes VSS

<dl>

[**CVssWriterEx2**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a>Novas enumerações VSS

<dl>

[**\_Opções de recuperação do VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a>Novas funções do VSS

<dl>

[**CreateVssExpressWriter**](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a>Modificações de interface VSS existentes

<dl>

Interface [**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)<dl> Método adicionado: [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Rastreamento e log de eventos do VSS

A partir do Windows Server 2008 R2 e do Windows 7, você pode usar a ferramenta VssTrace, a ferramenta Logman ou a ferramenta tracelog para coletar informações de rastreamento para a infraestrutura do VSS. Para obter mais informações, consulte [usando ferramentas de rastreamento com o VSS](using-tracing-tools-with-vss.md).

## <a name="lun-resynchronization"></a>Ressincronização de LUN

No Windows Server 2008 R2 e no Windows 7, os solicitantes do VSS podem usar um recurso de provedor de cópias de sombra de hardware chamado de "LUN Resync" (ressincronização de LUN). Esse é um esquema de recuperação rápida que permite que um administrador de aplicativos restaure dados de uma cópia de sombra para o número de unidade lógica (LUN) original ou para um novo LUN. A cópia de sombra pode ser um clone completo ou uma cópia de sombra diferencial. Em ambos os casos, no final da operação de ressincronização, o LUN de destino terá o mesmo conteúdo que o LUN de cópia de sombra. Durante a operação de ressincronização, a matriz executa uma cópia no nível do bloco da cópia de sombra para o LUN de destino. Para saber mais, consulte o seguinte:

-   [Ressincronização de LUN – um cenário de recuperação rápida no servidor 2008 R2](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   "Como as cópias de sombra são usadas" em [serviço de cópias de sombra de volume](/windows-server/storage/file-server/volume-shadow-copy-service)
-   [Armadilhas comuns de ressincronização de LUN](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a>Gravadores expressos

No Windows Server 2008 R2 e no Windows 7, a interface do VSS Express permite que um aplicativo registre o local de seus arquivos de dados sem implementar um gravador VSS. Para obter mais informações, consulte os [gravadores do serviço de cópias de sombra de volume (VSS) Express](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).

## <a name="new-vss-writers"></a>Novos gravadores VSS

O Windows Server 2008 R2 e o Windows 7 apresentam os seguintes gravadores VSS:

-   Gravador de contadores de desempenho
-   Gravador de Agendador de Tarefas
-   Gravador de repositório de metadados do VSS

Esses novos gravadores são documentados em [gravadores VSS](in-box-vss-writers.md)integrados.

 

 
