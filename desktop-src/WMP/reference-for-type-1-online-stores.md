---
title: Referência para lojas online do tipo 1
description: Referência para lojas online do tipo 1
ms.assetid: e6f45a50-029e-4347-9b25-10e9e32a56eb
keywords:
- Repositórios online do Windows Media Player, referência
- lojas online, referência
- tipo 1 lojas online, referência
- referência para repositórios online do tipo 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475f7dee43f2f6152c3b3ebd0e6090a1efb33a72
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104365746"
---
# <a name="reference-for-type-1-online-stores"></a><span data-ttu-id="47e21-107">Referência para lojas online do tipo 1</span><span class="sxs-lookup"><span data-stu-id="47e21-107">Reference for Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="47e21-108">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="47e21-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="47e21-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="47e21-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="47e21-110">O Windows Media Player 11 fornece um compilador de catálogo, um objeto e várias interfaces que dão suporte a lojas online do tipo 1.</span><span class="sxs-lookup"><span data-stu-id="47e21-110">Windows Media Player 11 provides a catalog compiler, an object, and several interfaces that support type 1 online stores.</span></span> <span data-ttu-id="47e21-111">As seções a seguir documentam esses detalhes.</span><span class="sxs-lookup"><span data-stu-id="47e21-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="47e21-112">Seção</span><span class="sxs-lookup"><span data-stu-id="47e21-112">Section</span></span>                                                                                    | <span data-ttu-id="47e21-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="47e21-113">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47e21-114">Compilador de catálogo para repositórios online do tipo 1</span><span class="sxs-lookup"><span data-stu-id="47e21-114">Catalog Compiler for Type 1 Online Stores</span></span>](catalog-compiler-for-type-1-online-stores.md) | <span data-ttu-id="47e21-115">Fornece material de referência para o compilador que uma loja online usa para compilar seu catálogo de música.</span><span class="sxs-lookup"><span data-stu-id="47e21-115">Provides reference material for the compiler that an online store uses to compile its music catalog.</span></span>                                                                                                                               |
| [<span data-ttu-id="47e21-116">Interface IWMPContentContainer</span><span class="sxs-lookup"><span data-stu-id="47e21-116">IWMPContentContainer Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)                                 | <span data-ttu-id="47e21-117">Fornece páginas de referência para métodos que o plug-in do repositório online chama para inspecionar um contêiner de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="47e21-117">Provides reference pages for methods that the online store's plug-in calls to inspect a content container.</span></span> <span data-ttu-id="47e21-118">Um contêiner de conteúdo representa um conjunto de itens de mídia a serem baixados ou comprados.</span><span class="sxs-lookup"><span data-stu-id="47e21-118">A content container represents a set of media items to be downloaded or purchased.</span></span> <span data-ttu-id="47e21-119">Implementado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="47e21-119">Implemented by Windows Media Player.</span></span> |
| [<span data-ttu-id="47e21-120">Interface IWMPContentContainerList</span><span class="sxs-lookup"><span data-stu-id="47e21-120">IWMPContentContainerList Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)                         | <span data-ttu-id="47e21-121">Fornece páginas de referência para métodos que o plug-in do repositório online chama para inspecionar uma lista de contêineres de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="47e21-121">Provides reference pages for methods that the online store's plug-in calls to inspect a list of content containers.</span></span> <span data-ttu-id="47e21-122">Implementado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="47e21-122">Implemented by Windows Media Player.</span></span>                                                                           |
| [<span data-ttu-id="47e21-123">Interface IWMPContentPartner</span><span class="sxs-lookup"><span data-stu-id="47e21-123">IWMPContentPartner Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)                                     | <span data-ttu-id="47e21-124">Fornece páginas de referência para métodos que o Windows Media Player chama para obter informações da loja online e notificar a loja online sobre as ações do usuário.</span><span class="sxs-lookup"><span data-stu-id="47e21-124">Provides reference pages for methods that Windows Media Player calls to get information from the online store and to notify the online store about the user's actions.</span></span> <span data-ttu-id="47e21-125">Implementado pelo plug-in da loja online.</span><span class="sxs-lookup"><span data-stu-id="47e21-125">Implemented by the online store's plug-in.</span></span>                  |
| [<span data-ttu-id="47e21-126">Interface IWMPContentPartnerCallback</span><span class="sxs-lookup"><span data-stu-id="47e21-126">IWMPContentPartnerCallback Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)                     | <span data-ttu-id="47e21-127">Fornece páginas de referência para métodos que o plug-in do repositório online chama para notificar o Windows Media Player sobre a conclusão de operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="47e21-127">Provides reference pages for methods that the online store's plug-in calls to notify Windows Media Player about the completion of asynchronous operations.</span></span> <span data-ttu-id="47e21-128">Implementado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="47e21-128">Implemented by Windows Media Player.</span></span>                                    |
| [<span data-ttu-id="47e21-129">Objeto externo para repositórios online do tipo 1</span><span class="sxs-lookup"><span data-stu-id="47e21-129">External Object for Type 1 Online Stores</span></span>](external-object-for-type-1-online-stores.md)   | <span data-ttu-id="47e21-130">Fornece páginas de referência para propriedades, métodos e eventos usados pelo script em páginas da Web fornecidas pela loja online.</span><span class="sxs-lookup"><span data-stu-id="47e21-130">Provides reference pages for properties, methods, and events used by script in webpages provided by the online store.</span></span>                                                                                                              |
| [<span data-ttu-id="47e21-131">Enumerações para repositórios online do tipo 1</span><span class="sxs-lookup"><span data-stu-id="47e21-131">Enumerations for Type 1 Online Stores</span></span>](enumerations-for-type-1-online-stores.md)         | <span data-ttu-id="47e21-132">Fornece páginas de referência para as enumerações usadas na comunicação entre o Windows Media Player e o plug-in do loja online.</span><span class="sxs-lookup"><span data-stu-id="47e21-132">Provides reference pages for the enumerations used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                               |
| [<span data-ttu-id="47e21-133">Estruturas para lojas online do tipo 1</span><span class="sxs-lookup"><span data-stu-id="47e21-133">Structures for Type 1 Online Stores</span></span>](structures-for-type-1-online-stores.md)             | <span data-ttu-id="47e21-134">Fornece páginas de referência para as estruturas usadas na comunicação entre o Windows Media Player e o plug-in do loja online.</span><span class="sxs-lookup"><span data-stu-id="47e21-134">Provides reference pages for the structures used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="47e21-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47e21-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47e21-136">**Tipos 1 lojas online**</span><span class="sxs-lookup"><span data-stu-id="47e21-136">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




