---
title: Rep-PS
description: Iniciar um representante... endrep-bloco de PS.
ms.assetid: vs|directx_sdk|~\rep___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6873a6aee9e31b1f28ba2755b1869cddb177306
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638864"
---
# <a name="rep---ps"></a>Rep-PS

Iniciar um representante... [endrep-bloco de PS](endrep---ps.md) .

## <a name="syntax"></a>Syntax



| representante i\# |
|---------|



 

onde eu \# é um registro de número inteiro que especifica a contagem de repetições no componente. x. Consulte [o registro de inteiro constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| representante                   |      |      |      |      |      | x    | x     | x    | x     |



 

-   i \# . x especifica a contagem de iteração. O intervalo legal é \[ 0, 255 \] . Observe que essa instrução não incrementa nem Decrementa o valor de i \# . x.
-   i \# . yzw não são usadas pelo bloco REPEAT.
-   Os blocos de repetição podem ser aninhados. Consulte [limitações de controle de fluxo](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   Os blocos de repetição podem estar completamente dentro de um \* bloco If ou completamente em torno dele. Não é permitido ampliar.
-   O uso do mesmo i \# para instruções de representante diferentes ou aninhadas é bem-cada loop será iterado com base na contagem especificada.

## <a name="example"></a>Exemplo


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




