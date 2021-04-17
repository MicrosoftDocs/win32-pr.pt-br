---
description: 'Saiba mais sobre: convertendo o tipo de dados de uma coluna'
ms.assetid: 78a137a9-ef69-4ce3-8a96-73e722951300
title: Convertendo o tipo de dados de uma coluna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71a72a84c915d066d4b088719808687a965d86b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798210"
---
# <a name="casting-the-data-type-of-a-column"></a><span data-ttu-id="a6b18-103">Convertendo o tipo de dados de uma coluna</span><span class="sxs-lookup"><span data-stu-id="a6b18-103">Casting the Data Type of a Column</span></span>

<span data-ttu-id="a6b18-104">Às vezes, talvez seja necessário converter dados de cadeia de caracteres extraídos de documentos como outro tipo de dados, para que uma comparação apropriada possa ser feita.</span><span class="sxs-lookup"><span data-stu-id="a6b18-104">At times you may need to cast string data extracted from documents as another data type, so that an appropriate comparison can be made.</span></span> <span data-ttu-id="a6b18-105">Converta um identificador ou um literal como outro tipo de dados usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="a6b18-105">Cast an identifier or literal as another data type using the following syntax:</span></span>


```
CAST (<identifier> | <literal> AS <datatype>)
```



<span data-ttu-id="a6b18-106">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a6b18-106">For example:</span></span>


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a><span data-ttu-id="a6b18-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6b18-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6b18-108">Mapeamentos de tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a6b18-108">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



