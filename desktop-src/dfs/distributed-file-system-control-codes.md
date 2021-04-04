---
title: Sistema de Arquivos Distribuído códigos de controle
description: Sistema de Arquivos Distribuído códigos de controle do DFS
ms.assetid: 1d9bebe6-f494-41e5-8a8d-51bf98eaa374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe054f87210c40da595dd731b263c485311729a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917434"
---
# <a name="distributed-file-system-control-codes"></a>Sistema de Arquivos Distribuído códigos de controle

A seguir estão os códigos de controle de Sistema de Arquivos Distribuído (DFS):

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

O código de controle de [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) pode obter as mesmas informações que a função [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , mas pode fornecer melhor desempenho em algumas configurações com latências altas para os servidores DFS. Não é recomendável usar o código de controle de **FSCTL_DFS_GET_PKT_ENTRY_STATE** , a menos que haja problemas de desempenho.

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

</dd> </dl>