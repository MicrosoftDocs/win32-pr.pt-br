---
title: Como reproduzir uma lista de comandos
description: Este tópico mostra como reproduzir uma lista de comandos.
ms.assetid: 4e6c0a98-85ff-45ca-963b-7d5c55f47195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d04df73b481adea17e1f985e2c1851039fd016a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988513"
---
# <a name="how-to-play-back-a-command-list"></a>Como reproduzir uma lista de comandos

Uma [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md) é uma lista registrada de comandos de renderização. Use uma lista de comandos para gravar previamente os comandos de desenho e reproduzi-los novamente mais tarde. Este tópico mostra como reproduzir uma lista de [comandos](overviews-direct3d-11-render-multi-thread-command-list.md). Uma lista de comandos pode ser usada para dividir tarefas de renderização entre threads.

Esta seção descreve como reproduzir uma lista de comandos. Para gravar uma lista de comandos, consulte [como gravar uma lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-record.md).

**Para reproduzir uma lista de comandos**

-   Chame [**ID3D11DeviceContext:: ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) e passe um objeto [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) válido.
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) deve ser executado no [contexto imediato](overviews-direct3d-11-devices-intro.md) para comandos gravados a serem executados na GPU (unidade de processamento gráfico). Use o contexto imediato para alimentar os comandos para a GPU para execução, use um contexto adiado para gravar comandos para reprodução em outra lista de comandos. Ao chamar **ExecuteCommandList** em outro contexto adiado, você cria uma lista de comandos adiados ' mesclados '. Para executar os comandos na lista de comandos adiados mesclados, você precisa executá-los no contexto imediato.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




