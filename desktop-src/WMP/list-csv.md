---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Armazenamentos online do Windows Media Player, list.csv
- lojas online, list.csv
- Digite 1 lojas online, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f41ed237c5f4a185f01feace8f09b4615e4922b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084342"
---
# <a name="listcsv"></a>list.csv

Esse arquivo contém uma entrada para cada uma das listas que o catálogo contém. As listas podem ser listas de faixas, álbuns, artistas, gêneros, subgêneros ou feeds de rádio; ou podem ser listas de outras listas. Cada entrada de lista é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir. Os campos devem aparecer na ordem listada.

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
<td>ListID</td>
<td>Sim</td>
<td>Inteiro não negativo.</td>
<td>Identificador de lista, exclusivo dentro de list.csv. Deve ser não negativo e menor que 2 ^ 32. <strong>Exibindo um nó de lista no controle de exibição de árvore:</strong> Se ListId for 0, 1, 2, 3, 4, 5, 6 ou 7, a lista será exibida como um nó personalizado no nó de nível superior da loja online no controle de exibição de árvore do Player. Os nós personalizados aparecem antes dos nós padrão no nó de nível superior da loja online e são posicionados em ordem crescente por lista de classificação. Por exemplo, se houver três nós personalizados, com ListIDs de 1, 3 e 5, eles serão exibidos primeiro, segundo e terceiro sob o nó de nível superior da loja online.<br/></td>
</tr>
<tr class="even">
<td>ListTitle</td>
<td>Não</td>
<td>Cadeia de caracteres Unicode. Exemplo: dez principais ocorrências<br/></td>
<td>Título da lista.</td>
</tr>
<tr class="odd">
<td>ListSubtitle</td>
<td>Não</td>
<td>Cadeia de caracteres Unicode</td>
<td>Listar título alternativo, exibido na segunda linha da exibição de bloco.</td>
</tr>
<tr class="even">
<td>ListDescription</td>
<td>Sim</td>
<td>Cadeia de caracteres Unicode</td>
<td>Listar texto de exibição amigável (exibido em páginas de propriedades).</td>
</tr>
<tr class="odd">
<td>Linked_ItemType</td>
<td>Sim</td>
<td>Cadeia de caracteres Unicode. Formato: [T | P | A | L | G | S | D<br/> Exemplo: T<br/></td>
<td>Indica o tipo dos itens vinculados.
<ul>
<li>T = faixa</li>
<li>P = executor</li>
<li>A = álbum</li>
<li>L = lista</li>
<li>G = gênero</li>
<li>S = subgênero</li>
<li>R = rádio</li>
</ul></td>
</tr>
<tr class="even">
<td>ListPrice</td>
<td>Sim</td>
<td>Cadeia de caracteres Unicode. Exemplo: $9.99<br/></td>
<td>Preço da lista. O símbolo de moeda deve ser incluído. Um zero significa que a lista é gratuita. Nenhum valor significa que o preço é desconhecido. Um hífen significa que a lista não pode ser comprada.<br/></td>
</tr>
<tr class="odd">
<td>Popularidade</td>
<td>Sim</td>
<td>Valor inteiro ou Decimal. Exemplo: 1259,3<br/></td>
<td>Indica a classificação de popularidade quando essa lista aparece em outras listas. Pode ser zero se não for aplicável..</td>
</tr>
<tr class="even">
<td>IsRecentlyAdded</td>
<td>Sim</td>
<td>Booliano. formato: [0 | 1]<br/> Exemplo: 0<br/></td>
<td>Indica se a lista foi adicionada recentemente.</td>
</tr>
<tr class="odd">
<td>Isfeatured</td>
<td>Sim</td>
<td>Booliano. formato: [0 | 1]<br/> Exemplo: 0<br/></td>
<td>Indica se a lista está em destaque. Pode ser usado para determinar a ordem de classificação.</td>
</tr>
<tr class="even">
<td>EditorialGlyph</td>
<td>Sim</td>
<td>Inteiro não negativo. Deve ser 0.</td>
<td>Não usado nesta versão. Deve ser 0.</td>
</tr>
<tr class="odd">
<td>ViewType</td>
<td>Sim</td>
<td>Cadeia de caracteres Unicode. Formato: [I | T | R | L | O] exemplo: T<br/></td>
<td>Indica o tipo de exibição a ser usado para a lista.
<ul>
<li>I = ícone</li>
<li>T = bloco</li>
<li>R = relatório</li>
<li>L = lista</li>
<li>O = lista ordenada</li>
</ul></td>
</tr>
<tr class="even">
<td>ViewImageSize</td>
<td>Sim</td>
<td>Inteiro não negativo. Exemplo: 180<br/></td>
<td>O tamanho no qual a imagem da lista é exibida. Se for 0, o tamanho será determinado automaticamente.</td>
</tr>
<tr class="odd">
<td>GroupBy</td>
<td>Sim</td>
<td>Cadeia de caracteres Unicode. Formato: [-| P | A | C | R | 3D<br/> Exemplo: P<br/></td>
<td>Indica qual campo é usado para agrupar os itens na lista.
<ul>
<li>- = Automático</li>
<li>P = executor</li>
<li>A = álbum</li>
<li>C = Composer</li>
<li>R = classificação</li>
<li>D = data</li>
</ul></td>
</tr>
<tr class="even">
<td>ListItemsAreDynamic</td>
<td>Sim</td>
<td>Booliano. Pode ser 0 ou 1.</td>
<td>Indica se a lista é gerada dinamicamente. Listas dinâmicas não têm itens em listitem.csv. Se uma lista for marcada como dinâmica, seus itens serão fornecidos por <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner:: GetListContents</a></td>
</tr>
</tbody>
</table>



 

 

 





