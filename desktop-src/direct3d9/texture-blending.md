---
description: O Direct3D pode mesclar até oito texturas em primitivas em uma única passagem.
ms.assetid: vs|directx_sdk|~\texture_blending.htm
title: Mesclagem de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a89a87160bb85c1f62339380d46fa4b39736609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646179"
---
# <a name="texture-blending-direct3d-9"></a>Mesclagem de textura (Direct3D 9)

O Direct3D pode mesclar até oito texturas em primitivas em uma única passagem. O uso da mesclagem de várias texturas pode aumentar profundamente a taxa de quadros de um aplicativo Direct3D. Um aplicativo emprega a mesclagem de várias texturas para aplicar texturas, sombras, iluminação especular, iluminação difusa e outros efeitos especiais em uma única passagem.

Para usar a mesclagem de texturas, seu aplicativo deve verificar primeiro se o hardware do usuário tem suporte para isso. Essas informações são encontradas no membro TextureCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . Para obter detalhes sobre como consultar o hardware do usuário para recursos de mesclagem de textura, consulte [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).

## <a name="texture-stages-and-the-texture-blending-cascade"></a>Estágios de textura e a cascata de mesclagem de textura

O Direct3D dá suporte para a mesclagem de várias texturas em uma única passagem por meio do uso de estágios de textura. Um estágio de textura pega dois argumentos e executa uma operação de mesclagem neles, passando o resultado para processamento adicional ou para rasterização. Você pode visualizar um estágio de textura conforme mostrado no diagrama a seguir.

![diagrama de um estágio de textura](images/texstg.png)

Como mostra o diagrama anterior, os estágios de textura combinam dois argumentos usando um operador especificado. As operações comuns incluem modulação simples ou adição dos componentes de cor ou alfa dos argumentos, mas há suporte para dezenas de operações. Os argumentos para um estágio podem ser uma textura associada, a cor iterada ou o alfa (iterado durante o sombreamento Gouraud), cor ou alfa arbitrário ou o resultado do estágio de textura anterior. Para obter mais informações, consulte [parâmetros e operações de mesclagem de textura (Direct3D 9)](texture-blending-operations-and-arguments.md).

> [!Note]  
> O Direct3D distingue a mistura de cores da mistura alfa. Os aplicativos definem as operações e os argumentos de mesclagem de cor e alfa individualmente, e os resultados dessas configurações são independentes uns dos outros.

 

A combinação de argumentos e operações usados por vários estágios da mesclagem definem uma linguagem simples de mesclagem baseada em fluxo. Os resultados de um estágio fluem para outro estágio, e desse estágio para o próximo e assim por diante. O conceito da fluência de resultados de estágio para estágio para, finalmente, serem rasterizados em um polígono geralmente é chamado de mesclagem de texturas em cascata. O diagrama a seguir mostra como estágios de textura individuais compõem a mesclagem de texturas em cascata.

![diagrama dos estágios de textura na mesclagem de texturas em cascata](images/tcascade.png)

Cada estágio em um dispositivo tem um índice baseado em zero. O Direct3D permite até oito estágios de mesclagem, embora você deva sempre verificar as funcionalidades do dispositivo para determinar quantos estágios o hardware atual aceita. O primeiro estágio de mesclagem está no índice 0, o segundo é no 1 e assim por diante, até o índice 7. O sistema mescla os estágios aumentando a ordem de indexação.

Use apenas o número de estágios de que você precisa; os estágios de mesclagem não utilizados são desabilitados por padrão. Portanto, se seu aplicativo usar apenas os dois primeiros estágios, ele só precisará definir as operações e os argumentos para os estágios de 0 e 1. O sistema mescla os dois estágios e ignora os estágios desabilitados.

> [!Note]  
> Se seu aplicativo usa um número de estágios variado para diferentes situações – como quatro estágios para alguns objetos e apenas dois para outros – você não precisa explicitamente desabilitar todos os estágios usados anteriormente. Uma opção é desabilitar a operação de cor para o primeiro estágio não utilizado. Assim, todos os estágios com um índice mais alto não serão aplicados. Outra opção é desabilitar o mapeamento de textura completamente definindo a operação de cor para o primeiro estágio de textura (estágio 0) para D3DTOP \_ Disable. Uma terceira opção é quando um estágio de textura tem D3DTSS \_ COLORARG1 igual a D3DTA \_ Texture e o ponteiro de textura para o estágio é **NULL**, esse estágio e todos os estágios depois de não serem processados.

 

Informações adicionais estão contidas nos tópicos a seguir.

-   [Operações e argumentos de mesclagem de textura (Direct3D 9)](texture-blending-operations-and-arguments.md)
-   [Atribuindo as texturas atuais (Direct3D 9)](assigning-the-current-textures.md)
-   [Criando estágios de mesclagem (Direct3D 9)](creating-blending-stages.md)
-   [Mesclagem de textura alfa (Direct3D 9)](alpha-texture-blending.md)
-   [Mesclagem de textura de passagem (Direct3D 9)](multipass-texture-blending.md)
-   [Mapeamento claro com texturas (Direct3D 9)](light-mapping-with-textures.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Texturas do Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
