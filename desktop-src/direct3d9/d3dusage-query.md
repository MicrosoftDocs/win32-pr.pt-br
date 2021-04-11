---
description: Essas opções identificam os tipos de recursos de consulta.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f5dda7f84dfa36e4f3b7ece1b359a4841bbbf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089235"
---
# <a name="d3dusage_query"></a>\_Consulta D3DUSAGE

Essas opções identificam os tipos de recursos de consulta.



|                                            |                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definir                                   | Descrição                                                                                                                                                                                                                                                                                                                                         |
| \_Filtro de consulta do D3DUSAGE \_                    | Consulte o formato de recurso para ver se ele dá suporte a tipos de filtro de textura diferentes do \_ ponto D3DTEXF (que tem sempre suporte).                                                                                                                                                                                                                         |
| D3DUSAGE \_ consulta \_ LEGACYBUMPMAP             | Consulte o recurso sobre um mapa de relevo herdado.                                                                                                                                                                                                                                                                                                         |
| D3DUSAGE \_ consulta \_ POSTPIXELSHADER \_ Blending | Consulte o recurso para verificar o suporte para o suporte de mesclagem de sombreador de pixel de lançamento. Se [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) falhar com a \_ \_ \_ mesclagem POSTPIXELSHADER de consulta D3DUSAGE, não haverá suporte para operações de mesclagem de pixels post. Isso inclui teste alfa, sombra de pixel, mesclagem de destino de renderização, habilitação de gravação de cor e pontilhamento. |
| D3DUSAGE \_ consulta \_ SRGBREAD                  | Consulte o recurso para verificar se uma textura dá suporte à correção de gama durante uma operação de leitura.                                                                                                                                                                                                                                                        |
| D3DUSAGE \_ consulta \_ SRGBWRITE                 | Consulte o recurso para verificar se uma textura dá suporte à correção de gama durante uma operação de gravação.                                                                                                                                                                                                                                                       |
| D3DUSAGE \_ consulta \_ VERTEXTEXTURE             | Consulte o recurso para verificar o suporte para amostragem de textura de sombreador de vértice.                                                                                                                                                                                                                                                                            |
| D3DUSAGE \_ consulta \_ WRAPANDMIP                | Consulte o recurso para verificar o suporte para disposição de textura e mapeamento de MIP.                                                                                                                                                                                                                                                                          |



 

Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) para consultar o suporte de hardware para esses usos e alguns outros usos listados em [D3DUSAGE](d3dusage.md).

## <a name="constant-information"></a>Informações constantes



|                          |             |
|--------------------------|-------------|
| parâmetro                   | d3d9types. h |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
