---
description: Essas constantes se aplicam a variáveis de efeito.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: D3D10_EFFECT_VARIABLE constantes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6367fe89f66ff90991b8493a03a6d1b4244f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784562"
---
# <a name="d3d10_effect_variable-constants"></a>\_Constantes variáveis de efeito d3d10 \_

Essas constantes se aplicam a variáveis de efeito.



| \#definir                                       | Descrição  | Valor                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Anotação de \_ variável de efeito d3d10 \_            | 1 << 0 | Indica que esta é uma anotação ou uma variável global.                                                                                                                                                                                                        |
| Variável de efeito de D3D10 em \_ \_ \_ pool                | 1 << 1 | Indica que essa variável ou buffer de constante reside em um pool de efeitos. Se esse sinalizador não for definido, a variável residirá em um efeito autônomo ou um efeito filho (os efeitos autônomos retornarão false de [**ID3D10Effect:: ispool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool). |
| \_Ponto de \_ \_ ligação explícito \_ da variável de efeito d3d10 \_ | 1 << 2 | Indica que a variável foi explicitamente associada usando a palavra-chave Register.                                                                                                                                                                                 |



 

Esses sinalizadores são definidos como macros em d3d10effect. h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes de efeito (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



