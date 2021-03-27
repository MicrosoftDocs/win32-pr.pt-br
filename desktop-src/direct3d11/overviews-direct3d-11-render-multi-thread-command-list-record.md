---
title: Como registrar uma lista de comandos
description: Este tópico mostra como criar e registrar uma lista de comandos.
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636250"
---
# <a name="how-to-record-a-command-list"></a>Como gravar uma lista de comandos

Uma [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md) é uma lista registrada de comandos de renderização. Este tópico mostra como criar e registrar uma [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md). Use uma lista de comandos para registrar comandos de renderização e reproduzi-los novamente mais tarde. Uma lista de comandos é conveniente para dividir tarefas de renderização entre threads.

**Para registrar uma lista de comandos**

1.  Uma lista de comandos deve ser criada a partir de um contexto adiado, que contém ações de processamento e estado do dispositivo. Dado um dispositivo, crie um contexto adiado chamando [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  Use o contexto adiado para renderizar.

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    Este exemplo simples limpa um destino de renderização, mas você pode adicionar outros comandos de renderização.

3.  Crie/registre uma lista de comandos chamando [**ID3D11DeviceContext:: FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) e passando um ponteiro para uma interface [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) não inicializada.

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    Quando o método retorna, uma lista de comandos é criada contendo todos os comandos de renderização e uma interface é retornada ao aplicativo.

    O parâmetro booliano informa ao tempo de execução o que fazer com o estado do pipeline no contexto adiado. **Verdadeiro** significa restaurar o estado do contexto do dispositivo para sua condição de lista de pré-comandos quando a gravação for concluída, **falso** significa que não altere o estado após a gravação. Isso significa que o contexto do dispositivo refletirá as alterações de estado contidas na lista de comandos.

Para ver um exemplo de reprodução de uma lista de comandos, consulte [como: reproduzir uma lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-play.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




