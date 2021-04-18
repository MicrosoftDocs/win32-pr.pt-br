---
description: As seguintes funções administrativas permitem que um provedor de rede adote uma ação específica da rede para exibir e manipular diretórios específicos da rede, em outras palavras, diretórios mapeados para protocolos não Windows.
ms.assetid: df2f1bd6-5257-46e4-a4d4-ad2f5c0a1517
title: Funções administrativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83cb5b7c515fe8e22dc5542a4d29e54e8b01329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749972"
---
# <a name="administrative-functions"></a><span data-ttu-id="2e914-103">Funções administrativas</span><span class="sxs-lookup"><span data-stu-id="2e914-103">Administrative Functions</span></span>

<span data-ttu-id="2e914-104">As seguintes funções administrativas permitem que um provedor de rede adote uma ação específica da rede para exibir e manipular diretórios específicos da rede, em outras palavras, diretórios mapeados para protocolos não Windows.</span><span class="sxs-lookup"><span data-stu-id="2e914-104">The following administrative functions enable a network provider to take network-specific action to display and manipulate network-specific directories, in other words, directories mapped to non-Windows protocols.</span></span>



| <span data-ttu-id="2e914-105">Função</span><span class="sxs-lookup"><span data-stu-id="2e914-105">Function</span></span>                                         | <span data-ttu-id="2e914-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e914-106">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e914-107">**NPGetDirectoryType**</span><span class="sxs-lookup"><span data-stu-id="2e914-107">**NPGetDirectoryType**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) | <span data-ttu-id="2e914-108">Chamado pelo Gerenciador de arquivos para determinar o tipo de um diretório de rede.</span><span class="sxs-lookup"><span data-stu-id="2e914-108">Called by File Manager to determine the type of a network directory.</span></span>                                                                                          |
| [<span data-ttu-id="2e914-109">**NPDirectoryNotify**</span><span class="sxs-lookup"><span data-stu-id="2e914-109">**NPDirectoryNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npdirectorynotify)   | <span data-ttu-id="2e914-110">Chamado pelo Gerenciador de arquivos para notificar o provedor de rede sobre operações de diretório.</span><span class="sxs-lookup"><span data-stu-id="2e914-110">Called by File Manager to notify the network provider of directory operations.</span></span> <span data-ttu-id="2e914-111">Essa função pode ser usada para executar um comportamento especial para determinados diretórios.</span><span class="sxs-lookup"><span data-stu-id="2e914-111">This function can be used to perform special behavior for certain directories.</span></span> |



 

 

 



