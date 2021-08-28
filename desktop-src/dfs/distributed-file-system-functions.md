---
title: Funções de Sistema de Arquivos Distribuído
description: A seguir estão as funções de Sistema de Arquivos Distribuído (DFS).
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3fd41879293f376dfdb3d769d5152b2e747fc6e387f8f9538854d4d3e06e7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096716"
---
# <a name="distributed-file-system-functions"></a>Funções de Sistema de Arquivos Distribuído

A seguir estão as funções de Sistema de Arquivos Distribuído (DFS).

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[NetDfsAdd](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
Cria um novo link de Sistema de Arquivos Distribuído (DFS) ou adiciona destinos a um link existente em um namespace do DFS.

</dd> <dt>

[NetDfsAddFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
Cria um novo namespace do Sistema de Arquivos Distribuído (DFS) baseado em domínio. Se o namespace já existir, a função adicionará o destino de raiz especificado a ele.

</dd> <dt>

[NetDfsAddRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
Cria um namespace DFS baseado em domínio ou autônomo ou adiciona um novo destino de raiz a um namespace baseado em domínio existente.

</dd> <dt>

[NetDfsAddStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
Cria um novo namespace de Sistema de Arquivos Distribuído autônomo (DFS).

</dd> <dt>

[NetDfsEnum](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
Enumera os namespaces de Sistema de Arquivos Distribuído (DFS) hospedados em um servidor ou links DFS de um namespace hospedado por um servidor.

</dd> <dt>

[NetDfsGetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
Recupera informações sobre uma raiz do Sistema de Arquivos Distribuído (DFS) ou o link do cache mantido pelo cliente do DFS.

</dd> <dt>

[NetDfsGetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
Recupera o descritor de segurança do objeto de contêiner para os namespaces do DFS baseados em domínio no domínio de Active Directory especificado.

</dd> <dt>

[NetDfsGetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
Recupera informações sobre uma raiz do Sistema de Arquivos Distribuído (DFS) especificada ou um link em um namespace do DFS.

</dd> <dt>

[NetDfsGetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
Recupera o descritor de segurança para o objeto raiz do namespace do DFS especificado.

</dd> <dt>

[NetDfsGetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
Recupera o descritor de segurança para o objeto de contêiner do namespace DFS autônomo especificado.

</dd> <dt>

[NetDfsGetSupportedNamespaceVersion](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
Determina o número de versão de metadados com suporte.

</dd> <dt>

[NetDfsMove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
Renomeia ou move um link DFS.

</dd> <dt>

[NetDfsRemove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
Remove um link de Sistema de Arquivos Distribuído (DFS) ou um destino de link específico de um link DFS em um namespace DFS. Ao remover um destino de link específico, o link em si será removido se o último destino de link do link for removido.

</dd> <dt>

[NetDfsRemoveFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
Remove o destino raiz especificado de um namespace de Sistema de Arquivos Distribuído baseado em domínio (DFS). Se o último destino raiz do namespace do DFS estiver sendo removido, a função também excluirá o namespace do DFS. Um namespace DFS pode ser excluído sem primeiro excluir todos os links nele.

</dd> <dt>

[NetDfsRemoveFtRootForced](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
Remove o destino raiz especificado de um namespace de Sistema de Arquivos Distribuído baseado em domínio (DFS), mesmo que o servidor de destino raiz esteja offline. Se o último destino raiz do namespace do DFS estiver sendo removido, a função também excluirá o namespace do DFS. Um namespace DFS pode ser excluído sem primeiro excluir todos os links nele.

> [!Note]
> A função [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) não atualiza o registro no servidor de destino raiz DFS. Para obter mais informações, consulte a seção Comentários.

</dd> <dt>

[NetDfsRemoveRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
Remove um destino raiz do DFS de um namespace DFS baseado em domínio. Se o destino raiz for o último destino raiz no namespace DFS, essa função removerá o namespace DFS. Essa função também pode ser usada para remover um namespace autônomo do DFS.

</dd> <dt>

[NetDfsRemoveStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
Exclui um namespace de Sistema de Arquivos Distribuído autônomo (DFS).

</dd> <dt>

[NetDfsSetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
Modifica informações sobre uma raiz de Sistema de Arquivos Distribuído (DFS) ou link no cache mantido pelo cliente DFS.

</dd> <dt>

[NetDfsSetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
Define o descritor de segurança do objeto de contêiner para os namespaces DFS baseados em domínio no domínio de Active Directory especificado.

</dd> <dt>

[NetDfsSetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
Define ou modifica informações sobre uma raiz Sistema de Arquivos Distribuído (DFS) específica, destino raiz, link ou destino de link.

</dd> <dt>

[NetDfsSetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
Define o descritor de segurança para o objeto raiz do namespace do DFS especificado.

</dd> <dt>

[NetDfsSetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
Define o descritor de segurança para o objeto de contêiner do namespace DFS autônomo especificado.

</dd> </dl>

Observe que um aplicativo que invoca qualquer uma das funções pode fazer com que o servidor de namespace do DFS local atenda à chamada de função para executar uma sincronização completa dos metadados de namespace relacionados do mestre do emulador PDC para esse domínio. Essa sincronização completa pode ocorrer mesmo quando o modo de escalabilidade raiz está configurado para esse namespace.
