---
description: Um efeito (que geralmente é armazenado em um arquivo com uma extensão de arquivo. FX) declara o estado do pipeline definido por um efeito.
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Formato de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c9511304a3c24784381092017659fb1a6c593808253383443c8e9f6917c2be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852817"
---
# <a name="effect-format-direct3d-10"></a>Formato de efeito (Direct3D 10)

Um efeito (que geralmente é armazenado em um arquivo com uma extensão de arquivo. FX) declara o estado do pipeline definido por um efeito. O estado do efeito pode ser basicamente dividido em três categorias:

-   [Variáveis](d3d10-effect-variable-syntax.md), que geralmente são declaradas na parte superior de um efeito.
-   [Funções](d3d10-effect-function-syntax.md), que implementam o código de sombreador ou são usadas como funções auxiliares por outras funções.
-   [Uma técnica](d3d10-effect-technique-syntax.md), que implementa sequências de renderização usando um ou mais efeitos aprovados. Cada passagem define um ou mais [grupos de Estados](d3d10-effect-states.md) e chama funções de sombreador.

![diagrama das categorias de estado de efeito](images/d3d10-effect-intro.png)

O diagrama anterior mostra as categorias de estado de efeito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de efeito](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



