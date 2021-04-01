---
title: Documento do serviceInfo para uma loja online tipo 1
description: Documento do serviceInfo para uma loja online tipo 1
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Repositórios online do Windows Media Player, documento do serviceInfo
- repositórios online, documento do serviceInfo
- Digite 1 lojas online, documento do serviceInfo
- Documento do serviceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ce17cf2494a84193116fc340f843934b6f073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005665"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a><span data-ttu-id="607c1-107">Documento do serviceInfo para uma loja online tipo 1</span><span class="sxs-lookup"><span data-stu-id="607c1-107">ServiceInfo Document for a Type 1 Online Store</span></span>

<span data-ttu-id="607c1-108">As lojas online do tipo 1 devem fornecer à Microsoft a URL de um documento XML que descreve a loja online.</span><span class="sxs-lookup"><span data-stu-id="607c1-108">Type 1 online stores must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="607c1-109">O Windows Media Player 11 usa este documento para determinar como configurar a interface do usuário para hospedar o repositório online.</span><span class="sxs-lookup"><span data-stu-id="607c1-109">Windows Media Player 11 uses this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="607c1-110">O documento do serviceInfo para um repositório do tipo 1 fornece as seguintes informações para o Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="607c1-110">The ServiceInfo document for a type 1 store provides the following information to Windows Media Player:</span></span>

-   <span data-ttu-id="607c1-111">Informações usadas para configurar o botão **lojas online** (também chamado de guia), como o texto do botão, a cor do botão e a dica de ferramenta do botão.</span><span class="sxs-lookup"><span data-stu-id="607c1-111">Information used to configure the **Online Stores** button (also called a tab), such as the button text, the button color, and the tooltip for the button.</span></span>
-   <span data-ttu-id="607c1-112">URLs para imagens que o Windows Media Player exibe para identificar a loja online.</span><span class="sxs-lookup"><span data-stu-id="607c1-112">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="607c1-113">URLs de páginas da Web, fornecidas pela loja online, que o Windows Media Player hospeda em sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="607c1-113">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="607c1-114">URL em que o Windows Media Player pode recuperar o plug-in do repositório online para que o plug-in possa ser instalado no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="607c1-114">URL where Windows Media Player can retrieve the online store's plug-in so that the plug-in can be installed on the user's computer.</span></span>

<span data-ttu-id="607c1-115">Quando o Windows Media Player recupera o documento de informações da Web, ele anexa uma cadeia de caracteres de consulta à URL.</span><span class="sxs-lookup"><span data-stu-id="607c1-115">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="607c1-116">A cadeia de caracteres de consulta contém parâmetros que fornecem informações sobre a localidade e a localização geográfica do usuário e a versão do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="607c1-116">The query string contains parameters that provide information about the user's locale and geographic location and the version of Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="607c1-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="607c1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="607c1-118">**Sobre o tipo 1 lojas online**</span><span class="sxs-lookup"><span data-stu-id="607c1-118">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="607c1-119">**Criando o documento do serviceInfo dinamicamente**</span><span class="sxs-lookup"><span data-stu-id="607c1-119">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="607c1-120">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="607c1-120">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="607c1-121">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="607c1-121">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




