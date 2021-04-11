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
# <a name="downloading-media-content"></a>Baixando conteúdo de mídia

O Windows Media Player lida com downloads de arquivos de música para a loja online. Um download pode ser iniciado quando a página de descoberta chama [external. download](external-download.md) ou quando o usuário escolhe, no Player, para baixar um conjunto de faixas. Em ambos os casos, o Windows Media Player chama [IWMPContentPartner::D aixar](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passando uma lista de contêineres de conteúdo que descreve o conjunto de faixas a serem baixadas e um cookie que representa a transação de download. O plug-in de parceiro de conteúdo deve então chamar [IWMPContentPartnerCallback::D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) uma vez para cada faixa no conjunto. Quando o plug-in chama **DownloadTrack**, ele passa um **HRESULT** no parâmetro *hrDownload* . Se o plug-in passar um código de êxito no *hrDownload*, o Windows Media Player baixará a faixa. Se o plug-in passar um código de falha em *hrDownload*, o Player não baixará a faixa. Para cada chamada para **Download**, o plug-in deve fornecer o cookie de transação e a ID da faixa em questão. Para as faixas que serão realmente baixadas, o plug-in também deverá fornecer a URL da faixa.

Depois que um arquivo é baixado, o Windows Media Player atualiza automaticamente a biblioteca para refletir as músicas adquiridas recentemente. O Player fornece informações de status para o plug-in sobre a operação de download chamando [IWMPContentPartner::D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete). Nesse método, o Player fornece um **HRESULT** para indicar o êxito ou a falha do download, a ID de faixa e a cadeia de caracteres de parâmetros personalizados que o repositório online forneceu quando ele chamou **DownloadTrack**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação para lojas online do tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




