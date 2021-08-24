---
description: 'Os sinalizadores a seguir são usados para especificar opções de renderização de sprite para o parâmetro flags no método Begin:'
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e2247f414636039906277f882fb9dfc95f6b6b33aa29de2ac51a722c045901
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749756"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

Os sinalizadores a seguir são usados para especificar opções de renderização de sprite para o parâmetro flags no [**método Begin:**](id3dxsprite--begin.md)



| \#Definir                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXSPRITE \_ DONOTSAVESTATE           | O estado do dispositivo não deve ser salvo ou restaurado quando [**Begin**](id3dxsprite--begin.md) ou [**End**](id3dxsprite--end.md) é chamado.                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE | O estado de renderização do dispositivo não deve ser alterado [**quando Begin**](id3dxsprite--begin.md) é chamado. Presume-se que o dispositivo está em um estado válido para desenhar vértices que contêm UsageIndex = 0 nos dados D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ TEXCOORD e D3DDECLUSAGE \_ COLOR.                                                                                                                                                     |
| D3DXSPRITE \_ OBJECTSPACE              | O mundo, a exibição e as transformaçãos de projeção não são modificadas. As transformação atualmente definidas para o dispositivo são usadas para transformar os sprites quando os sprites em lote são desenhados (quando [**Flush**](id3dxsprite--flush.md) ou [**End**](id3dxsprite--end.md) é chamado). Se esse sinalizador não for especificado, as transformações de mundo, exibição e projeção serão modificadas para que os sprites sejam desenhados em coordenadas de espaço na tela.              |
| D3DXSPRITELAND \_                | Cada sprite será girado sobre seu centro para que ele seja voltado para o visualizador. [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) ou [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) devem ser chamados primeiro.                                                                                                                                                                                                                |
| ALFABLEND D3DXSPRITE \_               | Habilita a combinação alfa com ALPHATESTENABLE D3DRS definido \_ como **TRUE** (para alfa não zero). D3DBLEND SRCALPHA será o estado de combinação de origem \_ e D3DBLEND INVSRCALPHA será o estado de combinação de destino em chamadas para \_ [**SetRenderState**](/windows/desktop/api). Consulte [Estado de combinação alfa (Direct3D 9)](alpha-blending-state.md). [**ID3DXFont**](id3dxfont.md) espera que esse sinalizador seja definido ao desenhar texto. |
| TEXTURA DE CLASSIFICAÇÃO D3DXSPRITE \_ \_            | Classificar sprites por textura antes do desenho. Isso pode melhorar o desempenho ao desenhar sprites não sobrepostos de profundidade uniforme. Você também pode combinar A TEXTURA DE CLASSIFICAÇÃO D3DXSPRITE com FRONTTOBACK DE PROFUNDIDADE DE CLASSIFICAÇÃO D3DXSPRITE ou BACKTOFRONT DA PROFUNDIDADE DE CLASSIFICAÇÃO \_ \_ \_ \_ \_ D3DXSPRITE. \_ \_ \_ Isso classificará a lista de sprites por profundidade primeiro e segundo textura.<br/>                                                                           |
| FRONTTOBACK DA PROFUNDIDADE DE CLASSIFICAÇÃO D3DXSPRITE \_ \_ \_ | Os sprites são classificação por profundidade na ordem de frente para trás antes do desenho. Este procedimento é recomendado ao desenhar sprites opacos de profundidades variadas. Você pode combinar D3DXSPRITE \_ SORT \_ DEPTH FRONTTOBACK com \_ D3DXSPRITE SORT TEXTURE para classificar primeiro por profundidade \_ e segundo por \_ textura.<br/>                                                                                                                                   |
| BACKTOFRONT DA PROFUNDIDADE DE CLASSIFICAÇÃO D3DXSPRITE \_ \_ \_ | Os sprites são classificação por profundidade na ordem de voltar para frente antes do desenho. Este procedimento é recomendado ao desenhar sprites transparentes de profundidades variadas. Você pode combinar D3DXSPRITE \_ SORT \_ DEPTH BACKTOFRONT com \_ D3DXSPRITE SORT TEXTURE para classificar primeiro por profundidade \_ e segundo por \_ textura.<br/>                                                                                                                              |
| D3DXSPRITE \_ NÃO \_ ADICIONAR \_ TEXTURA \_ | Desabilita chamar AddRef() em cada desenho e Release() em Flush() para melhorar o desempenho.                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>Informações constantes



| Requisito                         | Valor            |
|--------------------------|-------------|
| parâmetro                   | d3dx9core.h |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




