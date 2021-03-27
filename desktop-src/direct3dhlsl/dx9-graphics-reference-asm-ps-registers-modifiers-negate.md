---
title: Negação de registro de origem
description: Executa um negação (y x) em todos os componentes de registro.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005408"
---
# <a name="source-register-negate"></a>Negação de registro de origem

Executa um negação (y =-x) em todos os componentes de registro.

## <a name="syntax"></a>Syntax


```
- register
```



## <a name="registers"></a>Registros

Registro de origem. Para obter mais informações sobre tipos de registro, consulte [PS \_ 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Comentários

O conteúdo do registro não é alterado. O modificador é aplicado somente aos dados lidos do registro. A operação de negação é aplicada a todos os quatro canais de cores (RGBA).

Essa operação é executada após qualquer outro modificador presente no mesmo argumento.

Esse modificador é mutuamente exclusivo com o [registro de origem inverter](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) para que não possa ser aplicado ao mesmo registro.

Este modificador é para uso somente com instruções aritméticas.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar esse modificador.


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




