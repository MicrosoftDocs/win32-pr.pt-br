---
title: Inverter registro de origem
description: Executa um cálculo (1 valor) para cada canal do registro especificado.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104967054"
---
# <a name="source-register-invert"></a>Inverter registro de origem

Executa um cálculo (1 valor) para cada canal do registro especificado.

## <a name="syntax"></a>Syntax


```
1 - register
```



## <a name="registers"></a>Registros

Registro de origem. Para obter mais informações sobre tipos de registro, consulte [PS \_ 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Comentários

O conteúdo do registro não é alterado. O modificador é aplicado somente aos dados lidos do registro. A operação Inverter é aplicada a todos os quatro canais de cor (RGBA).

Esse modificador só pode ser usado com instruções aritméticas. Além disso, esse modificador não pode ser combinado com a outra [máscara de gravação de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).

## <a name="example"></a>Exemplo

Este exemplo usa inversão para gerar o complemento do registro R1.


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




