---
title: Documento do serviceInfo para uma loja online tipo 2
description: Documento do serviceInfo para uma loja online tipo 2
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Repositórios online do Windows Media Player, documento do serviceInfo
- repositórios online, documento do serviceInfo
- tipo 2 lojas online, documento do serviceInfo
- Documento do serviceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb558661332ab08edd2057fa024a1a0e2034b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005663"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a><span data-ttu-id="8c942-107">Documento do serviceInfo para uma loja online tipo 2</span><span class="sxs-lookup"><span data-stu-id="8c942-107">ServiceInfo Document for a Type 2 Online Store</span></span>

<span data-ttu-id="8c942-108">O tipo 2 provedores de loja online devem fornecer à Microsoft a URL de um documento XML que descreve a loja online.</span><span class="sxs-lookup"><span data-stu-id="8c942-108">Type 2 online store providers must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="8c942-109">Windows Media Player 10 e Windows Media Player 11 Use este documento para determinar como configurar a interface do usuário para hospedar o repositório online.</span><span class="sxs-lookup"><span data-stu-id="8c942-109">Windows Media Player 10 and Windows Media Player 11 use this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="8c942-110">No Windows Media Player 10, o documento do serviceInfo fornece o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8c942-110">In Windows Media Player 10, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="8c942-111">Informações sobre como configurar os painéis de tarefas que o Windows Media Player exibe quando o repositório online está ativo.</span><span class="sxs-lookup"><span data-stu-id="8c942-111">Information about how to configure the task panes that Windows Media Player displays when the online store is active.</span></span> <span data-ttu-id="8c942-112">Um repositório online pode ter um, dois ou três painéis de tarefas.</span><span class="sxs-lookup"><span data-stu-id="8c942-112">An online store can have one, two, or three task panes.</span></span>
-   <span data-ttu-id="8c942-113">Informações usadas para configurar os botões do painel de tarefas, como o texto do botão, a cor do botão e as dicas de ferramenta para os botões.</span><span class="sxs-lookup"><span data-stu-id="8c942-113">Information used to configure the task pane buttons, such as the button text, the button color, and tool tips for the buttons.</span></span>
-   <span data-ttu-id="8c942-114">URLs para imagens que o Windows Media Player exibe para identificar a loja online.</span><span class="sxs-lookup"><span data-stu-id="8c942-114">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="8c942-115">URLs de páginas da Web, fornecidas pela loja online, que o Windows Media Player hospeda em sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8c942-115">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="8c942-116">Informações sobre como a instalação do Windows Media Player deve configurar o primeiro armazenamento online que o usuário vê.</span><span class="sxs-lookup"><span data-stu-id="8c942-116">Information about how Windows Media Player setup should configure the first online store the user sees.</span></span>

<span data-ttu-id="8c942-117">No Windows Media Player 11, o documento do serviceInfo fornece o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8c942-117">In Windows Media Player 11, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="8c942-118">Informações usadas para configurar o botão para lojas online guia, como o texto do botão e a dica de ferramenta para o botão.</span><span class="sxs-lookup"><span data-stu-id="8c942-118">Information used to configure the button for Online Stores tab, such as the button text and the tool tip for the button.</span></span>
-   <span data-ttu-id="8c942-119">URLs para imagens que o Windows Media Player exibe para identificar a loja online.</span><span class="sxs-lookup"><span data-stu-id="8c942-119">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="8c942-120">URLs de páginas da Web, fornecidas pela loja online, que o Windows Media Player hospeda em sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8c942-120">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>

<span data-ttu-id="8c942-121">Ao começar a desenvolver sua loja online, você deve fornecer à Microsoft a URL para seu documento do serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="8c942-121">When you start developing your online store, you must provide Microsoft with the URL to your ServiceInfo document.</span></span> <span data-ttu-id="8c942-122">Durante a fase de desenvolvimento, sua loja online aparecerá no Windows Media Player somente quando uma chave de registro especial for definida.</span><span class="sxs-lookup"><span data-stu-id="8c942-122">During the development phase, your online store will appear in Windows Media Player only when a special registry key is set.</span></span>

<span data-ttu-id="8c942-123">Depois que a loja online é publicada, o cenário ususal é que o Windows Media Player recupera o documento do seu serviceInfo da Web automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8c942-123">After your online store is published, the ususal scenario is that Windows Media Player retrieves your ServiceInfo document from the Web automatically.</span></span> <span data-ttu-id="8c942-124">Em alguns casos, no entanto, o Windows Media Player recupera o documento de informações do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="8c942-124">In some cases, however, Windows Media Player retrieves the ServiceInfo document from the user's computer.</span></span> <span data-ttu-id="8c942-125">Para obter mais informações, consulte [definindo a loja online inicial](setting-the-initial-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="8c942-125">For more information, see [Setting the Initial Online Store](setting-the-initial-online-store.md).</span></span>

<span data-ttu-id="8c942-126">Quando o Windows Media Player recupera o documento de informações da Web, ele anexa uma cadeia de caracteres de consulta à URL.</span><span class="sxs-lookup"><span data-stu-id="8c942-126">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="8c942-127">A cadeia de caracteres de consulta contém parâmetros que fornecem informações sobre a localidade do usuário e a versão do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8c942-127">The query string contains parameters that provide information about the user's locale and the Windows Media Player version.</span></span>

<span data-ttu-id="8c942-128">Você pode criar documentos de informações estáticas ou dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="8c942-128">You can create static or dynamic ServiceInfo documents.</span></span> <span data-ttu-id="8c942-129">Um documento do serviceInfo estático tem uma extensão de nome de arquivo. xml.</span><span class="sxs-lookup"><span data-stu-id="8c942-129">A static ServiceInfo document has an .xml file name extension.</span></span> <span data-ttu-id="8c942-130">Um documento de informações dinâmicas é uma página ASP e tem uma extensão de nome de arquivo. asp ou. aspx.</span><span class="sxs-lookup"><span data-stu-id="8c942-130">A dynamic ServiceInfo document is an ASP page and has an .asp or .aspx file name extension.</span></span>

<span data-ttu-id="8c942-131">Nem todos os elementos disponíveis para uso no documento do serviceInfo podem ser usados por cada loja online e alguns elementos são opcionais para todas as lojas online.</span><span class="sxs-lookup"><span data-stu-id="8c942-131">Not all the elements available for use in the ServiceInfo document can be used by every online store, and some elements are optional for all online stores.</span></span> <span data-ttu-id="8c942-132">Para obter informações sobre os tipos de lojas online que você pode criar e os recursos disponíveis para cada tipo, consulte [lojas online do Windows Media Player](windows-media-player-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="8c942-132">For information about the types of online stores you can create and the features available for each type, see [Windows Media Player Online Stores](windows-media-player-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c942-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c942-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c942-134">**Sobre as lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="8c942-134">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8c942-135">**Criando o documento do serviceInfo dinamicamente**</span><span class="sxs-lookup"><span data-stu-id="8c942-135">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="8c942-136">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="8c942-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="8c942-137">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="8c942-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




