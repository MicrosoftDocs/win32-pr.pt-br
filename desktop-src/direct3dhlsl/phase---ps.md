---
title: phase - ps
description: A instrução de fase marca a transição entre a fase 1 e a fase 2. Se nenhuma instrução de fase estiver presente, o sombreador inteiro será executado como se fosse um sombreador de fase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aac29792274a36ad4bb7266ffa02d0ea5d2bb1b6cec8efe2db213e9b0dd4890b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118088689"
---
# <a name="phase---ps"></a>phase - ps

A instrução de fase marca a transição entre a fase 1 e a fase 2. Se nenhuma instrução de fase estiver presente, o sombreador inteiro será executado como se fosse um sombreador de fase 2.

Essa instrução se aplica somente à versão \_ 1 4.

## <a name="syntax"></a>Sintaxe


```
phase
```



## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| fase                 |      |      |      | x    |      |      |       |      |       |



 

Instruções de sombreador que ocorrem antes da instrução de fase são instruções da fase 1. Todas as outras instruções são instruções da fase 2. Ao ter duas fases para obter instruções, o número máximo de instruções por sombreador é aumentado.

O efeito colateral infelizmente da transição de fase é que o componente alfa dos registros [temporários](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) não persistem durante a transição. Em outras palavras, o componente alfa deve ser reinicializado após a instrução de fase.

## <a name="example"></a>Exemplo

Este exemplo mostra como agrupar instruções como instruções da fase 1 ou 2 em um sombreador.

A instrução de fase também é normalmente chamada de marcador de fase porque marca a transição entre as instruções da fase 1 e 2. Em um sombreador de pixel versão 1 4, se o marcador de fase não estiver presente, o sombreador será executado como se estivesse em execução \_ na fase 2. Isso é importante porque há diferenças entre as instruções da fase 1 e 2 e a disponibilidade do registro. As diferenças são notadas em toda a seção de referência.


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




