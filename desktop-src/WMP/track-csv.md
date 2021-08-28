---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player lojas online track.csv
- lojas online, track.csv
- Digite 1 lojas online, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9561897fb68f53aaa4ba33e433cf6d6120ec315
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474912"
---
# <a name="trackcsv"></a>track.csv

Esse arquivo contém uma entrada para cada faixa no catálogo. Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir. Os campos devem aparecer na ordem listada.

A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado. Ele não se refere ao tipo de dados do conteúdo. Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.




| Campo | Obrigatório | Formatar | Descrição | 
|-------|----------|--------|-------------|
| TrackID | Sim | Inteiro não negativo. Exemplo: 32789<br /> | Identificador exclusivo fornecido pelo provedor de conteúdo. Deve ser menor que 2 ^ 32. dica de desempenho: se as IDs atribuídas a faixas do mesmo álbum forem numeradas consecutivamente, a compactação do catálogo será mais eficiente. No entanto, a numeração consecutiva de faixas do álbum não é necessária.<br /> | 
| TrackTitle | Sim | Cadeia de caracteres Unicode. Exemplo: O Raygun Robbers ' azuis | Nome da faixa. | 
| Duration | Yes | Inteiro não negativo. Exemplo: 543<br /> | Duração da faixa em segundos. | 
| TrackNumber | Sim | Inteiro não negativo. Exemplo: 7<br /> | Faixa número no álbum da faixa. Os números de faixa começam em 1 e aumentam em conjuntos de discos. O número de faixa deve ser menor que 256. Um número de faixa maior ou igual a 256 causará um comportamento inesperado no Windows Media Player. | 
| TrackPrice | Sim | Cadeia de caracteres Unicode. Exemplo: $0.99. | Preço de acompanhamento. O símbolo de moeda deve ser incluído. A cadeia de caracteres vazia, 0 e-ter significado especial. Uma cadeia de caracteres vazia indica que o preço é desconhecido. Um zero neste campo significa que a faixa é gratuita e um hífen (-) indica que a faixa não pode ser comprada. | 
| Canstream | Sim | Booliano. Pode ser 0 ou 1. exemplo: 0<br /> | Indica se a faixa pode ser transmitida. | 
| Canbaixado | Sim | Booliano. Pode ser 0 ou 1. exemplo: 0<br /> | Indica se a faixa pode ser baixada. | 
| HasPreviewClip | Sim | Booliano. Pode ser 0 ou 1. exemplo: 0<br /> | Indica se a faixa tem um clipe de visualização. | 
| HasVideoClip | Sim | Booliano. Pode ser 0 ou 1. exemplo: 0<br /> | Indica se a faixa tem um clipe de vídeo. | 
| ParentalRating | Sim | Enumeração. Pode ser N, E ou C. exemplo: N<br /> | Indica a classificação de consultoria do responsável. Os valores N, E e C são para normal, explícita e limpa. | 
| LinkedAlbumID | Sim | Inteiro não negativo. Deve ser a ID de um álbum. Exemplo: 32423 | A ID do álbum que contém essa faixa.<blockquote>[!Note]<br />Cada faixa deve pertencer a um álbum. Ou seja, para cada faixa, o campo LinkedAlbumID deve ser igual a uma das IDs do álbum no arquivo album.csv.</blockquote><br /> | 
| LinkedTrackArtist_ArtistIDs | Sim | Lista de inteiros. A lista contém IDs de artista, separadas por ponto e vírgula. Exemplo: 41322; 12321; 82123; | Uma lista de IDs correspondentes aos artistas colaboradores. | 
| Compositor | Não | Cadeia de caracteres Unicode. Exemplo: Sinfonia | O compositor da faixa. se o gênero da faixa não tiver o campo HasComposer definido, o valor do campo Composer será ignorado. Normalmente usado apenas para faixas de jazz ou clássicas. | 
| Popularidade | Sim | Inteiro ou float não negativo. exemplo: 1252,6<br /> | Determina a posição da faixa na lista quando classificada por popularidade. Um número mais baixo indica maior popularidade. | 
| StarRating | Não | Float.Example: 4.21<br /> | A classificação em estrela será arredondada para a 1/4 estrela mais próxima Windows Media Player antes de ser exibida na interface do Windows Media Player usuário. | 




 

 

 





