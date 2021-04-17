---
description: O servidor de origem permite que um cliente recupere a versão exata dos arquivos de origem que foram usados para criar um aplicativo.
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: Servidor de Origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8d76c70b67c176126d8e424bd5b55b616697
ms.sourcegitcommit: bfb5d94f754d017307b4cc9d914a2716701331d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756014"
---
# <a name="source-server"></a>Servidor de Origem

O servidor de origem permite que um cliente recupere a versão exata dos arquivos de origem que foram usados para criar um aplicativo. Como o código-fonte de um módulo pode ser alterado entre as versões e, durante um curso de anos, é importante observar o código-fonte como ele existia quando a versão do módulo em questão foi criada.

O servidor de origem recupera os arquivos apropriados do controle do código-fonte. Para usar o servidor de origem, o aplicativo deve ter sido de origem indexado.

## <a name="source-indexing"></a>Indexação da fonte

O sistema de indexação de origem é uma coleção de arquivos executáveis e scripts Perl. Os scripts do Perl exigem Perl 5,6 ou superior.

Em geral, os binários são indexados de origem durante o processo de compilação após a criação do aplicativo. As informações necessárias para o servidor de origem são armazenadas nos arquivos PDB.

Atualmente, o servidor de origem é fornecido com scripts que devem funcionar com os seguintes sistemas de controle de origem.

-   Team Foundation Server
-   Perforce
-   Visual SourceSafe
-   TORNA
-   Subversion

Você também pode criar um script personalizado para indexar seu código para um sistema de controle de origem diferente.

A tabela a seguir lista as ferramentas do servidor de origem.



| Ferramenta        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Srcsrv.ini  | Esse arquivo é a lista mestra de todos os servidores de controle do código-fonte. Cada entrada tem o seguinte formato:*meuservidor* = *serverinfo*<br/> Ao usar o Perforce, as informações do servidor consistem no caminho de rede completo para o servidor, seguido por dois-pontos, seguidos pelo número da porta que ele usa. Por exemplo:<br/> MEUSERVIDOR = Machine. Corp. Company. com: 1666<br/> Esse arquivo pode ser instalado no computador que executa o depurador. Quando o servidor de origem é iniciado, ele examina Srcsrv.ini valores; esses valores substituirão as informações contidas no arquivo PDB. Isso permite que os usuários configurem um depurador para usar um servidor de controle do código-fonte alternativo no momento da depuração.<br/> Para obter mais informações, consulte o exemplo Srcsrv.ini instalado com as ferramentas do servidor de origem.<br/> |
| SSINDEX. cmd | Esse script cria a lista de arquivos verificados no controle do código-fonte junto com as informações de versão de cada arquivo. Ele armazena um subconjunto dessas informações nos arquivos. pdb gerados quando você criou o aplicativo. O script usa um dos seguintes módulos do Perl para fazer interface com o controle do código-fonte: P4.pm (Perforce) ou Vss.pm (Visual Source Safe). Para obter mais informações, execute o script com o-? ou-?? (ajuda detalhada) ou examine o script.<br/>                                                                                                                                                                                                                                                                                                             |
| Srctool.exe | Esse utilitário lista todos os arquivos indexados em um arquivo. pdb. Para cada arquivo, ele lista o caminho completo, o servidor de controle do código-fonte e o número de versão do arquivo. Você pode usar essas informações para recuperar arquivos sem usar o servidor de origem. Para obter mais informações, execute o utilitário com o/? opção.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Pdbstr.exe  | Esse utilitário é usado pelos scripts de indexação para inserir as informações de controle de versão no fluxo alternativo "srcsrv" do arquivo. pdb de destino. Ele também pode ler qualquer fluxo de um arquivo. pdb. Você pode usar essas informações para verificar se os scripts de indexação estão funcionando corretamente. Para obter mais informações, execute o utilitário com o/? opção.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a>Recuperando o arquivo de origem

A API DbgHelp fornece acesso à funcionalidade do servidor de origem por meio da função [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) . Para recuperar o nome do arquivo de origem a ser recuperado, chame a função [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) ou [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) .

## <a name="using-source-server-with-a-debugger"></a>Usando o servidor de origem com um depurador

Para usar o servidor de origem com o WinDbg, KD, NTSD ou CDB, verifique se você instalou uma versão recente do pacote de ferramentas de depuração para Windows (versão 6,3 ou posterior). Em seguida, inclua SRV \* no comando. srcpath da seguinte maneira:

**\. srcpath SRV \* ;** _c: \\ MySource_

Observe que esse exemplo também inclui um caminho de origem tradicional. Se o depurador não puder recuperar o arquivo do servidor de origem, ele pesquisará o caminho especificado.

Se um arquivo de origem for recuperado pelo servidor de origem, ele permanecerá no disco rígido depois que a sessão de depuração terminar. Os arquivos de origem são armazenados localmente no subdiretório src do diretório de instalação das ferramentas de depuração para Windows.

## <a name="source-server-data-blocks"></a>Blocos de dados do servidor de origem

O servidor de origem depende de dois blocos de dados dentro do arquivo PDB.

-   Lista de arquivos de origem. Criar um módulo cria automaticamente uma lista de caminhos totalmente qualificados para os arquivos de origem usados para compilar o módulo.
-   Bloco de dados. A indexação da origem, conforme descrito anteriormente, adiciona um fluxo alternativo ao arquivo PDB chamado "srcsrv". O script que insere esses dados depende do processo de compilação específico e do sistema de controle do código-fonte em uso.

Na especificação de linguagem versão 1, o bloco de dados é dividido em três seções: ini, variáveis e arquivos de origem. Ele tem a seguinte sintaxe.

``` syntax
SRCSRV: ini ------------------------------------------------ 
VERSION=1
VERCTRL=<source_control_str>
DATETIME=<date_time_str>
SRCSRV: variables ------------------------------------------ 
SRCSRVTRG=%sdtrg% 
SRCSRVCMD=%sdcmd% 
SRCSRVENV=var1=string1\bvar2=string2 
DEPOT=//depot 
SDCMD=sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%#%var4%
SDTRG=%targ%\%var2%\%fnbksl%(%var3%)\%var4%\%fnfile%(%var1%) 
WIN_SDKTOOLS= sserver.microsoft.com:4444 
SRCSRV: source files --------------------------------------- 
<path1>*<var2>*<var3>*<var4> 
<path2>*<var2>*<var3>*<var4> 
<path3>*<var2>*<var3>*<var4> 
<path4>*<var2>*<var3>*<var4> 
SRCSRV: end ------------------------------------------------
```

Todo o texto é interpretado literalmente, exceto o texto entre sinais de porcentagem (%). O texto entre sinais de porcentagem é tratado como um nome de variável a ser resolvido recursivamente, a menos que seja uma das seguintes funções:

<dl> <dt>

<span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()
</dt> <dd>

O texto do parâmetro deve ser colocado entre sinais de porcentagem e tratado como uma variável a ser expandida.

</dd> <dt>

<span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()
</dt> <dd>

Todas as barras (/) no texto do parâmetro devem ser substituídas por barras invertidas ( \\ ).

</dd> <dt>

<span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()
</dt> <dd>

Todas as informações de caminho no texto do parâmetro devem ser removidas, deixando apenas o nome do arquivo.

</dd> </dl>

A seção ini contém variáveis que descrevem os requisitos. O script de indexação pode adicionar qualquer número de variáveis a esta seção. Os exemplos são os seguintes:

<dl> <dt>

<span id="VERSION"></span><span id="version"></span>Versão
</dt> <dd>

A versão de especificação da linguagem. Esta variável é obrigatória.

</dd> <dt>

<span id="VERCTL"></span><span id="verctl"></span>VERCTL
</dt> <dd>

Uma cadeia de caracteres que descreve o produto de controle do código-fonte. Essa variável é opcional.

</dd> <dt>

<span id="DATETIME"></span><span id="datetime"></span>HORÁRIO
</dt> <dd>

Uma cadeia de caracteres que indica a data e a hora em que o arquivo PDB foi processado. Essa variável é opcional.

</dd> </dl>

A seção Variables contém variáveis que descrevem como extrair um arquivo do controle do código-fonte. Ele também pode ser usado para definir texto comumente usado como variáveis para reduzir o tamanho do bloco de dados.

<dl> <dt>

<span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG
</dt> <dd>

Descreve como criar o caminho de destino para o arquivo extraído. Essa é uma variável necessária.

</dd> <dt>

<span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD
</dt> <dd>

Descreve como criar o comando para extrair o arquivo do controle do código-fonte. Isso inclui o nome do arquivo executável e seus parâmetros de linha de comando. Essa é uma variável necessária.

</dd> <dt>

<span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV
</dt> <dd>

Uma cadeia de caracteres que lista as variáveis de ambiente a serem criadas durante a extração do arquivo. Separe várias entradas com um caractere de Backspace ( \\ b). Essa é uma variável opcional.

</dd> </dl>

A seção de arquivos de origem contém uma entrada para cada arquivo de origem que foi indexado. O conteúdo de cada linha é interpretado como variáveis com os nomes VAR1, VAR2, VAR3 e assim por diante até VAR10. As variáveis são separadas por asteriscos. VAR1 deve especificar o caminho totalmente qualificado para o arquivo de origem, conforme listado em outro lugar no arquivo PDB. Por exemplo, a seguinte linha:

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

é interpretado da seguinte maneira:

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

Neste exemplo, VAR4 é um número de versão. No entanto, a maioria dos sistemas de controle do código-fonte dá suporte ao rotulamento de arquivos de forma que o estado de origem de uma determinada compilação possa ser restaurado. Portanto, você poderia usar como alternativa o rótulo para a compilação. O bloco de dados de exemplo pode ser modificado para conter uma variável, como a seguinte:

``` syntax
LABEL=BUILD47
```

Em seguida, supondo que o sistema de controle do código-fonte Use o sinal de arroba (@) para indicar um rótulo, você pode modificar a variável SRCSRVCMD da seguinte maneira:

**sd.exe-p% fnvar%(% var2%) impressão-o% srcsrvtrg%-q% Depot%/%var3% @% Label%**

## <a name="how-source-server-works"></a>Como funciona o servidor de origem

O cliente do servidor de origem é implementado no Symsrv.dll. O cliente não extrai informações diretamente do arquivo PDB; Ele usa um manipulador de símbolo como o implementado em Dbghelp.dll. Ele é essencialmente um mecanismo de substituição de variáveis recursiva que cria uma linha de comando que pode ser usada para extrair o arquivo de origem apropriado do sistema de controle do código-fonte. Seu código não deve chamar Symsrv.dll diretamente. Para integrar sua funcionalidade ao seu aplicativo, use a função [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .

A primeira versão do servidor de origem funciona da seguinte maneira. Esse comportamento pode ser alterado em versões futuras.

-   O cliente chama a função **SrcSrvInit** com o caminho de destino a ser usado como base para todas as extrações de arquivo de origem. Ele armazena esse caminho na variável Tino.
-   O cliente extrai o fluxo srcsrv do PDB quando o módulo PDB é carregado e chama a função **SrcSrvLoadModule** para passar o bloco de dados para o servidor de origem.
-   Quando o dbghelp recupera um arquivo de origem, o cliente chama a função **SrcSrvGetFile** para recuperar os arquivos de origem do controle do código-fonte.
-   O servidor de origem pesquisa as entradas do arquivo de origem no bloco de dados para uma entrada que corresponda ao arquivo solicitado. Ele preenche VAR1 para VAR *n* com o conteúdo da entrada do arquivo de origem. Em seguida, ele expande a variável SRCSRVTRG usando VAR1 para VAR *n*. Se o arquivo já estiver nesse local, ele retornará o local para o chamador. Caso contrário, ele expande a variável SRCSRVCMD para criar o comando necessário para recuperar o arquivo do controle do código-fonte e copiá-lo para o local de destino. Por fim, ele executa esse comando.

## <a name="creating-a-source-control-provider-module"></a>Criando um módulo de provedor de controle do código-fonte

O servidor de origem inclui módulos de provedor para Perforce (p4.pm) e vss.pm (segurança de código-fonte Visual). Para criar seu próprio módulo de provedor, você deve implementar o seguinte conjunto de interfaces.

<dl> <dt>

<span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module:: SimpleUsage ()**
</dt> <dd>

Finalidade: exibe informações de uso de módulo simples para STDOUT.

Parâmetros: nenhum

Valor de retorno: nenhum

</dd> <dt>

<span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module:: VerboseUsage ()**
</dt> <dd>

Finalidade: exibe informações detalhadas de uso do módulo para STDOUT.

Parâmetros: nenhum

Valor de retorno: nenhum

</dd> <dt>

<span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module:: novo ( \@ CommandArguments)**
</dt> <dd>

Finalidade: Inicializa uma instância do módulo do provedor.

Parâmetros: todos os @ARGV argumentos que não foram reconhecidos pelo SSIndex. cmd como argumentos gerais.

Valor de retorno: uma referência que pode ser usada em operações posteriores.

</dd> <dt>

<span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation ($SourcePath, $ServerHashReference)**
</dt> <dd>

Finalidade: habilita o módulo para coletar as informações de indexação de fonte necessárias para o diretório especificado pelo parâmetro $SourcePath. O módulo não deve pressupor que essa entrada será chamada apenas uma vez para cada instância de objeto, já que SSIndex. cmd pode chamá-la várias vezes para caminhos diferentes.

Parâmetros: (1) o diretório local que contém a origem a ser indexada. (2) uma referência a um hash que contém todas as entradas do arquivo de Srcsrv.ini especificado.

Valor de retorno: nenhum

</dd> <dt>

<span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo ($LocalFile)**
</dt> <dd>

Finalidade: fornece as informações necessárias para extrair um único arquivo específico do sistema de controle do código-fonte.

Parâmetros: um nome de arquivo totalmente qualificado

Valor de retorno: (1) uma referência de hash das variáveis necessárias para interpretar o $FileEntry retornado. O SSIndex. cmd armazena essas variáveis em cache para cada arquivo de origem usado por um único arquivo de depuração para reduzir a quantidade de informações gravadas no fluxo do índice de origem. (2) a entrada de arquivo a ser gravada no fluxo do índice de origem para permitir que SrcSrv.dll extraia esse arquivo do controle do código-fonte. O formato exato dessa linha é específico do sistema de controle do código-fonte.

</dd> <dt>

<span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName ()**
</dt> <dd>

Finalidade: fornece uma cadeia de caracteres descritiva para identificar o provedor de controle do código-fonte para o usuário final.

Parâmetros: nenhum

Valor de retorno: o nome descritivo do sistema de controle do código-fonte.

</dd> <dt>

<span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables ()**
</dt> <dd>

Finalidade: habilita o provedor de controle do código-fonte a adicionar variáveis específicas de controle do código-fonte ao fluxo de origem para cada arquivo de depuração. Os módulos de exemplo usam esse método para gravar as variáveis de destino de extração \_ cmd e extração necessárias \_ .

Parâmetros: nenhum

Valor de retorno: a lista de entradas para as variáveis de fluxo de origem.

</dd> </dl>

 

 




