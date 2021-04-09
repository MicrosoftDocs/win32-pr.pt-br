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
# <a name="music-catalog"></a>Catálogo de música

Uma loja online tipo 1 cria seu catálogo de música como um conjunto de arquivos TSV (valores separados por tabulação). Em seguida, a loja online usa o [compilador de catálogo](catalog-compiler-for-type-1-online-stores.md) da Microsoft para compilar os arquivos TSV em um catálogo compactado que pode ser baixado pelo Windows Media Player. O Windows Media Player pode baixar arquivos de catálogo completos ou arquivos de atualização de catálogo. As atualizações do catálogo contêm apenas as informações do catálogo que foram alteradas desde a última atualização do catálogo. Cabe ao plug-in de parceiro de conteúdo determinar se um catálogo completo ou uma atualização deve ser baixado. Em ambos os casos, o Windows Media Player aplica as alterações ao catálogo atual após a notificação do plug-in.

Se o repositório online tiver um novo catálogo preparado, o plug-in poderá notificar o Player chamando [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) e passando wmpcnNewCatalogAvailable como o valor para o parâmetro de *tipo* .

Quando o Windows Media Player estiver pronto para baixar um catálogo ou uma atualização, o jogador chamará [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). Esse método fornece o plug-in com informações sobre o catálogo atual, como a versão do catálogo e o identificador de localidade. O plug-in responde fornecendo o Uniform Resource Locator (URL) do catálogo completo ou da atualização correta, bem como um número de versão atualizado e uma data de validade. O Windows Media Player solicitará periodicamente atualizações de catálogo com base nas informações fornecidas pelo plug-in no **GetCatalogURL**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o tipo 1 lojas online**](about-type-1-online-stores.md)
</dt> <dt>

[**Compilador de catálogo para repositórios online do tipo 1**](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[**Interface IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




