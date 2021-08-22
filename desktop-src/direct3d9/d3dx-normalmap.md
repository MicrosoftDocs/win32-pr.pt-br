---
description: Constantes de geração de mapas normais.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d3a3d2f35fa409e4432dd7600cb544df25110d10aa9af7f5ee18fd622ea1309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374946"
---
# <a name="d3dx_normalmap"></a>D3DX \_ NORMALMAP

Constantes de geração de mapas normais.



| \#Definir                            | Descrição                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX \_ NORMALMAP \_ MIRROR \_ U          | Indica que os pixels fora da borda da textura no eixo u devem ser espelhados, não empacotados.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR \_ V          | Indica que os pixels fora da borda da textura no eixo v devem ser espelhados, não empacotados.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR             | O mesmo que especificar D3DX \_ NORMALMAP \_ MIRROR U \_ \| D3DX \_ NORMALMAP MIRROR \_ \_ V.                                                                                                                       |
| D3DX \_ NORMALMAP \_ INVERTSIGN         | Inverte a direção de cada normal.                                                                                                                                                              |
| OCLUSÃO DE COMPUTAÇÃO DE NORMALMAP D3DX \_ \_ \_ | Calcula o termo de oclusão por pixel e o codifica no alfa. Um alfa de 1 significa que o pixel não é obscurecido de nenhuma forma e um alfa de 0 significa que o pixel está completamente obscurecido. |



 

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

 

 



