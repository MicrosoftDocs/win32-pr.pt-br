---
title: Catálogo de música
description: Catálogo de música
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Lojas online do Windows Media Player, catálogos de música
- lojas online, catálogos de música
- Digite 1 lojas online, catálogos de música
- Armazenamentos online do Windows Media Player, compilador de catálogo
- lojas online, compilador de catálogo
- tipo 1 lojas online, compilador de catálogo
- catálogos musicais
- compilador de catálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007082"
---
# <a name="music-catalog"></a><span data-ttu-id="57e80-111">Catálogo de música</span><span class="sxs-lookup"><span data-stu-id="57e80-111">Music Catalog</span></span>

<span data-ttu-id="57e80-112">Uma loja online tipo 1 cria seu catálogo de música como um conjunto de arquivos TSV (valores separados por tabulação).</span><span class="sxs-lookup"><span data-stu-id="57e80-112">A type 1 online store creates its music catalog as a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="57e80-113">Em seguida, a loja online usa o [compilador de catálogo](catalog-compiler-for-type-1-online-stores.md) da Microsoft para compilar os arquivos TSV em um catálogo compactado que pode ser baixado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="57e80-113">Then the online store uses Microsoft's [catalog compiler](catalog-compiler-for-type-1-online-stores.md) to compile the TSV files into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="57e80-114">O Windows Media Player pode baixar arquivos de catálogo completos ou arquivos de atualização de catálogo.</span><span class="sxs-lookup"><span data-stu-id="57e80-114">Windows Media Player can download full catalog files or catalog update files.</span></span> <span data-ttu-id="57e80-115">As atualizações do catálogo contêm apenas as informações do catálogo que foram alteradas desde a última atualização do catálogo.</span><span class="sxs-lookup"><span data-stu-id="57e80-115">Catalog updates contain only the catalog information that has changed since the last catalog update.</span></span> <span data-ttu-id="57e80-116">Cabe ao plug-in de parceiro de conteúdo determinar se um catálogo completo ou uma atualização deve ser baixado.</span><span class="sxs-lookup"><span data-stu-id="57e80-116">It is up to the content partner plug-in to determine whether to download a full catalog or an update.</span></span> <span data-ttu-id="57e80-117">Em ambos os casos, o Windows Media Player aplica as alterações ao catálogo atual após a notificação do plug-in.</span><span class="sxs-lookup"><span data-stu-id="57e80-117">In either case, Windows Media Player applies the changes to the current catalog upon notification from the plug-in.</span></span>

<span data-ttu-id="57e80-118">Se o repositório online tiver um novo catálogo preparado, o plug-in poderá notificar o Player chamando [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) e passando wmpcnNewCatalogAvailable como o valor para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="57e80-118">If the online store has a new catalog prepared, the plug-in can notify the Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) and passing wmpcnNewCatalogAvailable as the value for the *type* parameter.</span></span>

<span data-ttu-id="57e80-119">Quando o Windows Media Player estiver pronto para baixar um catálogo ou uma atualização, o jogador chamará [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="57e80-119">When Windows Media Player is ready to download a catalog or update, the Player calls [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> <span data-ttu-id="57e80-120">Esse método fornece o plug-in com informações sobre o catálogo atual, como a versão do catálogo e o identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="57e80-120">This method provides the plug-in with information about the current catalog, such as the catalog version and locale identifier.</span></span> <span data-ttu-id="57e80-121">O plug-in responde fornecendo o Uniform Resource Locator (URL) do catálogo completo ou da atualização correta, bem como um número de versão atualizado e uma data de validade.</span><span class="sxs-lookup"><span data-stu-id="57e80-121">The plug-in responds by supplying the uniform resource locator (URL) of the correct full catalog or update, as well as an updated version number and expiration date.</span></span> <span data-ttu-id="57e80-122">O Windows Media Player solicitará periodicamente atualizações de catálogo com base nas informações fornecidas pelo plug-in no **GetCatalogURL**.</span><span class="sxs-lookup"><span data-stu-id="57e80-122">Windows Media Player will periodically request catalog updates based upon the information provided by the plug-in in **GetCatalogURL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57e80-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57e80-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57e80-124">**Sobre o tipo 1 lojas online**</span><span class="sxs-lookup"><span data-stu-id="57e80-124">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="57e80-125">**Compilador de catálogo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="57e80-125">**Catalog Compiler for Type 1 Online Stores**</span></span>](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="57e80-126">**Interface IWMPContentPartner**</span><span class="sxs-lookup"><span data-stu-id="57e80-126">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




