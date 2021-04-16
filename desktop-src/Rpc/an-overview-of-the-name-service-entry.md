---
title: Uma visão geral da entrada de serviço de nome
description: A entrada de serviço de nome consiste em três seções distintas.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105758724"
---
# <a name="an-overview-of-the-name-service-entry"></a><span data-ttu-id="22d1b-103">Uma visão geral da entrada de serviço de nome</span><span class="sxs-lookup"><span data-stu-id="22d1b-103">An Overview of the Name Service Entry</span></span>

<span data-ttu-id="22d1b-104">A entrada de serviço de nome consiste em três seções distintas.</span><span class="sxs-lookup"><span data-stu-id="22d1b-104">The name service entry consists of three distinct sections.</span></span> <span data-ttu-id="22d1b-105">A primeira seção é para interfaces (UUID + Version), a segunda seção contém os UUIDs de objeto e a terceira seção é para identificadores de associação.</span><span class="sxs-lookup"><span data-stu-id="22d1b-105">The first section is for interfaces (UUID + version), the second section contains the object UUIDs, and the third section is for binding handles.</span></span> <span data-ttu-id="22d1b-106">Você fornece um nome para a entrada que servirá como uma maneira de identificá-lo.</span><span class="sxs-lookup"><span data-stu-id="22d1b-106">You provide a name for the entry that will serve as a way to identify it.</span></span>

<span data-ttu-id="22d1b-107">Ao chamar [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), o servidor especifica o nome da entrada na qual as informações exportadas são colocadas.</span><span class="sxs-lookup"><span data-stu-id="22d1b-107">When calling [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), the server specifies the name of the entry in which to place the exported information.</span></span> <span data-ttu-id="22d1b-108">Essa interface recentemente exportada é adicionada à seção interface da entrada serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="22d1b-108">This newly exported interface is then added to the interface section of the name service entry.</span></span> <span data-ttu-id="22d1b-109">Todas as interfaces que já estão presentes na entrada de serviço de nome permanecem também.</span><span class="sxs-lookup"><span data-stu-id="22d1b-109">Any interfaces that are already present in the name service entry remain as well.</span></span> <span data-ttu-id="22d1b-110">Esse mesmo processo é seguido para UUIDs de objeto e identificadores de associação.</span><span class="sxs-lookup"><span data-stu-id="22d1b-110">This same process is followed for object UUIDs and binding handles.</span></span>

<span data-ttu-id="22d1b-111">O cliente chama [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (ou [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) para pesquisar um identificador de associação apropriado.</span><span class="sxs-lookup"><span data-stu-id="22d1b-111">The client calls [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (or [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) to search for an appropriate binding handle.</span></span> <span data-ttu-id="22d1b-112">O nome da entrada, o identificador de interface e um UUID de objeto são extraídos.</span><span class="sxs-lookup"><span data-stu-id="22d1b-112">The entry name, interface handle, and an object UUID are extracted.</span></span> <span data-ttu-id="22d1b-113">Elas restringem as entradas das quais os identificadores de associação são retornados.</span><span class="sxs-lookup"><span data-stu-id="22d1b-113">These restrict the entries from which binding handles are returned.</span></span> <span data-ttu-id="22d1b-114">Se uma entrada corresponder aos critérios de pesquisa, todos os identificadores de associação nessa entrada serão retornados de [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span><span class="sxs-lookup"><span data-stu-id="22d1b-114">If an entry matches the search criteria, all the binding handles in that entry are returned from [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span>

 

 




