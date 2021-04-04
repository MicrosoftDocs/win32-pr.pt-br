---
title: programação de 64 bits para desenvolvedores de jogos
description: Este artigo aborda problemas de compatibilidade e portabilidade e ajuda os desenvolvedores a facilitarem sua transição para plataformas de 64 bits.
ms.assetid: 23a7ed41-6637-0607-327e-983b622e9104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12e57ea1b3cc3272ca40465df31a04244d99e68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007869"
---
# <a name="64-bit-programming-for-game-developers"></a>programação de 64 bits para desenvolvedores de jogos

Os fabricantes de processador estão fornecendo exclusivamente processadores de 64 bits em seus computadores desktop e até mesmo os chipsets da maioria dos computadores laptop dão suporte à tecnologia x64. É importante que os desenvolvedores de jogos tirem proveito dos aprimoramentos que os processadores de 64 bits oferecem com seus novos aplicativos e para garantir que seus aplicativos anteriores sejam executados corretamente nos novos processadores e nas edições de 64 bits do Windows Vista e do Windows 7. Este artigo aborda problemas de compatibilidade e portabilidade e ajuda os desenvolvedores a facilitarem sua transição para plataformas de 64 bits.

A Microsoft atualmente tem os seguintes sistemas operacionais de 64 bits:

-   Windows Server 2003 Service Pack 1
-   Windows XP Professional x64 Edition (disponível para OEMs e desenvolvedores por meio do MSDN)
-   Windows Vista
-   Windows Server 2008
-   Windows 7
-   Windows Server 2008 R2

> [!Note]  
> O Windows Server 2008 R2 só está disponível como uma edição de 64 bits.

 

-   [Diferenças na memória endereçável](#differences-in-addressable-memory)
-   [Especificando o reconhecimento de endereço grande ao compilar](#specifying-large-address-aware-when-building)
-   [Compatibilidade de aplicativos de 32 bits em plataformas de 64 bits](#compatibility-of-32-bit-applications-on-64-bit-platforms)
    -   [Armadilhas de compatibilidade em potencial](#potential-compatibility-pitfalls)
-   [Portando aplicativos para plataformas de 64 bits](#porting-applications-to-64-bit-platforms)
-   [Criação de perfil e otimização de aplicativos portados](#profiling-and-optimization-of-ported-applications)
-   [Código gerenciado em um sistema operacional de 64 bits](#managed-code-on-a-64-bit-operating-system)
-   [Implicações de desempenho da execução de um sistema operacional de 64 bits](#performance-implications-of-running-a-64-bit-operating-system)
-   [Resumo](#summary)

## <a name="differences-in-addressable-memory"></a>Diferenças na memória endereçável

A primeira coisa que a maioria dos desenvolvedores observa é que os processadores de 64 bits fornecem um grande salto na quantidade de memória física e virtual que pode ser resolvida.

-   aplicativos de 32 bits em plataformas de 32 bits podem resolver até 2 GB.
-   os aplicativos de 32 bits criados com o sinalizador de vinculador/LARGEADDRESSAWARE: YES em 32 bits Windows XP ou Windows Server 2003 com a opção de inicialização especial/3GB podem lidar com até 3 GB. Isso restringe o kernel a apenas 1 GB, o que pode fazer com que alguns drivers e/ou serviços falhem.
-   os aplicativos de 32 bits criados com o sinalizador de vinculador/LARGEADDRESSAWARE: YES nas edições de 32 bits do Windows Vista, do Windows Server 2008 e do Windows 7 podem endereçar a memória até o número especificado pelo elemento BCD (dados de configuração de inicialização) IncreaseUserVa. IncreaseUserVa pode ter um valor que varia de 2048, o padrão, para 3072 (que corresponde à quantidade de memória configurada pela opção de inicialização/3GB no Windows XP). O restante de 4 GB é alocado para o kernel e pode resultar em falha nas configurações de driver e serviço.

    Para obter mais informações sobre o BCD, consulte [dados de configuração da inicialização](https://msdn.microsoft.com/library/aa362692.aspx) no msdn.

-   aplicativos de 32 bits em plataformas de 64 bits podem lidar com até 2 GB ou até 4 GB com o sinalizador de vinculador/LARGEADDRESSAWARE: YES.
-   os aplicativos de 64 bits usam 43 bits para endereçamento, que fornece 8 TB de endereço virtual para aplicativos e 8 TB reservados para o kernel.

Além de apenas memória, os aplicativos de 64 bits que usam o benefício de e/s de arquivo mapeado por memória são muito maiores do que o maior espaço de endereço virtual. A arquitetura de 64 bits também melhorou o desempenho do ponto flutuante e a passagem mais rápida de parâmetros. Os processadores de 64 bits têm o dobro do número de registros, dos tipos de uso geral e de SSE (Streaming SIMD Extensions), bem como suporte para conjuntos de instruções SSE e SSE2; muitos processadores de 64 bits até mesmo dão suporte a conjuntos de instruções SSE3.

## <a name="specifying-large-address-aware-when-building"></a>Especificando o reconhecimento de endereço grande ao compilar

É uma boa prática especificar um reconhecimento de endereço grande ao criar aplicativos de 32 bits, usando o sinalizador do vinculador/LARGEADDRESSAWARE, mesmo que o aplicativo não se destine a uma plataforma de 64 bits, devido às vantagens que são obtidas sem nenhum custo. Conforme explicado anteriormente, a habilitação desse sinalizador para uma compilação permite que um programa de 32 bits acesse mais memória com opções de inicialização especiais em um sistema operacional de 32 bits ou em um sistema operacional de 64 bits. No entanto, os desenvolvedores devem ter cuidado para que as suposições do ponteiro não sejam feitas, como supondo que o alto bit nunca seja definido em um ponteiro de 32 bits. Em geral, a habilitação do sinalizador/LARGEADDRESSAWARE é uma boa prática.

Os aplicativos de 32 bits com reconhecimento de endereço grande podem determinar em tempo de execução quanto espaço de endereço virtual total está disponível para eles com a configuração do sistema operacional atual chamando [**GlobalMemoryStatusEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex). O resultado de ullTotalVirtual vai variar de 2147352576 bytes (2 GB) a 4294836224 bytes (4 GB). Valores maiores que 3221094400 (3 GB) só podem ser obtidos em edições de 64 bits do Windows. Por exemplo, se IncreaseUserVa tiver um valor de 2560, o resultado será ullTotalVirtual com um valor de 2684223488 bytes.

## <a name="compatibility-of-32-bit-applications-on-64-bit-platforms"></a>Compatibilidade de aplicativos de 32 bits em plataformas de 64 bits

Os sistemas operacionais Windows de 64 bits são binários compatíveis com a arquitetura IA32 e a maioria das APIs que os aplicativos de 32 bits usam estão disponíveis por meio do Windows 32 bits no emulador de bits do Windows de 64, WOW64. O WOW64 ajuda a garantir que essas APIs funcionem conforme o esperado.

O WOW64 tem uma camada de execução que manipula o marshaling de dados de 32 bits. O WOW64 redireciona as solicitações de arquivo DLL, redireciona algumas ramificações do registro para aplicativos de 32 bits e reflete algumas ramificações do registro para aplicativos de 32 e 64 bits.

Mais informações sobre o WOW64 podem ser encontradas em [detalhes de implementação do WOW64](/windows/desktop/WinProg64/wow64-implementation-details) no msdn. Para obter as práticas recomendadas para a criação de aplicativos executados no WOW64, consulte [práticas recomendadas para o WOW64](https://www.microsoft.com/whdc/system/platform/64bit/WoW64_bestprac.mspx) no Windows hardware Developer Central.

### <a name="potential-compatibility-pitfalls"></a>Armadilhas de compatibilidade em potencial

A maioria dos aplicativos desenvolvidos para uma plataforma de 32 bits será executada sem problemas em uma plataforma de 64 bits. Alguns aplicativos podem ter problemas, que podem incluir o seguinte:

-   Todos os drivers para as edições de 64 bits dos sistemas operacionais Windows devem ser versões de 64 bits. Exigir novos drivers de 64 bits tem implicações para esquemas de proteção de cópia que dependem de drivers antigos. Observe que os drivers do modo kernel devem ser assinados por Authenticode para serem carregados por edições de 64 bits do Windows.
-   os processos de 64 bits não podem carregar DLLs de 32 bits e os processos de 32 bits não podem carregar DLLs de 64 bits. Os desenvolvedores devem garantir que as versões de 64 bits de DLLs de terceiros estejam disponíveis antes de prosseguir com o desenvolvimento. Se você precisar usar uma DLL de 32 bits em um processo de 64 bits, a comunicação entre processos do Windows (IPC) poderá ser usada. Os componentes COM também podem fazer uso de servidores fora do processo e marshalling para comunicação entre limites, mas isso pode introduzir uma penalidade de desempenho.
-   Muitos processadores x64 também são processadores de vários núcleos, e os desenvolvedores precisam testar como isso afeta seus aplicativos herdados. Mais informações sobre processadores de vários núcleos e as implicações para aplicativos de jogos podem ser encontradas nos [processadores de tempo de jogo e de diversos núcleos](/windows/desktop/DxTechArts/game-timing-and-multicore-processors).
-   Os aplicativos também devem chamar [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) para descobrir caminhos de arquivo, pois alguns nomes de pastas foram alterados em determinados casos. Por exemplo, \_ os arquivos de programa CSIDL \_ retornariam "C: \\ Program Files (x86)" para um aplicativo de 32 bits em execução em uma plataforma de 64 bits em vez de "C: \\ Program Files". Os desenvolvedores devem estar atentos à forma como os recursos de redirecionamento e reflexão do emulador do WOW64 funcionam.

Além disso, os desenvolvedores precisam ser cautelosos em programas de 16 bits que ainda podem estar usando. O WOW64 não pode lidar com aplicativos de 16 bits; Isso inclui instaladores antigos e todos os programas do MS-DOS.

> [!Note]  
> Os problemas de compatibilidade mais comuns são instaladores que executam código de 16 bits e não têm drivers de 64 bits para esquemas de proteção de cópia.

 

A próxima seção discute problemas relacionados à portagem de código para o 64-bit nativo para desenvolvedores que desejam garantir que seus programas herdados funcionem em plataformas de 64 bits. Ele também é para os desenvolvedores que não estão familiarizados com a programação de 64 bits.

## <a name="porting-applications-to-64-bit-platforms"></a>Portando aplicativos para plataformas de 64 bits

Ter as ferramentas e bibliotecas certas ajudará a facilitar a transição de 32 para o desenvolvimento de 64 bits. O SDK do DirectX 9 tem bibliotecas para dar suporte a projetos baseados em x86 e x64. Microsoft Visual Studio 2005 e o Visual Studio 2008 oferecem suporte à geração de código para x86 e x64, e eles são fornecidos com bibliotecas otimizadas para gerar código x64. No entanto, também será necessário que os desenvolvedores distribuam os tempos de execução do Visual C com seus aplicativos. Observe que as edições Express do Visual Studio 2005 e do Visual Studio 2008 não incluem o compilador x64, mas as edições Standard, Professional e Team System fazem.

Os desenvolvedores que estão visando plataformas de 32 bits podem se preparar para o desenvolvimento de 64 bits para facilitar a transição mais tarde. Ao compilar projetos de 32 bits, os desenvolvedores devem usar o sinalizador/Wp64, o que fará com que a geração de avisos sobre problemas afete a portabilidade. A mudança para ferramentas e bibliotecas de 64 bits provavelmente irá gerar muitos erros de compilação inicialmente; Portanto, é aconselhável alternar ferramentas e bibliotecas com neutralidade de bits e corrigir quaisquer avisos antes de alternar para um Build de 64 bits.

No entanto, a alteração de ferramentas, a alteração de bibliotecas e o uso de determinados sinalizadores de compilador não serão suficientes. As suposições em padrões de codificação devem ser reavaliadas para garantir que os padrões de codificação atuais não permitam problemas de portabilidade. Problemas de portabilidade podem incluir truncamento de ponteiro, tamanho e alinhamento de tipos de dados, confiança em DLLs de 32 bits, uso de APIs herdadas, código de assembly e arquivos binários antigos.

> [!Note]  
> Visual C++ 2010 inclui os cabeçalhos stdint. h e cstdint C99 que definem os tipos de portabilidade padrão Int32 \_ t, UInt32 \_ t, Int64 \_ t, UInt64 t, IntPtr t e \_ \_ UIntPtr \_ t. Usar esses tipos de dados padrão ptrdiff \_ t e Size \_ t pode ser preferível aos tipos de portabilty do Windows usados abaixo para melhorar a portabilidade do código.

 

Os principais problemas de portabilidade incluem o seguinte:

<dl> <dt>

<span id="Pointer_Truncation"></span><span id="pointer_truncation"></span><span id="POINTER_TRUNCATION"></span>**Truncamento do ponteiro**
</dt> <dd>

OS ponteiros são 64 bits em um sistema operacional de 64 bits, portanto, a conversão de ponteiros para outros tipos de dados pode resultar em truncamento, e a aritmética de ponteiro pode resultar em corrupção. Usar o sinalizador/Wp64 geralmente fornecerá um aviso sobre esse tipo de problema, mas usando tipos polimórficos (INT \_ PTR, DWORD \_ PTR, Size \_ T, uint \_ PTR e assim por diante) durante a conversão de tipos de ponteiro é uma boa prática para ajudar a evitar esse problema completamente. Como os ponteiros são de 64 bits em novas plataformas, os desenvolvedores devem verificar a ordenação de ponteiros e os tipos de dados em classes e estruturas para reduzir ou eliminar o preenchimento.

</dd> <dt>

<span id="Data_Types_and_Binary_Files"></span><span id="data_types_and_binary_files"></span><span id="DATA_TYPES_AND_BINARY_FILES"></span>**Tipos de dados e arquivos binários**
</dt> <dd>

Embora os ponteiros aumentem de 32 bits para 64 em uma plataforma de 64 bits, outros tipos de dados não. Os tipos de dados de precisão fixa (DWORD32, DWORD64, INT32, INT64, LONG32, LONG64, UINT32 e UINT64) podem ser usados em locais onde o tamanho do tipo de dados deve ser conhecido; por exemplo, em uma estrutura de arquivo binário. As alterações no tamanho do ponteiro e no alinhamento de dados exigem tratamento especial para garantir a compatibilidade de 32 bits para 64 bits. Mais informações podem ser encontradas em [preparando-se para o Windows de 64 bits: os novos tipos de dados](/windows/desktop/WinProg64/the-new-data-types).

</dd> <dt>

<span id="Older_Win32_APIs_and_Data_Alignment"></span><span id="older_win32_apis_and_data_alignment"></span><span id="OLDER_WIN32_APIS_AND_DATA_ALIGNMENT"></span>**APIs e alinhamento de dados mais antigos do Win32**
</dt> <dd>

Algumas APIs do Win32 foram preteridas e substituídas por chamadas de API mais neutras, como SetWindowLongPtr no lugar de SetWindowLong.

A penalidade de desempenho para acessos não alinhados é maior em plataforma x64 do que em uma plataforma x86. As \_ macros de alinhamento de tipo (t) e deslocamento de campo \_ (t, membro) podem ser usadas para determinar as informações de alinhamento que podem ser usadas diretamente pelo código. O uso correto dessas macros mencionadas anteriormente deve eliminar penalidades de acesso não alinhadas.

Mais informações sobre a macro de alinhamento de tipo \_ , a macro de deslocamento de campo \_ e informações gerais de programação de 64 bits podem ser encontradas em [programação de 64 bits do Windows: dicas de migração: considerações adicionais](/windows/desktop/WinProg64/additional-considerations) e [preparação para janelas de 64 bits: regras para usar ponteiros](/windows/desktop/WinProg64/rules-for-using-pointers).

</dd> <dt>

<span id="Assembly_Code"></span><span id="assembly_code"></span><span id="ASSEMBLY_CODE"></span>**Código do assembly**
</dt> <dd>

O código de assembly embutido não tem suporte em plataformas de 64 bits e precisa ser substituído. As alterações na arquitetura podem ter alterado afunilamentos de aplicativo, e C/C++ ou intrínsecos podem obter resultados semelhantes com o código que é mais fácil de ler. A prática mais recomendável é alternar todo o código do assembly para C ou C++. Intrínsecos podem ser usados no lugar do código do assembly, mas só devem ser usados após a execução da criação de perfil completa e da análise.

X87, MMX e 3DNow! os conjuntos de instruções são preteridos nos modos de 64 bits. Os conjuntos de instruções ainda estão presentes para compatibilidade com versões anteriores para o modo de 32 bits; no entanto, para evitar problemas de compatibilidade no futuro, seu uso em projetos atuais e futuros é desencorajado.

</dd> <dt>

<span id="Deprecated_APIs"></span><span id="deprecated_apis"></span><span id="DEPRECATED_APIS"></span>**APIs preteridas**
</dt> <dd>

Algumas APIs mais antigas do DirectX foram descartadas para aplicativos nativos de 64 bits: DirectPlay 4 e anteriores, DirectDraw 6 e anteriores, Direct3D 8 e anteriores e DirectInput 7 e anteriores. Além disso, a API principal do DirectMusic está disponível para aplicativos nativos de 64 bits, mas a camada de desempenho e o produtor do DirectMusic são preteridos.

O Visual Studio emite avisos de substituição e essas alterações não são um problema para os desenvolvedores que usam as APIs mais recentes.

</dd> </dl>

## <a name="profiling-and-optimization-of-ported-applications"></a>Criação de perfil e otimização de aplicativos portados

Todos os desenvolvedores precisam recriar o perfil de todos os aplicativos que estão sendo portados para novas arquiteturas. Muitos aplicativos sendo portados para plataformas de 64 bits terão perfis de desempenho diferentes de suas versões de 32 bits. Os desenvolvedores precisam executar testes de desempenho de 64 bits antes de avaliar o que precisa ser otimizado. A boa notícia sobre isso é que muitas otimizações tradicionais funcionam em plataformas de 64 bits. Além disso, os compiladores de 64 bits também podem executar muitas otimizações com o uso correto de sinalizadores de compilador e dicas de codificação.

Algumas estruturas podem ter seus tipos de dados internos reordenados para conservar espaço de memória e melhorar o Caching. Os índices de matriz podem ser usados em vez de um ponteiro completo de 64 bits em alguns casos. O sinalizador/fp: Fast pode melhorar a otimização e a vetorização de ponto flutuante. \_ \_ O uso de restrict, declspec (restrict) e declspec (noalias) pode ajudar o compilador a resolver o alias e melhorar o uso do arquivo de registro.

Mais informações sobre o/fp: Fast podem ser encontradas em [/FP (especificar o comportamento do Floating-Point)](/cpp/build/reference/fp-specify-floating-point-behavior).

Mais informações sobre \_ \_ o restringir podem ser encontradas em [modificadores específicos da Microsoft](/cpp/cpp/microsoft-specific-modifiers).

Mais informações sobre declspec (restrict) podem ser encontradas em [práticas recomendadas de otimização](/cpp/build/optimization-best-practices).

Mais informações sobre declspec (noalias) podem ser encontradas em [ \_ \_ declspec (noalias)](https://msdn.microsoft.com/library/k649tyc7(VS.80).aspx).

## <a name="managed-code-on-a-64-bit-operating-system"></a>Código gerenciado em um sistema operacional de 64 bits

O código gerenciado é usado por muitos desenvolvedores de jogos em sua cadeia de ferramentas, portanto, uma compreensão de como ele se comporta em um sistema operacional de 64 bits pode ser útil. O código gerenciado é um conjunto de instruções neutro, portanto, quando você executa um aplicativo gerenciado em um sistema operacional de 64 bits, o CLR (Common Language Runtime) pode executá-lo como um processo de 32 bits ou de 64 bits. Por padrão, o CLR executa aplicativos gerenciados como 64 bits e eles devem funcionar bem sem problemas. No entanto, se seu aplicativo depender de uma DLL nativa de 32 bits, o aplicativo falhará quando tentar chamar essa DLL. Um processo de 64 bits precisa de um código de 64 bits completamente e uma DLL de bits de 32 não pode ser chamada de um processo de 64 bits. A melhor solução a longo prazo é compilar seu código nativo como 64-bit também, mas uma solução perfeitamente razoável de curto prazo é simplesmente marcar seu aplicativo gerenciado como somente para x86 usando o sinalizador de Build/Platform: x86.

## <a name="performance-implications-of-running-a-64-bit-operating-system"></a>Implicações de desempenho da execução de um sistema operacional de 64 bits

Como OS processadores com AMD64 e a arquitetura Intel 64 podem executar instruções de 32 bits nativamente, eles podem executar aplicativos de 32 bits em plena velocidade, mesmo em um sistema operacional de 64 bits. Há um custo modesto para converter parâmetros entre 32 bits e 64 bits ao chamar funções do sistema operacional, mas esse custo geralmente é insignificante. Isso significa que você não deve ver nenhuma lentidão ao executar aplicativos de 32 bits em um sistema operacional de 64 bits.

Quando você compila aplicativos como 64 bits, os cálculos ficam mais complicados. Um programa de 64 bits usa ponteiros de 64 bits e suas instruções são um pouco maiores, portanto, o requisito de memória é um pouco maior. Isso pode causar um pequeno descarte no desempenho. Por outro lado, ter duas vezes mais registros e ter a capacidade de fazer cálculos de inteiro de 64 bits em uma única instrução geralmente será maior do que Compensate. O resultado líquido é que um aplicativo de 64 bits pode ser executado um pouco mais devagar do que o mesmo aplicativo compilado como 32 bits, mas geralmente é executado ligeiramente mais rapidamente.

## <a name="summary"></a>Resumo

As arquiteturas de 64 bits permitem que os desenvolvedores enviem as limitações sobre a aparência, o som e a reprodução dos jogos. No entanto, a transição da programação de 32 bits para a programação de 64 bits não é trivial. Ao compreender as diferenças entre os dois, e usando as ferramentas mais recentes, a transição para plataformas de 64 bits pode ser mais fácil e rápida.

Mais informações sobre a programação de 64 bits podem ser encontradas em [Visual C++ Developer Center: programação de 64 bits](https://msdn.microsoft.com/vstudio//aa336463.aspx).

 

 