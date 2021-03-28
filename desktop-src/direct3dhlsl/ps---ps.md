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
ms.openlocfilehash: bdf251d8b5618916365348ab3bf62a89ea552de1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988611"
---
# <a name="ps"></a>ps

Essa instrução especifica o número de versão do sombreador e funciona em todas as versões do sombreador.

## <a name="syntax"></a>Syntax


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a>Argumentos de entrada

Os argumentos de entrada contêm um único número de versão principal com um único número de subversão. As combinações permitidas são listadas na tabela a seguir.



| Versões principais | Sub-versões                   |
|---------------|--------------------------------|
| 1             | 1, 2, 3, 4                     |
| 2             | 0, x (estendido), SW (software) |
| 3             | 0, SW (software)               |



 

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| ps                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Essa instrução deve ser a primeira instrução que não seja de comentário em um sombreador de pixel.

As versões aceleradas por hardware do software (versões sem \_ SW no número de versão) podem processar vértices com accelearation de hardware ou usar o processamento de vértice de software. Versões de software (versões com \_ SW no número de versão) processam vértices somente com software.

## <a name="examples"></a>Exemplos

Este exemplo parcial declara um sombreador de pixel da versão 1 \_ 1.


```
ps_1_1
```



Este exemplo parcial declara um \_ sombreador de 4 pixels da versão 1.


```
ps_1_4
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




