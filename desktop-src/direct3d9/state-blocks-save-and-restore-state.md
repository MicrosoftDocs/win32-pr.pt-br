---
description: Um bloco de estado é um grupo de Estados de dispositivo.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: Estado de salvamento e restauração de blocos de estado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8f19d6409e0dc9c40f1d4c7711440a0dc09fe2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919691"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a>Estado de salvamento e restauração de blocos de estado (Direct3D 9)

Um bloco de estado é um grupo de Estados de dispositivo. O estado do dispositivo é composto de estado de renderização, estado de vértice, estado de pixel ou todos os itens acima. Um bloco de estado contém um instantâneo do estado atual de um dispositivo ou você pode criar um bloco de estado que registra cada alteração de estado que seu aplicativo faz.

## <a name="capture-a-block-of-state"></a>Capturar um bloco de estado

Escolha o tipo de estado que você deseja capturar e crie um bloco de estado como este:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



[**IDirect3DDevice9:: CreateStateBlock**](/windows/desktop/api) cria um bloco de estado e captura automaticamente o estado do dispositivo. O estado do dispositivo é especificado pelo tipo de bloco de estado no primeiro argumento. Esse Estado pode ser um dos seguintes: todo o estado do dispositivo (consulte [salvar todos os Estados do dispositivo com um StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), todo o estado de pixel (consulte [economizando estado de pixel com um StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)) ou todo o estado de vértice (consulte [salvar Estados de vértice com um StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).

O sistema de efeitos usa um bloco de estado para salvar o estado. Após [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) ser chamado, um bloco de estado é criado e o estado é capturado. Quando [**ID3DXEffect:: End**](id3dxeffect--end.md) é chamado, o estado do bloco de estado é reaplicado ao dispositivo.

## <a name="capture-individual-states"></a>Capturar Estados individuais

Para salvar uma sequência de estado Personalizada, empacote o estado que você deseja salvar em um par [**IDirect3DDevice9:: BeginStateBlock**](/windows/desktop/api) e [**IDirect3DDevice9:: EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) . BeginStateBlock informa ao dispositivo atual para configurar um bloco de estado e adicioná-lo a cada alteração de estado que ocorre até que EndStateBlock seja chamado. Veja um exemplo:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



Isso irá salvar qualquer número de alterações de estado em qualquer sequência para um stateblock personalizado. Posteriormente, quando você quiser usar o stateblock para redefinir o estado do dispositivo, chame [**IDirect3DStateBlock9:: apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply). Isso substituirá apenas o estado do dispositivo que foi capturado no bloco de estado. Qualquer outro Estado de dispositivo que não foi capturado com o stateblock personalizado não será alterado. Mais uma vez, como o objeto stateblock é uma interface, você precisará liberá-lo quando terminar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estados (Direct3D 9)](states.md)
</dt> </dl>

 

 
