---
title: texreg2rgb-PS
description: Interpreta os componentes de cor vermelho, verde e azul (RGB) do registro de origem como dados de endereço de textura para obter amostras da textura no estágio correspondente ao número de registro de destino. O resultado é armazenado no registro de destino.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8bcd2bbd7e57ba9dc692f34404a5610cdc517f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104498946"
---
# <a name="texreg2rgb---ps"></a>texreg2rgb-PS

Interpreta os componentes de cor vermelho, verde e azul (RGB) do registro de origem como dados de endereço de textura para obter amostras da textura no estágio correspondente ao número de registro de destino. O resultado é armazenado no registro de destino.

## <a name="syntax"></a>Syntax



| texreg2rgb DST, src |
|---------------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2rgb            |      | x    | x    |      |      |      |       |      |       |



 

Essa instrução é útil para operações de remapeamento de espaço de cor. Ele dá suporte a coordenadas bidimensionais (2D) e tridimensionais (3D). Ele pode ser usado exatamente como [texreg2ar-PS](texreg2ar---ps.md) ou [texreg2gb-PS](texreg2gb---ps.md) para remapear dados 2D. No entanto, essa instrução também dá suporte a dados 3D para que ele possa ser usado com mapas de cubo e texturas de volume 3D.

Veja a seguir um exemplo da seqüência da instrução.


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



Veja mais detalhes sobre como o remapeamento é realizado.

<dl> A primeira instrução carrega a cor de textura (RGBA) em registrar TN  
Tex TN  
A segunda instrução remapeia a cor  
t (m)<sub>RGBA</sub> = TextureSample (estágio m)<sub>RGBA</sub> usando t (n)<sub>RGB</sub> como coordenadas
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




