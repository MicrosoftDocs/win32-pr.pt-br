---
description: A antialização de cena completa refere-se ao desfoque das bordas de cada polígono na cena, pois ela é rasterizada em uma única passagem; nenhuma segunda passagem é necessária.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Full-Scene antialiasing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fdeab18997db57ed1391af97f40f1500e7c326411019ddcb42453e4a68cc7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893986"
---
# <a name="full-scene-antialiasing-direct3d-9"></a>Full-Scene antialiasing (Direct3D 9)

A antialização de cena completa refere-se ao desfoque das bordas de cada polígono na cena, pois ela é rasterizada em uma única passagem; nenhuma segunda passagem é necessária. A antialização de cena inteira, quando suportada, afeta apenas triângulos e grupos de triângulos. As linhas não podem ser anticiadas usando serviços Direct3D. A antialiação de cena completa é feita no Direct3D usando multisampling em cada pixel. Quando a multisampling está habilitada, todos os subsamplos de um pixel são atualizados em uma passagem, mas quando usados para outros efeitos que envolvem várias passagens de renderização, o aplicativo pode especificar que apenas algumas subsamplos devem ser afetadas por uma determinada passagem de renderização. Essa última abordagem permite simulação de desfoque de movimento, efeitos de foco de profundidade de campo, desfoque de reflexão e assim por diante.

Em ambos os casos, os vários exemplos registrados para cada pixel são mesclados e são produzidos na tela. Isso permite a qualidade aprimorada da imagem de antialiasing ou outros efeitos.

Antes de criar um dispositivo com o [**método IDirect3D9::CreateDevice,**](/windows/desktop/api) você precisa determinar se há suporte para a antialização de cena completa. Faça isso chamando o [**método IDirect3D9::CheckDeviceMultiSampleType,**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) conforme mostrado no exemplo de código abaixo.


```
/*
* The code below assumes that pD3D is a valid pointer 
*   to a IDirect3D9 interface.
*/

if( SUCCEEDED(pD3D->CheckDeviceMultiSampleType( D3DADAPTER_DEFAULT, 
                    D3DDEVTYPE_HAL , D3DFMT_R8G8B8, FALSE, 
                    D3DMULTISAMPLE_2_SAMPLES, NULL ) ) )
// Full-scene antialiasing is supported. Enable it here.
```



O primeiro parâmetro [**que IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) aceita é um número ordinal que indica o adaptador de exibição a ser consultado. Este exemplo usa D3DADAPTER \_ DEFAULT para especificar o adaptador de exibição primário. O segundo parâmetro é um valor do tipo enumerado [**D3DDEVTYPE,**](./d3ddevtype.md) especificando o tipo de dispositivo. O terceiro parâmetro especifica o formato da superfície. O quarto parâmetro informa ao Direct3D se deve-se perguntar sobre a multisampling de janela inteira **(TRUE)** ou a antialiação de cena completa **(FALSE).** Este exemplo usa **FALSE** para dizer ao Direct3D que ele está consultando sobre a antialiação de cena completa. O último parâmetro especifica a técnica de multisampling que você deseja testar. Use um valor do tipo [**enumerado D3DMULTISAMPLE \_ TYPE.**](./d3dmultisample-type.md) Este exemplo testa se há suporte para dois níveis de multisampling.

Se o dispositivo dá suporte ao nível de multisampling que você deseja usar, a próxima etapa é definir os parâmetros de apresentação preenchendo os membros apropriados da estrutura [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md) para criar uma superfície de renderização multisamplo. Depois disso, você pode criar o dispositivo. O código de exemplo a seguir mostra como configurar um dispositivo com uma superfície de renderização multisampling.


```
/*
* The example below assumes that pD3D is a valid pointer 
* to a IDirect3D9 interface, d3dDevice is a pointer to a 
* IDirect3DDevice9 interface, and hWnd is a valid handle
* to a window.
*/

D3DPRESENT_PARAMETER d3dPP
ZeroMemory( &d3dPP, sizeof( d3dPP ) );
d3dPP.Windowed        = FALSE
d3dPP.SwapEffect      = D3DSWAPEFFECT_DISCARD;
d3dPP.MultiSampleType = D3DMULTISAMPLE_2_SAMPLES;
pD3D->CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                    &d3dpp, &d3dDevice)
```



Para usar multisampling, o membro SwapEffect de D3DPRESENT PARAMETER deve \_ ser definido como D3DSWAPEFFECT \_ DISCARD.

A última etapa é habilitar a antialização multisampling chamando o método [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e definindo o D3DRS \_ MULTISAMPLEANTIALIAS como **TRUE.** Depois de definir esse valor como **TRUE,** qualquer renderização que você fizer terá várias respostas aplicadas a ele. Talvez você queira habilitar e desabilitar o multisampling, dependendo do que você está renderando.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suavização](antialiasing.md)
</dt> </dl>

 

 
