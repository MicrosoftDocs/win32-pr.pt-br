---
title: Co-Branding lojas online
description: Co-Branding lojas online
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Lojas online do Windows Media Player, co-marca
- lojas online, co-marca
- Digite 1 lojas online, co-marca
- Digite 2 lojas online, co-marca
- lojas online de co-identidade visual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788183"
---
# <a name="co-branding-online-stores"></a><span data-ttu-id="7312e-108">Co-Branding lojas online</span><span class="sxs-lookup"><span data-stu-id="7312e-108">Co-Branding Online Stores</span></span>

<span data-ttu-id="7312e-109">Os OEMs de computadores pessoais que não operam uma loja de música podem comarcações com provedores de loja online.</span><span class="sxs-lookup"><span data-stu-id="7312e-109">Personal computer OEMs who do not operate a music store can co-brand with online store providers.</span></span> <span data-ttu-id="7312e-110">A instalação do Windows Media Player dá suporte ao parâmetro de linha de comando do netextra para permitir que os OEMs de hardware definam um atributo personalizado que pode ser usado pela loja online para identificar qual OEM instalou o armazenamento online inicial.</span><span class="sxs-lookup"><span data-stu-id="7312e-110">Windows Media Player setup supports the ServiceExtra command line parameter to enable hardware OEMs to set a custom attribute that the online store can use to identify which OEM installed the initial online store.</span></span>

<span data-ttu-id="7312e-111">Por exemplo, se um criador de computadores chamado Fabrikam quiser definir a loja online inicial para a loja de músicas da Proseware, ele poderá usar a seguinte linha de comando para instalar o Windows Media Player 10:</span><span class="sxs-lookup"><span data-stu-id="7312e-111">For example, if a computer maker named Fabrikam wants to set the initial online store to the Proseware music store, it might use the following command line to install Windows Media Player 10:</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



<span data-ttu-id="7312e-112">Quando o Windows Media Player é instalado dessa maneira, o Player acrescenta a cadeia de caracteres de todos os minutos sempre que abre o serviço de Proseware.</span><span class="sxs-lookup"><span data-stu-id="7312e-112">When Windows Media Player is installed in this manner, the Player appends the ServiceExtra string each time it opens the Proseware service.</span></span> <span data-ttu-id="7312e-113">O exemplo a seguir mostra a URL que o Windows Media Player enviaria ao serviço de Proseware para recuperar o documento do ServiceInfo:</span><span class="sxs-lookup"><span data-stu-id="7312e-113">The following example shows the URL that Windows Media Player would send to the Proseware service to retrieve the ServiceInfo document:</span></span>


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



<span data-ttu-id="7312e-114">A loja online da Proseware pode usar a cadeia de caracteres de consulta para determinar qual OEM instalou o Windows Media Player e retornar um documento do serviceInfo gerado dinamicamente que aponta para a versão de marca da loja online.</span><span class="sxs-lookup"><span data-stu-id="7312e-114">The Proseware online store can then use the query string to determine which OEM installed Windows Media Player and return a dynamically generated ServiceInfo document that points to the co-branded version of the online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7312e-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7312e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7312e-116">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="7312e-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="7312e-117">**Parâmetros de linha de comando de instalação para lojas online**</span><span class="sxs-lookup"><span data-stu-id="7312e-117">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




