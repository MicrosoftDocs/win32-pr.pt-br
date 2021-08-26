---
description: Este tópico fornece orientação para desenvolvedores sobre como maximizar o desempenho e a eficiência na pilha de apresentação em versões modernas do Windows.
ms.assetid: B6B92F4F-B1D0-40B9-987D-F0C0F2CC7AD1
title: Para obter o melhor desempenho, use o modelo de flip DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: RS5
ms.openlocfilehash: ce999bc735042132902158cfd6bd6d41296d29a3afc98ab27d9480dc6bd8b3b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951216"
---
# <a name="for-best-performance-use-dxgi-flip-model"></a>Para obter o melhor desempenho, use o modelo de flip DXGI

Este tópico fornece orientação para desenvolvedores sobre como maximizar o desempenho e a eficiência na pilha de apresentação em versões modernas do Windows. ele começa onde o [DXGI flip model](dxgi-flip-model.md), [DirectX 12: modos de apresentação em Windows 10 (vídeo)](https://www.youtube.com/watch?v=E3wTajGZOsA)e [aprimoramentos de apresentação no Windows 10: uma aparência antecipada (vídeo)](https://www.youtube.com/watch?v=nUZVV_mssWQ) parou.

## <a name="call-to-action"></a>Chamada para ação

Se você ainda estiver usando o efeito de permuta de **dxgi/ \_ \_ \_ descarte** de efeito de permuta ou de **\_ troca \_ \_** de dxgi (também conhecido como o modelo presente "BLT"), é hora de parar!

Alternando para o efeito de permuta de dxgi inverter sequência de **\_ efeito de permuta \_ \_ \_** **\_ \_ \_ \_ seqüencial** ou dxgi (também conhecido como o modelo de inversão) fornecerá melhor desempenho, menor consumo de energia e fornecer um conjunto mais rico de recursos. (Consulte [ \_ enumeração de \_ efeito de permuta de dxgi](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) para obter mais informações sobre esses valores.)

O flip Model apresenta até o modo em janela, efetivamente equivalente ou melhor quando comparado ao modo clássico de "tela inteira". Na verdade, talvez você queira reconsiderar se seu aplicativo realmente precisa de um modo em tela inteira, já que os benefícios de uma janela invertida sem borda de modelo incluem mais rapidez Alt-Tab troca e melhor integração com recursos de exibição modernos.

Por que agora? Antes da atualização de abril de 2018, o modelo BLT apresenta poderia resultar na divisão visível quando usada em configurações de GPU híbridas, muitas vezes encontradas em laptops de ponta (consulte [KB 3158621](https://support.microsoft.com/help/3158621/hybrid-graphics-and-vsync-results-in-graphic-tearing-in-some-games-and)). Na atualização de abril de 2018, essa divisão foi corrigida, com o custo de algum trabalho adicional. Se você estiver fazendo BLT presentes em altas taxas de quadros entre GPUs híbridas, especialmente em altas resoluções como 4K, esse trabalho adicional poderá afetar o desempenho geral. Para manter o melhor desempenho nesses sistemas, alterne do BLT para o modelo de inversão atual. Além disso, considere reduzir a resolução do seu SwapChain, especialmente se não for o ponto principal de interação do usuário (como geralmente é o caso com o Windows de visualização VR).

## <a name="a-brief-history"></a>Um breve histórico

O que é o modelo de inversão? Qual é a alternativa?

antes do Windows 7, a única maneira de apresentar conteúdo do D3D era "blt" ou copiá-lo para uma superfície que era de propriedade da janela ou da tela. começando com o efeito de permuta D3D9's FLIPEX e chegando a DXGI por meio do \_ efeito de permuta sequencial invertido no Windows 8, desenvolvemos uma maneira mais eficiente de colocar o conteúdo na tela, compartilhando-o diretamente com o compositor da área de trabalho, com cópias mínimas. Consulte [modelo de inversão dxgi](dxgi-flip-model.md) para obter uma visão geral de alto nível da tecnologia.

essa otimização é possível graças ao DWM (Gerenciador de Janelas da Área de Trabalho), que é o compositor que orienta a área de trabalho Windows.

## <a name="when-should-i-use-the-blt-model"></a>Quando devo usar o modelo BLT?

Há uma parte da funcionalidade que o modelo invertido não fornece: a capacidade de ter várias APIs diferentes que produzem conteúdo, que todas as camadas estão juntas no mesmo **HWND**, em uma base atual. um exemplo disso seria usar o D3D para desenhar um plano de fundo da janela e, em seguida, [Windows GDI](/windows/desktop/gdi/windows-gdi) para desenhar algo na parte superior, ou usando duas APIs de gráficos diferentes, ou duas permuta da mesma API, para produzir quadros alternados. Se você não exigir a interoperabilidade no nível do **HWND** entre componentes gráficos, não precisará do modelo blt.

Há uma segunda parte da funcionalidade que não foi fornecida no design original do modelo de inversão, mas está disponível agora, que é a capacidade de apresentar em uma taxa de quadros sem limitação. Para um aplicativo que usa o intervalo de sincronização 0, não recomendamos mudar para o modelo inverter a menos que a API [IDXGIFactory5:: CheckFeatureSupport](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) esteja disponível e o suporte a relatórios para o **\_ recurso dxgi \_ presente \_ permita a \_ divisão**. esse recurso é praticamente onipresente em versões recentes do Windows 10 e no hardware moderno.

## <a name="directflip"></a>DirectFlip

se você tiver observado [DirectX 12: modos de apresentação no Windows 10](https://www.youtube.com/watch?v=E3wTajGZOsA), verá uma conversa sobre "Direct flip" e "inverter independente". Essas são otimizações que são habilitadas para aplicativos usando o flip Model permuta. Dependendo da configuração da janela e do buffer, é possível ignorar totalmente a composição de área de trabalho e enviar os quadros de aplicativo diretamente para a tela, da mesma forma que a tela inteira exclusiva.

Hoje em dia, essas otimizações podem se envolver em um dos três cenários, a fim de aumentar a funcionalidade:

1.  **DirectFlip**: os buffers do SwapChain correspondem às dimensões da tela e a região do cliente do Windows cobre a tela. Em vez de usar o DWM SwapChain para exibir na tela, o aplicativo SwapChain é usado.
2.  **DirectFlip com Panel Fitters**: sua região de cliente de janela cobre a tela e os buffers de SwapChain estão dentro de um fator de dimensionamento dependente de hardware (por exemplo, 0,25 x a 4x) da tela. O hardware de verificação de GPU é usado para dimensionar o buffer enquanto o envia para a exibição.
3.  **DirectFlip com o MPO (sobreposição de vários planos)**: os buffers do SwapChain estão dentro de um fator de dimensionamento dependente de hardware das dimensões da janela. O DWM é capaz de reservar um plano de exame de hardware dedicado para seu aplicativo, que é então examinado e potencialmente ampliado para uma sub-região de triagem alfa da tela.

Com o modelo de inversão em janela, o aplicativo pode consultar o suporte de hardware para diferentes cenários de DirectFlip e implementar diferentes tipos de dimensionamento dinâmico por meio do uso de [IDXGIOutput6:: CheckHardwareCompositionSupport](/windows/desktop/api/DXGI1_6/nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport). Uma limitação a ter em mente é que, se o painel Fitters for utilizado, é possível que o cursor sofra um alongamento de efeitos colaterais, o que é indicado por meio do **cursor de sinalizador de suporte de composição de hardware dxgi \_ \_ \_ \_ \_ \_ alongado**.

Depois que o SwapChain tiver sido "DirectFlipped", o DWM poderá ir para o estado de suspensão e somente acordar quando algo for alterado fora do seu aplicativo. Os quadros de aplicativo são enviados diretamente para a tela, independentemente, com a mesma eficiência que a tela de ativação exclusiva. Essa é uma "inversão independente" e pode se envolver em todos os cenários acima. Se outros conteúdos da área de trabalho aparecerem na parte superior, o DWM poderá fazer a transição diretamente para o modo composto, com eficiência "reverter a composição" do conteúdo na parte superior do aplicativo antes de invertê-lo ou aproveitar o MPO para manter o modo invertido independente.

Confira a ferramenta [PresentMon](https://github.com/GameTechDev/PresentMon) para obter informações sobre qual das opções acima foram usadas.

## <a name="what-else-is-new-in-the-flip-model"></a>O que mais é novo no modelo de inversão?

Além dos aprimoramentos acima, que se aplicam a permuta padrão sem nada especial, há vários recursos disponíveis para o uso de aplicativos de modelo de flip:

-   Diminuindo a latência usando o **\_ objeto de \_ espera de \_ latência do quadro do sinalizador de \_ \_ \_ \_ cadeia de permuta dxgi**. quando estiver no modo inadequado inativo, você poderá obter até 1 quadro de latência em versões recentes do Windows, com fallback normal para o mínimo possível quando composto.
    -   advertência: houve um problema que fornecia um mínimo de dois quadros de latência na atualização Windows 10 aniversário e anterior. Consulte [Este tópico do fórum](https://www.gamedev.net/forums/topic/686507-windows-10-dx12-low-latency-tearing-free-rendering/) para obter mais informações. Isso é corrigido na atualização do criador de outono.
-   **Dxgi \_ O \_ efeito de permuta \_ inverter \_ descartar** permite um modo de "composição inversa" de inverter direto, o que resulta em menos trabalho geral para exibir a área de trabalho. O DWM pode rabiscar os buffers de aplicativo e enviá-los para a tela, em vez de executar uma cópia completa em seus próprios permuta.
-   **Dxgi \_ O \_ sinalizador de cadeia de permuta \_ \_ permite que a \_ divisão** possa habilitar uma latência ainda menor do que o objeto que pode ser aguardado, mesmo em uma janela em sistemas com suporte à sobreposição de vários planos.
-   Os aplicativos têm controle sobre o dimensionamento de conteúdo que ocorre durante o redimensionamento da janela, usando a propriedade de [ \_ dimensionamento dxgi](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling) definida durante a criação de SwapChain.
-   O conteúdo em formatos HDR (R10G10B10A2 \_ UNORM ou R16G16B16A16 \_ float) não é clamped, a menos que seja composto para uma área de trabalho SDR.
-   As estatísticas presentes estão disponíveis no modo de janela.
-   há maior compatibilidade com o modelo de aplicativo UWP (Plataforma Universal do Windows) e DX12, já que eles são compatíveis apenas com o modelo de inversão.

## <a name="what-do-i-have-to-do-to-use-the-flip-model"></a>O que preciso fazer para usar o modelo de flip?

O flip Model permuta tem alguns requisitos adicionais na parte superior do BLT permuta:

1.  A contagem de buffers deve ser pelo menos 2.
2.  Após as chamadas [presentes](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) , o buffer de fundo precisará ser reassociado explicitamente ao contexto D3D11 imediato para que possa ser usado novamente.
3.  Depois de chamar [Setfullscreenstate](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate), o aplicativo deve chamar [ResizeBuffers](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) antes de **presente**.
4.  Não há suporte direto para permuta de MSAA (multiamostrar a suavização) no modelo de inversão, portanto, o aplicativo precisará fazer uma resolução de MSAA antes de emitir o **presente**.

## <a name="how-to-choose-the-right-rendering-and-presentation-resolutions"></a>Como escolher a renderização correta e as resoluções de apresentação

O padrão tradicional para aplicativos no passado foi fornecer ao usuário uma lista de resoluções para escolher quando o usuário seleciona o modo de tela inteira exclusiva. Com a capacidade de exibições modernas para iniciar o dimensionamento de conteúdo diretamente, considere fornecer aos usuários a capacidade de escolher uma resolução de renderização para o dimensionamento de desempenho, independentemente de uma resolução de saída e até mesmo no modo de janela. Além disso, os aplicativos devem aproveitar **IDXGIOutput6:: CheckHardwareCompositionSupport** para determinar se precisam dimensionar o conteúdo antes de apresentá-lo, ou se eles devem permitir que o hardware faça o dimensionamento para eles.

Seu conteúdo pode precisar ser migrado de uma GPU para outra como parte da operação atual ou de composição. Isso geralmente é verdadeiro em laptops de várias GPUS ou sistemas com GPUs externas conectadas. Como essas configurações são mais comuns, e como as exibições de alta resolução se tornam mais comuns, o custo da apresentação de uma SwapChain de resolução completa aumenta. Se o destino de seu SwapChain não for o ponto principal de interação do usuário, como é geralmente o caso com títulos VR que apresentam uma visualização 2D da cena VR em uma janela secundária, considere usar uma SwapChain de resolução mais baixa para minimizar a quantidade de largura de banda que precisa ser transferida em GPUs diferentes.

## <a name="other-considerations"></a>Outras considerações

Na primeira vez que você solicitar que a GPU grave no buffer de fundo do SwapChain é o tempo que a GPU irá parar de esperar que o buffer fique disponível. Quando possível, adie esse ponto até o quadro o mais possível.

 

 
