---
description: Os identificadores especificam os nomes das colunas (às vezes chamados de propriedades), catálogos e aliases.
ms.assetid: 799afe2c-9217-4006-a4a3-644e5393993c
title: Identificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df79bd0d70564ea3e87ff4821a1cb59e3d0a5eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090066"
---
# <a name="identifiers"></a><span data-ttu-id="001c9-103">Identificadores</span><span class="sxs-lookup"><span data-stu-id="001c9-103">Identifiers</span></span>

<span data-ttu-id="001c9-104">Os identificadores especificam os nomes das colunas (às vezes chamados de propriedades), catálogos e aliases.</span><span class="sxs-lookup"><span data-stu-id="001c9-104">Identifiers specify the names of columns (sometimes referred to as properties), catalogs, and aliases.</span></span> <span data-ttu-id="001c9-105">Por exemplo, System. ItemName e System. DateCreated são os identificadores de duas colunas de propriedade definidas pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="001c9-105">For example, System.ItemName and System.DateCreated are the identifiers of two system-defined property columns.</span></span> <span data-ttu-id="001c9-106">Literais, por outro lado, especificam valores numéricos e de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="001c9-106">Literals, by contrast, specify string and numeric values.</span></span>


<span data-ttu-id="001c9-107">Você pode criar identificadores com até 128 caracteres de comprimento e em um dos dois tipos, diferenciados pelos caracteres usados no nome do identificador:</span><span class="sxs-lookup"><span data-stu-id="001c9-107">You can create identifiers that are up to 128 characters long, and in one of two types, distinguished by the characters used in the identifier name:</span></span>

-   <span data-ttu-id="001c9-108">Os **identificadores regulares** contêm apenas os caracteres a-z, a-z, 0-9, sublinhado ( \_ ) e ponto (.) e começam com uma letra.</span><span class="sxs-lookup"><span data-stu-id="001c9-108">**Regular identifiers** contain only the characters A-Z, a-z, 0-9, underscore (\_), and dot (.), and they begin with a letter.</span></span> <span data-ttu-id="001c9-109">Você não precisa incluir identificadores regulares entre aspas duplas ("").</span><span class="sxs-lookup"><span data-stu-id="001c9-109">You do not need to enclose regular identifiers in double quotation marks (" ").</span></span>
-   <span data-ttu-id="001c9-110">**Identificadores delimitados** podem conter qualquer caractere Unicode válido e devem ser colocados entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="001c9-110">**Delimited identifiers** can contain any valid Unicode character and must be enclosed in double quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="001c9-111">Nas cláusulas FREETEXT e CONTAINS, você pode usar o asterisco ( \* ) como um identificador de coluna especial quando desejar especificar que a pesquisa do Windows inclui todas as propriedades indexadas na consulta.</span><span class="sxs-lookup"><span data-stu-id="001c9-111">In FREETEXT and CONTAINS clauses, you can use the asterisk (\*) as a special column identifier when you want to specify that Windows Search includes all of the indexed properties in the query.</span></span> <span data-ttu-id="001c9-112">Embora não seja um identificador regular, ele não exige aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="001c9-112">Although it is not a regular identifier, it does not require double quotation marks.</span></span>

 

 

 



