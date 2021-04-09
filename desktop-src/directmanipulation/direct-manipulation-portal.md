---
description: As APIs de manipulação direta permitem que você crie grandes experiências de usuário panorâmica, zoom e arrastar. Para fazer isso, ele processa a entrada por toque em uma região ou um objeto, gera transformações de saída e aplica as transformações aos elementos da interface do usuário.
ms.assetid: 26358bc5-71e9-40f0-9243-9bddd961a0e5
title: Manipulação direta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6db2a50893914dfb25050768f88cb289a1ecf3ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087538"
---
# <a name="direct-manipulation"></a>Manipulação direta

As APIs de manipulação direta permitem que você crie grandes experiências de usuário panorâmica, zoom e arrastar. Para fazer isso, ele processa a entrada por toque em uma região ou um objeto, gera transformações de saída e aplica as transformações aos elementos da interface do usuário. Você pode usar a manipulação direta para otimizar a capacidade de resposta e reduzir a latência por meio do processamento de entrada fora do thread, testes de clique de entrada fora do thread opcional e previsão de entrada/saída.

Qualquer aplicativo que usa a manipulação direta para processar interações de toque exibe as animações do fluido do Windows 8 e os comportamentos de comentários de interação que estão em conformidade com as [diretrizes para interações comuns do usuário](/windows/uwp/design/input/).

## <a name="developer-audience"></a>Público do desenvolvedor

A API de manipulação direta é para desenvolvedores experientes que conhecem o C/C++, têm uma compreensão sólida do [com (Component Object Model)](../com/component-object-model--com--portal.md)e estão familiarizados com os conceitos de programação do Windows.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A manipulação direta foi introduzida no Windows 8. Ele está incluído nas versões de 32 bits e 64 bits.

## <a name="why-use-directmanipulation"></a>Por que usar DirectManipulation

### <a name="handles-interactions-in-a-straightforward-and-consistent-manner"></a>Manipula as interações de maneira direta e consistente

A manipulação direta funciona pré-declarando os comportamentos e as interações para uma região ou objeto. Por exemplo, uma página da Web geralmente é configurada para panorâmica e zoom. Em tempo de execução, a entrada é então associada a essa região/objeto por meio de uma chamada de API simples. Desse ponto, a manipulação direta faz todo o trabalho pesado de processar a entrada, aplicar restrições e personalidade e gerar as transformações de saída.

### <a name="build-responsive-touch-applications"></a>Crie aplicativos responsivos de toque

Para otimizar a capacidade de resposta e minimizar a latência, o processamento de manipulação direta ocorre em um thread separado e independente do thread da interface do usuário. Como resultado, as transformações de saída podem ser executadas em paralelo à atividade no thread da interface do usuário. A atividade thread de interface do usuário pode incluir lógica do aplicativo, renderização, layout e qualquer outra coisa que consuma ciclos no processador.

### <a name="implementation-flexibility"></a>Flexibilidade de implementação

As interfaces incluídas com a manipulação direta fornecem suporte abrangente para tratamento de entrada, reconhecimento de interação, notificações de comentários e atualizações de interface do usuário. As interfaces também incorporam serviços do sistema, como [DirectComposition](../directcomp/directcomposition-portal.md).

## <a name="basic-concepts"></a>Conceitos básicos

A implementação de manipulação direta mais básica consiste em um *visor*, *conteúdo* e *interações*. O *visor* é uma região que é capaz de receber e processar a entrada de interações do usuário. Também é a região do conteúdo que é visível para o usuário final. O *conteúdo* é o objeto real que os usuários finais podem ver e é o que move ou dimensiona em resposta a uma interação do usuário. As *interações* do usuário primário (também conhecidas como *manipulações*) com suporte para a manipulação direta são a panorâmica e o zoom. Essas interações aplicam uma transformação de conversão ou de escala ao conteúdo dentro do visor, respectivamente. Vários visores (cada um com seu próprio conteúdo) podem ser configurados em uma única janela para criar uma experiência de interface do usuário rica.

Esta figura mostra uma implementação básica de manipulação direta antes e depois do movimento panorâmico.

![implementação básica de manipulação direta antes e depois do movimento panorâmico.](images/dm-art-1.png)

Durante a inicialização da manipulação direta, um objeto **DCompDirectManipulationCompositor** é instanciado e está associado à manipulação direta. Esse objeto é um wrapper em volta de [DirectComposition](../directcomp/directcomposition-portal.md), que é o compositor do sistema. O objeto é responsável por aplicar as transformações de saída e orientar as atualizações visuais.

Um contato representa um ponto de toque identificado pelo **ponteiroid** fornecido na mensagem do [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) . Quando uma mensagem do **WM \_ POINTERDOWN** é recebida, o aplicativo chama [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact). O aplicativo notifica Manipulationabout diretos os contatos que devem ser manipulados e as visores que devem reagir a esses contatos. A entrada de teclado e de mouse têm valores de **ponteiroid** especiais para que possam ser manipuladas adequadamente pela manipulação direta.

Em nosso caso básico acima, quando [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) é chamado de algumas coisas acontecem:

- Quando o usuário executa uma panorâmica, uma mensagem do [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) é enviada ao aplicativo para notificar que o contato foi consumido pela manipulação direta.
- Quando o usuário move as movimentações, o visor aciona eventos de atualização que são usados pelo wrapper [DirectComposition](../directcomp/directcomposition-portal.md) para direcionar as atualizações visuais para a tela. Para um panorama de um usuário em um visor, o conteúdo parecerá ser movido suavemente sob o contato.
- Quando o usuário levanta o contato, o usuário vê que o conteúdo continua a ser movido à medida que faz a transição para uma animação inércia, gradualmente decelerating até atingir seu local de repouso final.

## <a name="processing-keyboard-and-mouse-input"></a>Processando entrada de teclado e mouse

A manipulação direta permite que as mensagens de teclado e mouse sejam encaminhadas manualmente do thread de interface do usuário do aplicativo por meio da API [**ProcessInput**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-processinput) de forma que elas possam ser manipuladas adequadamente pela manipulação direta.

## <a name="directmanipulation-and-the-hwnd"></a>DirectManipulation e HWND

A manipulação direta está associada a um HWND Win32 para receber e processar mensagens de entrada de ponteiro para essa janela. Como a manipulação direta computa valores de saída, ele faz retornos de chamada assíncronos para os objetos [com (Component Object Model](../com/component-object-model--com--portal.md) de manipulação direta) que são implementados no aplicativo. Esses retornos de chamada informam o aplicativo sobre a transformação que foi aplicada aos objetos. A manipulação direta é ativada no HWND especificado chamando [**Activate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-activate).

## <a name="supporting-documentation"></a>Documentação de suporte

- [Visores e conteúdo](directmanipulation-viewports-and-content.md)
- [Usando vários viewports no DirectManipulation](directmanipulation-multiple-vieports.md)
- [Processando a entrada com DirectManipulation](directmanipulation-processing-input-with-directmanipulation.md)
- [Mecanismo de composição](directmanipulation-composition-engine.md)
- [Referência de manipulação direta](direct-manipulation-reference.md)

- [BUILD 2013: WCL-022: torne seu aplicativo de área de trabalho ótimo com toque, mouse e caneta](https://channel9.msdn.com/Events/Build/2013/4-022)
- [Exemplo de processamento de entrada de toque com manipulação direta](https://github.com/microsoft/Windows-classic-samples/tree/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/TouchInputDirectManipulation)
