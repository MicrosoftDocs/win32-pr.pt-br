---
description: Constantes de geração de mapas normais.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4263237cedf92a5e322f2fe139e9afe2297f6b9b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342851"
---
# <a name="d3dx_normalmap"></a>D3DX \_ NORMALMAP

Constantes de geração de mapas normais.



| \#Definir                            | Descrição                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX \_ NORMALMAP \_ MIRROR \_ U          | Indica que os pixels fora da borda da textura no eixo u devem ser espelhados, não empacotados.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR \_ V          | Indica que os pixels fora da borda da textura no eixo v devem ser espelhados, não empacotados.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR             | O mesmo que especificar D3DX \_ NORMALMAP \_ MIRROR U \_ \| D3DX \_ NORMALMAP MIRROR \_ \_ V.                                                                                                                       |
| D3DX \_ NORMALMAP \_ INVERTSIGN         | Inverte a direção de cada normal.                                                                                                                                                              |
| OCLUSÃO DE COMPUTAÇÃO DE NORMALMAP D3DX \_ \_ \_ | Calcula o termo de oclusão por pixel e o codifica no alfa. Um alfa de 1 significa que o pixel não é obscurecido de nenhuma maneira, e um alfa de 0 significa que o pixel está completamente obscurecido. |



 

## <a name="constant-information"></a>Informações constantes



| Requisito                         | Valor           |
|--------------------------|------------|
| parâmetro                   | d3dx9tex.h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[**D3DXComputeNormalMap**](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



