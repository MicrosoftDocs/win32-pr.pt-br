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
# <a name="identifiers"></a>Identificadores

Os identificadores especificam os nomes das colunas (às vezes chamados de propriedades), catálogos e aliases. Por exemplo, System. ItemName e System. DateCreated são os identificadores de duas colunas de propriedade definidas pelo sistema. Literais, por outro lado, especificam valores numéricos e de cadeia de caracteres.


Você pode criar identificadores com até 128 caracteres de comprimento e em um dos dois tipos, diferenciados pelos caracteres usados no nome do identificador:

-   Os **identificadores regulares** contêm apenas os caracteres a-z, a-z, 0-9, sublinhado ( \_ ) e ponto (.) e começam com uma letra. Você não precisa incluir identificadores regulares entre aspas duplas ("").
-   **Identificadores delimitados** podem conter qualquer caractere Unicode válido e devem ser colocados entre aspas duplas.

> [!Note]  
> Nas cláusulas FREETEXT e CONTAINS, você pode usar o asterisco ( \* ) como um identificador de coluna especial quando desejar especificar que a pesquisa do Windows inclui todas as propriedades indexadas na consulta. Embora não seja um identificador regular, ele não exige aspas duplas.

 

 

 



