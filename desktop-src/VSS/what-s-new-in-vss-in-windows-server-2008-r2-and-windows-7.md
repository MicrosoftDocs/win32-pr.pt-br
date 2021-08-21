---
description: Windows O Servidor 2008 R2 e Windows 7 apresentam as seguintes alterações no Serviço de Cópias de Sombra de Volume.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Novidades: VSS no Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eeaaf42a82e13c5766ee3cfa6ba9fe73a36a783824497482ac97fc20d058a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121522"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a>Novidades: VSS no Windows Server 2008 R2 & Windows 7

Windows O Servidor 2008 R2 e Windows 7 apresentam as seguintes alterações no Serviço de Cópias de Sombra de Volume.

## <a name="new-vss-interfaces"></a>Novas interfaces vss

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

## <a name="new-vss-enumerations"></a>Novas enumerações vss

<dl>

[**OPÇÕES DE \_ RECUPERAÇÃO DO \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a>Novas funções vss

<dl>

[**CreateVssExpressWriter**](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a>Modificações de interface do VSS existentes

<dl>

[**Interface IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)<dl> Método adicionado: [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Rastreamento e registro em log de eventos do VSS

A partir do Windows Server 2008 R2 e Windows 7, você pode usar a ferramenta VssTrace, a ferramenta Logman ou a ferramenta Tracelog para coletar informações de rastreamento para a infraestrutura do VSS. Para obter mais informações, consulte [Usando ferramentas de rastreamento com VSS](using-tracing-tools-with-vss.md).

## <a name="lun-resynchronization"></a>Ressincronização de LUN

No Windows Server 2008 R2 e no Windows 7, os solicitantes do VSS podem usar um recurso de provedor de cópias de sombra de hardware chamado de "LUN Resync" (ressincronização de LUN). Esse é um esquema de recuperação rápida que permite que um administrador de aplicativos restaure dados de uma cópia de sombra para o LUN (número de unidade lógica) original ou para um novo LUN. A cópia de sombra pode ser um clone completo ou uma cópia de sombra diferencial. Em ambos os casos, no final da operação de ressincronização, o LUN de destino terá o mesmo conteúdo que o LUN de cópia de sombra. Durante a operação de ressincronização, a matriz executa uma cópia no nível do bloco da cópia de sombra para o LUN de destino. Para saber mais, consulte o seguinte:

-   [Lun Resync – um cenário de recuperação rápida no Servidor 2008 R2](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   "Como cópias de sombra são usadas" [em Serviço de Cópias de Sombra de Volume](/windows-server/storage/file-server/volume-shadow-copy-service)
-   [Gotchas comuns do LUN Resync](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a>Express Writers

No Windows Server 2008 R2 e Windows 7, a interface expressa do VSS permite que um aplicativo registre o local de seus arquivos de dados sem implementar um vss writer. Para obter mais informações, [consulte Serviço de Cópias de Sombra de Volume (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).

## <a name="new-vss-writers"></a>Novos vss writers

Windows O Server 2008 R2 e Windows 7 apresentam os seguintes autores VSS:

-   Contador de Desempenho Writer
-   Agendador de Tarefas writer
-   VSS Metadata Store Writer

Esses novos autores estão documentados em [In-Box VSS Writers](in-box-vss-writers.md).

 

 
