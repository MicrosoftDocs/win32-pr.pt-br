---
title: defi-PS
description: Define um valor constante inteiro, que deve ser carregado sempre que um sombreador for definido como um dispositivo.
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084762"
---
# <a name="defi---ps"></a>defi-PS

Define um valor constante inteiro, que deve ser carregado sempre que um sombreador for definido como um dispositivo.

## <a name="syntax"></a>Syntax



| defi DST, inteirovalue |
|------------------------|



 

-   DST é o registro de destino.
-   integerValue é um valor inteiro constante.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| defi                  |      |      |      |      |      | x    | x     | x    | x     |



 

A instrução defi define uma constante de sombreador cujo valor é carregado sempre que um sombreador é definido como um dispositivo. Elas são chamadas de constantes imediatas. Constantes imediatas têm precedência sobre constantes definidas pelo método de API SetPixelShaderConstantB.

Há duas maneiras de definir uma constante em um sombreador.

1.  Use defi para definir a constante diretamente dentro de um sombreador.
2.  Use os métodos de API para definir uma constante.
    -   Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) para definir uma constante booliana.
    -   Use [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) para definir uma constante de ponto flutuante.
    -   Use [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) para definir uma constante de inteiro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 