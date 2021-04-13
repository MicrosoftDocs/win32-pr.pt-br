---
description: Os destinos de renderização múltipla (MRT) referem-se à capacidade de renderização em várias superfícies (consulte IDirect3D9Surface) com uma única chamada de desenho.
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: Vários destinos de renderização (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb7aafeedb621e43abb288eb9bbceb17ddb0cc0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456706"
---
# <a name="multiple-render-targets-direct3d-9"></a>Vários destinos de renderização (Direct3D 9)

Os destinos de renderização múltipla (MRT) referem-se à capacidade de renderização em várias superfícies (consulte [**IDirect3D9Surface**](/windows/desktop/api)) com uma única chamada de desenho. Essas superfícies podem ser criadas independentemente uma da outra. Os destinos de renderização podem ser definidos usando [**IDirect3DDevice9:: SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).

Vários destinos de renderização têm as seguintes restrições:

-   Todas as superfícies de destino de renderização usadas juntas devem ter a mesma profundidade de bits, mas podem ser de formatos diferentes, a menos que o \_ limite de MRTINDEPENDENTBITDEPTHS D3DPMISCCAPS seja definido.
-   Todas as superfícies de um destino de processamento múltiplo devem ter a mesma largura e altura.
-   Algumas implementações não podem executar operações de sombreador pós-pixel em vários destinos de renderização, incluindo: sem pontilhamento, teste alfa, sem fogging, sem mesclagem ou mascaramento, exceto o teste de z e de estêncil. Dispositivos que podem dar suporte a operações de sombreador após pixel definem o bit de extremidade como D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING.

    Quando o \_ limite de MRTPOSTPIXELSHADERBLENDING D3DPMISCCAPS é definido, você deve primeiro consultar o [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) com o \_ resultado de \_ mesclagem POSTPIXELSHADER de consulta de uso \_ para o formato de superfície específico. Se for false, nenhuma operação de mesclagem de sombreador após pixel estará disponível para esse formato de superfície específico. Se for true, o dispositivo deverá aplicar o mesmo estado a todos os destinos de renderização simultâneos da seguinte maneira:

    -   Mistura alfa: o valor de cor em oCi é combinado com o destino de renderização i.
    -   Teste alfa: a comparação ocorrerá com oC0. Se a comparação falhar, o teste de pixel será encerrado para todos os destinos de renderização.
    -   Neblina: o destino de renderização 0 receberá fogged. Outros destinos de renderização são indefinidos. As implementações podem optar por fazer a sombra de todas elas usando o mesmo estado.
    -   Pontilhamento: indefinido.

-   Não há suporte para anti-aliasing.
-   Algumas das implementações não aplicam a máscara de gravação de saída (D3DRS \_ COLORWRITEENABLE). Os que podem ter máscaras de gravação de cores independentes. Isso é expresso usando um novo bit de recurso. O número de máscaras de gravação de cor independentes disponíveis será igual ao número máximo de elementos que o dispositivo é capaz de.

Novos limites de hardware:


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de pixel](pixel-pipeline.md)
</dt> </dl>

 

 
