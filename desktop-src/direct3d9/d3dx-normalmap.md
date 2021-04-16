---
description: Constantes de geração de mapas normais.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37985456e81b20af9b3e4396d10045d5e58c9b7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105765123"
---
# <a name="d3dx_normalmap"></a>D3DX \_ NormalMap

Constantes de geração de mapas normais.



|                                     |                                                                                                                                                                                                    |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definir                            | Descrição                                                                                                                                                                                        |
| D3DX \_ NormalMap \_ Mirror \_ U          | Indica que os pixels da borda da textura no eixo u devem ser espelhados, não encapsulados.                                                                                                   |
| D3DX \_ NormalMap \_ Mirror \_ V          | Indica que os pixels da borda da textura no eixo v devem ser espelhados, não encapsulados.                                                                                                   |
| D3DX \_ NormalMap \_ Mirror             | O mesmo que especificar D3DX \_ NormalMap \_ espelho \_ U \| D3DX \_ NormalMap \_ Mirror \_ V.                                                                                                                       |
| D3DX \_ NormalMap \_ INVERTSIGN         | Inverte a direção de cada normal.                                                                                                                                                              |
| D3DX \_ NormalMap \_ \_ oclusão Compute | Computa o termo oclusão por pixel e o codifica no Alpha. Um alfa de 1 significa que o pixel não é obscurecido de nenhuma forma e um alfa de 0 significa que o pixel está completamente obscurecido. |



 

## <a name="constant-information"></a>Informações constantes



|                          |            |
|--------------------------|------------|
| parâmetro                   | d3dx9tex. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[**D3DXComputeNormalMap**](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



