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
ms.openlocfilehash: 03dd2d9051c185d1be1ccb6fce18549bf5aa3414975c9a600bb8f8c47f78d4c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854546"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a>Swizzling de registro de origem (referência de HLSL VS)

Antes de uma instrução ser executada, os dados em um registro de origem são copiados para um registro temporário. Swizzling refere-se à capacidade de copiar qualquer componente de registro de origem para qualquer componente de registro temporário. Swizzling não afeta os dados de registro de origem.

## <a name="component-swizzling"></a>Swizzling de componente

Conforme mostrado na tabela a seguir, swizzling pode ser aplicado aos componentes individuais dos dados de registro de origem (onde é um dos registradores de entrada válidos do sombreador de vértice [-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).



| Modificador de componente                 | Descrição    |
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

 

 




