---
title: Comparando a aceleração Direct2D hardware GDI e Direct2D GDI
description: Direct2D gDI são APIs de renderização 2D de modo imediato e ambas oferecem algum grau de aceleração de hardware.
ms.assetid: 0028a0c3-445d-46b7-b55b-46dff3bce9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daa5fcb0f186915570d220a2807f816eae7a20fb393fbcd3113f6abf686fcd44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826531"
---
# <a name="comparing-direct2d-and-gdi-hardware-acceleration"></a>Comparando a aceleração Direct2D hardware GDI e Direct2D GDI

[Direct2D](./direct2d-portal.md) [gDI](/windows/desktop/gdi/windows-gdi) são APIs de renderização 2D de modo imediato e ambas oferecem algum grau de aceleração de hardware. Este tópico explora as diferenças entre Direct2D GDI, incluindo diferenças passadas e presentes nos recursos de aceleração de hardware de ambas as APIs.

Este tópico tem as seguintes partes:

-   [Diferenças entre Direct2D gDI](#differences-between-direct2d-and-gdi)
-   [GDI e aceleração Direct2D hardware](#gdi-and-direct2d-hardware-acceleration)
    -   [Aumentar a complexidade e o tamanho dos drivers de exibição](#increasing-complexity-and-size-of-display-drivers)
    -   [Dificuldade na sincronização de sessão e espaços de endereço do kernel global](#difficulty-in-synchronizing-session-and-global-kernel-address-spaces)
    -   [Gerenciamento de janela composta](#composited-window-management)
-   [Renderização de GDI Windows 7](#gdi-rendering-in-windows-7)
-   [Comparação entre Direct2D e aceleração de GDI Windows 7](#contrasting-direct2d-and-gdi-acceleration-in-windows-7)
    -   [Local dos recursos](#location-of-resources)
    -   [Método de renderização](#rendering-method)
    -   [Escalabilidade](#scalability)
    -   [Localização](#location-of-resources)
    -   [Disponibilidade de aceleração de hardware](#availability-of-hardware-acceleration)
    -   [Modelo de apresentação](#presentation-model)
-   [Conclusão](#conclusion)

## <a name="differences-between-direct2d-and-gdi"></a>Diferenças entre Direct2D gDI

[A GDI](/windows/desktop/gdi/windows-gdi) renderiza geometrias opacas, com alias, como polígonos, reellipses e linhas. Ele renderiza um texto com alias e ClearType e pode dar suporte à mesclagem de transparência por meio da API AlphaBlend. No entanto, seu tratamento de transparência é inconsistente e a maioria das APIs GDI simplesmente ignora o canal alfa. Algumas APIs GDI garantem o que o canal alfa conterá após uma operação. O mais importante é que a renderização da GDI não mapeia facilmente para operações 3D e uma GPU moderna renderiza com mais eficiência na parte 3D do mecanismo de renderização. Por exemplo, [Direct2D](./direct2d-portal.md)linhas com alias de Direct2D são projetadas para serem implementadas simplesmente como dois triângulos renderizados na GPU, enquanto a GDI usa o algoritmo de desenho de linha de Bresenham.

[Direct2D](./direct2d-portal.md) renderiza primitivos opacos, transparentes, com alias e sem alias. UIs modernas geralmente usam transparência e animação. Direct2D facilita a criação de uma interface do usuário moderna porque ela tem garantias estritas sobre como aceita e renderiza conteúdo transparente e todos os seus primitivos são renderizados usando aceleração de hardware. Direct2D não é um superconjunto puro de [GDI:](/windows/desktop/gdi/windows-gdi)primitivos que teriam sido irrediavelmente lentos quando implementados em uma GPU não estão presentes no Direct2D. Como Direct2D é criado com essa ênfase na aceleração 3D, também é fácil de usar com o Direct3D.

Desde Windows NT 4, [o GDI](/windows/desktop/gdi/windows-gdi) foi executado no modo kernel. O aplicativo chama gDI que, em seguida, chama seu equivalente de modo kernel, que passa os primitivos para seu próprio modelo de driver. Em seguida, esse driver envia os resultados para o driver de exibição do modo kernel global.

A partir Windows 2000, os drivers GDI e [GDI](/windows/desktop/gdi/windows-gdi) foram executados em um espaço independente no kernel chamado "espaço de sessão". Um espaço de endereço de sessão é criado para cada sessão de logon e cada instância do GDI é executado independentemente nesse espaço de endereço de modo kernel distinto. Direct2D, no entanto, é executado no modo de usuário e passa comandos de desenho por meio do driver Direct3D do modo de usuário para o driver de modo kernel.

![figura 1 – direct2d em comparação com gdi](images/direct2d-vs-gdi1.png)

## <a name="gdi-and-direct2d-hardware-acceleration"></a>GDI e aceleração Direct2D hardware

A diferença mais importante entre a Direct2D e [a](./direct2d-portal.md) [aceleração de](/windows/desktop/gdi/windows-gdi) hardware GDI é a tecnologia subjacente que as orienta. Direct2D é em camadas no Direct3D superior e a GDI tem seu próprio modelo de driver, a DDI (Interface do Driver de Dispositivo) GDI, que corresponde aos primitivos da GDI. O modelo de driver Direct3D corresponde ao que o hardware de renderização 3D em uma GPU renderiza. Quando a DDI GDI foi definida pela primeira vez, a maioria dos hardwares de aceleração de exibição foi direcionada aos primitivos da GDI. Ao longo do tempo, cada vez mais ênfase foi colocada na aceleração de jogos 3D e menos na aceleração do aplicativo. Como consequência, a API do BitBlt foi acelerada por hardware e a maioria das outras operações de GDI não.

Isso definirá o estágio de uma sequência de alterações em como [a GDI](/windows/desktop/gdi/windows-gdi) é renderiza para a exibição. A ilustração a seguir mostra como a renderização de exibição GDI foi alterada Windows XP para Windows 7.

![Figura 2 – evolução da renderização de exibição gdi](images/direct2d-vs-gdi2.png)

Também houve vários fatores adicionais que causaram alterações no modelo de driver [GDI,](/windows/desktop/gdi/windows-gdi) conforme explicado abaixo.

### <a name="increasing-complexity-and-size-of-display-drivers"></a>Aumentar a complexidade e o tamanho dos drivers de exibição

Drivers 3D se tornaram mais complexos ao longo do tempo. O código mais complexo tende a ter mais defeitos, tornando-o benéfico para o driver existir no modo de usuário em que um bug de driver não pode causar uma reinicialização do sistema. Como pode ser visto na figura acima, o driver de exibição é dividido em um componente de modo de usuário complexo e um componente de modo kernel mais simples.

### <a name="difficulty-in-synchronizing-session-and-global-kernel-address-spaces"></a>Dificuldade na sincronização de sessão e espaços de endereço do kernel global

No Windows XP, existe um driver de exibição em dois espaços de endereço diferentes: espaço de sessão e espaço do kernel. Partes do driver precisam responder a eventos como eventos de gerenciamento de energia. Isso precisa ser sincronizado com o estado do driver no espaço de endereço da sessão. Essa é uma tarefa difícil e pode levar a defeitos quando drivers de exibição tentam lidar com esses espaços de endereço distintos.

### <a name="composited-window-management"></a>Gerenciamento de janela composta

O Gerenciador de Janelas da Área de Trabalho (DWM), o gerenciador de janelas de composição introduzido no Windows 7, renderiza todas as janelas em superfícies fora da tela e, em seguida, as compõe juntas para serem exibidas na tela. Isso exige [que a GDI](/windows/desktop/gdi/windows-gdi) seja capaz de renderizar em uma superfície que será renderizada pelo Direct3D para exibição. Isso era um problema no modelo de driver XP, uma vez que GDI e Direct3D eram pilhas de driver paralelas.

Como resultado, no Windows Vista, o driver de exibição DDI [GDI](/windows/desktop/gdi/windows-gdi) foi implementado como o CDD (Driver de Exibição Canônico) fornecido pela Microsoft, que renderizou o conteúdo GDI para um bitmap de memória do sistema a ser composto na tela.

## <a name="gdi-rendering-in-windows-7"></a>Renderização de GDI Windows 7

O modelo de driver usado no Windows Vista exigia que cada janela [GDI](/windows/desktop/gdi/windows-gdi) fosse apoiada por uma superfície de memória de vídeo e uma superfície de memória do sistema. Isso resultou na memória do sistema que está sendo usada para cada janela GDI.

Por esse motivo, [a GDI](/windows/desktop/gdi/windows-gdi) foi alterada novamente Windows 7. . Em vez de renderizar para uma superfície de memória do sistema, a GDI foi modificada para renderizar para um segmento de memória de abertura. A memória de abertura pode ser atualizada da superfície de memória de vídeo que mantém o conteúdo da janela. A GDI pode renderizar de volta para a memória de abertura e o resultado pode ser enviado de volta para a superfície da janela. Como o segmento de memória de abertura é acessível pela GPU, a GPU pode acelerar essas atualizações para a superfície de memória de vídeo. Por exemplo, a renderização de texto, BitBlts, AlphaBlend, TransparentBlt e StretchBlt são aceleradas nesses casos.

## <a name="contrasting-direct2d-and-gdi-acceleration-in-windows-7"></a>Comparação entre Direct2D e aceleração de GDI Windows 7

[Direct2D](./direct2d-portal.md) e [GDI são](/windows/desktop/gdi/windows-gdi) APIs de renderização de modo imediato 2D e são aceleradas por hardware. No entanto, há várias diferenças que permanecem em ambas as APIs.

### <a name="location-of-resources"></a>Local dos recursos

[A GDI](/windows/desktop/gdi/windows-gdi) mantém seus recursos, em bitmaps específicos, na memória do sistema por padrão. [Direct2D](./direct2d-portal.md) mantém seus recursos na memória de vídeo no adaptador de exibição. Quando a GDI precisa atualizar a memória de vídeo, isso deve ser feito no barramento, a menos que o recurso já esteja no segmento de memória de abertura ou se a operação puder ser expressa diretamente. Por outro lado, Direct2D pode simplesmente traduzir seus primitivos para primitivos direct3D porque os recursos já estão na memória de vídeo.

### <a name="rendering-method"></a>Método de renderização

Para manter a compatibilidade, a [GDI](/windows/desktop/gdi/windows-gdi) executa uma grande parte de sua renderização para a memória de abertura usando a CPU. Por outro lado, [Direct2D](./direct2d-portal.md) converte suas chamadas de APIs em primitivos Direct3D e operações de desenho. O resultado é renderizado na GPU. Parte da renderização GDI é executada na GPU quando a memória de abertura é copiada para a superfície de memória de vídeo que representa a janela GDI.

### <a name="scalability"></a>Escalabilidade

[Direct2D](./direct2d-portal.md)chamadas de renderização do são todos fluxos de comando independentes para a GPU. Cada Direct2D factory representa um dispositivo Direct3D diferente. [A GDI](/windows/desktop/gdi/windows-gdi) usa um fluxo de comandos para todos os aplicativos no sistema. O método da GDI pode resultar em um build de sobrecarga de contexto de renderização de GPU e CPU.

### <a name="location"></a>Localização

[Direct2D](./direct2d-portal.md) funciona inteiramente no modo de usuário, incluindo o tempo de run time do Direct3D e o driver Direct3D do modo de usuário. Isso ajuda a evitar falhas do sistema causadas por defeitos de código no kernel. [No entanto,](/windows/desktop/gdi/windows-gdi)a GDI tem a maior parte de sua funcionalidade no espaço de sessão no modo kernel, com sua superfície de API no modo de usuário.

### <a name="availability-of-hardware-acceleration"></a>Disponibilidade de aceleração de hardware

[A GDI](/windows/desktop/gdi/windows-gdi) é acelerada por hardware no Windows XP e acelerada no Windows 7 quando o Gerenciador de Janelas da Área de Trabalho está em execução e um driver WDDM 1.1 está em uso. [Direct2D](./direct2d-portal.md) hardware é acelerado em quase qualquer driver WDDM e se o DWM está ou não em uso. No Vista, o GDI sempre renderizará na CPU.

### <a name="presentation-model"></a>Modelo de apresentação

quando Windows foi criado pela primeira vez, havia memória insuficiente para permitir que cada janela fosse armazenada em seu próprio bitmap. Como resultado, a [GDI](/windows/desktop/gdi/windows-gdi) sempre é renderizada logicamente diretamente na tela, com várias regiões de recorte aplicadas para garantir que um aplicativo não fosse renderizado fora de sua janela. no modelo de [Direct2D](./direct2d-portal.md) , um aplicativo é renderizado para um buffer de back-out e o resultado é exibido quando o aplicativo é feito o desenho. isso permite que Direct2D manipule cenários de animação de forma muito mais fluida do que o GDI pode.

## <a name="conclusion"></a>Conclusão

o código [GDI](/windows/desktop/gdi/windows-gdi) existente continuará funcionando bem em Windows 7. no entanto, ao escrever um novo código de renderização de gráficos, [Direct2D](./direct2d-portal.md) deve ser considerado, pois aproveita melhor as GPUs modernas.

 

 