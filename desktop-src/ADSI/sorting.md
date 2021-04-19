---
title: Classificação (ADSI)
description: Um cliente pode solicitar que um servidor Classifique o conjunto de resultados.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4ee790a646367366afe33639abd8f5aa57ed4f
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "105748337"
---
# <a name="sorting-adsi"></a>Classificação (ADSI)

Um cliente pode solicitar que um servidor Classifique o conjunto de resultados. É possível especificar:

-   Ordem de classificação: a ordem de classificação crescente ou decrescente pode ser especificada.
-   Atributos de classificação: vários atributos podem ser especificados em uma cadeia de caracteres de classificação. Por exemplo, classificar por sobrenome e, em seguida, primeiro nome.

Ao especificar a ordem de classificação, você deve tentar usar um dos atributos indexados. Caso contrário, o servidor deve calcular um conjunto de resultados completo antes de enviá-lo para o cliente. Isso é verdadeiro mesmo se você solicitou uma pesquisa paginada e especificou um tamanho de página.

> [!Note]  
> Nem todos os servidores de diretório dão suporte a várias classificações de atributo ou ordem de classificação.

 

 

 




