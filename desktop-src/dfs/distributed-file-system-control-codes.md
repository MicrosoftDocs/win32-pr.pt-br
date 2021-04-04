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
# <a name="distributed-file-system-control-codes"></a><span data-ttu-id="bebfc-103">Sistema de Arquivos Distribuído códigos de controle</span><span class="sxs-lookup"><span data-stu-id="bebfc-103">Distributed File System Control Codes</span></span>

<span data-ttu-id="bebfc-104">A seguir estão os códigos de controle de Sistema de Arquivos Distribuído (DFS):</span><span class="sxs-lookup"><span data-stu-id="bebfc-104">The following are the Distributed File System (DFS) control codes:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bebfc-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="bebfc-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="bebfc-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span><span class="sxs-lookup"><span data-stu-id="bebfc-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span></span>](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

<span data-ttu-id="bebfc-107">O código de controle de [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) pode obter as mesmas informações que a função [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , mas pode fornecer melhor desempenho em algumas configurações com latências altas para os servidores DFS.</span><span class="sxs-lookup"><span data-stu-id="bebfc-107">The [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="bebfc-108">Não é recomendável usar o código de controle de **FSCTL_DFS_GET_PKT_ENTRY_STATE** , a menos que haja problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="bebfc-108">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="bebfc-109">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="bebfc-109">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span>

</dd> </dl>