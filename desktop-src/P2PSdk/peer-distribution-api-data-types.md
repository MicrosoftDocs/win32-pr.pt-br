---
description: A API de distribuição de pares define os seguintes tipos de dados.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Tipos de dados da API de distribuição de pares (PeerDist. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753245"
---
# <a name="peer-distribution-api-data-types"></a><span data-ttu-id="a741c-103">Tipos de dados da API de distribuição de pares</span><span class="sxs-lookup"><span data-stu-id="a741c-103">Peer Distribution API Data Types</span></span>

<span data-ttu-id="a741c-104">A API de distribuição de pares define os seguintes tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="a741c-104">The Peer Distribution API defines the following data types.</span></span>


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| <span data-ttu-id="a741c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a741c-105">Data type</span></span>                                                                                                                     | <span data-ttu-id="a741c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a741c-106">Description</span></span>                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a741c-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**\_identificador de instância PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="a741c-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**PEERDIST\_INSTANCE\_HANDLE**</span></span>          | <span data-ttu-id="a741c-108">Um identificador associado à instância de distribuição de pares.</span><span class="sxs-lookup"><span data-stu-id="a741c-108">A handle associated with the Peer Distribution instance.</span></span> <span data-ttu-id="a741c-109">Esse identificador é criado por [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)e usado na maioria das operações de distribuição de pares.</span><span class="sxs-lookup"><span data-stu-id="a741c-109">This handle is created by [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup), and used in most Peer Distribution operations.</span></span><br/>                                          |
| <span data-ttu-id="a741c-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**\_identificador de conteúdo PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="a741c-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**PEERDIST\_CONTENT\_HANDLE**</span></span>             | <span data-ttu-id="a741c-111">Um identificador associado ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a741c-111">A handle associated with content.</span></span> <span data-ttu-id="a741c-112">Esse identificador é criado por [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) e é referenciado ao abrir, fechar, adicionar ou publicar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a741c-112">This handle is created by [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) and is referenced when opening, closing, adding, or publishing content.</span></span><br/>                     |
| <span data-ttu-id="a741c-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**\_identificador CONTENTINFO \_ PEERDIST**</span><span class="sxs-lookup"><span data-stu-id="a741c-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**PEERDIST\_CONTENTINFO\_HANDLE**</span></span> | <span data-ttu-id="a741c-114">Um identificador associado às informações de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a741c-114">A handle associated with content information.</span></span> <span data-ttu-id="a741c-115">Esse identificador é criado por [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)e é usado ao recuperar informações de conteúdo codificado.</span><span class="sxs-lookup"><span data-stu-id="a741c-115">This handle is created by [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation), and is used when retrieving encoded content information.</span></span><br/> |
| <span data-ttu-id="a741c-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**\_identificador de fluxo PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="a741c-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**PEERDIST\_STREAM\_HANDLE**</span></span>                | <span data-ttu-id="a741c-117">Um identificador associado a um fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="a741c-117">A handle associated with a data stream.</span></span> <span data-ttu-id="a741c-118">Esse identificador é criado por [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) e é referenciado durante a publicação, o fechamento ou a adição ao conteúdo transmitido.</span><span class="sxs-lookup"><span data-stu-id="a741c-118">This handle is created by [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) and is referenced when publishing, closing, or adding to streamed content.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="a741c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a741c-119">Requirements</span></span>



| <span data-ttu-id="a741c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a741c-120">Requirement</span></span> | <span data-ttu-id="a741c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a741c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a741c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a741c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a741c-123">\[Somente aplicativos da área de trabalho do Windows 7 Professional\]</span><span class="sxs-lookup"><span data-stu-id="a741c-123">Windows 7 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a741c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a741c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a741c-125">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="a741c-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a741c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a741c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a741c-127"><dt>PeerDist. h</dt></span><span class="sxs-lookup"><span data-stu-id="a741c-127"><dt>Peerdist.h</dt></span></span> </dl> |



 

 




