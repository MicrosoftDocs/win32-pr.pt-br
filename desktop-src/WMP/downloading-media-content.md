---
title: Baixando conteúdo de mídia
description: Baixando conteúdo de mídia
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Armazenamentos online do Windows Media Player, baixando conteúdo de mídia
- lojas online, baixando conteúdo de mídia
- Digite 1 lojas online, baixando conteúdo de mídia
- Lojas online do Windows Media Player, download de conteúdo de mídia
- lojas online, download de conteúdo de mídia
- tipos 1 lojas online, download de conteúdo de mídia
- conteúdo de mídia, baixando
- baixando conteúdo de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00efe44f2bac25a9eeda86f6adcc78b34beea7cd
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104365739"
---
# <a name="downloading-media-content"></a><span data-ttu-id="f1606-111">Baixando conteúdo de mídia</span><span class="sxs-lookup"><span data-stu-id="f1606-111">Downloading Media Content</span></span>

<span data-ttu-id="f1606-112">O Windows Media Player lida com downloads de arquivos de música para a loja online.</span><span class="sxs-lookup"><span data-stu-id="f1606-112">Windows Media Player handles music file downloads for the online store.</span></span> <span data-ttu-id="f1606-113">Um download pode ser iniciado quando a página de descoberta chama [external. download](external-download.md) ou quando o usuário escolhe, no Player, para baixar um conjunto de faixas.</span><span class="sxs-lookup"><span data-stu-id="f1606-113">A download can be initiated when the discovery page calls [External.download](external-download.md) or when the user chooses, in the Player, to download a set of tracks.</span></span> <span data-ttu-id="f1606-114">Em ambos os casos, o Windows Media Player chama [IWMPContentPartner::D aixar](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passando uma lista de contêineres de conteúdo que descreve o conjunto de faixas a serem baixadas e um cookie que representa a transação de download.</span><span class="sxs-lookup"><span data-stu-id="f1606-114">In either case, Windows Media Player calls [IWMPContentPartner::Download](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passing a content container list that describes the set of tracks to be downloaded and a cookie that represents the download transaction.</span></span> <span data-ttu-id="f1606-115">O plug-in de parceiro de conteúdo deve então chamar [IWMPContentPartnerCallback::D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) uma vez para cada faixa no conjunto.</span><span class="sxs-lookup"><span data-stu-id="f1606-115">The content partner plug-in must then call [IWMPContentPartnerCallback::DownloadTrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) once for each track in the set.</span></span> <span data-ttu-id="f1606-116">Quando o plug-in chama **DownloadTrack**, ele passa um **HRESULT** no parâmetro *hrDownload* .</span><span class="sxs-lookup"><span data-stu-id="f1606-116">When the plug-in calls **DownloadTrack**, it passes an **HRESULT** in the *hrDownload* parameter.</span></span> <span data-ttu-id="f1606-117">Se o plug-in passar um código de êxito no *hrDownload*, o Windows Media Player baixará a faixa. Se o plug-in passar um código de falha em *hrDownload*, o Player não baixará a faixa. Para cada chamada para **Download**, o plug-in deve fornecer o cookie de transação e a ID da faixa em questão.</span><span class="sxs-lookup"><span data-stu-id="f1606-117">If the plug-in passes a success code in *hrDownload*, Windows Media Player downloads the track. If the plug-in passes a failure code in *hrDownload*, the Player does not download the track. For each call to **Download**, the plug-in must supply the transaction cookie and the ID of the track in question.</span></span> <span data-ttu-id="f1606-118">Para as faixas que serão realmente baixadas, o plug-in também deverá fornecer a URL da faixa.</span><span class="sxs-lookup"><span data-stu-id="f1606-118">For tracks that will actually be downloaded, the plug-in must also supply the URL of the track.</span></span>

<span data-ttu-id="f1606-119">Depois que um arquivo é baixado, o Windows Media Player atualiza automaticamente a biblioteca para refletir as músicas adquiridas recentemente.</span><span class="sxs-lookup"><span data-stu-id="f1606-119">After a file is downloaded, Windows Media Player automatically updates the library to reflect the newly purchased music.</span></span> <span data-ttu-id="f1606-120">O Player fornece informações de status para o plug-in sobre a operação de download chamando [IWMPContentPartner::D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete).</span><span class="sxs-lookup"><span data-stu-id="f1606-120">The Player provides status information to the plug-in about the download operation by calling [IWMPContentPartner::DownloadTrackComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete).</span></span> <span data-ttu-id="f1606-121">Nesse método, o Player fornece um **HRESULT** para indicar o êxito ou a falha do download, a ID de faixa e a cadeia de caracteres de parâmetros personalizados que o repositório online forneceu quando ele chamou **DownloadTrack**.</span><span class="sxs-lookup"><span data-stu-id="f1606-121">In this method, the Player provides an **HRESULT** to indicate success or failure of the download, the track ID, and the custom parameters string that the online store provided when it called **DownloadTrack**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1606-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1606-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1606-123">**Guia de programação para lojas online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="f1606-123">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




