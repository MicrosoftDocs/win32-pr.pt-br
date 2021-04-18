---
description: A cláusula ORDER IN GROUP é usada em conjunto com a instrução GROUP ON, que retorna conjuntos de resultados em grupos.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: Cláusula ORDER IN GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b4a3a39ffeb2704a099389a6668a075fb4a24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296239"
---
# <a name="order-in-group-clause"></a><span data-ttu-id="7026a-103">Cláusula ORDER IN GROUP</span><span class="sxs-lookup"><span data-stu-id="7026a-103">ORDER IN GROUP Clause</span></span>

<span data-ttu-id="7026a-104">A cláusula ORDER IN GROUP é usada em conjunto com a instrução [Group on](-search-sql-group-on-over.md) , que retorna conjuntos de resultados em grupos.</span><span class="sxs-lookup"><span data-stu-id="7026a-104">The ORDER IN GROUP clause is used in conjunction with the [GROUP ON](-search-sql-group-on-over.md) statement, which returns result sets in groups.</span></span> <span data-ttu-id="7026a-105">A cláusula ORDER IN GROUP permite que você classifique cada grupo retornado de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="7026a-105">The ORDER IN GROUP clause enables you to sort each returned group in a different way.</span></span> <span data-ttu-id="7026a-106">Se você agrupar em System. Kind, por exemplo, poderá classificar todos os documentos por System.Document. LastAuthor, todos os arquivos de música por System. Music. AlbumArtist e todos os emails por System. Message. FromName.</span><span class="sxs-lookup"><span data-stu-id="7026a-106">If you group on System.Kind, for example, you can then sort all documents by System.Document.LastAuthor, all music files by System.Music.AlbumArtist, and all emails by System.Message.FromName.</span></span>

## <a name="syntax"></a><span data-ttu-id="7026a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7026a-107">Syntax</span></span>

<span data-ttu-id="7026a-108">A seguir está a sintaxe da cláusula ORDER IN GROUP:</span><span class="sxs-lookup"><span data-stu-id="7026a-108">The following is the syntax of the ORDER IN GROUP clause:</span></span>


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



<span data-ttu-id="7026a-109">O especificador de nome de grupo é um intervalo ou valor conhecido da coluna de grupo, conforme especificado na instrução GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="7026a-109">The group name specifier is a range or known value from the group column, as specified in the GROUP ON statement.</span></span> <span data-ttu-id="7026a-110">Por exemplo, os valores conhecidos para System. Photo. ISOSpeed incluem ' ISO-100 ', ' ISO-200 ' e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7026a-110">For example, known values for System.Photo.ISOSpeed would include 'ISO-100', 'ISO-200', and so on.</span></span> <span data-ttu-id="7026a-111">Um intervalo para System. Photo. DateTaken incluiria ' 2006-1-1 ' e ' 2007-1-1 ' para uma instrução como GROUP em System. Date \[ ' 2006-1-1 ', ' 2007-1-1 ' \] .</span><span class="sxs-lookup"><span data-stu-id="7026a-111">A range for System.Photo.DateTaken would include '2006-1-1' and '2007-1-1' for a statement like GROUP ON System.ItemDate \['2006-1-1', '2007-1-1'\].</span></span>

<span data-ttu-id="7026a-112">O especificador de coluna deve ser uma coluna válida especificada no grupo ou na instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="7026a-112">The column specifier must be a valid column specified in either the GROUP ON or the SELECT statement.</span></span> <span data-ttu-id="7026a-113">Você pode incluir mais de uma coluna, separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="7026a-113">You can include more than one column, separated by commas.</span></span> <span data-ttu-id="7026a-114">Por exemplo, se você agrupar em System. Photo. ISOSpeed, poderá classificar todas as fotos ISO-100, primeiro por System. Photo. ShutterSpeed e, em seguida, por System. Photo. Obturation.</span><span class="sxs-lookup"><span data-stu-id="7026a-114">For example, if you group on System.Photo.ISOSpeed, you can sort all ISO-100 photos, first by System.Photo.ShutterSpeed, and then by System.Photo.Aperture.</span></span>

<span data-ttu-id="7026a-115">O especificador de direção opcional pode ser ASC para crescente (baixo para alto) ou DESC para decrescente (alto para baixo).</span><span class="sxs-lookup"><span data-stu-id="7026a-115">The optional direction specifier can be either ASC for ascending (low to high) or DESC for descending (high to low).</span></span> <span data-ttu-id="7026a-116">Se você não fornecer um especificador de direção, o padrão, Ascending, será usado.</span><span class="sxs-lookup"><span data-stu-id="7026a-116">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="7026a-117">Se você especificar mais de uma coluna, mas não especificar todas as direções, a direção especificada por último será aplicada a cada coluna sucessiva até que você altere explicitamente a direção.</span><span class="sxs-lookup"><span data-stu-id="7026a-117">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each successive column until you explicitly change the direction.</span></span>

<span data-ttu-id="7026a-118">Os intervalos ou valores que não são explicitamente especificados em uma cláusula GROUP ORDER IN são classificados em ordem crescente pelos valores no grupo na coluna.</span><span class="sxs-lookup"><span data-stu-id="7026a-118">Ranges or values that are not explicitly specified in an ORDER GROUP IN clause are sorted in ascending order by the values in the GROUP ON column.</span></span>

## <a name="examples"></a><span data-ttu-id="7026a-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7026a-119">Examples</span></span>

<span data-ttu-id="7026a-120">O exemplo a seguir agrupa os resultados pela propriedade System. Kind.</span><span class="sxs-lookup"><span data-stu-id="7026a-120">The following example groups results by the System.Kind property.</span></span> <span data-ttu-id="7026a-121">A consulta ordenaria o grupo ' Program ' pelo nome do aplicativo e o grupo ' Music ' por título de álbum e número de faixa.</span><span class="sxs-lookup"><span data-stu-id="7026a-121">The query would order the 'program' group by the application name and the 'music' group by album title and track number.</span></span> <span data-ttu-id="7026a-122">O grupo **nulo** seria ordenado pelo nome do item.</span><span class="sxs-lookup"><span data-stu-id="7026a-122">The **NULL** group would be ordered by the item name.</span></span> <span data-ttu-id="7026a-123">Todos os outros grupos seriam ordenados pela data do item.</span><span class="sxs-lookup"><span data-stu-id="7026a-123">All other groups would by ordered by the item date.</span></span>


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



<span data-ttu-id="7026a-124">O exemplo a seguir agrupa os resultados pela propriedade System. ItemProperty e, em seguida, classifica cada grupo por URL, tipo ou nome do item.</span><span class="sxs-lookup"><span data-stu-id="7026a-124">The following example groups results by the System.ItemDate property, and then sorts each group by item URL, kind, or name.</span></span>


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



<span data-ttu-id="7026a-125">Os resultados da consulta anterior seriam retornados em cinco grupos e classificados conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7026a-125">The results of the preceding query would be returned in five groups and sorted as described in the following table.</span></span>



| <span data-ttu-id="7026a-126">Grupo</span><span class="sxs-lookup"><span data-stu-id="7026a-126">Group</span></span>    | <span data-ttu-id="7026a-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="7026a-127">Description</span></span>                                               | <span data-ttu-id="7026a-128">Classificado por</span><span class="sxs-lookup"><span data-stu-id="7026a-128">Sorted by</span></span>                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="7026a-129">MINVALUE</span><span class="sxs-lookup"><span data-stu-id="7026a-129">MINVALUE</span></span> | <span data-ttu-id="7026a-130">Itens com datas anteriores a 2006-1-1</span><span class="sxs-lookup"><span data-stu-id="7026a-130">Items with dates before 2006-1-1</span></span>                          | <span data-ttu-id="7026a-131">Classificado pela URL do item, em ordem crescente</span><span class="sxs-lookup"><span data-stu-id="7026a-131">Sorted by the item's URL, in ascending order</span></span> |
| <span data-ttu-id="7026a-132">2006-1-1</span><span class="sxs-lookup"><span data-stu-id="7026a-132">2006-1-1</span></span> | <span data-ttu-id="7026a-133">Itens com datas em ou após 2006-1-1, mas antes de 2007-1-1</span><span class="sxs-lookup"><span data-stu-id="7026a-133">Items with dates on or after 2006-1-1 but before 2007-1-1</span></span> | <span data-ttu-id="7026a-134">Classificado por data do item, em ordem crescente</span><span class="sxs-lookup"><span data-stu-id="7026a-134">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="7026a-135">2007-1-1</span><span class="sxs-lookup"><span data-stu-id="7026a-135">2007-1-1</span></span> | <span data-ttu-id="7026a-136">Itens com datas em ou após 2007-1-1, mas antes de 2008-1-1</span><span class="sxs-lookup"><span data-stu-id="7026a-136">Items with dates on or after 2007-1-1 but before 2008-1-1</span></span> | <span data-ttu-id="7026a-137">Classificado por valor de tipo, em ordem crescente</span><span class="sxs-lookup"><span data-stu-id="7026a-137">Sorted by kind value, in ascending order</span></span>     |
| <span data-ttu-id="7026a-138">2008-1-1</span><span class="sxs-lookup"><span data-stu-id="7026a-138">2008-1-1</span></span> | <span data-ttu-id="7026a-139">Itens com datas em ou após 2008-1-1</span><span class="sxs-lookup"><span data-stu-id="7026a-139">Items with dates on or after 2008-1-1</span></span>                     | <span data-ttu-id="7026a-140">Classificado por data do item, em ordem crescente</span><span class="sxs-lookup"><span data-stu-id="7026a-140">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="7026a-141">**NULL**</span><span class="sxs-lookup"><span data-stu-id="7026a-141">**NULL**</span></span> | <span data-ttu-id="7026a-142">Itens sem valor na coluna System. Item Date</span><span class="sxs-lookup"><span data-stu-id="7026a-142">Items with no value in the System.ItemDate column</span></span>         | <span data-ttu-id="7026a-143">Classificado por nome de item, em ordem crescente</span><span class="sxs-lookup"><span data-stu-id="7026a-143">Sorted by item name, in ascending order</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="7026a-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7026a-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7026a-145">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7026a-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7026a-146">AGRUPAR EM... SOBRE... Privacidade</span><span class="sxs-lookup"><span data-stu-id="7026a-146">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
</dt> <dt>

[<span data-ttu-id="7026a-147">Cláusula ORDER BY</span><span class="sxs-lookup"><span data-stu-id="7026a-147">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> </dl>

 

 



