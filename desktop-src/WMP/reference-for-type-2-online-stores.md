---
title: Referência para lojas online do tipo 2
description: Referência para lojas online do tipo 2
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Repositórios online do Windows Media Player, referência
- lojas online, referência
- tipo 2 lojas online, referência
- referência para lojas online do tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c164ad74481030a52cd31605b29833d3bfbd3f1d
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "103640321"
---
# <a name="reference-for-type-2-online-stores"></a><span data-ttu-id="efa59-107">Referência para lojas online do tipo 2</span><span class="sxs-lookup"><span data-stu-id="efa59-107">Reference for Type 2 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="efa59-108">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="efa59-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="efa59-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="efa59-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="efa59-110">O Windows Media Player 10 ou posterior fornece objetos, interfaces, propriedades e métodos que dão suporte às lojas online do tipo 2.</span><span class="sxs-lookup"><span data-stu-id="efa59-110">Windows Media Player 10 or later provides objects, interfaces, properties, and methods that support type 2 online stores.</span></span> <span data-ttu-id="efa59-111">As seções a seguir documentam esses detalhes.</span><span class="sxs-lookup"><span data-stu-id="efa59-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="efa59-112">Seção</span><span class="sxs-lookup"><span data-stu-id="efa59-112">Section</span></span>                                                                                                        | <span data-ttu-id="efa59-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="efa59-113">Description</span></span>                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efa59-114">Interface IWMPSubscriptionService</span><span class="sxs-lookup"><span data-stu-id="efa59-114">IWMPSubscriptionService Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)                                               | <span data-ttu-id="efa59-115">Fornece métodos para aumentar o DRM (gerenciamento de direitos digitais) e iniciar processos em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="efa59-115">Provides methods to augment digital rights management (DRM) and initiate background processes.</span></span>                                                                              |
| [<span data-ttu-id="efa59-116">Interface IWMPSubscriptionService2</span><span class="sxs-lookup"><span data-stu-id="efa59-116">IWMPSubscriptionService2 Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)                                             | <span data-ttu-id="efa59-117">Fornece métodos para iniciar processos em segundo plano, para fornecer informações sobre a atividade da loja online e para fornecer um ponteiro para a interface principal do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="efa59-117">Provides methods to initiate background processes, to provide information about online store activity, and to provide a pointer to the Windows Media Player core interface.</span></span> |
| [<span data-ttu-id="efa59-118">Interface IWMPSubscriptionServiceCallback</span><span class="sxs-lookup"><span data-stu-id="efa59-118">IWMPSubscriptionServiceCallback Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)                               | <span data-ttu-id="efa59-119">Define um método que as lojas online usam para notificar o Windows Media Player quando um processo em segundo plano é concluído.</span><span class="sxs-lookup"><span data-stu-id="efa59-119">Defines a method that online stores use to notify Windows Media Player when a background process is completed.</span></span>                                                              |
| [<span data-ttu-id="efa59-120">WMPNotifySubscriptionPluginAddRemove</span><span class="sxs-lookup"><span data-stu-id="efa59-120">WMPNotifySubscriptionPluginAddRemove</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove)                               | <span data-ttu-id="efa59-121">Uma função usada para notificar o Windows Media Player de que um plug-in foi instalado ou desinstalado.</span><span class="sxs-lookup"><span data-stu-id="efa59-121">A function used to notify Windows Media Player that a plug-in has been installed or uninstalled.</span></span>                                                                            |
| [<span data-ttu-id="efa59-122">Objeto downloadcollection</span><span class="sxs-lookup"><span data-stu-id="efa59-122">DownloadCollection Object</span></span>](downloadcollection-object.md)                                                     | <span data-ttu-id="efa59-123">Fornece métodos e propriedades para gerenciar coleções de itens de download.</span><span class="sxs-lookup"><span data-stu-id="efa59-123">Provides methods and properties to manage collections of download items.</span></span>                                                                                                    |
| [<span data-ttu-id="efa59-124">Objeto DownloadItem</span><span class="sxs-lookup"><span data-stu-id="efa59-124">DownloadItem Object</span></span>](downloaditem-object.md)                                                                 | <span data-ttu-id="efa59-125">Fornece métodos e propriedades relacionados a solicitações de download.</span><span class="sxs-lookup"><span data-stu-id="efa59-125">Provides methods and properties relating to download requests.</span></span>                                                                                                              |
| [<span data-ttu-id="efa59-126">Objeto DownloadManager</span><span class="sxs-lookup"><span data-stu-id="efa59-126">DownloadManager Object</span></span>](downloadmanager-object.md)                                                           | <span data-ttu-id="efa59-127">Fornece métodos para gerenciar coleções de download.</span><span class="sxs-lookup"><span data-stu-id="efa59-127">Provides methods to manage download collections.</span></span>                                                                                                                            |
| [<span data-ttu-id="efa59-128">Objeto externo para lojas online do tipo 2</span><span class="sxs-lookup"><span data-stu-id="efa59-128">External Object for Type 2 Online Stores</span></span>](external-object-for-type-2-online-stores.md)                       | <span data-ttu-id="efa59-129">Fornece propriedades, métodos e um evento acessível por meio de páginas da Web da loja online.</span><span class="sxs-lookup"><span data-stu-id="efa59-129">Provides properties, methods, and an event accessible from online store webpages.</span></span>                                                                                           |
| [<span data-ttu-id="efa59-130">Enumerações para lojas online do tipo 2</span><span class="sxs-lookup"><span data-stu-id="efa59-130">Enumerations for Type 2 Online Stores</span></span>](enumerations-for-type-2-online-stores.md)                             | <span data-ttu-id="efa59-131">Descreve as enumerações usadas por lojas online.</span><span class="sxs-lookup"><span data-stu-id="efa59-131">Describes enumerations used by online stores.</span></span>                                                                                                                               |
| [<span data-ttu-id="efa59-132">Convenção de trabalho BITS do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="efa59-132">Windows Media Player BITS Job Convention</span></span>](windows-media-player-bits-job-convention.md)                       | <span data-ttu-id="efa59-133">Descreve uma Convenção para usar o Serviço de Transferência Inteligente em Segundo Plano (BITS).</span><span class="sxs-lookup"><span data-stu-id="efa59-133">Describes a convention for using the Background Intelligent Transfer Service (BITS).</span></span>                                                                                        |
| [<span data-ttu-id="efa59-134">Chaves e entradas do registro para uma loja online tipo 2</span><span class="sxs-lookup"><span data-stu-id="efa59-134">Registry Keys and Entries for a Type 2 Online Store</span></span>](registry-keys-and-entries-for-a-type-2-online-store.md) | <span data-ttu-id="efa59-135">Descreve as entradas do registro que um repositório online deve criar no registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="efa59-135">Describes registry entries that an online store must create in the registry on the user's computer.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="efa59-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="efa59-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efa59-137">**Tipo 2 lojas online**</span><span class="sxs-lookup"><span data-stu-id="efa59-137">**Type 2 Online Stores**</span></span>](type-2-online-stores.md)
</dt> </dl>

 

 




