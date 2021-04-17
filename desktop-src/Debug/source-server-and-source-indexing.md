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
# <a name="source-server"></a><span data-ttu-id="6750b-103">Servidor de Origem</span><span class="sxs-lookup"><span data-stu-id="6750b-103">Source Server</span></span>

<span data-ttu-id="6750b-104">O servidor de origem permite que um cliente recupere a versão exata dos arquivos de origem que foram usados para criar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6750b-104">Source server enables a client to retrieve the exact version of the source files that were used to build an application.</span></span> <span data-ttu-id="6750b-105">Como o código-fonte de um módulo pode ser alterado entre as versões e, durante um curso de anos, é importante observar o código-fonte como ele existia quando a versão do módulo em questão foi criada.</span><span class="sxs-lookup"><span data-stu-id="6750b-105">Because the source code for a module can change between versions and over a course of years, it is important to look at the source code as it existed when the version of the module in question was built.</span></span>

<span data-ttu-id="6750b-106">O servidor de origem recupera os arquivos apropriados do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6750b-106">Source server retrieves the appropriate files from source control.</span></span> <span data-ttu-id="6750b-107">Para usar o servidor de origem, o aplicativo deve ter sido de origem indexado.</span><span class="sxs-lookup"><span data-stu-id="6750b-107">To use source server, the application must have been source indexed.</span></span>

## <a name="source-indexing"></a><span data-ttu-id="6750b-108">Indexação da fonte</span><span class="sxs-lookup"><span data-stu-id="6750b-108">Source Indexing</span></span>

<span data-ttu-id="6750b-109">O sistema de indexação de origem é uma coleção de arquivos executáveis e scripts Perl.</span><span class="sxs-lookup"><span data-stu-id="6750b-109">The source indexing system is a collection of executable files and Perl scripts.</span></span> <span data-ttu-id="6750b-110">Os scripts do Perl exigem Perl 5,6 ou superior.</span><span class="sxs-lookup"><span data-stu-id="6750b-110">The Perl scripts require Perl 5.6 or greater.</span></span>

<span data-ttu-id="6750b-111">Em geral, os binários são indexados de origem durante o processo de compilação após a criação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6750b-111">Generally, binaries are source indexed during the build process after the application has been built.</span></span> <span data-ttu-id="6750b-112">As informações necessárias para o servidor de origem são armazenadas nos arquivos PDB.</span><span class="sxs-lookup"><span data-stu-id="6750b-112">The information needed by source server is stored in the PDB files.</span></span>

<span data-ttu-id="6750b-113">Atualmente, o servidor de origem é fornecido com scripts que devem funcionar com os seguintes sistemas de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="6750b-113">Source server currently ships with scripts that should work with the following source-control systems.</span></span>

-   <span data-ttu-id="6750b-114">Team Foundation Server</span><span class="sxs-lookup"><span data-stu-id="6750b-114">Team Foundation Server</span></span>
-   <span data-ttu-id="6750b-115">Perforce</span><span class="sxs-lookup"><span data-stu-id="6750b-115">Perforce</span></span>
-   <span data-ttu-id="6750b-116">Visual SourceSafe</span><span class="sxs-lookup"><span data-stu-id="6750b-116">Visual SourceSafe</span></span>
-   <span data-ttu-id="6750b-117">TORNA</span><span class="sxs-lookup"><span data-stu-id="6750b-117">CVS</span></span>
-   <span data-ttu-id="6750b-118">Subversion</span><span class="sxs-lookup"><span data-stu-id="6750b-118">Subversion</span></span>

<span data-ttu-id="6750b-119">Você também pode criar um script personalizado para indexar seu código para um sistema de controle de origem diferente.</span><span class="sxs-lookup"><span data-stu-id="6750b-119">You can also create a custom script to index your code for a different source-control system.</span></span>

<span data-ttu-id="6750b-120">A tabela a seguir lista as ferramentas do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="6750b-120">The following table lists the source server tools.</span></span>



| <span data-ttu-id="6750b-121">Ferramenta</span><span class="sxs-lookup"><span data-stu-id="6750b-121">Tool</span></span>        | <span data-ttu-id="6750b-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="6750b-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6750b-123">Srcsrv.ini</span><span class="sxs-lookup"><span data-stu-id="6750b-123">Srcsrv.ini</span></span>  | <span data-ttu-id="6750b-124">Esse arquivo é a lista mestra de todos os servidores de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6750b-124">This file is the master list of all source control servers.</span></span> <span data-ttu-id="6750b-125">Cada entrada tem o seguinte formato:*meuservidor* = *serverinfo*</span><span class="sxs-lookup"><span data-stu-id="6750b-125">Each entry has the following format:*MYSERVER*=*serverinfo*</span></span><br/> <span data-ttu-id="6750b-126">Ao usar o Perforce, as informações do servidor consistem no caminho de rede completo para o servidor, seguido por dois-pontos, seguidos pelo número da porta que ele usa.</span><span class="sxs-lookup"><span data-stu-id="6750b-126">When using Perforce, the server info consists of the full network path to the server, followed by a colon, followed by the port number it uses.</span></span> <span data-ttu-id="6750b-127">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6750b-127">For example:</span></span><br/> <span data-ttu-id="6750b-128">MEUSERVIDOR = Machine. Corp. Company. com: 1666</span><span class="sxs-lookup"><span data-stu-id="6750b-128">MYSERVER=machine.corp.company.com:1666</span></span><br/> <span data-ttu-id="6750b-129">Esse arquivo pode ser instalado no computador que executa o depurador.</span><span class="sxs-lookup"><span data-stu-id="6750b-129">This file can be installed on the computer running the debugger.</span></span> <span data-ttu-id="6750b-130">Quando o servidor de origem é iniciado, ele examina Srcsrv.ini valores; esses valores substituirão as informações contidas no arquivo PDB.</span><span class="sxs-lookup"><span data-stu-id="6750b-130">When source server starts, it looks at Srcsrv.ini for values; these values will override the information contained in the PDB file.</span></span> <span data-ttu-id="6750b-131">Isso permite que os usuários configurem um depurador para usar um servidor de controle do código-fonte alternativo no momento da depuração.</span><span class="sxs-lookup"><span data-stu-id="6750b-131">This enables users to configure a debugger to use an alternate source control server at debug time.</span></span><br/> <span data-ttu-id="6750b-132">Para obter mais informações, consulte o exemplo Srcsrv.ini instalado com as ferramentas do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="6750b-132">For more information, see the example Srcsrv.ini installed with the source server tools.</span></span><br/> |
| <span data-ttu-id="6750b-133">SSINDEX. cmd</span><span class="sxs-lookup"><span data-stu-id="6750b-133">Ssindex.cmd</span></span> | <span data-ttu-id="6750b-134">Esse script cria a lista de arquivos verificados no controle do código-fonte junto com as informações de versão de cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="6750b-134">This script builds the list of files checked into source control along with the version information of each file.</span></span> <span data-ttu-id="6750b-135">Ele armazena um subconjunto dessas informações nos arquivos. pdb gerados quando você criou o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6750b-135">It stores a subset of this information in the .pdb files generated when you built the application.</span></span> <span data-ttu-id="6750b-136">O script usa um dos seguintes módulos do Perl para fazer interface com o controle do código-fonte: P4.pm (Perforce) ou Vss.pm (Visual Source Safe). Para obter mais informações, execute o script com o-?</span><span class="sxs-lookup"><span data-stu-id="6750b-136">The script uses one of the following Perl modules to interface with source control: P4.pm (Perforce) or Vss.pm (Visual Source Safe).For more information, run the script with the -?</span></span> <span data-ttu-id="6750b-137">ou-??</span><span class="sxs-lookup"><span data-stu-id="6750b-137">or -??</span></span> <span data-ttu-id="6750b-138">(ajuda detalhada) ou examine o script.</span><span class="sxs-lookup"><span data-stu-id="6750b-138">(verbose help) option or examine the script.</span></span><br/>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="6750b-139">Srctool.exe</span><span class="sxs-lookup"><span data-stu-id="6750b-139">Srctool.exe</span></span> | <span data-ttu-id="6750b-140">Esse utilitário lista todos os arquivos indexados em um arquivo. pdb.</span><span class="sxs-lookup"><span data-stu-id="6750b-140">This utility lists all files indexed within a .pdb file.</span></span> <span data-ttu-id="6750b-141">Para cada arquivo, ele lista o caminho completo, o servidor de controle do código-fonte e o número de versão do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6750b-141">For each file, it lists the full path, source control server, and version number of the file.</span></span> <span data-ttu-id="6750b-142">Você pode usar essas informações para recuperar arquivos sem usar o servidor de origem. Para obter mais informações, execute o utilitário com o/?</span><span class="sxs-lookup"><span data-stu-id="6750b-142">You can use this information to retrieve files without using the source server.For more information, run the utility with the /?</span></span> <span data-ttu-id="6750b-143">opção.</span><span class="sxs-lookup"><span data-stu-id="6750b-143">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6750b-144">Pdbstr.exe</span><span class="sxs-lookup"><span data-stu-id="6750b-144">Pdbstr.exe</span></span>  | <span data-ttu-id="6750b-145">Esse utilitário é usado pelos scripts de indexação para inserir as informações de controle de versão no fluxo alternativo "srcsrv" do arquivo. pdb de destino.</span><span class="sxs-lookup"><span data-stu-id="6750b-145">This utility is used by the indexing scripts to insert the version control information into the "srcsrv" alternate stream of the target .pdb file.</span></span> <span data-ttu-id="6750b-146">Ele também pode ler qualquer fluxo de um arquivo. pdb.</span><span class="sxs-lookup"><span data-stu-id="6750b-146">It can also read any stream from a .pdb file.</span></span> <span data-ttu-id="6750b-147">Você pode usar essas informações para verificar se os scripts de indexação estão funcionando corretamente. Para obter mais informações, execute o utilitário com o/?</span><span class="sxs-lookup"><span data-stu-id="6750b-147">You can use this information to verify that the indexing scripts are working properly.For more information, run the utility with the /?</span></span> <span data-ttu-id="6750b-148">opção.</span><span class="sxs-lookup"><span data-stu-id="6750b-148">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a><span data-ttu-id="6750b-149">Recuperando o arquivo de origem</span><span class="sxs-lookup"><span data-stu-id="6750b-149">Retrieving the Source File</span></span>

<span data-ttu-id="6750b-150">A API DbgHelp fornece acesso à funcionalidade do servidor de origem por meio da função [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .</span><span class="sxs-lookup"><span data-stu-id="6750b-150">The DbgHelp API provides access to source server functionality through the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span> <span data-ttu-id="6750b-151">Para recuperar o nome do arquivo de origem a ser recuperado, chame a função [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) ou [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) .</span><span class="sxs-lookup"><span data-stu-id="6750b-151">To retrieve the name of the source file to be retrieved, call the [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) or [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) function.</span></span>

## <a name="using-source-server-with-a-debugger"></a><span data-ttu-id="6750b-152">Usando o servidor de origem com um depurador</span><span class="sxs-lookup"><span data-stu-id="6750b-152">Using Source Server with a Debugger</span></span>

<span data-ttu-id="6750b-153">Para usar o servidor de origem com o WinDbg, KD, NTSD ou CDB, verifique se você instalou uma versão recente do pacote de ferramentas de depuração para Windows (versão 6,3 ou posterior).</span><span class="sxs-lookup"><span data-stu-id="6750b-153">To use the source server with WinDbg, KD, NTSD, or CDB, ensure that you have installed a recent version of the Debugging Tools for Windows package (version 6.3 or later).</span></span> <span data-ttu-id="6750b-154">Em seguida, inclua SRV \* no comando. srcpath da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6750b-154">Then, include srv\* in the .srcpath command as follows:</span></span>

<span data-ttu-id="6750b-155">**\. srcpath SRV \* ;** _c: \\ MySource_</span><span class="sxs-lookup"><span data-stu-id="6750b-155">**\.srcpath srv\*;**_c:\\mysource_</span></span>

<span data-ttu-id="6750b-156">Observe que esse exemplo também inclui um caminho de origem tradicional.</span><span class="sxs-lookup"><span data-stu-id="6750b-156">Note that this example also includes a traditional source path.</span></span> <span data-ttu-id="6750b-157">Se o depurador não puder recuperar o arquivo do servidor de origem, ele pesquisará o caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="6750b-157">If the debugger cannot retrieve the file from the source server, it will search the specified path.</span></span>

<span data-ttu-id="6750b-158">Se um arquivo de origem for recuperado pelo servidor de origem, ele permanecerá no disco rígido depois que a sessão de depuração terminar.</span><span class="sxs-lookup"><span data-stu-id="6750b-158">If a source file is retrieved by the source server, it will remain on your hard drive after the debugging session is over.</span></span> <span data-ttu-id="6750b-159">Os arquivos de origem são armazenados localmente no subdiretório src do diretório de instalação das ferramentas de depuração para Windows.</span><span class="sxs-lookup"><span data-stu-id="6750b-159">Source files are stored locally in the src subdirectory of the Debugging Tools for Windows installation directory.</span></span>

## <a name="source-server-data-blocks"></a><span data-ttu-id="6750b-160">Blocos de dados do servidor de origem</span><span class="sxs-lookup"><span data-stu-id="6750b-160">Source Server Data Blocks</span></span>

<span data-ttu-id="6750b-161">O servidor de origem depende de dois blocos de dados dentro do arquivo PDB.</span><span class="sxs-lookup"><span data-stu-id="6750b-161">Source server relies on two blocks of data within the PDB file.</span></span>

-   <span data-ttu-id="6750b-162">Lista de arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="6750b-162">Source file list.</span></span> <span data-ttu-id="6750b-163">Criar um módulo cria automaticamente uma lista de caminhos totalmente qualificados para os arquivos de origem usados para compilar o módulo.</span><span class="sxs-lookup"><span data-stu-id="6750b-163">Building a module automatically creates a list of fully qualified paths to the source files used to build the module.</span></span>
-   <span data-ttu-id="6750b-164">Bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="6750b-164">Data block.</span></span> <span data-ttu-id="6750b-165">A indexação da origem, conforme descrito anteriormente, adiciona um fluxo alternativo ao arquivo PDB chamado "srcsrv".</span><span class="sxs-lookup"><span data-stu-id="6750b-165">Indexing the source as described previously adds an alternate stream to the PDB file named "srcsrv".</span></span> <span data-ttu-id="6750b-166">O script que insere esses dados depende do processo de compilação específico e do sistema de controle do código-fonte em uso.</span><span class="sxs-lookup"><span data-stu-id="6750b-166">The script that inserts this data is dependent on the specific build process and source control system in use.</span></span>

<span data-ttu-id="6750b-167">Na especificação de linguagem versão 1, o bloco de dados é dividido em três seções: ini, variáveis e arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="6750b-167">In the language specification version 1, the data block is divided into three sections: ini, variables, and source files.</span></span> <span data-ttu-id="6750b-168">Ele tem a seguinte sintaxe.</span><span class="sxs-lookup"><span data-stu-id="6750b-168">It has the following syntax.</span></span>

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

<span data-ttu-id="6750b-169">Todo o texto é interpretado literalmente, exceto o texto entre sinais de porcentagem (%).</span><span class="sxs-lookup"><span data-stu-id="6750b-169">All text is interpreted literally, except for text enclosed in percent signs (%).</span></span> <span data-ttu-id="6750b-170">O texto entre sinais de porcentagem é tratado como um nome de variável a ser resolvido recursivamente, a menos que seja uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="6750b-170">Text enclosed in percent signs is treated as a variable name to be resolved recursively, unless it is one of the following functions:</span></span>

<dl> <dt>

<span data-ttu-id="6750b-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()</span><span class="sxs-lookup"><span data-stu-id="6750b-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()</span></span>
</dt> <dd>

<span data-ttu-id="6750b-172">O texto do parâmetro deve ser colocado entre sinais de porcentagem e tratado como uma variável a ser expandida.</span><span class="sxs-lookup"><span data-stu-id="6750b-172">The parameter text should be enclosed in percent signs and treated as a variable to be expanded.</span></span>

</dd> <dt>

<span data-ttu-id="6750b-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()</span><span class="sxs-lookup"><span data-stu-id="6750b-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()</span></span>
</dt> <dd>

<span data-ttu-id="6750b-174">Todas as barras (/) no texto do parâmetro devem ser substituídas por barras invertidas ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="6750b-174">All forward slashes (/) in the parameter text should be replaced with backward slashes (\\).</span></span>

</dd> <dt>

<span data-ttu-id="6750b-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()</span><span class="sxs-lookup"><span data-stu-id="6750b-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()</span></span>
</dt> <dd>

<span data-ttu-id="6750b-176">Todas as informações de caminho no texto do parâmetro devem ser removidas, deixando apenas o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6750b-176">All path information in the parameter text should be stripped out, leaving only the file name.</span></span>

</dd> </dl>

<span data-ttu-id="6750b-177">A seção ini contém variáveis que descrevem os requisitos.</span><span class="sxs-lookup"><span data-stu-id="6750b-177">The ini section contains variables that describe the requirements.</span></span> <span data-ttu-id="6750b-178">O script de indexação pode adicionar qualquer número de variáveis a esta seção.</span><span class="sxs-lookup"><span data-stu-id="6750b-178">The indexing script can add any number of variables to this section.</span></span> <span data-ttu-id="6750b-179">Os exemplos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="6750b-179">The following are examples:</span></span>

<dl> <dt>

<span data-ttu-id="6750b-180"><span id="VERSION"></span><span id="version"></span>Versão</span><span class="sxs-lookup"><span data-stu-id="6750b-180"><span id="VERSION"></span><span id="version"></span>VERSION</span></span>
</dt> <dd>

<span data-ttu-id="6750b-181">A versão de especificação da linguagem.</span><span class="sxs-lookup"><span data-stu-id="6750b-181">The language specification version.</span></span> <span data-ttu-id="6750b-182">Esta variável é obrigatória.</span><span class="sxs-lookup"><span data-stu-id="6750b-182">This variable is required.</span></span>

</dd> <dt>

<span data-ttu-id="6750b-183"><span id="VERCTL"></span><span id="verctl"></span>VERCTL</span><span class="sxs-lookup"><span data-stu-id="6750b-183"><span id="VERCTL"></span><span id="verctl"></span>VERCTL</span></span>
</dt> <dd>

<span data-ttu-id="6750b-184">Uma cadeia de caracteres que descreve o produto de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6750b-184">A string that describes the source control product.</span></span> <span data-ttu-id="6750b-185">Essa variável é opcional.</span><span class="sxs-lookup"><span data-stu-id="6750b-185">This variable is optional.</span></span>

</dd> <dt>

<span data-ttu-id="6750b-186"><span id="DATETIME"></span><span id="datetime"></span>HORÁRIO</span><span class="sxs-lookup"><span data-stu-id="6750b-186"><span id="DATETIME"></span><span id="datetime"></span>DATETIME</span></span>
</dt> <dd>

<span data-ttu-id="6750b-187">Uma cadeia de caracteres que indica a data e a hora em que o arquivo PDB foi processado.</span><span class="sxs-lookup"><span data-stu-id="6750b-187">A string that indicates the date and time the PDB file was processed.</span></span> <span data-ttu-id="6750b-188">Essa variável é opcional.</span><span class="sxs-lookup"><span data-stu-id="6750b-188">This variable is optional.</span></span>

</dd> </dl>

<span data-ttu-id="6750b-189">A seção Variables contém variáveis que descrevem como extrair um arquivo do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6750b-189">The variables section contains variables that describe how to extract a file from source control.</span></span> <span data-ttu-id="6750b-190">Ele também pode ser usado para definir texto comumente usado como variáveis para reduzir o tamanho do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="6750b-190">It can also be used to define commonly used text as variables to reduce the size of the data block.</span></span>

<dl> <dt>

<span data-ttu-id="6750b-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG</span><span class="sxs-lookup"><span data-stu-id="6750b-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG</span></span>
</dt> <dd>

<span data-ttu-id="6750b-192">Descreve como criar o caminho de destino para o arquivo extraído.</span><span class="sxs-lookup"><span data-stu-id="6750b-192">Describes how to build the target path for the extracted file.</span></span> <span data-ttu-id="6750b-193">Essa é uma variável necessária.</span><span class="sxs-lookup"><span data-stu-id="6750b-193">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="6750b-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD</span><span class="sxs-lookup"><span data-stu-id="6750b-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD</span></span>
</dt> <dd>

<span data-ttu-id="6750b-195">Descreve como criar o comando para extrair o arquivo do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6750b-195">Describes how to build the command to extract the file from source control.</span></span> <span data-ttu-id="6750b-196">Isso inclui o nome do arquivo executável e seus parâmetros de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="6750b-196">This includes the name of the executable file and its command-line parameters.</span></span> <span data-ttu-id="6750b-197">Essa é uma variável necessária.</span><span class="sxs-lookup"><span data-stu-id="6750b-197">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="6750b-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV</span><span class="sxs-lookup"><span data-stu-id="6750b-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV</span></span>
</dt> <dd>

<span data-ttu-id="6750b-199">Uma cadeia de caracteres que lista as variáveis de ambiente a serem criadas durante a extração do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6750b-199">A string that lists environment variables to be created during the file extraction.</span></span> <span data-ttu-id="6750b-200">Separe várias entradas com um caractere de Backspace ( \\ b).</span><span class="sxs-lookup"><span data-stu-id="6750b-200">Separate multiple entries with a backspace character (\\b).</span></span> <span data-ttu-id="6750b-201">Essa é uma variável opcional.</span><span class="sxs-lookup"><span data-stu-id="6750b-201">This is an optional variable.</span></span>

</dd> </dl>

<span data-ttu-id="6750b-202">A seção de arquivos de origem contém uma entrada para cada arquivo de origem que foi indexado.</span><span class="sxs-lookup"><span data-stu-id="6750b-202">The source files section contains an entry for each source file that has been indexed.</span></span> <span data-ttu-id="6750b-203">O conteúdo de cada linha é interpretado como variáveis com os nomes VAR1, VAR2, VAR3 e assim por diante até VAR10.</span><span class="sxs-lookup"><span data-stu-id="6750b-203">The contents of each line are interpreted as variables with the names VAR1, VAR2, VAR3, and so on until VAR10.</span></span> <span data-ttu-id="6750b-204">As variáveis são separadas por asteriscos.</span><span class="sxs-lookup"><span data-stu-id="6750b-204">The variables are separated by asterisks.</span></span> <span data-ttu-id="6750b-205">VAR1 deve especificar o caminho totalmente qualificado para o arquivo de origem, conforme listado em outro lugar no arquivo PDB.</span><span class="sxs-lookup"><span data-stu-id="6750b-205">VAR1 must specify the fully qualified path to the source file as listed elsewhere in the PDB file.</span></span> <span data-ttu-id="6750b-206">Por exemplo, a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="6750b-206">For example, the following line:</span></span>

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

<span data-ttu-id="6750b-207">é interpretado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6750b-207">is interpreted as follows:</span></span>

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

<span data-ttu-id="6750b-208">Neste exemplo, VAR4 é um número de versão.</span><span class="sxs-lookup"><span data-stu-id="6750b-208">In this example, VAR4 is a version number.</span></span> <span data-ttu-id="6750b-209">No entanto, a maioria dos sistemas de controle do código-fonte dá suporte ao rotulamento de arquivos de forma que o estado de origem de uma determinada compilação possa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="6750b-209">However, most source control systems support labeling files in such a way that the source state for a given build can be restored.</span></span> <span data-ttu-id="6750b-210">Portanto, você poderia usar como alternativa o rótulo para a compilação.</span><span class="sxs-lookup"><span data-stu-id="6750b-210">Therefore, you could alternately use the label for the build.</span></span> <span data-ttu-id="6750b-211">O bloco de dados de exemplo pode ser modificado para conter uma variável, como a seguinte:</span><span class="sxs-lookup"><span data-stu-id="6750b-211">The sample data block could be modified to contain a variable such as the following:</span></span>

``` syntax
LABEL=BUILD47
```

<span data-ttu-id="6750b-212">Em seguida, supondo que o sistema de controle do código-fonte Use o sinal de arroba (@) para indicar um rótulo, você pode modificar a variável SRCSRVCMD da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6750b-212">Then, presuming the source control system uses the at sign (@) to indicate a label, you could modify the SRCSRVCMD variable as follows:</span></span>

<span data-ttu-id="6750b-213">**sd.exe-p% fnvar%(% var2%) impressão-o% srcsrvtrg%-q% Depot%/%var3% @% Label%**</span><span class="sxs-lookup"><span data-stu-id="6750b-213">**sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%@%label%**</span></span>

## <a name="how-source-server-works"></a><span data-ttu-id="6750b-214">Como funciona o servidor de origem</span><span class="sxs-lookup"><span data-stu-id="6750b-214">How Source Server Works</span></span>

<span data-ttu-id="6750b-215">O cliente do servidor de origem é implementado no Symsrv.dll.</span><span class="sxs-lookup"><span data-stu-id="6750b-215">The source server client is implemented in Symsrv.dll.</span></span> <span data-ttu-id="6750b-216">O cliente não extrai informações diretamente do arquivo PDB; Ele usa um manipulador de símbolo como o implementado em Dbghelp.dll.</span><span class="sxs-lookup"><span data-stu-id="6750b-216">The client does not extract information directly from the PDB file; it uses a symbol handler such as the one implemented in Dbghelp.dll.</span></span> <span data-ttu-id="6750b-217">Ele é essencialmente um mecanismo de substituição de variáveis recursiva que cria uma linha de comando que pode ser usada para extrair o arquivo de origem apropriado do sistema de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6750b-217">It is essentially a recursive variable substitution engine that creates a command line that can be used to extract the proper source file from the source control system.</span></span> <span data-ttu-id="6750b-218">Seu código não deve chamar Symsrv.dll diretamente.</span><span class="sxs-lookup"><span data-stu-id="6750b-218">Your code should not call Symsrv.dll directly.</span></span> <span data-ttu-id="6750b-219">Para integrar sua funcionalidade ao seu aplicativo, use a função [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .</span><span class="sxs-lookup"><span data-stu-id="6750b-219">To integrate its functionality into your application, use the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span>

<span data-ttu-id="6750b-220">A primeira versão do servidor de origem funciona da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="6750b-220">The first version of source server works as follows.</span></span> <span data-ttu-id="6750b-221">Esse comportamento pode ser alterado em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="6750b-221">This behavior may change in future versions.</span></span>

-   <span data-ttu-id="6750b-222">O cliente chama a função **SrcSrvInit** com o caminho de destino a ser usado como base para todas as extrações de arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="6750b-222">The client calls the **SrcSrvInit** function with the target path to be used as a base for all source file extractions.</span></span> <span data-ttu-id="6750b-223">Ele armazena esse caminho na variável Tino.</span><span class="sxs-lookup"><span data-stu-id="6750b-223">It stores this path in the TARG variable.</span></span>
-   <span data-ttu-id="6750b-224">O cliente extrai o fluxo srcsrv do PDB quando o módulo PDB é carregado e chama a função **SrcSrvLoadModule** para passar o bloco de dados para o servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="6750b-224">The client extracts the Srcsrv stream from the PDB when the module PDB is loaded and calls the **SrcSrvLoadModule** function to pass the data block to source server.</span></span>
-   <span data-ttu-id="6750b-225">Quando o dbghelp recupera um arquivo de origem, o cliente chama a função **SrcSrvGetFile** para recuperar os arquivos de origem do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6750b-225">When Dbghelp retrieves a source file, the client calls the **SrcSrvGetFile** function to retrieve the source files from source control.</span></span>
-   <span data-ttu-id="6750b-226">O servidor de origem pesquisa as entradas do arquivo de origem no bloco de dados para uma entrada que corresponda ao arquivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="6750b-226">Source server searches the source file entries in the data block for an entry that matches the requested file.</span></span> <span data-ttu-id="6750b-227">Ele preenche VAR1 para VAR *n* com o conteúdo da entrada do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="6750b-227">It fills VAR1 to VAR *n* with the contents of the source file entry.</span></span> <span data-ttu-id="6750b-228">Em seguida, ele expande a variável SRCSRVTRG usando VAR1 para VAR *n*.</span><span class="sxs-lookup"><span data-stu-id="6750b-228">Next, it expands the SRCSRVTRG variable using VAR1 to VAR *n*.</span></span> <span data-ttu-id="6750b-229">Se o arquivo já estiver nesse local, ele retornará o local para o chamador.</span><span class="sxs-lookup"><span data-stu-id="6750b-229">If the file is already in this location, it returns the location to the caller.</span></span> <span data-ttu-id="6750b-230">Caso contrário, ele expande a variável SRCSRVCMD para criar o comando necessário para recuperar o arquivo do controle do código-fonte e copiá-lo para o local de destino.</span><span class="sxs-lookup"><span data-stu-id="6750b-230">Otherwise, it expands the SRCSRVCMD variable to build the command needed to retrieve the file from source control and copy it to the target location.</span></span> <span data-ttu-id="6750b-231">Por fim, ele executa esse comando.</span><span class="sxs-lookup"><span data-stu-id="6750b-231">Finally, it executes this command.</span></span>

## <a name="creating-a-source-control-provider-module"></a><span data-ttu-id="6750b-232">Criando um módulo de provedor de controle do código-fonte</span><span class="sxs-lookup"><span data-stu-id="6750b-232">Creating a Source Control Provider Module</span></span>

<span data-ttu-id="6750b-233">O servidor de origem inclui módulos de provedor para Perforce (p4.pm) e vss.pm (segurança de código-fonte Visual).</span><span class="sxs-lookup"><span data-stu-id="6750b-233">The source server includes provider modules for Perforce (p4.pm) and Visual Source Safe (vss.pm).</span></span> <span data-ttu-id="6750b-234">Para criar seu próprio módulo de provedor, você deve implementar o seguinte conjunto de interfaces.</span><span class="sxs-lookup"><span data-stu-id="6750b-234">To create your own provider module, you must implement the following set of interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="6750b-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module:: SimpleUsage ()**</span><span class="sxs-lookup"><span data-stu-id="6750b-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module::SimpleUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="6750b-236">Finalidade: exibe informações de uso de módulo simples para STDOUT.</span><span class="sxs-lookup"><span data-stu-id="6750b-236">Purpose: Displays simple module usage information to STDOUT.</span></span>

<span data-ttu-id="6750b-237">Parâmetros: nenhum</span><span class="sxs-lookup"><span data-stu-id="6750b-237">Parameters: None</span></span>

<span data-ttu-id="6750b-238">Valor de retorno: nenhum</span><span class="sxs-lookup"><span data-stu-id="6750b-238">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="6750b-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module:: VerboseUsage ()**</span><span class="sxs-lookup"><span data-stu-id="6750b-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module::VerboseUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="6750b-240">Finalidade: exibe informações detalhadas de uso do módulo para STDOUT.</span><span class="sxs-lookup"><span data-stu-id="6750b-240">Purpose: Displays in-depth module usage information to STDOUT.</span></span>

<span data-ttu-id="6750b-241">Parâmetros: nenhum</span><span class="sxs-lookup"><span data-stu-id="6750b-241">Parameters: None</span></span>

<span data-ttu-id="6750b-242">Valor de retorno: nenhum</span><span class="sxs-lookup"><span data-stu-id="6750b-242">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="6750b-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module:: novo ( \@ CommandArguments)**</span><span class="sxs-lookup"><span data-stu-id="6750b-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module::new(\@CommandArguments)**</span></span>
</dt> <dd>

<span data-ttu-id="6750b-244">Finalidade: Inicializa uma instância do módulo do provedor.</span><span class="sxs-lookup"><span data-stu-id="6750b-244">Purpose: Initializes an instance of the provider module.</span></span>

<span data-ttu-id="6750b-245">Parâmetros: todos os @ARGV argumentos que não foram reconhecidos pelo SSIndex. cmd como argumentos gerais.</span><span class="sxs-lookup"><span data-stu-id="6750b-245">Parameters: All @ARGV arguments that were not recognized by SSIndex.cmd as being general arguments.</span></span>

<span data-ttu-id="6750b-246">Valor de retorno: uma referência que pode ser usada em operações posteriores.</span><span class="sxs-lookup"><span data-stu-id="6750b-246">Return value: A reference that can be used in later operations.</span></span>

</dd> <dt>

<span data-ttu-id="6750b-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation ($SourcePath, $ServerHashReference)**</span><span class="sxs-lookup"><span data-stu-id="6750b-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation($SourcePath, $ServerHashReference)**</span></span>
</dt> <dd>

<span data-ttu-id="6750b-248">Finalidade: habilita o módulo para coletar as informações de indexação de fonte necessárias para o diretório especificado pelo parâmetro $SourcePath.</span><span class="sxs-lookup"><span data-stu-id="6750b-248">Purpose: Enables the module to gather the required source indexing information for the directory specified by the $SourcePath parameter.</span></span> <span data-ttu-id="6750b-249">O módulo não deve pressupor que essa entrada será chamada apenas uma vez para cada instância de objeto, já que SSIndex. cmd pode chamá-la várias vezes para caminhos diferentes.</span><span class="sxs-lookup"><span data-stu-id="6750b-249">The module should not assume that this entry will be called only once for each object instance, as SSIndex.cmd may call it multiple times for different paths.</span></span>

<span data-ttu-id="6750b-250">Parâmetros: (1) o diretório local que contém a origem a ser indexada.</span><span class="sxs-lookup"><span data-stu-id="6750b-250">Parameters: (1) The local directory containing the source to be indexed.</span></span> <span data-ttu-id="6750b-251">(2) uma referência a um hash que contém todas as entradas do arquivo de Srcsrv.ini especificado.</span><span class="sxs-lookup"><span data-stu-id="6750b-251">(2) A reference to a hash containing all of the entries from the specified Srcsrv.ini file.</span></span>

<span data-ttu-id="6750b-252">Valor de retorno: nenhum</span><span class="sxs-lookup"><span data-stu-id="6750b-252">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="6750b-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo ($LocalFile)**</span><span class="sxs-lookup"><span data-stu-id="6750b-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo($LocalFile)**</span></span>
</dt> <dd>

<span data-ttu-id="6750b-254">Finalidade: fornece as informações necessárias para extrair um único arquivo específico do sistema de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6750b-254">Purpose: Provides the necessary information to extract a single, specific file from the source control system.</span></span>

<span data-ttu-id="6750b-255">Parâmetros: um nome de arquivo totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="6750b-255">Parameters: A fully qualified file name</span></span>

<span data-ttu-id="6750b-256">Valor de retorno: (1) uma referência de hash das variáveis necessárias para interpretar o $FileEntry retornado.</span><span class="sxs-lookup"><span data-stu-id="6750b-256">Return value: (1) A hash reference of the variables necessary to interpret the returned $FileEntry.</span></span> <span data-ttu-id="6750b-257">O SSIndex. cmd armazena essas variáveis em cache para cada arquivo de origem usado por um único arquivo de depuração para reduzir a quantidade de informações gravadas no fluxo do índice de origem.</span><span class="sxs-lookup"><span data-stu-id="6750b-257">SSIndex.cmd caches these variables for every source file used by a single debug file to reduce the amount of information written to the source index stream.</span></span> <span data-ttu-id="6750b-258">(2) a entrada de arquivo a ser gravada no fluxo do índice de origem para permitir que SrcSrv.dll extraia esse arquivo do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6750b-258">(2) The file entry to be written to the source index stream to allow SrcSrv.dll to extract this file from source control.</span></span> <span data-ttu-id="6750b-259">O formato exato dessa linha é específico do sistema de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6750b-259">The exact format of this line is specific to the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="6750b-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName ()**</span><span class="sxs-lookup"><span data-stu-id="6750b-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName()**</span></span>
</dt> <dd>

<span data-ttu-id="6750b-261">Finalidade: fornece uma cadeia de caracteres descritiva para identificar o provedor de controle do código-fonte para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="6750b-261">Purpose: Provides a descriptive string to identify the source control provider to the end user.</span></span>

<span data-ttu-id="6750b-262">Parâmetros: nenhum</span><span class="sxs-lookup"><span data-stu-id="6750b-262">Parameters: None</span></span>

<span data-ttu-id="6750b-263">Valor de retorno: o nome descritivo do sistema de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6750b-263">Return value: The descriptive name of the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="6750b-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables ()**</span><span class="sxs-lookup"><span data-stu-id="6750b-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables()**</span></span>
</dt> <dd>

<span data-ttu-id="6750b-265">Finalidade: habilita o provedor de controle do código-fonte a adicionar variáveis específicas de controle do código-fonte ao fluxo de origem para cada arquivo de depuração.</span><span class="sxs-lookup"><span data-stu-id="6750b-265">Purpose: Enables the source control provider to add source control specific variables to the source stream for each debug file.</span></span> <span data-ttu-id="6750b-266">Os módulos de exemplo usam esse método para gravar as variáveis de destino de extração \_ cmd e extração necessárias \_ .</span><span class="sxs-lookup"><span data-stu-id="6750b-266">The sample modules use this method for writing the required EXTRACT\_CMD and EXTRACT\_TARGET variables.</span></span>

<span data-ttu-id="6750b-267">Parâmetros: nenhum</span><span class="sxs-lookup"><span data-stu-id="6750b-267">Parameters: None</span></span>

<span data-ttu-id="6750b-268">Valor de retorno: a lista de entradas para as variáveis de fluxo de origem.</span><span class="sxs-lookup"><span data-stu-id="6750b-268">Return value: The list of entries for the source stream variables.</span></span>

</dd> </dl>

 

 




