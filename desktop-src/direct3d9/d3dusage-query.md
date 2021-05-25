---
description: Essas opções identificam os tipos de recursos de consulta.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038cb64b1ad4f5f7ee2dd78ffc2e2a5ebab90d0e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342981"
---
# <a name="d3dusage_query"></a>CONSULTA D3DUSAGE \_

Essas opções identificam os tipos de recursos de consulta.



| \#Definir                                   | Descrição                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FILTRO DE CONSULTA D3DUSAGE \_ \_                    | Consulte o formato do recurso para ver se ele dá suporte a tipos de filtro de textura diferentes de D3DTEXF \_ POINT (que sempre tem suporte).                                                                                                                                                                                                                         |
| D3DUSAGE \_ QUERY \_ LEGACYBUMPMAP             | Consulte o recurso sobre um mapa de aumento herdado.                                                                                                                                                                                                                                                                                                         |
| D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ BLENDING | Consulte o recurso para verificar o suporte para suporte à combinação de sombreador de pixel pós-pixel. Se [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) falhar com D3DUSAGE \_ QUERY \_ POSTPIXELSHADER BLENDING, não há suporte para operações pós-mesclagem de \_ pixels. Isso inclui teste alfa, pixel pixel pixel, mesclagem de destino de renderização, habilitação de gravação de cor e dithering. |
| CONSULTA D3DUSAGE \_ \_ SRGBREAD                  | Consulte o recurso para verificar se uma textura dá suporte à correção gama durante uma operação de leitura.                                                                                                                                                                                                                                                        |
| D3DUSAGE \_ QUERY \_ SRGBWRITE                 | Consulte o recurso para verificar se uma textura dá suporte à correção gama durante uma operação de gravação.                                                                                                                                                                                                                                                       |
| D3DUSAGE \_ QUERY \_ VERTEXTEXTURE             | Consulte o recurso para verificar o suporte para amostragem de textura do sombreador de vértice.                                                                                                                                                                                                                                                                            |
| D3DUSAGE \_ QUERY \_ WRAPANDMIP                | Consulte o recurso para verificar o suporte para disposição de textura e mapeamento de MIP.                                                                                                                                                                                                                                                                          |



 

Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) para consultar o suporte de hardware para esses usos e alguns outros usos listados em [D3DUSAGE](d3dusage.md).

## <a name="constant-information"></a>Informações constantes



| Requisito                         | Valor            |
|--------------------------|-------------|
| parâmetro                   | d3d9types. h |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
