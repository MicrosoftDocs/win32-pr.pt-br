---
description: A seguir estão as estruturas Sistema de Arquivos Distribuído DFS
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: estruturas Sistema de Arquivos Distribuído dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1561a4586cc03304c6aa1c1e323eb42fd09766df0cc3c7210636367337873a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541277"
---
# <a name="distributed-file-system-structures"></a>estruturas Sistema de Arquivos Distribuído dados

Veja a seguir as estruturas Sistema de Arquivos Distribuído (DFS) :

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

Buffer de entrada usado com o [**código FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) controle
</dd> <dt>

[_DFS_INFO_1 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
Contém o nome de uma raiz Sistema de Arquivos Distribuído (DFS) ou link.

</dd> <dt>

[_DFS_INFO_2 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
Contém informações sobre uma raiz Sistema de Arquivos Distribuído (DFS) ou link. Essa estrutura contém o nome, o status e o número de destinos do DFS para a raiz ou link.

</dd> <dt>

[_DFS_INFO_3 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
Contém informações sobre uma raiz Sistema de Arquivos Distribuído (DFS) ou link. Essa estrutura contém o nome, o status, o número de destinos do DFS e informações sobre cada destino da raiz ou link.

</dd> <dt>

[_DFS_INFO_4 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
Contém informações sobre uma raiz Sistema de Arquivos Distribuído (DFS) ou link. Essa estrutura contém o nome, o status, **o GUID,** o tempo-máximo, o número de destinos e as informações sobre cada destino da raiz ou link.

</dd> <dt>

[_DFS_INFO_5 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
Contém informações sobre uma raiz Sistema de Arquivos Distribuído (DFS) ou link. Essa estrutura contém o nome, o status, **o GUID,** o tempo-máximo, as propriedades de namespace/raiz/link, o tamanho dos metadados e o número de destinos para a raiz ou link.

</dd> <dt>

[_DFS_INFO_6 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
Contém informações sobre uma raiz Sistema de Arquivos Distribuído (DFS) ou link. Essa estrutura contém o nome, status, **GUID**, tempo-out, propriedades de namespace/raiz/link, tamanho dos metadados, número de destinos e informações sobre cada destino da raiz ou link.

</dd> <dt>

[_DFS_INFO_7 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
Contém informações sobre um namespace do DFS. Essa estrutura contém o **GUID de** versão para os metadados do namespace.

</dd> <dt>

[_DFS_INFO_8 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
Contém o nome, status, **GUID,** tempo-final, sinalizadores de propriedade, tamanho dos metadados, informações de destino do DFS e descritor de segurança de ponto de nova análise de link para uma raiz ou link.

</dd> <dt>

[_DFS_INFO_9 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
Contém o nome, status, **GUID,** tempo-final, sinalizadores de propriedade, tamanho dos metadados, informações de destino do DFS, descritor de segurança do ponto de nova análise de link e uma lista de destinos do DFS para uma raiz ou link.

</dd> <dt>

[_DFS_INFO_50 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
Contém a versão de metadados do DFS e as funcionalidades de um namespace do DFS existente.

</dd> <dt>

[_DFS_INFO_100 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
Contém um comentário associado a uma raiz ou link Sistema de Arquivos Distribuído (DFS).

</dd> <dt>

[_DFS_INFO_101 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
Descreve o estado do armazenamento em uma raiz, link, destino raiz ou destino de link do DFS.

</dd> <dt>

[_DFS_INFO_102 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
Contém um valor de tempo-máximo a ser associado a uma raiz Sistema de Arquivos Distribuído (DFS) ou a um link em uma raiz nomeada do DFS.

</dd> <dt>

[_DFS_INFO_103 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
Contém propriedades que configuram comportamentos específicos para uma raiz ou link do DFS.

</dd> <dt>

[_DFS_INFO_104 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
Contém a prioridade de um destino raiz do DFS ou destino de link.

</dd> <dt>

[_DFS_INFO_105 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
Contém informações sobre uma raiz ou link do DFS, incluindo comportamentos de comentário, estado, tempo-de-saída e DFS especificados por sinalizadores de propriedade.

</dd> <dt>

[_DFS_INFO_106 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
Contém o estado de armazenamento e a prioridade para um destino raiz do DFS ou destino de link. Essa estrutura é apenas para uso com a [**função NetDfsSetInfo.**](netdfssetinfo.md)

</dd> <dt>

[_DFS_INFO_107 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
Contém informações sobre uma raiz ou link do DFS, incluindo o comentário, o estado, o tempo-de-tempo,os sinalizadores de propriedade e o descritor de segurança do ponto de nova reparse do link.

</dd> <dt>

[_DFS_INFO_150 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
Contém o descritor de segurança para o ponto de novapare de um link do DFS.

</dd> <dt>

[_DFS_INFO_200 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
Contém o nome de um namespace Sistema de Arquivos Distribuído (DFS) baseado em domínio.

</dd> <dt>

[_DFS_INFO_300 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
Contém o nome e o tipo (baseado em domínio ou autônomo) de um namespace do DFS.

</dd> <dt>

[_DFS_STORAGE_INFO estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
Contém informações sobre uma raiz do DFS ou um destino de link em um namespace do DFS ou do cache mantido pelo cliente DFS.

</dd> <dt>

[_DFS_STORAGE_INFO_1 estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
Contém informações sobre um destino DFS, incluindo o nome do servidor de destino e o nome do compartilhamento do DFS, bem como o estado e a prioridade do destino.

</dd> <dt>

[_DFS_SUPPORTED_NAMESPACE_VERSION_INFO estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
Contém informações de versão para um namespace do DFS.

</dd> <dt>

[_DFS_TARGET_PRIORITY estrutura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
Contém a classe de prioridade e a classificação de um destino específico do DFS.

</dd> </dl>
