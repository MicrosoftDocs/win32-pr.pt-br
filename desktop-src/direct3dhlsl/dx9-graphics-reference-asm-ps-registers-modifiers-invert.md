---
title: Inversão do Registro de Origem
description: Executa um cálculo (1 – valor) para cada canal do registro especificado.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a391219f085c18a4c8bf2925a248800b6a26838cc6e2b8556551eb98b5335241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562766"
---
# <a name="source-register-invert"></a>Inversão do Registro de Origem

Executa um cálculo (1 – valor) para cada canal do registro especificado.

## <a name="syntax"></a>Syntax


```
1 - register
```



## <a name="registers"></a>Registros

Registro de Origem. Para obter mais informações sobre tipos de registro, [consulte ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Comentários

O conteúdo do registro não é alterado. O modificador é aplicado somente aos dados lidos do registro. A operação de inversão é aplicada a todos os quatro canais de cores (RGBA).

Esse modificador só pode ser usado com instruções aritméticas. Além disso, esse modificador não pode ser combinado com a outra Máscara de Gravação do Registro [de Destino.](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)

## <a name="example"></a>Exemplo

Este exemplo usa inversão para gerar o complemento do registro r1.


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




