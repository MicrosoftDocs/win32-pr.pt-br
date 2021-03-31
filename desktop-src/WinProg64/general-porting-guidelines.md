---
title: Diretrizes gerais de portabilidade
description: Portar aplicativos de 32 bits para o Microsoft Windows de 64 bits será mais fácil do que portar aplicativos de 16 bits para o Windows de 32 bits. No entanto, a mudança ficará mais tranqüila com um planejamento cuidadoso. Veja a seguir algumas diretrizes gerais.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- portando aplicativos de 32 bits para programação do Windows de 64 bits Windows de 64 bits
- Guia de programação do Windows de 64 bits – programação do Windows de 64 bits, diretrizes de portabilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31734edd8b85bd61b8b84cb2c66d835f0085ac1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "104172414"
---
# <a name="general-porting-guidelines"></a>Diretrizes gerais de portabilidade

Portar aplicativos de 32 bits para o Microsoft Windows de 64 bits será mais fácil do que portar aplicativos de 16 bits para o Windows de 32 bits. No entanto, a mudança ficará mais tranqüila com um planejamento cuidadoso. Veja a seguir algumas diretrizes gerais.

## <a name="planning"></a>Planejamento

-   Determine a magnitude do esforço necessário para a porta. Avalie a quantidade de trabalho envolvida identificando os seguintes itens:
    -   Problema 32-código de bit. Compile o código de 32 bits com o compilador de 64 bits e examine a extensão dos erros e avisos.
    -   Componentes compartilhados ou dependências. Determine quais componentes em seu aplicativo se originam de outras equipes e se essas equipes planejam desenvolver versões de 64 bits de seu código.
    -   Código herdado ou assembly. aplicativos baseados no Windows de 16 bits não são executados em janelas de 64 bits e devem ser reescritos. Embora o código do assembly x86 seja executado no WOW64, talvez você queira reescrever esse código para aproveitar a velocidade da arquitetura Intel Itanium.
-   Portar todo o aplicativo, não apenas partes dele.

    Embora seja possível portar partes de um aplicativo ou limitar o código a 2G com/LARGEADDRESSAWARE: não, essa estratégia compensa o lucro de curto prazo para problemas de longo prazo.

    > [!Note]  
    > /LARGEADDRESSAWARE: não é ignorado para um binário ARM64.

     

-   Localize substitutos para tecnologias que não serão portadas.

    Algumas tecnologias, incluindo o DAO (objeto de acesso a dados) e o mecanismo de banco de dados do Jet Red, não serão portadas para o Windows de 64 bits.

-   Trate sua versão de 64 bits como uma versão de produto separada.

    Embora seu produto de 64 bits possa compartilhar a mesma base de código que o de 32 bits, ele precisa de testes adicionais e pode ter outras considerações de versão.

## <a name="development"></a>Desenvolvimento

-   Comece a desenvolver código em conformidade agora mesmo.

    Os desenvolvedores podem começar a escrever código em conformidade usando os arquivos de cabeçalho mais recentes do Windows e os novos tipos de dados sem efeitos adversos no desenvolvimento de produtos de 32 bits. Para obter mais informações, consulte [preparando-se para o Windows de 64 bits](getting-ready-for-64-bit-windows.md).

-   Verifique se seu código pode ser compilado para o Windows de 32 e de 64 bits.

    O novo modelo de dados foi projetado para permitir que aplicativos de 32 e 64 bits sejam criados a partir de uma única base de código com poucas modificações. As equipes de desenvolvimento SQL Server e Windows estão desenvolvendo versões de 32 e 64 bits de seus produtos na mesma base de código.

-   Use os novos recursos de otimização do compilador para obter o melhor desempenho.

    A otimização de código para processadores Intel Itanium é mais importante do que era para o x86. O compilador assume muitas das funções de otimização previamente tratadas pelo microprocessador. Você pode maximizar o desempenho de um aplicativo de 64 bits usando dois novos recursos de otimização do compilador: *otimização guiada por perfil* e *otimização de programa completa*. Os dois recursos resultam em tempos de compilação mais longos e exigem o desenvolvimento antecipado de bons cenários de teste.

    A *otimização guiada por perfil* envolve um processo de compilação em duas etapas. Durante a primeira compilação, o código é instrumentado para capturar o comportamento de execução. Essas informações são usadas durante a segunda compilação para guiar todos os recursos de otimização.

    A *otimização completa do programa* analisa o código em todos os arquivos de aplicativo, não apenas um único. Essa abordagem aumenta o desempenho de várias maneiras, incluindo a melhor linhagem, bem como a análise de efeito colateral e as convenções de chamada personalizadas aprimoradas.

## <a name="testing"></a>Teste

-   Determine se você testará o código de 64 ou 32 bits em execução no WOW64.

    Alguns aplicativos incluem código de 64 bits nativo e código de 32 bits em execução no WOW64. Investigue isso atentamente ao desenvolver um plano de teste e decida se suas ferramentas de teste devem ser de 64 bits, 32 bits ou uma combinação. Muitas vezes, você precisará testar as versões de 64 e 32 bits do seu aplicativo no Windows de 64 bits.

-   Teste os componentes de 32 bits usados com frequência.

    Primeiro, recompile seu código para 64 bits e teste. Em segundo lugar, corrija os problemas, recompile em 32 bits e, em seguida, teste. Terceiro, recompile para 64 bits e teste.

-   Testar componentes COM e RPC.

    Certifique-se de que os componentes COM e RPC de 32 e 64 bits se comuniquem corretamente. Você também pode precisar testar as comunicações com componentes de 16 bits em uma rede.

-   Teste sua versão de 32 bits em Windows de 64 bits.

    Os clientes podem continuar a usar aplicativos de 32 bits em janelas de 64 bits em que os problemas de desempenho e memória não são considerações importantes.

-   Teste configurações de memória diferentes.

    A adição de grandes quantidades de memória no servidor às vezes expõe problemas despercebidos anteriormente no aplicativo ou no sistema operacional.

 

 




