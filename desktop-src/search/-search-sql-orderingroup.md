---
description: A cláusula ORDER IN GROUP é usada em conjunto com a instrução GROUP ON, que retorna conjuntos de resultados em grupos.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: Cláusula ORDER IN GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b17981f6368b67852e393d38ef8c4b856601d73014d9bdce40292e7e4a499d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944646"
---
# <a name="order-in-group-clause"></a>Cláusula ORDER IN GROUP

A cláusula ORDER IN GROUP é usada em conjunto com a [instrução GROUP ON,](-search-sql-group-on-over.md) que retorna conjuntos de resultados em grupos. A cláusula ORDER IN GROUP permite classificar cada grupo retornado de uma maneira diferente. Se você agrupar em System.Kind, por exemplo, poderá classificar todos os documentos por System.Document. LastAuthor, todos os arquivos de música de System.Music.AlbumArtist e todos os emails por System.Message.FromName.

## <a name="syntax"></a>Syntax

Veja a seguir a sintaxe da cláusula ORDER IN GROUP:


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



O especificador de nome de grupo é um intervalo ou valor conhecido da coluna de grupo, conforme especificado na instrução GROUP ON. Por exemplo, os valores conhecidos para System.Photo.ISOSpeed incluiriam 'ISO-100', 'ISO-200' e assim por diante. Um intervalo para System.Photo.DateTaken incluiria '2006-1-1' e '2007-1-1' para uma instrução como GROUP ON System.ItemDate \[ '2006-1-1', '2007-1-1'. \]

O especificador de coluna deve ser uma coluna válida especificada na instrução GROUP ON ou SELECT. Você pode incluir mais de uma coluna, separadas por vírgulas. Por exemplo, se você agrupar em System.Photo.ISOSpeed, poderá classificar todas as fotos ISO-100, primeiro por System.Photo.ShutterSpeed e, em seguida, por System.Photo.Aperture.

O especificador de direção opcional pode ser ASC para crescente (baixo a alto) ou DESC para decrescente (de alto para baixo). Se você não fornecer um especificador de direção, o padrão, crescente, será usado. Se você especificar mais de uma coluna, mas não especificar todas as direções, a direção especificada por último será aplicada a cada coluna sucessiva até que você altere explicitamente a direção.

Intervalos ou valores que não são especificados explicitamente em uma cláusula ORDER GROUP IN são classificação em ordem crescente pelos valores na coluna GROUP ON.

## <a name="examples"></a>Exemplos

O exemplo a seguir grupos os resultados pela propriedade System.Kind. A consulta ordenaria o grupo 'program' pelo nome do aplicativo e o grupo 'música' por título do álbum e número da faixa. O **grupo NULL** seria ordenado pelo nome do item. Todos os outros grupos seriam ordenados pela data do item.


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



O exemplo a seguir agrupa os resultados pela propriedade System.ItemDate e classifica cada grupo por URL, tipo ou nome do item.


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



Os resultados da consulta anterior seriam retornados em cinco grupos e classificação conforme descrito na tabela a seguir.



| Grupo    | Descrição                                               | Classificado por                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| Minvalue | Itens com datas anteriores a 2006-1-1                          | Classificação pela URL do item, em ordem crescente |
| 2006-1-1 | Itens com datas em ou após 2006-1-1, mas antes de 2007-1-1 | Classificação por data do item, em ordem crescente      |
| 2007-1-1 | Itens com datas em ou após 2007-1-1, mas antes de 2008-1-1 | Classificação por valor de tipo, em ordem crescente     |
| 2008-1-1 | Itens com datas em ou após 2008-1-1                     | Classificação por data do item, em ordem crescente      |
| **NULL** | Itens sem valor na coluna System.ItemDate         | Classificação por nome do item, em ordem crescente      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[GROUP ON ... Sobre... Declaração](-search-sql-group-on-over.md)
</dt> <dt>

[Cláusula ORDER BY](-search-sql-orderby.md)
</dt> </dl>

 

 



