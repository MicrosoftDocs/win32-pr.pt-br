---
title: Depurando com símbolos
description: Este artigo fornece uma visão geral de alto nível de como usar melhor os símbolos no processo de depuração.
ms.assetid: 7ce0c9c7-485c-8d72-0353-27fd2e369a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff63e2404a07a2f0ab5adcb156d83dc989b42fd4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499095"
---
# <a name="debugging-with-symbols"></a>Depurando com símbolos

Este artigo fornece uma visão geral de alto nível de como usar melhor os símbolos no processo de depuração. Ele explica como usar o servidor de símbolos da Microsoft e também como configurar e usar seu próprio servidor de símbolos privado. Essas práticas recomendadas podem ajudar a aumentar sua eficácia e a capacidade de depurar problemas, mesmo em casos em que todos os símbolos e arquivos executáveis relacionados a um problema não estejam localizados no seu computador.

-   [Símbolos](#debugging-with-symbols)
-   [Usando símbolos para depuração](#using-symbols-for-debugging)
-   [Obtendo os símbolos necessários](#getting-the-symbols-you-need)
    -   [Verificar se um determinado arquivo DLL ou. exe e PDB na mesma pasta correspondem](#check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match)
    -   [Verificar se todos os arquivos dll e executáveis em um conjunto de pastas têm PDBs correspondentes](#check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs)
    -   [Como o Symchk funciona](#how-symchk-works)
-   [Servidores de símbolos](#symbol-servers)
-   [Usando o servidor de símbolos da Microsoft](#using-the-microsoft-symbol-server)
-   [Obtendo símbolos manualmente](#getting-symbols-manually)
-   [Configurando um servidor de símbolos](#setting-up-a-symbol-server)
-   [Adicionando símbolos a um servidor de símbolos](#adding-symbols-to-a-symbol-server)
-   [Práticas recomendadas](#best-practices)

## <a name="symbols"></a>Símbolos

Vários tipos diferentes de símbolos estão disponíveis para depuração. Eles incluem símbolos CodeView, COFF, DBG, SYM, PDB e até mesmo símbolos de exportação que são gerados de uma tabela de exportação de arquivos binários. Este white paper aborda apenas VS.NET e símbolos de formato PDB, pois eles são o formato preferencial mais recente. Eles são gerados por padrão para projetos que são compilados usando o Visual Studio.

A geração de arquivos PDB para executáveis de versão não afeta nenhuma otimização ou altera significativamente o tamanho dos arquivos gerados. Normalmente, a única diferença é o caminho e o nome de arquivo do arquivo PDB é inserido no executável. Por esse motivo, você sempre deve produzir arquivos PDB, mesmo que não queira enviá-los com o executável.

Os arquivos PDB são gerados se um projeto é criado usando a opção de compilador **/Zi** ou **/Zi** (produzir informações PDB), junto com a opção de vinculador de **/debug** (gerar informações de depuração). Os arquivos PDB gerados pelo compilador são combinados e gravados em um único arquivo PDB que é colocado no mesmo diretório que o executável.

Por padrão, os arquivos PDB contêm as seguintes informações:

-   Símbolos públicos (normalmente todas as funções, variáveis estáticas e globais)
-   Uma lista de arquivos de objeto que são responsáveis por seções de código no executável
-   Informações de otimização do ponteiro do quadro (FPO)
-   Informações de nome e tipo para variáveis locais e estruturas de dados
-   Informações de número de arquivo e linha de origem

Se você estiver preocupado com as pessoas que usam as informações do arquivo PDB para ajudá-las a fazer a engenharia reversa do seu executável, também poderá gerar arquivos PDB removidos usando a opção de vinculador **/PDBSTRIPPED: filename** . Se você tiver arquivos PDB existentes dos quais gostaria de remover informações particulares, poderá usar uma ferramenta chamada pdbcopy, que faz parte das ferramentas de depuração para Windows.

Por padrão, os arquivos PDB removidos contêm as seguintes informações:

-   Símbolos públicos (normalmente apenas funções não estáticas e variáveis globais)
-   Uma lista de arquivos de objeto que são responsáveis por seções de código no executável
-   Informações de otimização do ponteiro do quadro (FPO)

Essas são as informações mínimas necessárias para permitir a depuração confiável. As informações mínimas também dificultam a obtenção de qualquer informação adicional sobre o código-fonte original. Como um arquivo PDB removido e um arquivo PDB regular são gerados, você pode fornecer a versão removida aos usuários que podem precisar de recursos de depuração limitados, mas manter a confidencialidade completa. Observe que **/PDBSTRIPPED** gera um segundo arquivo PDB menor, portanto, certifique-se de usar o arquivo PDB correto ao gerar compilações para distribuir em grande escala. Para um projeto típico, um PDB regular pode ter alguns megabytes de tamanho, mas uma versão removida do PDB pode ter apenas algumas centenas de kilobytes.

## <a name="using-symbols-for-debugging"></a>Usando símbolos para depuração

Quando você estiver depurando um aplicativo que falhou, o depurador tentará mostrar as funções na pilha que levaram à falha. Sem um arquivo PDB, o depurador não pode resolver os nomes de função, seus parâmetros ou quaisquer variáveis locais que estejam armazenadas na pilha. Se você depurar executáveis de 32 bits, há situações em que você não pode até mesmo obter rastreamentos de pilha confiáveis sem símbolos. Às vezes, é possível examinar os valores brutos na pilha e solucionar quais valores podem retornar endereços, mas eles podem ser facilmente confundidos com referências de função ou dados.

Se as funções na pilha atual foram compiladas usando a otimização omitir ponteiros de quadro (**/Oy**) e, se os símbolos não estiverem presentes, o depurador não poderá determinar de forma confiável qual função chamou a função atual. Isso ocorre porque, sem as informações de FPO (otimização de ponteiro de quadro) que PDBs contêm, o depurador não pode contar com o EBP (registro de ponteiro de quadro) para apontar para o ponteiro de quadro anterior salvo e no endereço de retorno da função pai. Em vez disso, ele é adivinhado. Às vezes, ele fica certo. No entanto, ele geralmente fica errado, o que pode ser enganoso. Se você vir um aviso sobre símbolos ausentes ou nenhum símbolo carregado, como no exemplo a seguir, não confie na pilha a partir desse ponto abaixo.

``` syntax
SWPerfTest.exe!TextFunction(... ...)    Line 59    C++
d3dx9d.dll!008829b5()
[Frames below may be incorrect and/or missing, no symbols loaded for d3dx9d.dll]
SWPerfTest.exe!main(int argc=, const char * * argv=)  Line 328 + 0x12 bytes     C++
SWPerfTest.exe!__mainCRTStartup() Line 716 + 0x17 bytes    C
kernel32.dll!@BaseThreadInitThunk@12() + 0x12 bytes
ntdll.dll!__RtlUserThreadStart@8() + 0x27 bytes
```

Em muitos casos, é possível continuar a depuração sem símbolos, pois o problema está em um local que tem símbolos precisos e você não precisa examinar as funções mais adiante na pilha de chamadas. Mesmo que uma biblioteca que esteja em sua pilha de chamadas não tenha PDBs disponíveis, desde que elas tenham sido compiladas com ponteiros de quadro, o depurador deverá ser capaz de adivinhar corretamente nas funções pai. A partir do Windows XP Service Pack 2, todos os arquivos executáveis e DLL do Windows são compilados com o FPO desabilitado, pois torna a depuração mais precisa. Desabilitar o FPO também permite que os profileres de amostragem orientem a pilha durante o tempo de execução, com impacto mínimo no desempenho. Em versões do Windows anteriores ao Windows XP SP2, todos os binários do sistema operacional exigem arquivos de símbolo correspondentes que contenham informações FPO para permitir depuração e criação de perfil precisas.

Se você depurar executáveis nativos de 64 bits, não precisará de arquivos de símbolo para produzir rastreamentos de pilha válidos, pois os compiladores e sistemas operacionais x64 são projetados para não exigir. No entanto, você ainda precisa de arquivos de símbolo para recuperar os nomes de função, parâmetros de chamada e variáveis locais.

No entanto, alguns casos são particularmente difíceis de depurar sem símbolos. Por exemplo, se você depurar um programa para o qual criou um arquivo PDB e se falhar em um retorno de chamada de uma função em uma DLL para a qual você não tem símbolos, não será possível ver qual função causou o retorno de chamada, porque você não poderá decodificar a pilha. Isso geralmente ocorre em bibliotecas de terceiros, se PDBs não forem fornecidos ou em componentes antigos do sistema operacional, se PDBs não estiverem disponíveis. Os retornos de chamada geralmente ocorrem durante a passagem de mensagens, a enumeração, a alocação de memória ou o tratamento de exceções. A depuração dessas funções sem uma pilha precisa pode ser frustrante.

Para depurar com confiança os minidespejos gerados em um computador diferente ou que falharam no código que você não possui, é importante poder acessar todos os símbolos e binários para os executáveis que são referenciados no mini-despejo. Se os símbolos e os binários estiverem disponíveis em um servidor de símbolos, eles serão obtidos automaticamente pelo depurador. Para obter mais informações sobre minidespejos, consulte o white paper de [análise de despejo](/windows/desktop/DxTechArts/crash-dump-analysis) de memória.

## <a name="getting-the-symbols-you-need"></a>Obtendo os símbolos necessários

O Visual Studio e outros depuradores da Microsoft, como o WinDbg, normalmente são configurados para funcionar apenas se você estiver criando um aplicativo e Depurando-o em seu próprio computador. Se você precisar dar ao seu executável para outra pessoa, se você tiver várias versões de uma DLL ou um arquivo. exe em seu computador, ou se quiser depurar com precisão um aplicativo que usa o Windows ou outras bibliotecas, como o DirectX, você precisa entender como os depuradores localizam e carregam símbolos. O depurador usa o caminho de pesquisa de símbolo especificado pelo usuário — que é encontrado em opções \\ Depurando \\ símbolos no Visual Studio — ou na \_ \_ variável de \_ ambiente caminho de símbolo NT. Normalmente, o depurador procura PDBs correspondentes nos seguintes locais:

-   No local especificado dentro da DLL ou do arquivo executável.

    Se você tiver criado uma DLL ou um arquivo executável em seu computador, por padrão, o vinculador colocará o caminho completo e o nome do arquivo PDB dentro da DLL ou do arquivo executável. Quando você depura, o depurador verifica primeiro se o arquivo de símbolo existe no local especificado dentro da DLL ou no arquivo executável. Isso é útil, pois você sempre tem símbolos disponíveis para o código que você compilou em seu computador.

-   PDBs que podem estar presentes na mesma pasta que a DLL ou o arquivo executável.
-   Em algumas pastas de cache de símbolo locais.
-   Qualquer servidor de símbolos de compartilhamento de arquivos de rede local.
-   Qualquer servidor de símbolos da Internet, como o Microsoft Symbol Server.

Para ter certeza de que você tem todos os PDBs necessários para a depuração precisa, instale as ferramentas de depuração para Windows. As versões 32 e 64 bits podem ser encontradas em [ferramentas de depuração para Windows](/windows-hardware/drivers/debugger/).

Uma ferramenta útil instalada com esse pacote é symchk.exe. Ele pode ajudar a identificar símbolos ausentes ou incorretos. Essa ferramenta tem um grande número de opções de linha de comando potenciais. Aqui estão dois dos mais úteis e comumente usados.

### <a name="check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match"></a>Verificar se um determinado arquivo DLL ou. exe e PDB na mesma pasta correspondem

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" testing.dll /s

SYMCHK: FAILED files = 0
SYMCHK: PASSED + IGNORED files = 1
```

A opção **/s** diz ao **Symchk** para procurar símbolos somente na pasta atual e não examinar nenhum servidor de símbolos.

### <a name="check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs"></a>Verificar se todos os arquivos dll e executáveis em um conjunto de pastas têm PDBs correspondentes

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" *.* /r
```

A opção **/r** define **Symchk** para percorrer recursivamente as pastas, para verificar se todos os arquivos executáveis têm PDBs correspondentes. Sem a opção **/s** , **Symchk** usa o \_ caminho do símbolo NT atual \_ \_ para procurar por símbolos em qualquer servidor privado ou local ou nos servidores de símbolo da Microsoft. A ferramenta **Symchk** pesquisa apenas os símbolos para arquivos executáveis (. exe,. dll e semelhantes). Você não pode usar curingas para procurar por símbolos para arquivos não executáveis.

### <a name="how-symchk-works"></a>Como o Symchk funciona

Quando o vinculador gera arquivos. dll, executáveis e PDB, ele armazena GUIDs idênticos em cada arquivo. O GUID é usado pelas ferramentas para determinar se um determinado arquivo PDB corresponde a uma DLL ou a um arquivo executável. Se você alterar uma DLL ou um arquivo executável — usando um editor de recursos ou uma codificação de proteção de cópia ou alterando suas informações de versão, o GUID será atualizado e o depurador não poderá carregar o arquivo PDB. Por esse motivo, é muito importante evitar manipular a DLL ou o arquivo executável depois que ele é criado pelo vinculador.

Você também pode usar o utilitário DUMPBIN que vem com VS.NET para mostrar os caminhos de símbolo que são pesquisados e ver se são encontrados arquivos de símbolo que correspondam a um determinado DLL ou arquivo executável. Por exemplo:

``` syntax
DUMPBIN /PDBPATH:VERBOSE filename.exe
```

## <a name="symbol-servers"></a>Servidores de símbolos

Um servidor de símbolos é um repositório para várias versões de arquivos executáveis e de símbolo. Ele contém os próprios arquivos de símbolo ou os ponteiros para os arquivos de símbolo associados. Os depuradores entendem como usar servidores de símbolos e podem usá-los para pesquisar símbolos ausentes ou desconhecidos.

DLL e arquivos executáveis também estão disponíveis no servidor de símbolos da Microsoft. Isso torna possível depurar falhas e examinar o código de arquivos do sistema operacional que podem não existir em seu computador. Se um depurador encontrar um arquivo executável ou uma DLL que não exista no sistema que você está usando para depuração, ele solicitará automaticamente os símbolos e uma cópia do arquivo binário dos servidores de símbolos da Microsoft. Isso é útil se você estiver depurando um componente que tem muitas versões, por exemplo, msvcrt.dll — e você precisa examinar o código para uma versão que não existe em seu computador. Isso também ajuda a depurar minidespejos gerados em um sistema operacional diferente do sistema que você está usando para depuração.

A Microsoft publica todos os arquivos PDB de todos os sistemas operacionais e outros componentes redistribuídos, como o SDK do DirectX, em seu servidor de símbolos acessível externamente. Isso facilita a depuração de um aplicativo que usa esses arquivos DLL ou executáveis. Você pode usar o servidor de símbolos da Microsoft para resolver símbolos, junto com quaisquer símbolos locais para componentes que foram criados em seu computador.

Você pode configurar seu computador para usar o servidor de símbolos da Microsoft, que fornece acesso a todos os arquivos de símbolos da Microsoft. Você também pode configurar um servidor de símbolos privado para sua empresa, equipe ou rede, que pode ser usado para armazenar várias versões mais antigas de um projeto no qual você está trabalhando ou para fornecer um cache local para os símbolos que você usa do servidor de símbolos da Microsoft.

Para usar um servidor de símbolos, especifique o caminho de pesquisa em uma variável de ambiente chamada \_ NT \_ Symbol \_ Path. Os depuradores e as ferramentas modernas, como o WinDbg, o NTSD ou o Visual Studio, usam automaticamente esse caminho para procurar por símbolos.

Quando um depurador procura por símbolos, ele primeiro pesquisa localmente. Em seguida, ele examina os servidores de símbolo. Quando ele encontra um símbolo correspondente, ele transfere o arquivo de símbolo para o cache local. Os símbolos de um arquivo executável ou DLL típico variam de 1 a 100 MB de tamanho. Portanto, se você estiver depurando um processo que inclui muitas DLLs, pode levar algum tempo para resolver todos os símbolos e transferi-los para um cache local.

## <a name="using-the-microsoft-symbol-server"></a>Usando o servidor de símbolos da Microsoft

O servidor de símbolos da Microsoft permite que você obtenha todos os símbolos mais recentes, incluindo símbolos para arquivos atualizados ou corrigidos. O servidor de símbolos da Microsoft está disponível em <https://msdl.microsoft.com/download/symbols> .

Você pode acessar o servidor de símbolos de uma das seguintes maneiras:

-   Insira o endereço do servidor diretamente. No Visual Studio, no menu **ferramentas** , escolha **Opções**, escolha **depuração** e, em seguida, escolha **símbolos**.
-   Use a variável de \_ ambiente \_ caminho do símbolo NT \_ . Este método é recomendável.

    Isso é usado por todas as ferramentas de depuração. Ele também é usado pelo Visual Studio e é lido e decodificado quando o Visual Studio é aberto. Portanto, se você alterá-lo, precisará reiniciar o Visual Studio.

    Essa variável de ambiente permite que você especifique vários servidores de símbolo — por exemplo, um servidor de símbolos privado interno. Ele também permite que você especifique um diretório de cache local para armazenar PDBs para todos os símbolos que você procura dos servidores de símbolos, tanto internamente quanto pela Internet.

A sintaxe para a \_ \_ variável de caminho de símbolo NT \_ é:

``` syntax
srv*[local cache]*[private symbol server]*https://msdl.microsoft.com/download/symbols
```

Substitua \[ o cache local \] pelo nome de um diretório no computador em que você deseja armazenar um cache de quaisquer símbolos usados, por exemplo,% SystemRoot% \\ Symbols ou c: \\ Symbols.

O \[ servidor de símbolos privado \] é opcional. Ele pode apontar para um servidor de símbolos que está localizado em sua rede ou pode apontar para um servidor de símbolos compartilhado por sua equipe, grupo de produtos ou empresa.

Para usar apenas o servidor de símbolos da Microsoft junto com um cache local de símbolos, para acelerar o acesso pela Internet, use a seguinte configuração para o \_ \_ caminho do símbolo NT \_ :

``` syntax
srv*c:\symbols*https://msdl.microsoft.com/download/symbols
```

Você pode encontrar outras opções para o \_ \_ caminho do símbolo NT \_ no arquivo de ajuda que é instalado com o pacote Microsoft Debugging Tools for Windows.

Os executáveis sem símbolos podem aumentar o tempo necessário para iniciar um depurador se você usar um servidor de símbolos. Isso ocorre porque o depurador consulta o servidor de símbolos sempre que tenta carregar o executável. Por esse motivo, é melhor solicitar sempre símbolos para todos os componentes.

Talvez não seja possível solicitar símbolos para cada componente — por exemplo, os drivers de vídeo podem ter DLLs em seu espaço de processo e os arquivos PDB necessários estão disponíveis no servidor de símbolos da Microsoft. Nesse caso, há um pequeno atraso ao iniciar uma sessão de depuração.

Para evitar mesmo esse pequeno atraso, você pode executar o depurador uma vez para armazenar em cache todos os símbolos localmente do servidor de símbolos da Microsoft. Em seguida, modifique o caminho do seu \_ \_ símbolo NT \_ para remover o servidor de símbolos da Microsoft. A menos que os arquivos executáveis sejam alterados, o verifica se os arquivos executáveis que não têm símbolos não exigirão uma consulta pela Internet, porque você tem cópias em cache locais de todos os símbolos necessários do servidor de símbolos da Microsoft.

## <a name="getting-symbols-manually"></a>Obtendo símbolos manualmente

Se você tiver configurado o depurador corretamente, ele carregará automaticamente todos os símbolos que ele exigir do seu cache local ou de um servidor de símbolos. Se você quiser obter os símbolos para apenas um único executável, ou para uma pasta de executáveis, você pode usar **Symchk**. Por exemplo, se você quiser baixar os símbolos para o arquivo de \_30.dll d3dx9 na pasta de sistema do Windows para o diretório atual, poderá usar o seguinte comando:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" c:\Windows\System32\d3dx9_30.dll /oc \.
```

A ferramenta **Symchk** tem muitos outros usos. Para obter detalhes, consulte **Symchk/?** ou procure na documentação das ferramentas de depuração da Microsoft para Windows.

## <a name="setting-up-a-symbol-server"></a>Configurando um servidor de símbolos

A configuração de um servidor de símbolos é muito simples. Isso é útil pelos seguintes motivos:

-   Para economizar largura de banda ou para acelerar a resolução de símbolos para sua empresa, equipe ou produto. Um servidor de símbolos interno em um compartilhamento de arquivos local em sua rede armazena em cache todas as referências a servidores de símbolos externos, como o servidor de símbolos da Microsoft. Um servidor de símbolos local ou interno pode ser acessado rapidamente por muitas pessoas ao mesmo tempo. Portanto, ele economiza largura de banda e a latência que as solicitações de símbolo duplicadas podem criar.
-   Para armazenar símbolos para compilações antigas, versões ou versões externas do seu aplicativo. Ao armazenar os símbolos para essas compilações em um servidor de símbolos que você pode acessar facilmente, você pode depurar falhas e problemas nessas compilações em qualquer computador que tenha um depurador e uma conexão com o servidor de símbolo local. Isso é particularmente útil se você depurar minidespejos que são gerados por executáveis que você não criou, ou seja, compilações que foram geradas por outro programador ou por um computador de compilação. Se os símbolos para essas compilações forem armazenados no seu servidor de símbolos, você terá uma depuração confiável e precisa.
-   Para manter os símbolos atualizados. Quando os componentes são atualizados, como OS componentes do sistema operacional que são modificados por Windows Update ou pelo SDK do DirectX, você ainda pode depurar usando todos os símbolos mais recentes.

Configurar um servidor de símbolos em sua própria rede local é tão simples quanto criar um compartilhamento de arquivos em um servidor e dar aos usuários permissões completas para acessar o compartilhamento, para criar arquivos e pastas. Esse compartilhamento deve ser criado em um sistema operacional de servidor, como o Windows Server 2003, para que o número de pessoas que podem acessar o compartilhamento simultaneamente não seja limitado.

Por exemplo, se você configurar um compartilhamento de arquivos em \\ \\ \\ símbolos mainserver, os membros de sua equipe definirão o \_ caminho do símbolo do NT \_ \_ como o seguinte:

``` syntax
Srv*c:\symbols*\\mainserver\symbols*https://msdl.microsoft.com/download/symbols
```

À medida que os símbolos são recuperados, os arquivos e as pastas são exibidos no \\ \\ \\ diretório compartilhado mainserver Symbols, bem como em caches individuais, no diretório c: \\ Symbols.

Normalmente, isso é tudo que está envolvido na configuração e no uso do seu próprio servidor de símbolos ou do servidor de símbolos da Microsoft.

## <a name="adding-symbols-to-a-symbol-server"></a>Adicionando símbolos a um servidor de símbolos

Para adicionar, excluir ou editar arquivos em um compartilhamento de servidor de símbolos, use a ferramenta symstore.exe. Essa ferramenta faz parte do pacote das ferramentas de depuração para Windows da Microsoft. A documentação completa sobre servidores de símbolos, a ferramenta SymStore e os símbolos de indexação está incluída no pacote ferramentas de depuração para Windows.

Talvez você queira adicionar símbolos diretamente ao seu próprio servidor de símbolos, como parte de um processo de compilação, ou disponibilizar os símbolos para toda a equipe para bibliotecas ou ferramentas de terceiros. O processo de adicionar um símbolo a um compartilhamento de arquivos de servidor de símbolos é chamado de indexação de símbolos. Há duas maneiras comuns de indexar símbolos. Um arquivo de símbolo pode ser copiado para o servidor de símbolos. Ou, um ponteiro para o local do símbolo pode ser copiado para o servidor de símbolos. Se você tiver uma pasta de arquivo morto que contém suas compilações antigas, talvez queira indexar ponteiros para os arquivos PDB que já estão no compartilhamento, em vez de duplicar os símbolos. Como os símbolos podem ser, às vezes, dezenas de megabytes de tamanho, é uma boa ideia planejar com antecedência quanto espaço você pode precisar para arquivar todas as compilações do seu projeto durante o desenvolvimento. Se você indexar apenas ponteiros para símbolos, poderá ter problemas se remover compilações antigas ou alterar o nome de um compartilhamento de arquivos.

Por exemplo, para indexar recursivamente todos os símbolos em c: \\ dxsym os \\ \\ símbolos extras que você obteve do SDK do DirectX de outubro de 2006 em um compartilhamento de arquivos do servidor de símbolos chamado \\ \\ mainserver \\ Symbols, você pode usar o seguinte comando:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symstore" add /f "C:\dxsym\Extras\Symbols\*.pdb"
/s \\mainserver\symbols /t "October 2006 DirectX SDK " /r
```

O parâmetro **/t "Comment"** é usado para adicionar uma descrição à transação que adicionou os símbolos. Isso pode ser útil ao executar tarefas administrativas nos símbolos.

## <a name="best-practices"></a>Práticas Recomendadas

-   Configure seu próprio compartilhamento de arquivos de servidor de símbolos para sua equipe, empresa ou produto.
-   Configure \_ \_ \_ o caminho do símbolo do NT para apontar para um cache local, para um servidor de símbolos privado e para o servidor de símbolos da Microsoft.
-   Se um depurador não puder carregar símbolos para um componente que você está Depurando, entre em contato com o proprietário do componente para solicitar símbolos — pelo menos um PDB removido.
-   Configure um sistema de compilação automatizado para indexar símbolos no seu servidor de símbolos privado para cada compilação produzida. Certifique-se de que as compilações distribuídas sejam as compilações geradas por esse processo. Isso garante que os símbolos estejam sempre disponíveis para problemas de depuração.
-   Configure um servidor de símbolos para permitir que os depuradores acessem o código-fonte de um módulo específico diretamente de um sistema de controle do código-fonte com base em uma fonte Visual segura ou Perforce. Se as informações e os símbolos do arquivo de origem de uma versão lançada de um jogo forem indexados, os desenvolvedores que têm acesso ao servidor de símbolos podem ter depuração de nível de origem completa de problemas relatados, sem manter os ambientes de compilação ou versões antigas dos arquivos de origem em seus computadores de desenvolvimento. Para configurar o servidor de símbolos para permitir a indexação de informações do arquivo de origem, consulte a documentação do servidor de origem.

 

 