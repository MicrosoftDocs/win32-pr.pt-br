---
description: Para criar um dispositivo Direct3D, primeiro crie um objeto Direct3D (consulte Direct3DCreate9).
ms.assetid: 06810f31-fa6c-416e-bd7b-65cfb3e6d7f2
title: Criando um dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9c033ed25262f0a3bcdee9db73509ddf5cb53b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793933"
---
# <a name="creating-a-device-direct3d-9"></a>Criando um dispositivo (Direct3D 9)

Para criar um dispositivo Direct3D, primeiro crie um objeto Direct3D (consulte [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)). Todos os dispositivos de renderização criados por um objeto do Direct3D compartilham os mesmos recursos físicos. Se você criar vários dispositivos de renderização a partir de um único objeto do Direct3D, as penalidades de desempenho extremo serão incorridas porque compartilham o mesmo hardware.

Primeiro, inicialize os valores para a estrutura de [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md) que é usada para criar o dispositivo Direct3D. O exemplo de código a seguir especifica um aplicativo em janela onde o buffer de fundo é copiado para o buffer frontal durante uma operação de sincronização vertical somente.


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



Em seguida, crie o dispositivo Direct3D. A chamada [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) a seguir especifica o adaptador padrão, um dispositivo HAL (camada de abstração de hardware) e processamento de vértice de software.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



Observe que uma chamada para criar, liberar ou redefinir o dispositivo deve ocorrer somente no mesmo thread que o procedimento de janela da janela de foco.

Depois de criar o dispositivo, defina seu estado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
