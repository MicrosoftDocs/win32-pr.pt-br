---
title: Processando um conjunto de resultados
description: Um conjunto de resultados é retornado como uma série de linhas.
ms.assetid: e0949c1c-a31a-440a-ae10-2934ffeb7128
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ad422494fd2d384b612989e9e36cec7110e021
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294498"
---
# <a name="processing-a-result-set"></a><span data-ttu-id="a351d-103">Processando um conjunto de resultados</span><span class="sxs-lookup"><span data-stu-id="a351d-103">Processing a Result Set</span></span>

<span data-ttu-id="a351d-104">Um conjunto de resultados é retornado como uma série de linhas.</span><span class="sxs-lookup"><span data-stu-id="a351d-104">A result set is returned as a series of rows.</span></span> <span data-ttu-id="a351d-105">Cada linha pode ou não conter um determinado atributo.</span><span class="sxs-lookup"><span data-stu-id="a351d-105">Each row may or may not contain a given attribute.</span></span> <span data-ttu-id="a351d-106">Com o provedor de OLE DB, o conjunto de resultados é semelhante a um conjunto de resultados SQL normal.</span><span class="sxs-lookup"><span data-stu-id="a351d-106">With the OLE DB provider, the result set appears similar to a normal SQL result set.</span></span> <span data-ttu-id="a351d-107">Se você usar ADO para a consulta, o [ADODB. ](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) O objeto Recordset é usado para percorrer o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="a351d-107">If you use ADO for the query, the [ADODB.Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) object is used for traversing the result set.</span></span> <span data-ttu-id="a351d-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (disponível somente de linguagens que dão suporte a associações vtable) contém membros para mover o cursor de linha e verificar os valores de propriedade em uma determinada linha.</span><span class="sxs-lookup"><span data-stu-id="a351d-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (available only from languages that support vtable bindings) contains members for moving the row cursor and checking property values in a given row.</span></span> <span data-ttu-id="a351d-109">Como alternativa, você pode usar [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para obter e definir propriedades.</span><span class="sxs-lookup"><span data-stu-id="a351d-109">Alternatively, you can use [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) to get and set properties.</span></span>

 

 