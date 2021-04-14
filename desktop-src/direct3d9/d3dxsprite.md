---
description: 'Os sinalizadores a seguir são usados para especificar as opções de renderização sprite para o parâmetro flags no método Begin:'
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c394d2606584ec5f56aa28661a2da286f000a66d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500132"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

Os sinalizadores a seguir são usados para especificar as opções de renderização sprite para o parâmetro flags no método [**begin**](id3dxsprite--begin.md) :



|                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definir                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                       |
| D3DXSPRITE \_ DONOTSAVESTATE           | O estado do dispositivo não deve ser salvo ou restaurado quando [**begin**](id3dxsprite--begin.md) ou [**end**](id3dxsprite--end.md) é chamado.                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ DONOTMODIFY \_ renderingstate | O estado de processamento do dispositivo não deve ser alterado quando [**begin**](id3dxsprite--begin.md) é chamado. Supõe-se que o dispositivo esteja em um estado válido para desenhar vértices contendo UsageIndex = 0 na \_ posição D3DDECLUSAGE, D3DDECLUSAGE \_ TEXCOORD e D3DDECLUSAGE \_ dados de cor.                                                                                                                                                     |
| D3DXSPRITE \_ OBJECTspace              | As transformações do mundo, da exibição e da projeção não são modificadas. As transformações atualmente definidas para o dispositivo são usadas para transformar os sprites quando os sprites em lote são desenhados (quando [**flush**](id3dxsprite--flush.md) ou [**end**](id3dxsprite--end.md) é chamado). Se esse sinalizador não for especificado, as transformações do mundo, da exibição e da projeção serão modificadas para que os sprites sejam desenhados em coordenadas de espaço na tela.              |
| D3DXSPRITE de \_ mensagem                | Cada sprite será girado sobre seu centro para que ele esteja voltado para o visualizador. [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) ou [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) deve ser chamado primeiro.                                                                                                                                                                                                                |
| D3DXSPRITE \_ ALPHABLEND               | Habilita a mesclagem alfa com D3DRS \_ ALPHATESTENABLE definido como **true** (para alfa diferente de zero). D3DBLEND \_ SRCALPHA será o estado de mesclagem de origem e D3DBLEND \_ INVSRCALPHA será o estado de mesclagem de destino em chamadas para [**setrenderingstate**](/windows/desktop/api). Consulte [estado de mistura alfa (Direct3D 9)](alpha-blending-state.md). [**ID3DXFont**](id3dxfont.md) espera que esse sinalizador seja definido ao desenhar o texto. |
| \_Textura de classificação D3DXSPRITE \_            | Classificar sprites por textura antes do desenho. Isso pode melhorar o desempenho ao desenhar sprites não sobrepostos de profundidade uniforme. Você também pode combinar \_ \_ a textura de classificação D3DXSPRITE com D3DXSPRITE de \_ profundidade de classificação \_ \_ FRONTTOBACK ou D3DXSPRITE de \_ profundidade de classificação \_ \_ BACKTOFRONT. Isso classificará a lista de sprites por profundidade primeiro e a textura segundo.<br/>                                                                           |
| D3DXSPRITE \_ \_ FRONTTOBACK profundidade de classificação \_ | Os sprites são classificados por profundidade na ordem de frente para trás antes do desenho. Esse procedimento é recomendado ao desenhar sprites opacos de profundidades variadas. Você pode combinar D3DXSPRITE de \_ profundidade de classificação de \_ \_ FRONTTOBACK com \_ a textura de classificação D3DXSPRITE \_ para classificar primeiro por profundidade e segundo por textura.<br/>                                                                                                                                   |
| D3DXSPRITE \_ \_ BACKTOFRONT profundidade de classificação \_ | Os sprites são classificados por profundidade na ordem de fundo para frente antes do desenho. Esse procedimento é recomendado ao desenhar sprites transparentes de profundidades variadas. Você pode combinar D3DXSPRITE de \_ profundidade de classificação de \_ \_ BACKTOFRONT com \_ a textura de classificação D3DXSPRITE \_ para classificar primeiro por profundidade e segundo por textura.<br/>                                                                                                                              |
| D3DXSPRITE \_ não \_ é \_ textura de ADDREF \_ | Desabilita a chamada de AddRef () em cada empate e versão () em flush () para melhorar o desempenho.                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>Informações constantes



|                          |             |
|--------------------------|-------------|
| parâmetro                   | d3dx9core. h |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




