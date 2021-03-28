---
title: Swizzling de registro de origem (referência de HLSL VS)
description: Antes de uma instrução ser executada, os dados em um registro de origem são copiados para um registro temporário. Swizzling refere-se à capacidade de copiar qualquer componente de registro de origem para qualquer componente de registro temporário. Swizzling não afeta os dados de registro de origem.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c075d8ff47b1f76adf378b6a583cd4d675651a87
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104365313"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a>Swizzling de registro de origem (referência de HLSL VS)

Antes de uma instrução ser executada, os dados em um registro de origem são copiados para um registro temporário. Swizzling refere-se à capacidade de copiar qualquer componente de registro de origem para qualquer componente de registro temporário. Swizzling não afeta os dados de registro de origem.

## <a name="component-swizzling"></a>Swizzling de componente

Conforme mostrado na tabela a seguir, swizzling pode ser aplicado aos componentes individuais dos dados de registro de origem (onde é um dos registradores de entrada válidos do sombreador de vértice [-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).



| Modificador de componente                 | Description    |
|------------------------------------|----------------|
| r. \[ xyzw \] \[ xyzw \] \[ xyzw \] \[ xyzw\] | Swizzle de origem |



 

-   Todos os quatro componentes são sempre copiados. Se menos de quatro componentes forem especificados, o último componente será repetido (XY significa. xyyy). Se nenhum componente for especificado, x será repetido (. xxxx).
-   Os componentes podem aparecer em qualquer ordem. V0. YWX resulta em V0. ywxx.
-   Os componentes RGBA podem ser usados respectivamente para xyzw (r para x, g para b, etc.).
-   Essas instruções implementam a origem-registrar um único componente swizzles: exp, expp, log, LogP, pow, RCP, RSQ. O resultado dessas instruções é copiado para todos os quatro componentes de registro de destino.

Swizzling não pode ser usado nas instruções [M3X2-vs](m3x2---vs.md), [m3x3-vs](m3x3---vs.md), [m4x3-vs](m4x3---vs.md)e [m4x4-vs](m4x4---vs.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




