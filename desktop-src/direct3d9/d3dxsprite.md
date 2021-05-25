---
description: 'Os sinalizadores a seguir são usados para especificar opções de renderização de sprite para o parâmetro flags no método Begin:'
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23301f003eee54a7efbb933237576edd2946fcac
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343541"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

Os sinalizadores a seguir são usados para especificar opções de renderização de sprite para o parâmetro flags no [**método Begin:**](id3dxsprite--begin.md)



| \#Definir                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXSPRITE \_ DONOTSAVESTATE           | O estado do dispositivo não deve ser salvo ou restaurado quando [**Begin**](id3dxsprite--begin.md) ou [**End**](id3dxsprite--end.md) é chamado.                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE | O estado de renderização do dispositivo não deve ser alterado [**quando Begin**](id3dxsprite--begin.md) é chamado. Presume-se que o dispositivo está em um estado válido para desenhar vértices que contêm UsageIndex = 0 nos dados D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ TEXCOORD e D3DDECLUSAGE \_ COLOR.                                                                                                                                                     |
| D3DXSPRITE \_ OBJECTSPACE              | O mundo, a exibição e as transformaçãos de projeção não são modificadas. As transformação atualmente definidas para o dispositivo são usadas para transformar os sprites quando os sprites em lote são desenhados (quando [**Flush**](id3dxsprite--flush.md) ou [**End**](id3dxsprite--end.md) é chamado). Se esse sinalizador não for especificado, as transformaçãos de mundo, exibição e projeção serão modificadas para que os sprites sejam desenhados em coordenadas de espaço na tela.              |
| D3DXSPRITELAND \_                | Cada sprite será girado sobre seu centro para que ele seja voltado para o visualizador. [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) ou [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) devem ser chamados primeiro.                                                                                                                                                                                                                |
| ALFABLEND D3DXSPRITE \_               | Habilita a combinação alfa com ALPHATESTENABLE D3DRS definido \_ como **TRUE** (para alfa não zero). D3DBLEND SRCALPHA será o estado de combinação de origem \_ e D3DBLEND INVSRCALPHA será o estado de combinação de destino em chamadas para \_ [**SetRenderState**](/windows/desktop/api). Consulte [estado de mistura alfa (Direct3D 9)](alpha-blending-state.md). [**ID3DXFont**](id3dxfont.md) espera que esse sinalizador seja definido ao desenhar o texto. |
| \_Textura de classificação D3DXSPRITE \_            | Classificar sprites por textura antes do desenho. Isso pode melhorar o desempenho ao desenhar sprites não sobrepostos de profundidade uniforme. Você também pode combinar \_ \_ a textura de classificação D3DXSPRITE com D3DXSPRITE de \_ profundidade de classificação \_ \_ FRONTTOBACK ou D3DXSPRITE de \_ profundidade de classificação \_ \_ BACKTOFRONT. Isso classificará a lista de sprites por profundidade primeiro e a textura segundo.<br/>                                                                           |
| D3DXSPRITE \_ \_ FRONTTOBACK profundidade de classificação \_ | Os sprites são classificados por profundidade na ordem de frente para trás antes do desenho. Esse procedimento é recomendado ao desenhar sprites opacos de profundidades variadas. Você pode combinar D3DXSPRITE de \_ profundidade de classificação de \_ \_ FRONTTOBACK com \_ a textura de classificação D3DXSPRITE \_ para classificar primeiro por profundidade e segundo por textura.<br/>                                                                                                                                   |
| D3DXSPRITE \_ \_ BACKTOFRONT profundidade de classificação \_ | Os sprites são classificados por profundidade na ordem de fundo para frente antes do desenho. Esse procedimento é recomendado ao desenhar sprites transparentes de profundidades variadas. Você pode combinar D3DXSPRITE de \_ profundidade de classificação de \_ \_ BACKTOFRONT com \_ a textura de classificação D3DXSPRITE \_ para classificar primeiro por profundidade e segundo por textura.<br/>                                                                                                                              |
| D3DXSPRITE \_ não \_ é \_ textura de ADDREF \_ | Desabilita a chamada de AddRef () em cada empate e versão () em flush () para melhorar o desempenho.                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>Informações constantes



| Requisito                         | Valor            |
|--------------------------|-------------|
| parâmetro                   | d3dx9core. h |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




