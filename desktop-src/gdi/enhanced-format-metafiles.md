---
description: Metaarquivos Enhanced-Format
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Metaarquivos Enhanced-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae113c65e4dd05e67c155c2323698cd023191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967669"
---
# <a name="enhanced-format-metafiles"></a>Metaarquivos Enhanced-Format

O *metarquivo de formato avançado* consiste nos seguintes elementos:

-   Um cabeçalho
-   Uma tabela de identificadores para objetos GDI
-   Uma paleta privada
-   Uma matriz de registros de metarquivo

Os metaarquivos aprimorados fornecem uma verdadeira independência de dispositivo. Você pode considerar a imagem armazenada em um metarquivo avançado como um "instantâneo" da exibição de vídeo feita em um momento específico. Esse "instantâneo" mantém suas dimensões, independentemente de onde aparecem em uma impressora, em uma plotadora, na área de trabalho ou na área cliente de qualquer aplicativo.

Você pode usar os metaarquivos aprimorados para armazenar uma imagem criada usando as funções GDI (incluindo novas funções de caminho e transformação). Como o formato de metarquivo avançado é padronizado, as imagens armazenadas nesse formato podem ser copiadas de um aplicativo para outro; e, como as imagens são verdadeiramente independentes de dispositivo, eles têm a garantia de manter sua forma e proporção em qualquer dispositivo de saída.

-   [Registros de metarquivo avançados](enhanced-metafile-records.md)
-   [Criação de metarquivo aprimorada](enhanced-metafile-creation.md)
-   [Operações de metarquivo aprimoradas](enhanced-metafile-operations.md)

 

 



