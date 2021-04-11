---
title: Guia de programação para lojas online do tipo 1
description: Guia de programação para lojas online do tipo 1
ms.assetid: 6950cab8-4355-4699-8245-f2817c3e25fc
keywords:
- Lojas online do Windows Media Player, guia de programação
- lojas online, guia de programação
- Digite 1 lojas online, guia de programação
- Guia de programação, digite 1 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea04cb188a68c85173b5b1682235b6964840d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160223"
---
# <a name="programming-guide-for-type-1-online-stores"></a><span data-ttu-id="4faab-107">Guia de programação para lojas online do tipo 1</span><span class="sxs-lookup"><span data-stu-id="4faab-107">Programming Guide for Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="4faab-108">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="4faab-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4faab-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="4faab-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4faab-110">Esta seção contém os tópicos a seguir para ajudá-lo a criar uma loja online tipo 1.</span><span class="sxs-lookup"><span data-stu-id="4faab-110">This section contains the following topics to help you create a type 1 online store.</span></span>



| <span data-ttu-id="4faab-111">Seção</span><span class="sxs-lookup"><span data-stu-id="4faab-111">Section</span></span>                                                                                                              | <span data-ttu-id="4faab-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4faab-112">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4faab-113">Documento de informações de exemplo para uma loja online tipo 1</span><span class="sxs-lookup"><span data-stu-id="4faab-113">Example ServiceInfo Document for a Type 1 Online Store</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md) | <span data-ttu-id="4faab-114">Mostra um documento de informações de exemplo que você pode usar como um ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="4faab-114">Shows an example ServiceInfo document that you can use as a starting point.</span></span>                                                                    |
| [<span data-ttu-id="4faab-115">Criando o plug-in para uma loja online tipo 1</span><span class="sxs-lookup"><span data-stu-id="4faab-115">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)                 | <span data-ttu-id="4faab-116">Explica como criar o plug-in necessário para uma loja online tipo 1.</span><span class="sxs-lookup"><span data-stu-id="4faab-116">Explains how to build the required plug-in for a type 1 online store.</span></span>                                                                          |
| [<span data-ttu-id="4faab-117">Exibindo caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="4faab-117">Displaying Dialog Boxes</span></span>](displaying-dialog-boxes.md)                                                               | <span data-ttu-id="4faab-118">Explica como invocar caixas de diálogo por meio do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4faab-118">Explains how to invoke dialog boxes through Windows Media Player.</span></span>                                                                              |
| [<span data-ttu-id="4faab-119">Gerenciando o logon</span><span class="sxs-lookup"><span data-stu-id="4faab-119">Managing Login</span></span>](managing-login.md)                                                                                 | <span data-ttu-id="4faab-120">Explica como interagir com os elementos da interface do usuário do Windows Media Player que permitem que os usuários façam logon no e façam logoff da loja online.</span><span class="sxs-lookup"><span data-stu-id="4faab-120">Explains how to interact with Windows Media Player user interface elements that let users log in to and log out from the online store.</span></span>         |
| [<span data-ttu-id="4faab-121">Comprando conteúdo de mídia</span><span class="sxs-lookup"><span data-stu-id="4faab-121">Purchasing Media Content</span></span>](purchasing-media-content.md)                                                             | <span data-ttu-id="4faab-122">Explica como o Windows Media Player e o plug-in da loja online interagem quando o usuário adquire conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="4faab-122">Explains how Windows Media Player and the online store's plug-in interact when the user purchases media content.</span></span>                               |
| [<span data-ttu-id="4faab-123">Baixando conteúdo de mídia</span><span class="sxs-lookup"><span data-stu-id="4faab-123">Downloading Media Content</span></span>](downloading-media-content.md)                                                           | <span data-ttu-id="4faab-124">Explica como o Windows Media Player e o plug-in da loja online interagem quando o usuário baixa o conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="4faab-124">Explains how Windows Media Player and the online store's plug-in interact when the user downloads media content.</span></span>                               |
| [<span data-ttu-id="4faab-125">Atualizando licenças</span><span class="sxs-lookup"><span data-stu-id="4faab-125">Updating Licenses</span></span>](updating-licenses.md)                                                                           | <span data-ttu-id="4faab-126">Explica como o Windows Media Player e o plug-in da loja online interagem para manter as licenças de mídia do usuário atualizadas.</span><span class="sxs-lookup"><span data-stu-id="4faab-126">Explains how Windows Media Player and the online store's plug-in interact to keep the user's media licenses current.</span></span>                           |
| [<span data-ttu-id="4faab-127">Atualizando dispositivos portáteis</span><span class="sxs-lookup"><span data-stu-id="4faab-127">Updating Portable Devices</span></span>](updating-portable-devices.md)                                                           | <span data-ttu-id="4faab-128">Explica como o Windows Media Player e o plug-in da loja online interagem quando o conteúdo da mídia se move entre o computador e um dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="4faab-128">Explains how Windows Media Player and the online store's plug-in interact when media content moves between the computer and a portable device.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4faab-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4faab-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4faab-130">**Tipos 1 lojas online**</span><span class="sxs-lookup"><span data-stu-id="4faab-130">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




