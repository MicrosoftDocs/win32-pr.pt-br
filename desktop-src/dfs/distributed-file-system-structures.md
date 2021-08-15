---
description: A seguir estão as estruturas de DFS Sistema de Arquivos Distribuído
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: Estruturas de Sistema de Arquivos Distribuído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1561a4586cc03304c6aa1c1e323eb42fd09766df0cc3c7210636367337873a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541277"
---
# <a name="distributed-file-system-structures"></a>Estruturas de Sistema de Arquivos Distribuído

A seguir estão as estruturas de Sistema de Arquivos Distribuído (DFS):

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

Buffer de entrada usado com o código de controle de [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dd> <dt>

[Estrutura de _DFS_INFO_1](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
Contém o nome de uma raiz ou um link de Sistema de Arquivos Distribuído (DFS).

</dd> <dt>

[Estrutura de _DFS_INFO_2](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
Contém informações sobre um link ou uma raiz do Sistema de Arquivos Distribuído (DFS). Essa estrutura contém o nome, o status e o número de destinos DFS para a raiz ou o link.

</dd> <dt>

[Estrutura de _DFS_INFO_3](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
Contém informações sobre um link ou uma raiz do Sistema de Arquivos Distribuído (DFS). Essa estrutura contém o nome, o status, o número de destinos do DFS e informações sobre cada destino da raiz ou do link.

</dd> <dt>

[Estrutura de _DFS_INFO_4](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
Contém informações sobre um link ou uma raiz do Sistema de Arquivos Distribuído (DFS). Essa estrutura contém o nome, o status, o **GUID**, o tempo limite, o número de destinos e as informações sobre cada destino da raiz ou do link.

</dd> <dt>

[Estrutura de _DFS_INFO_5](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
Contém informações sobre um link ou uma raiz do Sistema de Arquivos Distribuído (DFS). Essa estrutura contém o nome, o status, o **GUID**, o tempo limite, as propriedades de namespace/raiz/link, o tamanho dos metadados e o número de destinos para a raiz ou o link.

</dd> <dt>

[Estrutura de _DFS_INFO_6](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
Contém informações sobre um link ou uma raiz do Sistema de Arquivos Distribuído (DFS). Essa estrutura contém o nome, o status, o **GUID**, o tempo limite, as propriedades de namespace/raiz/link, o tamanho dos metadados, o número de destinos e as informações sobre cada destino da raiz ou do link.

</dd> <dt>

[Estrutura de _DFS_INFO_7](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
Contém informações sobre um namespace do DFS. Essa estrutura contém o **GUID** de versão para os metadados do namespace.

</dd> <dt>

[Estrutura de _DFS_INFO_8](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
Contém o nome, o status, o **GUID**, o tempo limite, os sinalizadores de propriedade, o tamanho dos metadados, as informações de destino do DFS e o descritor de segurança do ponto de nova análise de link para uma raiz ou link.

</dd> <dt>

[Estrutura de _DFS_INFO_9](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
Contém o nome, o status, o **GUID**, o tempo limite, os sinalizadores de propriedade, o tamanho dos metadados, as informações de destino do DFS, o descritor de segurança do ponto de nova análise de link e uma lista de destinos do DFS para uma raiz ou link.

</dd> <dt>

[Estrutura de _DFS_INFO_50](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
Contém a versão de metadados do DFS e os recursos de um namespace do DFS existente.

</dd> <dt>

[Estrutura de _DFS_INFO_100](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
Contém um comentário associado a uma raiz ou link de Sistema de Arquivos Distribuído (DFS).

</dd> <dt>

[Estrutura de _DFS_INFO_101](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
Descreve o estado de armazenamento em uma raiz DFS, link, destino raiz ou destino de link.

</dd> <dt>

[Estrutura de _DFS_INFO_102](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
Contém um valor de tempo limite para associar a uma raiz de Sistema de Arquivos Distribuído (DFS) ou a um link em uma raiz DFS nomeada.

</dd> <dt>

[Estrutura de _DFS_INFO_103](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
Contém propriedades que definem comportamentos específicos para uma raiz ou link do DFS.

</dd> <dt>

[Estrutura de _DFS_INFO_104](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
Contém a prioridade de um destino de raiz de DFS ou destino de link.

</dd> <dt>

[Estrutura de _DFS_INFO_105](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
Contém informações sobre uma raiz ou link do DFS, incluindo comentários, estado, tempo limite e comportamentos de DFS especificados por sinalizadores de propriedade.

</dd> <dt>

[Estrutura de _DFS_INFO_106](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
Contém o estado de armazenamento e a prioridade para um destino de raiz de DFS ou destino de link. Essa estrutura é apenas para uso com a função [**NetDfsSetInfo**](netdfssetinfo.md) .

</dd> <dt>

[Estrutura de _DFS_INFO_107](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
Contém informações sobre uma raiz ou link do DFS, incluindo o comentário, o estado, o tempo limite, os sinalizadores de propriedade e o descritor de segurança do ponto de nova análise de link.

</dd> <dt>

[Estrutura de _DFS_INFO_150](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
Contém o descritor de segurança para um ponto de nova análise do link do DFS.

</dd> <dt>

[Estrutura de _DFS_INFO_200](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
Contém o nome de um namespace de Sistema de Arquivos Distribuído baseado em domínio (DFS).

</dd> <dt>

[Estrutura de _DFS_INFO_300](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
Contém o nome e o tipo (baseado em domínio ou autônomo) de um namespace do DFS.

</dd> <dt>

[Estrutura de _DFS_STORAGE_INFO](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
Contém informações sobre uma raiz DFS ou destino de link em um namespace DFS ou do cache mantido pelo cliente DFS.

</dd> <dt>

[Estrutura de _DFS_STORAGE_INFO_1](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
Contém informações sobre um destino DFS, incluindo o nome do servidor de destino DFS e o nome do compartilhamento, bem como o estado e a prioridade do destino.

</dd> <dt>

[Estrutura de _DFS_SUPPORTED_NAMESPACE_VERSION_INFO](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
Contém informações de versão para um namespace do DFS.

</dd> <dt>

[Estrutura de _DFS_TARGET_PRIORITY](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
Contém a classe de prioridade e a classificação de um destino DFS específico.

</dd> </dl>
