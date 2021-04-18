---
description: Um bloco de estado pode ser usado para capturar todos os Estados do dispositivo (consulte o estado de salvar e restaurar dos blocos de estado (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Salvando todos os Estados do dispositivo com um StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bfdb4f9b3a9c1e33c2e8e7f50765f1656bd59e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105796406"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a>Salvando todos os Estados do dispositivo com um StateBlock (Direct3D 9)

Um bloco de estado pode ser usado para capturar todos os Estados do dispositivo (consulte o [estado de salvar e restaurar dos blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)). Os seguintes elementos de estado estão incluídos no estado do dispositivo:

-   Estado do vértice (consulte [salvar Estados de vértice com um StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).
-   Estado de pixel (consulte [economizando estado de pixel com um StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).
-   Cada textura atribuída a uma amostra.
-   Cada textura de vértice.
-   Cada textura de mapa de deslocamento.
-   A paleta de textura atual.
-   Para cada fluxo de vértice: um ponteiro para o buffer de vértice, cada argumento de [**IDirect3DDevice9:: Setstreamname**](/windows/desktop/api)e o divisor (se houver) de [**IDirect3DDevice9:: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Um ponteiro para o buffer de índice.
-   O visor.
-   O retângulo de tesoura.
-   O mundo, a exibição e as matrizes de projeção.
-   A textura é transformada.
-   Os planos de recorte (se houver).
-   O material atual.

Para capturar todos os Estados de dispositivo com um bloco de estado, especifique D3DSBT \_ All ao chamar [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estado de salvamento e restauração de blocos de estado](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
