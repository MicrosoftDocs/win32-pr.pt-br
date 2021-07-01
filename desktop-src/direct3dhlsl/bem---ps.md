---
title: bem - ps
description: Aplicar uma transformação de mapa de ambiente de aumento falso.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1adae07e3e2ebbca085981ca03a3b6449e2ffd9d
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129925"
---
# <a name="bem---ps"></a>bem - ps

Aplicar uma transformação de mapa de ambiente de aumento falso.

## <a name="syntax"></a>Sintaxe



| bem dst.rg, src0, src1 |
|------------------------|



 

onde

-   dst.rg dst é o registro de destino. A máscara de gravação do componente vermelho e verde deve ser usada.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| bem                   |      |      |      | x    |      |      |       |      |       |



 

Essa instrução executa o cálculo a seguir.


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



Regras para usar bem:

1.  bem deve aparecer na primeira fase de um sombreador (ou seja, antes de um marcador de fase).
2.  bem consome dois slots de instrução aritmética.
3.  Somente um uso dessa instrução é permitido por sombreador.
4.  A máscara de gravação de destino deve ser .rg /.xy.
5.  Essa instrução não pode ser co-emitida.
6.  Além da restrição de que a máscara de gravação de destino seja .rg, os modificadores em src0 de origem, src1 e modificadores de instrução não são restritos.

## <a name="instruction-information"></a>Informações de instrução



| Requisito                         | Valor           |
|--------------------------|------------|
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




