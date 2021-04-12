---
title: Principais ferramentas e técnicas para fazer jogos Windows mais robustos
description: Este artigo descreve as ferramentas e técnicas que você pode usar para ajudar a reduzir o número de chamadas de suporte recebidas.
ms.assetid: ad3d100c-4f87-f1e4-3242-8b2052ba171d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76b49c228af6a932c453b11e92f612d3419a4af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454201"
---
# <a name="top-tools-and-techniques-for-making-more-robust-windows-games"></a>Principais ferramentas e técnicas para fazer jogos Windows mais robustos

Um dos custos mais indesejáveis voltados para a produção de jogos são chamadas de suporte. Cada vez que um usuário contata o atendimento ao cliente, o lucro do jogo é reduzido. Embora algumas chamadas para o suporte ao cliente não sejam impedidas, outras podem ser eliminadas ou reduzidas com o emprego de boas práticas de desenvolvimento. Este artigo descreve as ferramentas e técnicas que você pode usar para ajudar a reduzir o número de chamadas de suporte recebidas.

Todas as ferramentas descritas aqui são gratuitas, e as técnicas são simples o bastante para serem adicionadas à maioria dos métodos de desenvolvimento.

Ferramentas e técnicas:

-   [PREfast](#prefast)
-   [AppVerifier](#appverifier)
-   [Kit de ferramentas de compatibilidade de aplicativos da Microsoft](#microsoft-application-compatibility-toolkit)
-   [Teste de proteção de conta de usuário](#user-account-protection-testing)
-   [PIX para Windows](#pix-for-windows)
-   [Detecção de configuração](#configuration-detection)
-   [Habilitar avisos completos do compilador](#enable-full-compiler-warnings)
-   [Servidor de símbolos da Microsoft](#microsoft-symbol-server)
-   [Relatório de Erros do Windows](#windows-error-reporting)
-   [Ferramentas de ajuste de desempenho](#performance-tuning-tools)
-   [Resumo](#summary)

## <a name="prefast"></a>PREfast

O PREfast para drivers é uma ferramenta oferecida pela Microsoft que analisa caminhos de execução em C ou C++ compilados para ajudar a encontrar bugs em tempo de execução. O PREfast Opera trabalhando com todos os caminhos de execução em todas as funções e avaliando cada caminho quanto a problemas. Embora essa ferramenta normalmente seja usada para desenvolver drivers e outros códigos de kernel, ela pode ajudar os desenvolvedores de jogos a economizar tempo, eliminando alguns bugs que são difíceis de encontrar ou que são ignorados pelo compilador. O uso de PREfast é uma maneira excelente de reduzir a carga de trabalho de lançamento e os custos de suporte.

O PREfast é fornecido com o Visual Studio Team System e como parte do [Kit de driver do Windows](https://www.microsoft.com/whdc/devtools/WDK/). Para obter mais informações sobre o PREfast, consulte [PREfast para drivers](https://www.microsoft.com/whdc/devtools/tools/PREfast.mspx).

## <a name="appverifier"></a>AppVerifier

O Microsoft Application Verifier, ou AppVerifier, é uma ferramenta que pode ajudar os testadores fornecendo várias funções em uma ferramenta. O AppVerifier foi desenvolvido para facilitar o teste de erros comuns de programação. O AppVerifier pode verificar os parâmetros que são passados em chamadas à API, injetar entrada errada para verificar a capacidade de manipulação de erros e registrar alterações no registro e no sistema de arquivos. O AppVerifier também pode detectar saturações de buffer no heap, verificar se uma ACL (lista de controle de acesso) foi definida corretamente e impor o uso seguro de APIs de soquetes.

Embora não seja exaustiva, o AppVerifier pode ser mais um componente da caixa de ferramentas de um testador para ajudar um estúdio de desenvolvimento a lançar um produto de qualidade e reduzir os custos potenciais de lançamento.

Para obter mais informações sobre Application Verifier, consulte [Application Verifier](/previous-versions/ms220948(v=vs.80)) e [usando Application Verifier em seu ciclo de vida de desenvolvimento de software](/previous-versions/aa480483(v=msdn.10)) no msdn. Você pode baixar Application Verifier de [detalhes de download: Application Verifier](https://www.microsoft.com/download/details.aspx?id=20028) no centro de download da Microsoft.

Uma ferramenta semelhante para drivers, verificador de driver, também está disponível. Para obter mais informações, consulte [usando o verificador de driver para identificar problemas com drivers do Windows para usuários avançados](https://support.microsoft.com/Default.aspx?kbid=244617) em ajuda e suporte da Microsoft.

## <a name="microsoft-application-compatibility-toolkit"></a>Kit de ferramentas de compatibilidade de aplicativos da Microsoft

O Microsoft Application Compatibility Toolkit é um conjunto de ferramentas gratuitas para ajudar os desenvolvedores a verificar rapidamente como suas versões serão executadas em Service Packs lançados recentemente para o Microsoft Windows. Ao se preparar para novos service packs, os desenvolvedores podem impedir ou estar prontos para qualquer problema.

O kit de ferramentas de compatibilidade de aplicativos e mais informações podem ser encontrados em [compatibilidade de aplicativos do Windows](https://www.microsoft.com/technet/prodtechnol/windows/appcompatibility/default.mspx).

## <a name="user-account-protection-testing"></a>Teste de proteção de conta de usuário

O Windows Vista e o Windows 7 têm dois tipos principais de contas de usuário: usuário padrão e administrador. As contas de usuário padrão são o tipo preferencial para todos os usuários, pois reduzem o risco de danos ao sistema por aplicativos mal-intencionados. Como o usuário padrão tem restrições de acesso — como não conseguir gravar na pasta arquivos de programas ou no \_ computador local hKey \_ (HKLM) no registro — é importante que os jogos sejam projetados e testados para funcionar com uma conta de usuário padrão.

Mais informações sobre este tópico podem ser encontradas nos artigos [corrigindo o software de jogos no Windows XP, no Windows Vista e no Windows 7](./patching-methods-in-windows-xp-and-vista.md) e [no controle de conta de usuário para desenvolvedores de jogos](./user-account-control-for-game-developers.md).

## <a name="pix-for-windows"></a>PIX para Windows

O PIX é uma ferramenta para coletar e analisar informações de desempenho de um aplicativo em execução. O PIX pode coletar dados estatísticos sobre por que alguns quadros são renderizados mais lentamente do que outros e podem identificar o mau uso da API. O PIX também pode ser automatizado para testar a compilação diária e sinalizar alterações repentinas no desempenho do aplicativo. Usando o PIX em uma variedade de configurações de hardware, testadores e desenvolvedores podem ajudar a minimizar as chamadas de suporte relacionadas ao desempenho do jogo.

## <a name="configuration-detection"></a>Detecção de configuração

Os recursos do dispositivo expostos por drivers nem sempre estão corretos. Uma solução é usar um sistema controlado por banco de dados para configuração de aplicativos, como o sistema demonstrado no exemplo de ConfigSystem, que está incluído no SDK do DirectX. Um modelo de detecção semelhante ao sistema no exemplo pode ajudar a identificar os recursos do dispositivo que estão atrasando o desempenho do jogo e, portanto, reduzir o número de chamadas de suporte sobre o desempenho.

## <a name="enable-full-compiler-warnings"></a>Habilitar avisos completos do compilador

É uma prática recomendada restaurar quaisquer avisos do compilador que foram desabilitados pelo **\# aviso de pragma** quando um projeto se tornar estável. Os desenvolvedores devem tentar eliminar todos os avisos antes de lançar um produto. Mesmo que um aviso não cause uma falha ou erro no sistema de um desenvolvedor, ele ainda poderá causar um problema no sistema de um usuário. Se um aviso não puder ser eliminado, a equipe de teste precisará verificar se o aviso causará alguns ou nenhum erro no sistema de um usuário.

## <a name="microsoft-symbol-server"></a>Servidor de símbolos da Microsoft

A Microsoft fornece um servidor acessível pela Internet que fornece arquivos de símbolo para os sistemas operacionais Microsoft Windows, bem como outros produtos da Microsoft. Os símbolos também estão disponíveis no servidor para versões beta atuais e candidatos a lançamento de produtos Windows, bem como hot fixes e Service Packs. Você pode configurar o depurador para baixar símbolos conforme necessário durante uma sessão de depuração, em vez de baixar arquivos de símbolo separadamente antes de uma sessão de depuração. Os símbolos são baixados em um local de diretório que você especifica e o depurador os carrega a partir daí.

Para obter mais informações sobre o servidor de símbolos da Microsoft, consulte [ferramentas e símbolos de depuração: introdução](https://www.microsoft.com/whdc/devtools/debugging/debugstart.mspx).

## <a name="windows-error-reporting"></a>Relatório de Erros do Windows

O Relatório de Erros do Windows (WER) é um serviço fornecido pela Microsoft para ajudar os desenvolvedores a coletar informações de erro de aplicativos de maneira unificada e organizada. Embora seja completamente voluntário, os desenvolvedores devem aproveitar esse serviço para ajudar a determinar quais bugs ocorrem com mais frequência. O uso do WER pode ajudar com a depuração de problemas comumente relatados, o que ajudará a eliminar chamadas de suporte para os bugs mais Commons.

Para obter mais informações sobre o WER, consulte [análise de despejo](./crash-dump-analysis.md)de memória.

## <a name="performance-tuning-tools"></a>Ferramentas de ajuste de desempenho

Os desenvolvedores podem usar analisadores de desempenho para ajustar o desempenho de seus jogos. Além do PIX, há vários analisadores de desempenho populares para Windows, como o [analisador de desempenho Intel VTune](https://software.intel.com/intel-vtune/) e o [AMD CodeAnalyst performance Analyzer](https://developer.amd.com/cpu/CodeAnalyst/). Essas ferramentas ajudam na identificação de afunilamentos e na decisão de como melhorar o desempenho geral de um aplicativo. Melhorar os gargalos de desempenho antes do lançamento ajudará a reduzir os custos de lançamento.

## <a name="summary"></a>Resumo

Todos os envolvidos no design, no desenvolvimento e no teste precisam considerar como seu trabalho afetará o custo de lançamento de um produto. Usando as ferramentas e métodos mencionados anteriormente no processo de produção, o volume de chamadas de suporte pode ser reduzido. Isso, por sua vez, aumentará os lucros, reduzindo os custos de lançamento do desenvolvimento de jogos.

 

 