---
title: Negação do registro de origem
description: Executa uma negação (y -x), em todos os componentes de registro.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94898dbbf193254165850ee696d2fea72d6d446908021dfbb5fd32f1920b7010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512947"
---
# <a name="source-register-negate"></a>Negação do registro de origem

Executa uma negação (y = -x), em todos os componentes de registro.

## <a name="syntax"></a>Syntax


```
- register
```



## <a name="registers"></a>Registros

Registro de Origem. Para obter mais informações sobre tipos de registro, [consulte ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Comentários

O conteúdo do registro não é alterado. O modificador é aplicado somente aos dados lidos do registro. A operação de negação é aplicada a todos os quatro canais de cores (RGBA).

Essa operação é executada após qualquer outro modificador presente no mesmo argumento.

Esse modificador é mutuamente exclusivo com a [Inversão do Registro](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) de Origem, portanto, ele não pode ser aplicado ao mesmo registro.

Esse modificador é para uso somente com instruções aritméticas.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar esse modificador.


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




