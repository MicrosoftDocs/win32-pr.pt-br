---
description: No Direct3D 9, o Direct3D permitirá que o driver retorne códigos de erro como E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY e D3DERR \_ UNSUPPORTEDCOLORARG para que um aplicativo possa responder a eles.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Erros internos do driver (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c2290e2190081c54a1e0e97fcbf1d6f76fdb16b9b2b7d45648059f9c839396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849457"
---
# <a name="driver-internal-errors-direct3d-9"></a>Erros internos do driver (Direct3D 9)

No Direct3D 9, o Direct3D permitirá que o driver retorne códigos de erro como E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY e D3DERR \_ UNSUPPORTEDCOLORARG para que um aplicativo possa responder a eles. No entanto, às vezes, as chamadas à API que geraram esses tipos de retorno são carregadas em um buffer de comando e são armazenadas em lote para serem enviadas para a GPU (consulte [controlar o tempo de execução e otimizações de driver](accurately-profiling-direct3d-api-calls.md)). Nesse caso, os erros não podem ser retransmitidos para o aplicativo quando a ação precisa ser executada, portanto o código de erro é consumido pelo tempo de execução e uma observação é feita no objeto de dispositivo que isso aconteceu. Posteriormente, quando o aplicativo invoca [**IDirect3DDevice9::P reenviada**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9::P reenviada** retornará D3DERR \_ DRIVERINTERNALERROR. É por isso que a melhor abordagem a ser tomada por um aplicativo ao receber um D3DERR \_ DRIVERINTERNALERROR da **IDirect3DDevice9::P reenviada** é destruir e recriar o dispositivo.

Se você quiser tentar depurar mais detalhadamente, aqui estão algumas sugestões para tentar descobrir qual chamada à API está gerando o erro:

-   Como a lista de possíveis valores de retorno não está completa, você pode tentar descobrir qual chamada está falhando ao redor de cada chamada à API como esta:

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    O fluxo de depuração de saída deve mostrar a chamada que está causando o problema.

-   Além disso, para fins de depuração, tente chamar [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) imediatamente antes de cada [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para ver se há um problema adicional com o driver de dispositivo (operação sem suporte, combinação inutilizável de formatos de textura, etc).

    > [!Note]  
    > [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) deve ser usado com cuidado e com moderação devido à quantidade de trabalho de validação que o driver precisa executar para retornar uma resposta.

     

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dicas de programação](programming-tips.md)
</dt> </dl>

 

 
