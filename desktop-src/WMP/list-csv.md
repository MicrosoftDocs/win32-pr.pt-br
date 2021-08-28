---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player online, list.csv
- lojas online, list.csv
- tipo 1 lojas online, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7237afb37b30ccf8c96ddac95f0e81e148703d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480782"
---
# <a name="listcsv"></a>list.csv

Esse arquivo contém uma entrada para cada uma das listas que o catálogo contém. Listas podem ser listas de faixas, álbums, músicas, gêneros, subgêneres ou feeds de rádio; ou podem ser listas de outras listas. Cada entrada de lista é uma linha composta pelos campos delimitados por tabulação descritos na tabela abaixo. Os campos devem aparecer na ordem listada.

A coluna Formato na tabela a seguir descreve como cada campo de texto Unicode é formatado. Ele não se refere ao tipo de dados do conteúdo. Por exemplo, se Integer for indicado na coluna Formato, isso significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.




| Campo | Obrigatório | Formatar | Descrição | 
|-------|----------|--------|-------------|
| Listid | Sim | Inteiro não negativo. | Identificador de lista, exclusivo em list.csv. Deve ser não negativo e menor que 2^32. <strong>Exibindo um nó de lista no controle de exibição de árvore:</strong> Se a ListID for 0, 1, 2, 3, 4, 5, 6 ou 7, a lista será exibida como um nó personalizado no nó de nível superior da loja online no controle de exibição de árvore do Player. Nós personalizados aparecem antes dos nós padrão no nó de nível superior da loja online e eles são posicionados em ordem crescente por ListID. Por exemplo, se houver três nós personalizados, com ListIDs de 1, 3 e 5, eles serão exibidos primeiro, segundo e terceiro sob o nó de nível superior da loja online.<br /> | 
| ListTitle | Não | Cadeia de caracteres Unicode. Exemplo: Dez principais acertos<br /> | Título da lista. | 
| ListSubtitle | Não | Cadeia de caracteres Unicode | Listar título alternativo, exibido na segunda linha da exibição De peças. | 
| ListDescription | Sim | Cadeia de caracteres Unicode | Listar texto de exibição amigável (exibido em páginas de propriedades). | 
| Linked_ItemType | Sim | Cadeia de caracteres Unicode. Formato: [T|P|A|L|G|S|R]<br /> Exemplo: T<br /> | Indica o tipo dos itens vinculados.<ul><li>T= Track</li><li>P = Desempenho</li><li>A = Álbum</li><li>L = Lista</li><li>G = Gênero</li><li>S = Subgenre</li><li>R = Rádio</li></ul> | 
| ListPrice | Sim | Cadeia de caracteres Unicode. Exemplo: US$ 9,99<br /> | Preço da lista. O símbolo de moeda deve ser incluído. Um zero significa que a lista é gratuita. Nenhum valor significa que o preço é desconhecido. Um hífen significa que a lista não pode ser comprada.<br /> | 
| Popularidade | Sim | Valor inteiro ou decimal. Exemplo: 1259.3<br /> | Indica a classificação de popularidade quando essa lista aparece em outras listas. Pode ser zero se não aplicável.. | 
| IsRecentlyAdded | Sim | Boolean.Format: [0|1]<br /> Exemplo: 0<br /> | Indica se a lista foi adicionada recentemente. | 
| IsFeatured | Sim | Boolean.Format: [0|1]<br /> Exemplo: 0<br /> | Indica se a lista está em destaque. Pode ser usado para determinar a ordem de classificação. | 
| EditorialGlyph | Sim | Inteiro não negativo. Deve ser 0. | Não usado nesta versão. Deve ser 0. | 
| ViewType | Sim | Cadeia de caracteres Unicode. Formato: [I|T|R|L|O]Exemplo: T<br /> | Indica o tipo de exibição a ser usado para a lista.<ul><li>I = Ícone</li><li>T = Tile</li><li>R = Relatório</li><li>L = Lista</li><li>O = Lista ordenada</li></ul> | 
| ViewImageSize | Sim | Inteiro não negativo. Exemplo: 180<br /> | O tamanho no qual a imagem da lista é exibida. Se 0, o tamanho será determinado automaticamente. | 
| GroupBy | Sim | Cadeia de caracteres Unicode. Formato: [-|P|A|C|R|D]<br /> Exemplo: P<br /> | Indica qual campo é usado para agrupar os itens na lista.<ul><li>- = Automático</li><li>P = Desempenho</li><li>A = Álbum</li><li>C = Composer</li><li>R = Classificação</li><li>D = Data</li></ul> | 
| ListItemsAreDynamic | Sim | Booliano. Pode ser 0 ou 1. | Indica se a lista é gerada dinamicamente. As listas dinâmicas não têm itens listitem.csv. Se uma lista for marcada como dinâmica, seus itens serão fornecidos por <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a> | 




 

 

 





