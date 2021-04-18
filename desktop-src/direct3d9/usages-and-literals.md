---
description: O uso é semelhante ao escopo de um parâmetro, pois ele define o escopo no qual o parâmetro é válido.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Usos e literais (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ca6f010d2c1e05055fd4427b8b5f7d4ab445ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105793847"
---
# <a name="usages-and-literals-direct3d-9"></a>Usos e literais (Direct3D 9)

O uso é semelhante ao escopo de um parâmetro, pois ele define o escopo no qual o parâmetro é válido.



|        |                                                                                                                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor  | Descrição                                                                                                                                                                                                                                                                         |
| const  | O parâmetro será constante dentro do escopo de todas as funções. (Observe que esses parâmetros ainda podem ser gravados com o [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), pois isso ocorre fora do escopo de todas as funções.) |
| shared | O parâmetro será compartilhado no pool de efeitos.                                                                                                                                                                                                                                    |
| static | O parâmetro será invisível para o aplicativo, ou seja, você não poderá acessá-los de [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).                                                                                                  |



 

Marcar um parâmetro como literal indica que seu valor nunca será alterado. Isso permite que o compilador de efeito faça uma otimização extra.

Somente os parâmetros de nível superior não compartilhados podem ser marcados como literais. Os parâmetros só podem ser marcados como literais com [**ID3DXEffectCompiler**](id3dxeffectcompiler.md). Valores literais não podem ser definidos com [**ID3DXEffect**](id3dxeffect.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



