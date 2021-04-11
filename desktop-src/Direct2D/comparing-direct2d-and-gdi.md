---
title: Comparando a aceleração de hardware Direct2D e GDI
description: Direct2D e GDI são APIs de renderização 2D de modo imediato e ambas oferecem algum grau de aceleração de hardware.
ms.assetid: 0028a0c3-445d-46b7-b55b-46dff3bce9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f05dce8719f4d07d3160c65b88570391c3eb736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294101"
---
# <a name="comparing-direct2d-and-gdi-hardware-acceleration"></a>Comparando a aceleração de hardware Direct2D e GDI

[Direct2D](./direct2d-portal.md) e [GDI](/windows/desktop/gdi/windows-gdi) são APIs de renderização 2D de modo imediato e ambas oferecem algum grau de aceleração de hardware. Este tópico explora as diferenças entre Direct2D e GDI, incluindo as diferenças passadas e presentes nos recursos de aceleração de hardware de ambas as APIs.

Este tópico tem as seguintes partes:

-   [Diferenças entre Direct2D e GDI](#differences-between-direct2d-and-gdi)
-   [Aceleração de hardware GDI e Direct2D](#gdi-and-direct2d-hardware-acceleration)
    -   [Aumento da complexidade e do tamanho dos drivers de exibição](#increasing-complexity-and-size-of-display-drivers)
    -   [Dificuldade na sincronização de espaços de endereço de kernel global e sessão](#difficulty-in-synchronizing-session-and-global-kernel-address-spaces)
    -   [Gerenciamento de janelas compostas](#composited-window-management)
-   [Renderização GDI no Windows 7](#gdi-rendering-in-windows-7)
-   [Contraste de Direct2D e aceleração GDI no Windows 7](#contrasting-direct2d-and-gdi-acceleration-in-windows-7)
    -   [Local dos recursos](#location-of-resources)
    -   [Método de renderização](#rendering-method)
    -   [Escalabilidade](#scalability)
    -   [Localidade](#location-of-resources)
    -   [Disponibilidade de aceleração de hardware](#availability-of-hardware-acceleration)
    -   [Modelo de apresentação](#presentation-model)
-   [Conclusão](#conclusion)

## <a name="differences-between-direct2d-and-gdi"></a>Diferenças entre Direct2D e GDI

O [GDI](/windows/desktop/gdi/windows-gdi) renderiza geometrias opacas e com alias, como polígonos, elipses e linhas. Ele processa texto de alias e ClearType e pode dar suporte à mesclagem de transparência por meio da API AlphaBlend. No entanto, seu manuseio de transparência é inconsistente e a maioria das APIs GDI simplesmente ignora o canal alfa. Algumas APIs GDI garantem o que o canal alfa conterá após uma operação. O mais importante é que a renderização do GDI não é mapeada facilmente para operações 3D, e uma GPU moderna renderiza com mais eficiência a parte 3D de seu mecanismo de renderização. Por exemplo, as linhas com alias do [Direct2D](./direct2d-portal.md)são projetadas para serem implementadas simplesmente como dois triângulos renderizados na GPU, enquanto a GDI usa o algoritmo de desenho de linha do Bresenham.

O [Direct2D](./direct2d-portal.md) renderiza primitivos opacos, transparentes, com alias e com alias suavizados. As UIs modernas geralmente fazem uso de transparência e animação. O Direct2D facilita a criação de uma interface do usuário moderna, pois tem garantias estritas sobre como ela aceita e renderiza conteúdo transparente, e todos os seus primitivos são renderizados usando aceleração de hardware. Direct2D não é um superconjunto puro de [GDI](/windows/desktop/gdi/windows-gdi): primitivos que teriam pouco lentos quando implementado em uma GPU não estiver presente no Direct2D. Como o Direct2D é criado com essa ênfase na aceleração 3D, também é fácil de usar com o Direct3D.

Desde o Windows NT 4, o [GDI](/windows/desktop/gdi/windows-gdi) foi executado no modo kernel. O aplicativo chama o GDI, que chama seu equivalente de modo kernel, que passa os primitivos para seu próprio modelo de driver. Esse driver envia os resultados para o driver de vídeo do modo de kernel global.

A partir do Windows 2000, o [GDI](/windows/desktop/gdi/windows-gdi) e os drivers GDI foram executados em um espaço independente no kernel chamado "espaço de sessão". Um espaço de endereço de sessão é criado para cada sessão de logon, e cada instância de GDI é executada de forma independente nesse espaço de endereço de modo kernel distinto. No entanto, Direct2D é executado no modo de usuário e passa comandos de desenho por meio do driver Direct3D do modo de usuário para o driver de modo kernel.

![Figura 1-Direct2D em comparação com GDI](images/direct2d-vs-gdi1.png)

## <a name="gdi-and-direct2d-hardware-acceleration"></a>Aceleração de hardware GDI e Direct2D

A diferença mais importante entre a aceleração de hardware [Direct2D](./direct2d-portal.md) e [GDI](/windows/desktop/gdi/windows-gdi) é a tecnologia subjacente que as conduz. O Direct2D é colocado em camadas no Direct3D e o GDI superiores tem seu próprio modelo de driver, a DDI (interface de driver de dispositivo) do GDI, que corresponde aos primitivos GDI. O modelo de driver do Direct3D corresponde ao que o hardware de renderização 3D em uma GPU renderiza. Quando a DDI GDI foi definida pela primeira vez, a maioria dos hardwares de aceleração de exibição visaram os primitivos GDI. Ao longo do tempo, cada vez mais ênfase foi colocado na aceleração do jogo 3D e menos na aceleração do aplicativo. Como consequência, a API BitBlt foi acelerada pelo hardware e a maioria das outras operações GDI não era.

Isso define o estágio para uma sequência de alterações para o modo como a [GDI](/windows/desktop/gdi/windows-gdi) é renderizada para a exibição. A ilustração a seguir mostra como a renderização de vídeo GDI foi alterada do Windows XP para o Windows 7.

![Figura 2-evolução da renderização de exibição de GDI](images/direct2d-vs-gdi2.png)

Também havia vários fatores adicionais que causaram alterações no modelo de driver [GDI](/windows/desktop/gdi/windows-gdi) , conforme explicado abaixo.

### <a name="increasing-complexity-and-size-of-display-drivers"></a>Aumento da complexidade e do tamanho dos drivers de exibição

os drivers 3D se tornaram mais complexos ao longo do tempo. O código mais complexo tende a ter mais defeitos, o que o torna benéfico para que o driver exista no modo de usuário em que um bug de driver não pode causar uma reinicialização do sistema. Como pode ser visto na figura acima, o driver de vídeo é dividido em um componente de modo de usuário complexo e um componente de modo de kernel mais simples.

### <a name="difficulty-in-synchronizing-session-and-global-kernel-address-spaces"></a>Dificuldade na sincronização de espaços de endereço de kernel global e sessão

No Windows XP, existe um driver de vídeo em dois espaços de endereço diferentes: espaço de sessão e espaço do kernel. Partes do driver precisam responder a eventos como eventos de gerenciamento de energia. Isso precisa ser sincronizado com o estado do driver no espaço de endereço da sessão. Essa é uma tarefa difícil e pode levar a defeitos quando os drivers de exibição tentam lidar com esses espaços de endereço distintos.

### <a name="composited-window-management"></a>Gerenciamento de janelas compostas

O Gerenciador de Janelas da Área de Trabalho (DWM), o Gerenciador de janelas de composição introduzido no Windows 7, renderiza todas as janelas para superfícies fora da tela e as compõe para serem exibidas na tela. Isso exige que o [GDI](/windows/desktop/gdi/windows-gdi) seja capaz de renderizar para uma superfície que será renderizada pelo Direct3D para ser exibido. Isso representava um problema no modelo de driver XP, pois GDI e Direct3D eram pilhas de driver paralelas.

Como resultado, no Windows Vista, o driver de vídeo da DDI [GDI](/windows/desktop/gdi/windows-gdi) foi implementado como o CDD (driver de vídeo canônico) fornecido pela Microsoft, que processava o conteúdo GDI para um bitmap de memória do sistema para ser composto à tela.

## <a name="gdi-rendering-in-windows-7"></a>Renderização GDI no Windows 7

O modelo de driver usado no Windows Vista exigia que cada janela [GDI](/windows/desktop/gdi/windows-gdi) fosse apoiada por uma superfície de memória de vídeo e uma superfície de memória do sistema. Isso resultou na memória do sistema sendo usada para cada janela GDI.

Por esse motivo, o [GDI](/windows/desktop/gdi/windows-gdi) foi alterado novamente no Windows 7. . Em vez de renderizar para uma superfície de memória do sistema, o GDI foi modificado para renderizar para um segmento de memória de abertura. A memória de abertura pode ser atualizada a partir da superfície de memória de vídeo que contém o conteúdo da janela. O GDI pode retornar à memória de abertura e, em seguida, o resultado pode ser enviado de volta para a superfície da janela. Como o segmento de memória de abertura é endereçável pela GPU, a GPU pode acelerar essas atualizações para a superfície de memória de vídeo. Por exemplo, a renderização de texto, BitBlts, AlphaBlend, TransparentBlt e StretchBlt são aceleradas nesses casos.

## <a name="contrasting-direct2d-and-gdi-acceleration-in-windows-7"></a>Contraste de Direct2D e aceleração GDI no Windows 7

[Direct2D](./direct2d-portal.md) e [GDI](/windows/desktop/gdi/windows-gdi) são APIs de renderização de modo imediato 2D e são aceleradas por hardware. No entanto, há várias diferenças que permanecem em ambas as APIs.

### <a name="location-of-resources"></a>Local dos recursos

A [GDI](/windows/desktop/gdi/windows-gdi) mantém seus recursos, em determinados bitmaps, na memória do sistema por padrão. O [Direct2D](./direct2d-portal.md) mantém seus recursos na memória de vídeo no adaptador de vídeo. Quando a GDI precisa atualizar a memória de vídeo, isso deve ser feito no barramento, a menos que o recurso já esteja no segmento de memória de abertura ou se a operação puder ser expressa diretamente. Por outro lado, o Direct2D pode simplesmente traduzir seus primitivos para primitivos do Direct3D porque os recursos já estão na memória de vídeo.

### <a name="rendering-method"></a>Método de renderização

Para manter a compatibilidade, a [GDI](/windows/desktop/gdi/windows-gdi) realiza uma grande parte da renderização para a abertura da memória usando a CPU. Por outro lado, o [Direct2D](./direct2d-portal.md) converte suas chamadas de APIs em primitivos de Direct3D e operações de desenho. O resultado é então renderizado na GPU. Parte da renderização GDI? s é executada na GPU quando a memória de abertura é copiada para a superfície de memória de vídeo que representa a janela GDI.

### <a name="scalability"></a>Escalabilidade

As chamadas de renderização de [Direct2D](./direct2d-portal.md)são todos os fluxos de comando independentes para a GPU. Cada fábrica Direct2D representa um dispositivo Direct3D diferente. O [GDI](/windows/desktop/gdi/windows-gdi) usa um fluxo de comando para todos os aplicativos no sistema. O método da GDI pode resultar em uma criação de a sobrecarga de contexto de renderização de GPU e CPU.

### <a name="location"></a>Local

O [Direct2D](./direct2d-portal.md) funciona inteiramente no modo de usuário, incluindo o tempo de execução do Direct3D e o driver Direct3D do modo de usuário. Isso ajuda a evitar falhas do sistema causadas por defeitos de código no kernel. O [GDI](/windows/desktop/gdi/windows-gdi), no entanto, tem a maior parte de sua funcionalidade no espaço de sessão no modo kernel, com sua superfície de API no modo de usuário.

### <a name="availability-of-hardware-acceleration"></a>Disponibilidade de aceleração de hardware

O [GDI](/windows/desktop/gdi/windows-gdi) é acelerado por hardware no Windows XP e acelerado no Windows 7 quando o Gerenciador de janelas da área de trabalho está em execução e um driver WDDM 1,1 está em uso. O [Direct2D](./direct2d-portal.md) é acelerado por hardware em quase todos os drivers do WDDM e se o DWM está ou não em uso. No Vista, o GDI sempre será renderizado na CPU.

### <a name="presentation-model"></a>Modelo de apresentação

Quando o Windows foi criado pela primeira vez, havia memória insuficiente para permitir que cada janela fosse armazenada em seu próprio bitmap. Como resultado, a [GDI](/windows/desktop/gdi/windows-gdi) sempre é renderizada logicamente diretamente na tela, com várias regiões de recorte aplicadas para garantir que um aplicativo não fosse renderizado fora de sua janela. No modelo [Direct2D](./direct2d-portal.md) , um aplicativo é renderizado em um buffer de fundo e o resultado é exibido quando o aplicativo é feito o desenho. Isso permite que o Direct2D manipule cenários de animação de forma muito mais fluida do que o GDI pode.

## <a name="conclusion"></a>Conclusão

O código [GDI](/windows/desktop/gdi/windows-gdi) existente continuará funcionando bem no Windows 7. No entanto, ao escrever um novo código de renderização de gráficos, [Direct2D](./direct2d-portal.md) deve ser considerado, pois aproveita melhor as GPUs modernas.

 

 