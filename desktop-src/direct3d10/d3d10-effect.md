---
description: Essas constantes usadas ao criar um efeito para definir o comportamento de compilação ou o comportamento de efeito de runtime.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: D3D10_EFFECT constantes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3738a95a843020f7c0f8af30e8c5d035f0a86ac7098d36cae422eb01ed4dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736045"
---
# <a name="d3d10_effect-constants"></a>Constantes D3D10 \_ EFFECT

Essas constantes usadas ao criar um efeito para definir o comportamento de compilação ou o comportamento de efeito de runtime.



| \#Definir                                 | Valor        | Descrição                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EFEITO D3D10 \_ \_ EFEITO COMPILAR EFEITO \_ \_ FILHO    | 1 << 0 | Compile o arquivo .fx em um efeito filho. Os efeitos filho não têm inicializações para nenhum valor compartilhado porque eles são inicializados no pool de efeitos.                                                                                                           |
| D3D10 \_ EFFECT \_ COMPILE \_ ALLOW \_ SLOW \_ OPS | 1 << 1 | Por padrão, o modo de desempenho está habilitado. O modo de desempenho não permite objetos de estado mutáveis impedindo que expressões não literais apareçam em definições de objeto de estado. Especificar esse sinalizador desabilitará o modo e permitirá objetos de estado mutáveis. |
| THREAD ÚNICO DO EFEITO D3D10 \_ \_ \_          | 1 << 3 | Não tente sincronizar com outros threads carregando efeitos no mesmo pool.                                                                                                                                                                        |



 

Essas constantes são definidas como macros em d3d10effect.h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes de efeito (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



