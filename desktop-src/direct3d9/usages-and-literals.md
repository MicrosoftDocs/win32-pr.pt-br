---
description: O uso é semelhante ao escopo de um parâmetro, pois define o escopo no qual o parâmetro é válido.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Usos e literais (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8c9fa8eb30726e783ce763ec8700f715dbd5d2b85ff3bf98340cf604e8e2f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026006"
---
# <a name="usages-and-literals-direct3d-9"></a>Usos e literais (Direct3D 9)

O uso é semelhante ao escopo de um parâmetro, pois define o escopo no qual o parâmetro é válido.



| Valor  | Descrição                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| const  | O parâmetro será constante dentro do escopo de todas as funções. (Observe que esses parâmetros ainda podem ser gravados em [**com ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), porque isso ocorre fora do escopo de todas as funções.) |
| shared | O parâmetro será compartilhado no pool de efeitos.                                                                                                                                                                                                                                    |
| static | O parâmetro será invisível para o aplicativo, ou seja, você não poderá acessá-los de [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler.**](id3dxeffectcompiler.md)                                                                                                  |



 

Marcar um parâmetro como literal indica que seu valor nunca será alteração. Isso permite que o compilador de efeito faça otimização extra.

Somente parâmetros de nível superior não compartilhados podem ser marcados como literais. Os parâmetros só podem ser marcados como literais [**com ID3DXEffectCompiler.**](id3dxeffectcompiler.md) Os valores literais não podem ser definidos [**com ID3DXEffect.**](id3dxeffect.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



