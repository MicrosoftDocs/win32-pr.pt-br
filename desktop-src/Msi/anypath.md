---
description: O tipo de dados AnyPath é uma cadeia de caracteres de texto que contém um caminho completo ou um caminho relativo.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab5d8e7aaf4e92c2b33379b92b00263df07366ff340346aa19518478f8f2394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045776"
---
# <a name="anypath"></a>AnyPath

O tipo de dados AnyPath é uma cadeia de caracteres de texto que contém um caminho completo ou um caminho relativo. Ao especificar um caminho relativo, você pode incluir um nome de arquivo longo com o nome de arquivo curto separando os nomes curtos e longos com uma barra vertical ( \| ). Observe que você não pode especificar vários níveis de um diretório ou caminhos totalmente qualificados dessa maneira. O caminho pode conter propriedades entre colchetes ( \[ \] ).

Exemplos de dados AnyPath válidos:

-   \\\\temp \\ de \\ compartilhamento de servidor
-   c: \\ temp
-   \\Temp
-   projec~1 \| Project Status

Exemplos de dados AnyPath inválidos:

-   c: \\ temp \\ projec~1 \| c: temp one Project \\ \\ Status
-   \\temp \\ projec~1 \| \\ temp one Project \\ Status

 

 



