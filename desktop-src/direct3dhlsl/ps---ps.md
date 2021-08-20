---
title: ps
description: Essa instrução especifica o número de versão do sombreador e funciona em todas as versões do sombreador.
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06e070c16c482038097245325d884ef6b71d2249afb2aa89ad5ec1d37f86c9e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906343"
---
# <a name="ps"></a>ps

Essa instrução especifica o número de versão do sombreador e funciona em todas as versões do sombreador.

## <a name="syntax"></a>Syntax


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a>Argumentos de entrada

Os argumentos de entrada contêm um único número de versão principal com um único número de sub-versão. As combinações que permitem são listadas na tabela a seguir.



| Versões principais | Subversões                   |
|---------------|--------------------------------|
| 1             | 1, 2, 3, 4                     |
| 2             | 0, x (estendido), sw (software) |
| 3             | 0, sw (software)               |



 

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| ps                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Essa instrução deve ser a primeira instrução sem comentários em um sombreador de pixel.

As versões aceleradas de hardware do software (versões sem sw no número de versão), podem processar vértices com aceleração de hardware ou usar o processamento de \_ vértice de software. As versões de software \_ (versões com sw no número de versão) processam vértices somente com software.

## <a name="examples"></a>Exemplos

Este exemplo parcial declara um sombreador de pixel versão \_ 11.


```
ps_1_1
```



Este exemplo parcial declara um sombreador de \_ 14 pixels versão.


```
ps_1_4
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




