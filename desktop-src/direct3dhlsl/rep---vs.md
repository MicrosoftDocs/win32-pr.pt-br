---
title: rep - vs
description: Iniciar um representante... bloco endrep.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e800f2ef313cd5c9a4fc90d7205502db5532ae24f51ec0f1255d05cc9a589bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853786"
---
# <a name="rep---vs"></a>rep - vs

Iniciar um representante... [bloco endrep.](endrep---vs.md)

## <a name="syntax"></a>Syntax



| rep i\# |
|---------|



 

em que i \# é um registro inteiro que especifica a contagem de repetição no componente .x. Consulte [Registro de inteiro constante.](dx9-graphics-reference-asm-vs-registers-constant-integer.md)

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Representante                    |      | x    | x    | x     | x    | x     |



 

-   i \# .x especifica a contagem de iteração. O intervalo legal é \[ 0, 255 \] . Observe que essa instrução não incrementa nem diminui o valor de i \# .x.
-   i \# .yzw não são usados pelo bloco de repetição.
-   Blocos de repetição podem ser aninhados. Consulte [Flow limites de aninhamento de controle.](dx9-graphics-reference-asm-vs-instructions-flow-control.md)
-   Blocos de repetição podem estar completamente dentro de um bloco if \* ou completamente ao redor dele. Não é permitido nenhum retardo.
-   Usar o mesmo i para instruções de representante diferentes ou aninhados é bom – cada loop iterará com \# base na contagem especificada.

## <a name="example"></a>Exemplo


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




