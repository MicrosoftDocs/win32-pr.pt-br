---
title: Escala de registro de origem x 2
description: Multiplique o valor por dois antes de usá-lo na instrução.
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104967053"
---
# <a name="source-register-scale-x-2"></a>Escala de registro de origem x 2

Multiplique o valor por dois antes de usá-lo na instrução.

## <a name="syntax"></a>Syntax


```
register_x2
```



## <a name="register"></a>Registre-se

Registro de origem. Para obter mais informações sobre tipos de registro, consulte [PS \_ 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Comentários

O conteúdo do registro não é alterado. O modificador é aplicado somente aos dados lidos do registro.

Esse modificador é mutuamente exclusivo com o [registro de origem inverter](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)e, portanto, não pode ser aplicado ao mesmo registro.

Este modificador só está disponível para instruções aritméticas na versão 1 \_ 4.

## <a name="example"></a>Exemplo

Este exemplo amostra uma textura, converte dados no intervalo de-1 a + 1 e calcula um produto de ponto.


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




