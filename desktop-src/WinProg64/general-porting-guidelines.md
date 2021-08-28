---
title: Diretrizes gerais de portação
description: A portagem de aplicativos de 32 bits para o Microsoft Windows de 64 bits será mais fácil do que a portação de aplicativos de 16 bits para aplicativos de 32 bits Windows. No entanto, a movimentação será mais suave com algum planejamento cuidadoso. A seguir estão algumas diretrizes gerais.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- portando aplicativos de 32 bits para 64 bits Windows programação Windows 64 bits
- Guia de programação Windows de 64 Windows de 64 bits, diretrizes de portação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a586318ecc6ec8852077052cbcff41bffacff6c35c36d23de4b020ce19f12af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680236"
---
# <a name="general-porting-guidelines"></a>Diretrizes gerais de portação

A portagem de aplicativos de 32 bits para o Microsoft Windows de 64 bits será mais fácil do que a portação de aplicativos de 16 bits para aplicativos de 32 bits Windows. No entanto, a movimentação será mais suave com algum planejamento cuidadoso. A seguir estão algumas diretrizes gerais.

## <a name="planning"></a>Planejamento

-   Determine a magnitude do esforço necessário para a porta. Medir quanto trabalho está envolvido identificando os seguintes itens:
    -   Problema de código de 32 bits. Compile seu código de 32 bits com o compilador de 64 bits e examine a extensão dos erros e avisos.
    -   Componentes ou dependências compartilhados. Determine quais componentes em seu aplicativo se originam de outras equipes e se essas equipes planejam desenvolver versões de 64 bits do código.
    -   Código de assembly ou herdação. Aplicativos baseados em Windows de 16 bits não são executados em Windows de 64 bits e devem ser reescritos. Embora o código de assembly x86 seja executado no WOW64, talvez você queira reescrever esse código para aproveitar a velocidade da arquitetura do Intel Itanium.
-   Portar todo o aplicativo, não apenas partes dele.

    Embora seja possível por portabilidade de partes de um aplicativo ou para limitar o código a 2G com /LARGEADDRESSAWARE:NO, essa estratégia troca o ganho de curto prazo por danos de longo prazo.

    > [!Note]  
    > /LARGEADDRESSAWARE:NO é ignorado para um binário ARM64.

     

-   Encontre substitutos para tecnologias que não serão portadas.

    Algumas tecnologias, incluindo DAO (Objeto de Acesso a Dados) e o mecanismo de banco de dados Jet Red, não serão portadas para 64 bits Windows.

-   Trate sua versão de 64 bits como uma versão separada do produto.

    Embora seu produto de 64 bits possa compartilhar a mesma base de código que seu de 32 bits, ele precisa de testes adicionais e pode ter outras considerações sobre a versão.

## <a name="development"></a>Desenvolvimento

-   Comece a desenvolver código em conformidade agora.

    Os desenvolvedores podem começar a escrever código em conformidade usando os arquivos de Windows mais recentes e os novos tipos de dados sem efeitos adversos no desenvolvimento de produtos de 32 bits. Para obter mais informações, consulte [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).

-   Verifique se o código pode ser compilado para 32 e 64 bits Windows.

    O novo modelo de dados foi projetado para permitir que aplicativos de 32 e 64 bits sejam criados de uma única base de código com poucas modificações. As SQL Server e Windows de desenvolvimento estão desenvolvendo versões de 32 e 64 bits de seus produtos da mesma base de código.

-   Use os novos recursos de otimização do compilador para melhorar o desempenho.

    A otimização de código para processadores Intel Itanium é mais importante do que era para o x86. O compilador assume muitas das funções de otimização manipuladas anteriormente pelo microprocessador. Você pode maximizar o desempenho de um aplicativo de 64 bits  usando dois novos recursos de otimização do compilador: Otimização Guiada por Perfil e Otimização *de Programa Inteiro.* Ambos os recursos resultam em tempos de build mais longos e exigem o desenvolvimento antecipado de bons cenários de teste.

    *A Otimização Guiada por* Perfil envolve um processo de compilação em duas etapas. Durante a primeira compilação, o código é instrumentado para capturar o comportamento de execução. Essas informações são usadas durante a segunda compilação para orientar todos os recursos de otimização.

    *A Otimização do* Programa Inteiro analisa o código em todos os arquivos de aplicativo, não apenas um único. Essa abordagem aumenta o desempenho de várias maneiras, incluindo melhor emlining, bem como análise de efeito colateral aprimorada e convenções de chamada personalizadas.

## <a name="testing"></a>Testando

-   Determine se você testará o código de 64 ou 32 bits em execução no WOW64.

    Alguns aplicativos incluem código nativo de 64 bits e código de 32 bits em execução no WOW64. Investigue isso de perto ao desenvolver um plano de teste e decida se suas ferramentas de teste devem ser de 64 bits, 32 bits ou uma combinação. Muitas vezes, você precisará testar as versões de 64 e 32 bits do seu aplicativo em 64 bits Windows.

-   Testar componentes de 32 bits usados com frequência.

    Primeiro, recompile seu código para 64 bits e teste. Em segundo lugar, corrige problemas, recompile em 32 bits e teste. Em terceiro lugar, recompile para 64 bits e teste.

-   Testar componentes COM e RPC.

    Certifique-se de que os componentes COM e RPC de 32 e 64 bits se comuniquem corretamente. Talvez você também tenha que testar as comunicações com componentes de 16 bits em uma rede.

-   Teste sua versão de 32 bits em um Windows.

    Os clientes podem continuar a usar aplicativos de 32 bits em um Windows de 64 bits em que problemas de desempenho e memória não são considerações importantes.

-   Testar diferentes configurações de memória.

    Adicionar grandes quantidades de memória no servidor às vezes expõe problemas anteriormente desajustados no aplicativo ou no sistema operacional.

 

 




