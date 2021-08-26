---
description: 'Saiba mais sobre: <span id=vhd.vhd_functions></span> funções de disco virtual'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Funções de disco virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32133e3afa8402de8483a68eb4957b261b46e556
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477212"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span id="vhd.vhd_functions"></span>Funções de disco virtual

As funções a seguir são usadas em discos virtuais:

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>Nesta seção


| Tópico | Descrição | 
|-------|-------------|
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></p> | <p>Aplica um instantâneo do disco virtual atual para arquivos de conjunto VHD.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></p> | <p>Anexa um pai a um disco virtual aberto com o sinalizador <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> .</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></p> | <p>Anexa um VHD (disco rígido virtual) ou um arquivo de imagem de CD ou DVD (ISO) localizando um provedor VHD apropriado para realizar o anexo.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></p> | <p>Interrompe uma operação de espelhamento iniciada anteriormente e define o espelho como o disco virtual ativo.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></p> | <p>Reduz o tamanho de um arquivo de repositório de backup do VHD (disco rígido virtual).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></p> | <p>Cria um arquivo de imagem de disco rígido virtual (VHD), usando parâmetros padrão ou um disco virtual ou disco físico existente.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></p> | <p>Exclui um instantâneo de um arquivo de conjunto de VHD.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></p> | <p>Exclui os metadados de um disco virtual.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></p> | <p>Desanexa um VHD (disco rígido virtual) ou um arquivo de imagem de CD ou DVD (ISO) localizando um provedor de disco virtual apropriado para realizar a operação.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></p> | <p>Enumera os metadados associados a um disco virtual.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></p> | <p>Aumenta o tamanho de um VHD (disco rígido virtual) fixo ou expansível dinamicamente.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></p> | <p>Retorna as relações entre os discos rígidos virtuais (VHDs) ou o arquivo de imagem de CD ou DVD (ISO) ou os volumes contidos nesses discos e seu disco ou volume pai.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></p> | <p>Recupera informações sobre um VHD.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></p> | <p>Recupera os metadados especificados do disco virtual.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></p> | <p>Verifica o progresso de uma operação de disco rígido virtual (VHD) assíncrona.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></p> | <p>Recupera o caminho para o objeto de dispositivo físico que contém um VHD (disco rígido virtual) ou um arquivo de imagem de CD ou DVD (ISO).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></p> | <p>Mescla um VHD (disco rígido virtual) filho em uma cadeia diferencial com um ou mais discos virtuais pai na cadeia.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></p> | <p>Inicia uma operação de espelhamento para um disco virtual.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></p> | <p>Modifica o conteúdo interno de um arquivo de disco virtual. Pode ser usado para definir a folha ativa ou para corrigir entradas de instantâneo.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></p> | <p>Abre um disco rígido virtual (VHD) ou um arquivo de imagem de CD ou DVD (ISO) para uso.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></p> | <p>Recupera informações sobre alterações nas áreas especificadas de um disco rígido virtual (VHD) que são rastreadas pelo RCT (controle de alterações resiliente).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></p> | <p>Emite uma solicitação SCSI inserida diretamente para um disco rígido virtual.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></p> | <p>Redimensiona um disco virtual.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></p> | <p>Define informações sobre um VHD (disco rígido virtual).</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></p> | <p>Define um item de metadados para um disco virtual.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></p> | <p>Cria um instantâneo do disco virtual atual para arquivos de conjunto VHD.</p> | 


 

 

 
