---
title: Baixando conteúdo de mídia
description: Baixando conteúdo de mídia
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Windows Media Player lojas online, baixando conteúdo de mídia
- lojas online, baixando conteúdo de mídia
- Digite 1 lojas online, baixando conteúdo de mídia
- Windows Media Player lojas online, download de conteúdo de mídia
- lojas online, download de conteúdo de mídia
- tipos 1 lojas online, download de conteúdo de mídia
- conteúdo de mídia, baixando
- baixando conteúdo de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a314dc4b59966fd779660a2c1ab26fc2b37d413e4add068f936a6109acd423a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997026"
---
# <a name="downloading-media-content"></a>Baixando conteúdo de mídia

Windows Media Player lida com downloads de arquivos de música para a loja online. Um download pode ser iniciado quando a página de descoberta chama [external. download](external-download.md) ou quando o usuário escolhe, no Player, para baixar um conjunto de faixas. em ambos os casos, Windows Media Player chama [IWMPContentPartner::D aixar](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passando uma lista de contêineres de conteúdo que descreve o conjunto de faixas a serem baixadas e um cookie que representa a transação de Download. O plug-in de parceiro de conteúdo deve então chamar [IWMPContentPartnerCallback::D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) uma vez para cada faixa no conjunto. Quando o plug-in chama **DownloadTrack**, ele passa um **HRESULT** no parâmetro *hrDownload* . se o plug-in passar um código de êxito em *hrDownload*, Windows Media Player baixará o controle. Se o plug-in passar um código de falha em *hrDownload*, o Player não baixará a faixa. Para cada chamada para **Download**, o plug-in deve fornecer o cookie de transação e a ID da faixa em questão. Para as faixas que serão realmente baixadas, o plug-in também deverá fornecer a URL da faixa.

depois que um arquivo é baixado, Windows Media Player atualiza automaticamente a biblioteca para refletir as músicas adquiridas recentemente. O Player fornece informações de status para o plug-in sobre a operação de download chamando [IWMPContentPartner::D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete). Nesse método, o Player fornece um **HRESULT** para indicar o êxito ou a falha do download, a ID de faixa e a cadeia de caracteres de parâmetros personalizados que o repositório online forneceu quando ele chamou **DownloadTrack**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação para lojas online do tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




