---
description: O anti-aliasing em cena completa se refere a desfocar as bordas de cada polígono na cena, já que ela é rasterizada em uma única passagem; Não é necessária uma segunda passagem.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Anti-aliasing Full-Scene (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500265"
---
# <a name="full-scene-antialiasing-direct3d-9"></a>Anti-aliasing Full-Scene (Direct3D 9)

O anti-aliasing em cena completa se refere a desfocar as bordas de cada polígono na cena, já que ela é rasterizada em uma única passagem; Não é necessária uma segunda passagem. A suavização completa da cena, quando há suporte, afeta apenas os triângulos e os grupos de triângulos. Não é possível suavizar as linhas usando os serviços do Direct3D. A suavização completa da cena é feita no Direct3D usando a multiamostragem em cada pixel. Quando a multiamostragem está habilitada, todas as subamostras de um pixel são atualizadas em uma passagem, mas quando usadas para outros efeitos que envolvem várias passagens de renderização, o aplicativo pode especificar que apenas alguns subamostras serão afetados por uma determinada passagem de renderização. Essa última abordagem habilita a simulação de desfoque de movimento, efeitos de foco de profundidade de campo, Desfoque de reflexo e assim por diante.

Em ambos os casos, os vários exemplos registrados para cada pixel são mesclados e são impressos na tela. Isso permite a qualidade de imagem aprimorada de anti-aliasing ou outros efeitos.

Antes de criar um dispositivo com o método [**IDirect3D9:: CreateDevice**](/windows/desktop/api) , você precisa determinar se há suporte para anti-aliasing na cena completa. Faça isso chamando o método [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) , conforme mostrado no exemplo de código abaixo.


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



O primeiro parâmetro que [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) aceita é um número ordinal que denota o adaptador de vídeo a ser consultado. Este exemplo usa D3DADAPTER \_ padrão para especificar o adaptador de vídeo primário. O segundo parâmetro é um valor do tipo enumerado [**D3DDEVTYPE**](./d3ddevtype.md) , especificando o tipo de dispositivo. O terceiro parâmetro especifica o formato da superfície. O quarto parâmetro informa ao Direct3D se deve ser consultado sobre a multiamostragem completa (**true**) ou a anti-aliasing na cena completa (**false**). Este exemplo usa **false** para informar ao Direct3D que ele está consultando a anti-aliasing na cena completa. O último parâmetro especifica a técnica de multiamostragem que você deseja testar. Use um valor do tipo enumerado do [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) . Este exemplo testa para ver se há suporte para dois níveis de multiamostragens.

Se o dispositivo der suporte ao nível de várias amostras que você deseja usar, a próxima etapa será definir os parâmetros de apresentação preenchendo os membros apropriados da estrutura [**de \_ parâmetros D3DPRESENT**](d3dpresent-parameters.md) para criar uma superfície de renderização de várias amostras. Depois disso, você pode criar o dispositivo. O código de exemplo a seguir mostra como configurar um dispositivo com uma superfície de renderização de multiamostragem.


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



Para usar a multiamostral, o membro SwapEffect do \_ parâmetro D3DPRESENT deve ser definido como \_ descartar D3DSWAPEFFECT.

A última etapa é habilitar a suavização de várias amostras chamando o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e definindo D3DRS \_ MULTISAMPLEANTIALIAS como **true**. Depois de definir esse valor como **true**, qualquer renderização que você fizer terá uma multiamostra aplicada a ele. Talvez você queira habilitar e desabilitar a multiamostragem, dependendo do que está renderizando.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suavização](antialiasing.md)
</dt> </dl>

 

 
