---
title: fase-PS
description: A instrução Phase marca a transição entre a fase 1 e a fase 2. Se nenhuma instrução de fase estiver presente, o sombreador inteiro será executado como se fosse um sombreador da fase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9a16b01e186de5645ffe65e003ebbe6defca2d5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006917"
---
# <a name="phase---ps"></a>fase-PS

A instrução Phase marca a transição entre a fase 1 e a fase 2. Se nenhuma instrução de fase estiver presente, o sombreador inteiro será executado como se fosse um sombreador da fase 2.

Esta instrução aplica-se somente à versão 1 \_ 4.

## <a name="syntax"></a>Sintaxe


```
phase
```



## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| fase                 |      |      |      | x    |      |      |       |      |       |



 

As instruções do sombreador que ocorrem antes da instrução Phase são instruções da fase 1. Todas as outras instruções são instruções da fase 2. Tendo duas fases para obter instruções, o número máximo de instruções por sombreador é aumentado.

O efeito coverso da transição de fase é que o componente alfa de [registros temporários](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) não persiste na transição. Em outras palavras, o componente alfa deve ser reinicializado após a instrução phase.

## <a name="example"></a>Exemplo

Este exemplo mostra como agrupar instruções como instruções da fase 1 ou 2 em um sombreador.

A instrução Phase também é normalmente chamada de marcador de fase porque marca a transição entre as instruções da fase 1 e 2. Em um \_ sombreador de 4 pixels de versão 1, se o marcador de fase não estiver presente, o sombreador será executado como se ele fosse executado na fase 2. Isso é importante porque há diferenças entre as instruções da fase 1 e 2 e o registro da disponibilidade. As diferenças são indicadas em toda a seção de referência.


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

 

 




