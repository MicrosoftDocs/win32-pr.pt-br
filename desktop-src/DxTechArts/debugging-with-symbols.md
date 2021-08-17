---
title: Depuração com símbolos
description: Este artigo fornece uma visão geral de alto nível de como usar melhor símbolos em seu processo de depuração.
ms.assetid: 7ce0c9c7-485c-8d72-0353-27fd2e369a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdabd1a99f203adb2422cc4bbc71c3fb2f6108a0a3869077e97683bdcf830100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070556"
---
# <a name="debugging-with-symbols"></a>Depuração com símbolos

Este artigo fornece uma visão geral de alto nível de como usar melhor símbolos em seu processo de depuração. Ele explica como usar o servidor de símbolos da Microsoft e também como configurar e usar seu próprio servidor de símbolos privado. Essas práticas recomendadas podem ajudar a aumentar sua eficácia e a capacidade de depurar problemas, mesmo em casos em que todos os símbolos e arquivos executáveis relacionados a um problema não estão localizados no computador.

-   [Símbolos](#debugging-with-symbols)
-   [Usando símbolos para depuração](#using-symbols-for-debugging)
-   [Obter os símbolos necessários](#getting-the-symbols-you-need)
    -   [Verifique se uma determinada DLL ou .exe arquivo e PDB na mesma pasta corresponderem](#check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match)
    -   [Verifique se todas as DLLs e arquivos executáveis em um conjunto de pastas têm PDBs correspondentes](#check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs)
    -   [Como o Symchk funciona](#how-symchk-works)
-   [Servidores de símbolos](#symbol-servers)
-   [Usando o Servidor de Símbolos da Microsoft](#using-the-microsoft-symbol-server)
-   [Obter símbolos manualmente](#getting-symbols-manually)
-   [Configurando um servidor de símbolos](#setting-up-a-symbol-server)
-   [Adicionando símbolos a um servidor de símbolos](#adding-symbols-to-a-symbol-server)
-   [Práticas recomendadas](#best-practices)

## <a name="symbols"></a>Símbolos

Vários tipos diferentes de símbolos estão disponíveis para depuração. Eles incluem símbolos codeView, COFF, DBG, SYM, PDB e até mesmo símbolos de exportação gerados de uma tabela de exportação de arquivos binários. Este white paper aborda apenas os VS.NET e os símbolos de formato PDB, pois eles são o formato preferencial mais recente. Eles são gerados por padrão para projetos compilados usando Visual Studio.

A geração de arquivos PDB para executáveis de versão não afeta nenhuma otimização ou altera significativamente o tamanho dos arquivos gerados. Normalmente, a única diferença é o caminho e o nome do arquivo PDB é inserido no executável. Por esse motivo, você sempre deve produzir arquivos PDB, mesmo que não queira enviar com o executável.

Os arquivos PDB serão gerados se um projeto for criado usando a opção do compilador **/Zi** ou **/ZI** (Produzir informações de PDB), junto com a opção do linker **/DEBUG** (Gerar Informações de Depuração). Os arquivos PDB gerados pelo compilador são combinados e gravados em um único arquivo PDB que é colocado no mesmo diretório que o executável.

Por padrão, os arquivos PDB contêm as seguintes informações:

-   Símbolos públicos (normalmente todas as funções, variáveis estáticas e globais)
-   Uma lista de arquivos de objeto responsáveis por seções de código no executável
-   Informações de otimização de ponteiro de quadro (FPO)
-   Informações de nome e tipo para variáveis locais e estruturas de dados
-   Informações de número de linha e arquivo de origem

Se você estiver preocupado com as pessoas que usam as informações de arquivo PDB para ajudá-las a fazer engenharia reversa de seu executável, você também poderá gerar arquivos PDB removidos usando a opção de linker **/PDBSTRIPPED:filename.** Se você tiver arquivos PDB existentes dos quais gostaria de retirar informações privadas, poderá usar uma ferramenta chamada pdbcopy, que faz parte das ferramentas de depuração para Windows.

Por padrão, os arquivos PDB removidos contêm as seguintes informações:

-   Símbolos públicos (normalmente apenas funções não estáticas e variáveis globais)
-   Uma lista de arquivos de objeto responsáveis por seções de código no executável
-   Informações de otimização de ponteiro de quadro (FPO)

Essas são as informações mínimas necessárias para permitir a depuração confiável. As informações mínimas também dificultam a obtenção de informações adicionais sobre o código-fonte original. Como um arquivo PDB removido e um arquivo PDB regular são gerados, você pode fornecer a versão despojada aos usuários que podem precisar de capacidades limitadas de depuração, mas manter os PDBs completos confidenciais. Observe que **/PDBSTRIPPED** gera um segundo arquivo PDB menor, portanto, certifique-se de usar o arquivo PDB correto ao gerar builds para distribuir amplamente. Para um projeto típico, um PDB regular pode ter alguns megabytes de tamanho, mas uma versão despojada do PDB pode ter apenas algumas centenas de quilobytes.

## <a name="using-symbols-for-debugging"></a>Usando símbolos para depuração

Quando você está depurando um aplicativo que falha, o depurador tenta mostrar as funções na pilha que levaram à falha. Sem um arquivo PDB, o depurador não pode resolver os nomes de função, seus parâmetros ou quaisquer variáveis locais armazenadas na pilha. Se você depurar executáveis de 32 bits, haverá situações em que você não poderá obter rastreamentos de pilha confiáveis sem símbolos. Às vezes, é possível observar os valores brutos na pilha e descobrir quais valores podem ser endereços de retorno, mas eles podem ser facilmente confundidos com referências de função ou dados.

Se as funções na pilha atual foram compiladas usando a otimização Omitir Ponteiros de Quadro (**/Oy**) e se os símbolos não estão presentes, o depurador não poderá determinar de forma confiável qual função chamou a função atual. Isso porque, sem as informações de FPO (Otimização de Ponteiro de Quadro) que os PDBs contêm, o depurador não pode contar com o registro de ponteiro de quadro (EBP) para apontar para o ponteiro de quadro anterior salvo e no endereço de retorno da função pai. Em vez disso, ele adivinha. Às vezes, isso é correto. No entanto, muitas vezes, ele está errado, o que pode ser enganoso. Se você vir um aviso sobre símbolos ausentes ou nenhum símbolo carregado, como no exemplo a seguir, não confie na pilha desse ponto para baixo.

``` syntax
SWPerfTest.exe!TextFunction(... ...)    Line 59    C++
d3dx9d.dll!008829b5()
[Frames below may be incorrect and/or missing, no symbols loaded for d3dx9d.dll]
SWPerfTest.exe!main(int argc=, const char * * argv=)  Line 328 + 0x12 bytes     C++
SWPerfTest.exe!__mainCRTStartup() Line 716 + 0x17 bytes    C
kernel32.dll!@BaseThreadInitThunk@12() + 0x12 bytes
ntdll.dll!__RtlUserThreadStart@8() + 0x27 bytes
```

Em muitos casos, é possível continuar a depuração sem símbolos, porque o problema está em um local que tem símbolos precisos e você não precisa observar as funções mais abaixo na pilha de chamada. Mesmo que uma biblioteca que está em sua pilha de chamada não tenha PDBs disponíveis, desde que tenham sido compilados com ponteiros de quadro, o depurador deverá ser capaz de adivinhar corretamente as funções pai. A partir do Windows XP Service Pack 2, todas Windows DLL e arquivos executáveis são compilados com o FPO desabilitado, pois torna a depuração mais precisa. Desabilitar o FPO também permite que os profilers de amostragem andem pela pilha durante o tempo de execução, com impacto mínimo no desempenho. Em versões do Windows antes do Windows XP SP2, todos os binários do sistema operacional exigem arquivos de símbolo correspondentes que contêm informações de FPO para permitir depuração e criação de perfil precisas.

Se você depurar executáveis nativos de 64 bits, não precisará de arquivos de símbolo para produzir rastreamentos de pilha válidos, pois os sistemas operacionais e compiladores x64 foram projetados para não exigi-los. No entanto, você ainda precisa de arquivos de símbolo para recuperar os nomes de função, os parâmetros de chamada e as variáveis locais.

No entanto, alguns casos são particularmente difíceis de depurar sem símbolos. Por exemplo, se você depurar um programa para o qual criou um arquivo PDB e se você falhar em um retorno de chamada de uma função em uma DLL para a qual você não tem símbolos, não poderá ver qual função causou o retorno de chamada, pois não será possível decodificar a pilha. Isso ocorre com frequência em bibliotecas de terceiros, se os PDBs não são fornecidos ou em componentes antigos do sistema operacional, se os PDBs não estão disponíveis. Retornos de chamada geralmente ocorrem durante a passagem de mensagens, enumeração, alocação de memória ou tratamento de exceção. Depurar essas funções sem uma pilha precisa pode ser frustrante.

Para depurar minispejos de forma confiável que são gerados em um computador diferente ou que tiveram um erro no código que você não possui, é importante poder acessar todos os símbolos e binários para os executáveis referenciados no minispejo. Se os símbolos e binários estão disponíveis em um servidor de símbolos, eles são obtidos automaticamente pelo depurador. Para obter mais informações sobre mini-despejos, consulte a análise [de despejo de](/windows/desktop/DxTechArts/crash-dump-analysis) white paper.

## <a name="getting-the-symbols-you-need"></a>Obter os símbolos necessários

Visual Studio e outros depurador da Microsoft, como WinDbg, normalmente são definidos para funcionar apenas se você estiver criando um aplicativo e depurando-o em seu próprio computador. Se você precisar dar seu executável a outra pessoa, se você tiver várias versões de uma DLL ou um arquivo .exe em seu computador ou se quiser depurar com precisão um aplicativo que usa Windows ou outras bibliotecas, como o DirectX, precisará entender como os depurador encontram e carregam símbolos. O depurador usa o caminho de pesquisa de símbolos especificado pelo usuário , que é encontrado em Opções Depurando símbolos no Visual Studio ou na variável de ambiente \\ \\ \_ NT \_ SYMBOL \_ PATH. Normalmente, o depurador pesquisa PDBs correspondentes nos seguintes locais:

-   No local especificado dentro da DLL ou do arquivo executável.

    Se você tiver criado uma DLL ou um arquivo executável em seu computador, por padrão, o linker coloca o caminho completo e o nome de arquivo do arquivo PDB associado dentro da DLL ou do arquivo executável. Quando você depura, o depurador primeiro verifica se o arquivo de símbolo existe no local especificado dentro da DLL ou do arquivo executável. Isso é útil, porque você sempre tem símbolos disponíveis para o código que você compilou em seu computador.

-   PDBs que podem estar presentes na mesma pasta que a DLL ou arquivo executável.
-   Em algumas pastas de cache de símbolo locais.
-   Todos os servidores de símbolo de compartilhamento de arquivos de rede local.
-   Todos os servidores de símbolos da Internet, como o servidor de símbolos da Microsoft.

Para garantir que você tenha todos os PDBs necessários para depuração precisa, instale as ferramentas de depuração para Windows. As versões de 32 e 64 bits podem ser encontradas em [Ferramentas de Depuração para Windows](/windows-hardware/drivers/debugger/).

Uma ferramenta útil que é instalada com esse pacote é symchk.exe. Ele pode ajudar a identificar símbolos ausentes ou incorretos. Essa ferramenta tem um grande número de opções de linha de comando potenciais. Aqui estão duas das mais úteis e mais usadas.

### <a name="check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match"></a>Verifique se uma determinada DLL ou .exe arquivo e PDB na mesma pasta corresponderem

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" testing.dll /s .

SYMCHK: FAILED files = 0
SYMCHK: PASSED + IGNORED files = 1
```

O **/s.** A opção **informa ao Symchk** para procurar símbolos somente na pasta atual e não procurar em nenhum servidor de símbolo.

### <a name="check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs"></a>Verifique se todas as DLLs e arquivos executáveis em um conjunto de pastas têm PDBs correspondentes

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" *.* /r
```

A **opção /r** define **symchk** para percorrer as pastas recursivamente para verificar se todos os arquivos executáveis têm PDBs correspondentes. Sem a **opção /s,** **o symchk** usa o CAMINHO DE SÍMBOLO NT atual para pesquisar símbolos em qualquer servidor particular ou local ou nos servidores \_ de \_ \_ símbolos da Microsoft. A **ferramenta symchk** pesquisa apenas símbolos para arquivos executáveis (.exe, .dll e semelhantes). Você não pode usar curingas para pesquisar símbolos para arquivos não executáveis.

### <a name="how-symchk-works"></a>Como o Symchk funciona

Quando o linker gera arquivos .dll, executáveis e PDB, ele armazena GUIDs idênticos em cada arquivo. O GUID é usado pelas ferramentas para determinar se um determinado arquivo PDB corresponde a uma DLL ou a um arquivo executável. Se você alterar uma DLL ou um arquivo executável usando um editor de recursos ou codificação de proteção de cópia ou alterando suas informações de versão, o GUID será atualizado e o depurador não poderá carregar o arquivo PDB. Por esse motivo, é muito importante evitar manipular a DLL ou o arquivo executável depois que ele é criado pelo vinculador.

Você também pode usar o utilitário DUMPBIN que vem com VS.NET para mostrar os caminhos de símbolo que são pesquisados e para ver se foram encontrados arquivos de símbolo que corresponderem a uma determinada DLL ou arquivo executável. Por exemplo:

``` syntax
DUMPBIN /PDBPATH:VERBOSE filename.exe
```

## <a name="symbol-servers"></a>Servidores de símbolos

Um servidor de símbolos é um repositório para várias versões de arquivos executáveis e de símbolo. Ele contém os próprios arquivos de símbolo ou ponteiros para os arquivos de símbolo associados. Os depurador entendem como usar servidores de símbolos e podem usá-los para pesquisar símbolos ausentes ou desconhecidos.

A DLL e os arquivos executáveis também estão disponíveis no servidor de símbolos da Microsoft. Isso possibilita depurar falhas e examinar o código de arquivos do sistema operacional que podem não existir em seu computador. Se um depurador encontrar um arquivo executável ou uma DLL que não existe no sistema que você está usando para depuração, ele solicitará automaticamente os símbolos e uma cópia do arquivo binário dos servidores de símbolos da Microsoft. Isso é útil se você estiver depurando um componente que tem muitas versões, por exemplo, msvcrt.dll, e precisar examinar o código para uma versão que não existe no computador. Isso também ajuda a depurar mini-despejos gerados em um sistema operacional diferente do sistema que você está usando para depuração.

A Microsoft publica todos os arquivos PDB para todos os sistemas operacionais e outros componentes redistribuídos, como o SDK do DirectX, em seu servidor de símbolos acessível externamente. Isso facilita a depuração de um aplicativo que usa essas DLL ou arquivos executáveis. Você pode usar o servidor de símbolos da Microsoft para resolver símbolos, juntamente com quaisquer símbolos locais para componentes que foram construídos em seu computador.

Você pode configurar seu computador para usar o servidor de símbolos da Microsoft, que fornece acesso a todos os arquivos de símbolo da Microsoft. Você também pode configurar um servidor de símbolos privado para sua empresa, equipe ou rede, que pode ser usado para armazenar várias versões mais antigas de um projeto no qual você está trabalhando ou para fornecer um cache local para os símbolos que você usa do servidor de símbolos da Microsoft.

Para usar um servidor de símbolos, especifique o caminho de pesquisa em uma variável de ambiente chamada \_ NT \_ SYMBOL \_ PATH. Depurador e ferramentas modernas, como WinDbg, NTSD ou Visual Studio, usam automaticamente esse caminho para pesquisar símbolos.

Quando um depurador pesquisa símbolos, ele pesquisa primeiro localmente. Em seguida, ele procura em servidores de símbolos. Quando encontra um símbolo correspondente, ele transfere o arquivo de símbolo para o cache local. Os símbolos de uma DLL típica ou intervalo de arquivos executáveis de 1 a 100 MB de tamanho. Portanto, se você estiver depurando um processo que inclui muitas DLLs, poderá levar algum tempo para resolver todos os símbolos e transferi-los para um cache local.

## <a name="using-the-microsoft-symbol-server"></a>Usando o Servidor de Símbolos da Microsoft

O servidor de símbolos da Microsoft permite que você obtenha todos os símbolos mais recentes, incluindo símbolos para arquivos atualizados ou com patch. O servidor de símbolos da Microsoft está disponível em <https://msdl.microsoft.com/download/symbols> .

Você pode acessar o servidor de símbolos de uma das seguintes maneiras:

-   Insira o endereço do servidor diretamente. No Visual Studio, no **menu** Ferramentas, escolha **Opções** e, em seguida, escolha **Depuração** e, em seguida, **escolha Símbolos**.
-   Use a variável de ambiente \_ NT \_ SYMBOL \_ PATH. Este método é recomendável.

    Isso é usado por todas as ferramentas de depuração. Ele também é usado por Visual Studio e é lido e decodificado quando Visual Studio aberto. Portanto, se você alterá-lo, precisará reiniciar o Visual Studio.

    Essa variável de ambiente permite que você especifique vários servidores de símbolos, por exemplo, um servidor de símbolo privado interno. Ele também permite que você especifique um diretório de cache local para armazenar PDBs para todos os símbolos que você procurar em servidores de símbolos, internamente e pela Internet.

A sintaxe para a \_ variável PATH de SÍMBOLO NT \_ \_ é:

``` syntax
srv*[local cache]*[private symbol server]*https://msdl.microsoft.com/download/symbols
```

Substitua o cache local pelo nome de um diretório no computador em que você deseja armazenar um cache de todos os \[ \] símbolos usados– por exemplo, %SYSTEMROOT% Symbols ou \\ c: \\ symbols.

O \[ servidor de símbolo privado é \] opcional. Ele pode apontar para um servidor de símbolos localizado em sua rede ou pode apontar para um servidor de símbolos compartilhado por sua equipe, grupo de produtos ou empresa.

Para usar apenas o servidor de símbolos da Microsoft junto com um cache local de símbolos, para acelerar o acesso pela Internet, use a seguinte configuração para \_ NT \_ SYMBOL \_ PATH:

``` syntax
srv*c:\symbols*https://msdl.microsoft.com/download/symbols
```

Você pode encontrar outras opções para o CAMINHO DE SÍMBOLO NT no arquivo de ajuda instalado com as Ferramentas \_ \_ de \_ Depuração da Microsoft para Windows pacote.

Os executáveis sem símbolos podem aumentar o tempo necessário para iniciar um depurador se você usar um servidor de símbolos. Isso porque o depurador consulta o servidor de símbolo sempre que tenta carregar o executável. Por esse motivo, é melhor sempre solicitar símbolos para todos os componentes.

Talvez não seja possível solicitar símbolos para cada componente — por exemplo, os drivers de vídeo podem ter DLLs em seu espaço de processo e os arquivos PDB necessários estão disponíveis no servidor de símbolos da Microsoft. Nesse caso, há um pequeno atraso ao iniciar uma sessão de depuração.

Para evitar até mesmo esse pequeno atraso, você pode executar o depurador uma vez para armazenar em cache todos os símbolos localmente do servidor de símbolos da Microsoft. Em seguida, modifique \_ seu CAMINHO DE SÍMBOLO \_ \_ NT para remover o servidor de símbolos da Microsoft. A menos que os arquivos executáveis alterem, verifica se há arquivos executáveis que não têm símbolos não exigirão uma consulta pela Internet, pois você tem cópias armazenadas em cache local de todos os símbolos necessários do servidor de símbolos da Microsoft.

## <a name="getting-symbols-manually"></a>Obter símbolos manualmente

Se você tiver definido o depurador corretamente, ele carregará automaticamente todos os símbolos necessários do cache local ou de um servidor de símbolos. Se você quiser obter os símbolos para apenas um único executável ou para uma pasta de executáveis, poderá usar **symchk**. Por exemplo, se você quiser baixar os símbolos do arquivo30.dll d3dx9 na pasta Windows System no diretório atual, poderá usar o \_ seguinte comando:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" c:\Windows\System32\d3dx9_30.dll /oc \.
```

A **ferramenta symchk** tem muitos outros usos. Para obter detalhes, **consulte symchk /?** ou consulte a documentação ferramentas de depuração da Microsoft para Windows dados.

## <a name="setting-up-a-symbol-server"></a>Configurando um servidor de símbolos

Configurar um servidor de símbolos é muito simples. Ele é útil pelos seguintes motivos:

-   Para economizar largura de banda ou para acelerar a resolução de símbolos para sua empresa, equipe ou produto. Um servidor de símbolos interno em um compartilhamento de arquivos local em sua rede armazena em cache quaisquer referências a servidores de símbolos externos, como o servidor de símbolos da Microsoft. Um servidor de símbolos local ou interno pode ser acessado rapidamente por muitas pessoas ao mesmo tempo. Portanto, ele economiza largura de banda e a latência que solicitações de símbolo duplicadas podem criar.
-   Para armazenar símbolos para builds antigos, versões ou versões externas do seu aplicativo. Ao armazenar os símbolos desses builds em um servidor de símbolos que você pode acessar facilmente, você pode depurar falhas e problemas nesses builds em qualquer computador que tenha um depurador e uma conexão com o servidor de símbolo local. Isso é particularmente útil se você depurar mini-despejos gerados por executáveis que você não criou por conta própria, ou seja, builds que foram gerados por outro programador ou por um computador de build. Se os símbolos desses builds são armazenados no servidor de símbolos, você terá uma depuração confiável e precisa.
-   Para manter os símbolos atualizados. Quando os componentes são atualizados, como componentes do sistema operacional que são modificados pelo Windows Update ou pelo SDK do DirectX, você ainda pode depurar usando todos os símbolos mais recentes.

Configurar um servidor de símbolos em sua própria rede local é tão simples quanto criar um compartilhamento de arquivos em um servidor e dar aos usuários permissões completas para acessar o compartilhamento, para criar arquivos e pastas. Esse compartilhamento deve ser criado em um sistema operacional do servidor, como o Windows Server 2003, para que o número de pessoas que podem acessar o compartilhamento simultaneamente não seja limitado.

Por exemplo, se você configurar um compartilhamento de arquivos em \\ símbolos mainserver, os membros de sua equipe definirão o CAMINHO do \\ \\ SÍMBOLO \_ NT para o \_ \_ seguinte:

``` syntax
Srv*c:\symbols*\\mainserver\symbols*https://msdl.microsoft.com/download/symbols
```

Conforme os símbolos são recuperados, arquivos e pastas aparecem no diretório compartilhado de símbolos de servidor principal, bem como em caches individuais, no diretório \\ \\ \\ de \\ símbolos c: .

Normalmente, isso é tudo o que está envolvido na configuração e no uso de seu próprio servidor de símbolos ou do servidor de símbolos da Microsoft.

## <a name="adding-symbols-to-a-symbol-server"></a>Adicionando símbolos a um servidor de símbolos

Para adicionar, excluir ou editar arquivos em um compartilhamento de servidor de símbolos, use a ferramenta symstore.exe dados. Essa ferramenta faz parte do pacote Microsoft Debugging Tools for Windows. A documentação completa sobre servidores de símbolos, a ferramenta symstore e símbolos de indexação está incluída no pacote Ferramentas de Depuração Windows Aplicativo.

Talvez você queira adicionar símbolos diretamente ao seu próprio servidor de símbolos, como parte de um processo de build, ou disponibilizar símbolos para toda a sua equipe para bibliotecas ou ferramentas de terceiros. O processo de adicionar um símbolo a um compartilhamento de arquivos do servidor de símbolos é chamado de símbolos de indexação. Há duas maneiras comuns de indexar símbolos. Um arquivo de símbolo pode ser copiado para o servidor de símbolos. Ou um ponteiro para o local do símbolo pode ser copiado para o servidor de símbolos. Se você tiver uma pasta de arquivos que contém seus builds antigos, talvez queira indexar ponteiros para os arquivos PDB que já estão no compartilhamento, em vez de duplicar símbolos. Como os símbolos às vezes podem ter dezenas de megabytes de tamanho, é uma boa ideia planejar com antecedência quanto espaço você pode exigir para arquivar todos os builds do seu projeto durante o desenvolvimento. Se você indexar apenas ponteiros para símbolos, poderá ter problemas se remover builds antigos ou alterar o nome de um compartilhamento de arquivos.

Por exemplo, para indexar recursivamente todos os símbolos em c: dxsym Extras Symbols que você obteve do SDK do DirectX de outubro de 2006 em um compartilhamento de arquivos do servidor de \\ \\ \\ \\ \\ símbolos chamado \\ símbolos mainserver, você pode usar o seguinte comando:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symstore" add /f "C:\dxsym\Extras\Symbols\*.pdb"
/s \\mainserver\symbols /t "October 2006 DirectX SDK " /r
```

O **parâmetro /t "comment"** é usado para adicionar uma descrição à transação que adicionou os símbolos. Isso pode ser útil ao executar tarefas administrativas nos símbolos.

## <a name="best-practices"></a>Práticas Recomendadas

-   Configurar seu próprio compartilhamento de arquivos do servidor de símbolos para sua equipe, empresa ou produto.
-   Configurar o CAMINHO DO SÍMBOLO NT para apontar para um cache local, para um servidor de símbolos privado \_ e para o servidor de \_ \_ símbolos da Microsoft.
-   Se um depurador não puder carregar símbolos para um componente que você está depurando, entre em contato com o proprietário do componente para solicitar símbolos – pelo menos um PDB removido.
-   Configurar um sistema de build automatizado para indexar símbolos em seu servidor de símbolos privado para cada build produzido. Certifique-se de que os builds que você distribui sejam os builds gerados por esse processo. Isso garante que os símbolos estão sempre disponíveis para depurar problemas.
-   Configurar um servidor de símbolos para permitir que os depurador acessem o código-fonte de um módulo específico diretamente de um sistema de controle do código-fonte Cofre ou baseado em Perforce. Se as informações do arquivo de origem e os símbolos de uma versão lançada de um jogo são indexados, os desenvolvedores que têm acesso ao servidor de símbolos podem ter depuração de nível de origem completo de problemas relatados, sem manter ambientes de build ou versões antigas de arquivos de origem em seus computadores de desenvolvimento. Para configurar o servidor de símbolos para permitir a indexação de informações de arquivo de origem, consulte a documentação do servidor de origem.

 

 
