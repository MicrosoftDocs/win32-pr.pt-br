---
title: Classificação (ADSI)
description: Um cliente pode solicitar um servidor para classificar o conjunto de resultados.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555b4b6f1868b2e4fddc1891cdf349ef6f44bc47dca6eb80e021ec49cb91b5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082220"
---
# <a name="sorting-adsi"></a>Classificação (ADSI)

Um cliente pode solicitar um servidor para classificar o conjunto de resultados. É possível especificar:

-   Ordem de classificação: a ordem de classificação crescente ou decrescente pode ser especificada.
-   Classificar atributos: vários atributos podem ser especificados em uma cadeia de caracteres de classificação. Por exemplo, classificar por Sobrenome e, em seguida, Nome.

Ao especificar a ordem de classificação, você deve tentar usar um dos atributos indexados. Caso contrário, o servidor deverá calcular um conjunto de resultados completo antes de enviá-lo ao cliente. Isso é verdadeiro mesmo que você tenha solicitado uma pesquisa por página e especificado um tamanho de página.

> [!Note]  
> Nem todos os servidores de diretório suportam vários tipos de atributo ou ordem de classificação.

 

 

 




