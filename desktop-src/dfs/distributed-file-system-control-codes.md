---
title: Sistema de Arquivos Distribuído de controle
description: Sistema de Arquivos Distribuído de controle do DFS
ms.assetid: 1d9bebe6-f494-41e5-8a8d-51bf98eaa374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d0a429bdb1e203d9b89f77e951d422cf3c0cef05cd5de5de39b537bb405f6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853526"
---
# <a name="distributed-file-system-control-codes"></a>Sistema de Arquivos Distribuído de controle

Veja a seguir os códigos de Sistema de Arquivos Distribuído de controle (DFS) :

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

O [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) de controle pode obter as mesmas informações que a função [**NetDfsGetClientInfo,**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) mas pode fornecer melhor desempenho em algumas configurações com altas latências para os servidores DFS. Não é recomendável usar o código de **FSCTL_DFS_GET_PKT_ENTRY_STATE,** a menos que haja problemas de desempenho.

Para executar essa operação, chame a [**função DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

</dd> </dl>