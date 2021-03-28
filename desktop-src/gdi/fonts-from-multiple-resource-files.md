---
description: Fontes de vários arquivos de recurso
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: Fontes de vários arquivos de recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/17/2021
ms.locfileid: "104989458"
---
# <a name="fonts-from-multiple-resource-files"></a>Fontes de vários arquivos de recurso

Normalmente, uma fonte está contida em um único arquivo de recurso de fonte. No entanto, as informações de algumas fontes são distribuídas entre vários arquivos. Por exemplo, digite 1 várias fontes mestras exigem dois arquivos:

-   . PFM para as métricas de fonte
-   . pfb para os bits de fonte

Para adicionar uma fonte de vários arquivos ao sistema, use as funções [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) ou [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) . O parâmetro *lpszFileName* nessas funções deve apontar para uma cadeia de caracteres que contém os nomes de arquivo separados pela barra vertical ou pelo pipe ( \| ). Por exemplo, para especificar abcxxxxx. PFM e abcxxxxx. pfb para uma fonte do tipo 1, use a cadeia de caracteres "abcxxxxx. PFM \| abcxxxxx. pfb".

O [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) é diferente de [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) , pois o aplicativo que chama **AddFontResourceEx** pode especificar a fonte como particular para si mesmo ou não enumerável.

Para adicionar uma fonte de uma imagem de memória, use [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex). Isso permite que um aplicativo use uma fonte inserida em um documento ou em uma página da Web.

Para remover uma fonte que veio de vários arquivos de recursos, chame [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) ou [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), dependendo da função usada para adicionar a fonte. Você deve especificar os mesmos sinalizadores que foram usados para adicionar a fonte. Para remover uma fonte que foi adicionada de uma imagem de memória, use [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).

O uso de uma fonte proveniente de vários arquivos de recurso de fonte é idêntico ao uso de uma fonte de um único arquivo de recurso.

 

 
