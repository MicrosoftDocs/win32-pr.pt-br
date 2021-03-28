---
title: vs
description: Esta instrução especifica o número de versão do sombreador. Essa instrução funciona em todas as versões de sombreador.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365281"
---
# <a name="vs"></a>vs

Esta instrução especifica o número de versão do sombreador. Essa instrução funciona em todas as versões de sombreador.

## <a name="syntax"></a>Syntax


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a>Argumentos de entrada

Os argumentos de entrada contêm um único número de versão principal com um único número de subversão. As combinações permitidas são listadas na tabela a seguir.



| Versões principais | Sub-versões                   |
|---------------|--------------------------------|
| 1             | 1                              |
| 2             | 0, SW (software), x (estendido) |
| 3             | 0, SW (software)               |



 

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| vs                     | x    | x    | x    | x     | x    | x     |



 

Essa instrução deve ser a primeira instrução que não seja de comentário em um sombreador de vértice.

Essa instrução tem suporte em todas as versões de sombreador de vértice.

As versões aceleradas por hardware do software (versões sem \_ SW no número de versão) podem processar vértices com accelearation de hardware ou usar o processamento de vértice de software. Versões de software (versões com \_ SW no número de versão) processam vértices somente com software.

## <a name="examples"></a>Exemplos

Este exemplo parcial declara um sombreador de vértice da versão 1 \_ 1.


```
vs_1_1
```



Este exemplo parcial declara um sombreador de vértice de software da versão 2.


```
vs_2_sw
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




