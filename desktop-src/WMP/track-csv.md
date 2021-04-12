---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Armazenamentos online do Windows Media Player, track.csv
- lojas online, track.csv
- Digite 1 lojas online, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292354"
---
# <a name="trackcsv"></a>track.csv

Esse arquivo contém uma entrada para cada faixa no catálogo. Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir. Os campos devem aparecer na ordem listada.

A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado. Ele não se refere ao tipo de dados do conteúdo. Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo</th>
<th>Obrigatório</th>
<th>Formatar</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TrackID</td>
<td>Sim</td>
<td>Inteiro não negativo. Exemplo: 32789<br/></td>
<td>Identificador exclusivo fornecido pelo provedor de conteúdo. Deve ser menor que 2 ^ 32. dica de desempenho: se as IDs atribuídas a faixas do mesmo álbum forem numeradas consecutivamente, a compactação do catálogo será mais eficiente. No entanto, a numeração consecutiva de faixas do álbum não é necessária.<br/></td>
</tr>
<tr class="even">
<td>TrackTitle</td>
<td>Sim</td>
<td>Cadeia de caracteres Unicode. Exemplo: O Raygun Robbers ' azuis</td>
<td>Nome da faixa.</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Sim</td>
<td>Inteiro não negativo. Exemplo: 543<br/></td>
<td>Duração da faixa em segundos.</td>
</tr>
<tr class="even">
<td>TrackNumber</td>
<td>Sim</td>
<td>Inteiro não negativo. Exemplo: 7<br/></td>
<td>Faixa número no álbum da faixa. Os números de faixa começam em 1 e aumentam em conjuntos de discos. O número de faixa deve ser menor que 256. Um número de faixa maior ou igual a 256 causará um comportamento inesperado no Windows Media Player.</td>
</tr>
<tr class="odd">
<td>TrackPrice</td>
<td>Sim</td>
<td>Cadeia de caracteres Unicode. Exemplo: $0.99.</td>
<td>Preço de acompanhamento. O símbolo de moeda deve ser incluído. A cadeia de caracteres vazia, 0 e-ter significado especial. Uma cadeia de caracteres vazia indica que o preço é desconhecido. Um zero neste campo significa que a faixa é gratuita e um hífen (-) indica que a faixa não pode ser comprada.</td>
</tr>
<tr class="even">
<td>Canstream</td>
<td>Sim</td>
<td>Booliano. Pode ser 0 ou 1. exemplo: 0<br/></td>
<td>Indica se a faixa pode ser transmitida.</td>
</tr>
<tr class="odd">
<td>Canbaixado</td>
<td>Sim</td>
<td>Booliano. Pode ser 0 ou 1. exemplo: 0<br/></td>
<td>Indica se a faixa pode ser baixada.</td>
</tr>
<tr class="even">
<td>HasPreviewClip</td>
<td>Sim</td>
<td>Booliano. Pode ser 0 ou 1. exemplo: 0<br/></td>
<td>Indica se a faixa tem um clipe de visualização.</td>
</tr>
<tr class="odd">
<td>HasVideoClip</td>
<td>Sim</td>
<td>Booliano. Pode ser 0 ou 1. exemplo: 0<br/></td>
<td>Indica se a faixa tem um clipe de vídeo.</td>
</tr>
<tr class="even">
<td>ParentalRating</td>
<td>Sim</td>
<td>Enumeração. Pode ser N, E ou C. exemplo: N<br/></td>
<td>Indica a classificação de consultoria do responsável. Os valores N, E e C são para normal, explícita e limpa.</td>
</tr>
<tr class="odd">
<td>LinkedAlbumID</td>
<td>Sim</td>
<td>Inteiro não negativo. Deve ser a ID de um álbum. Exemplo: 32423</td>
<td>A ID do álbum que contém essa faixa.
<blockquote>
[!Note]<br />
Cada faixa deve pertencer a um álbum. Ou seja, para cada faixa, o campo LinkedAlbumID deve ser igual a uma das IDs do álbum no arquivo album.csv.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>LinkedTrackArtist_ArtistIDs</td>
<td>Sim</td>
<td>Lista de inteiros. A lista contém IDs de artista, separadas por ponto e vírgula. Exemplo: 41322; 12321; 82123;</td>
<td>Uma lista de IDs correspondentes aos artistas colaboradores.</td>
</tr>
<tr class="odd">
<td>Compositor</td>
<td>Não</td>
<td>Cadeia de caracteres Unicode. Exemplo: Sinfonia</td>
<td>O compositor da faixa. Se o gênero da faixa não tiver o campo HasComposer definido, o valor do campo do compositor será ignorado. Normalmente usado apenas para faixas de jazz ou clássicas.</td>
</tr>
<tr class="even">
<td>Popularidade</td>
<td>Sim</td>
<td>Inteiro ou float não negativo. exemplo: 1252,6<br/></td>
<td>Determina a posição da faixa na lista quando classificada por popularidade. Um número mais baixo indica maior popularidade.</td>
</tr>
<tr class="odd">
<td>StarRating</td>
<td>Não</td>
<td>Float. example: 4,21<br/></td>
<td>A classificação por estrelas será arredondada para a estrela de 1/4 a mais próxima do Windows Media Player antes de ser exibida na interface de usuário do Windows Media Player.</td>
</tr>
</tbody>
</table>



 

 

 





