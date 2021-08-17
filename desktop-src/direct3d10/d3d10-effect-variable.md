---
description: Essas constantes se aplicam a variáveis de efeito.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: D3D10_EFFECT_VARIABLE constantes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7541253fffd6671e01a8da38c06fd15924d45b461d5acc0e468fd17660746f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736065"
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

 

 



