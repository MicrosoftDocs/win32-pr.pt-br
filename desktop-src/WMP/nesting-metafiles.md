---
title: Aninhando metaarquivos
description: Aninhando metaarquivos
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Windows Metaarquivos de mídia, aninhamento
- Windows Metaarquivos de mídia, fazendo referência a outros metaarquivos
- aninhando metaarquivos
- metaarquivos, aninhamento
- metaarquivos, fazendo referência a outros metaarquivos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29a45bf545f839e111970b31d5faddd039959b7148a331fa5e347913b67327e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574269"
---
# <a name="nesting-metafiles"></a>Aninhando metaarquivos

Um metarquivo pode fazer referência A outro metarquivo. Para fazer referência a outro metarquivo, use o elemento **ENTRYREF** . Um elemento **ENTRYREF** no metarquivo primário aponta para um metarquivo externo.

o controle de Windows Media Player processa os elementos de **entrada** do metarquivo referenciado como se eles estivessem incluídos no metarquivo primário na posição do elemento **ENTRYREF** . No entanto, ele ignora todos os elementos de **entrada** no metarquivo referenciado que têm o atributo **SKIPIFREF** definido como Sim.

os controles Windows Media Player 7,0, 7,1 e Windows Media Player para Windows XP ignoram todos os elementos **ENTRYREF** no metarquivo referenciado. Portanto, os metaarquivos só podem ser aninhados em um nível profundo usando essas versões. Essas versões também ignoram o elemento **ASX** e seus atributos no arquivo referenciado. o Windows Media Player 9 Series ou posterior dá suporte ao aninhamento de metaarquivos de até 5 níveis.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando listas de reprodução de metarquivo**](creating-metafile-playlists.md)
</dt> </dl>

 

 




