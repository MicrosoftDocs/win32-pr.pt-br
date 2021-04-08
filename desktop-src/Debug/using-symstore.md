---
description: SymStore (symstore.exe) é uma ferramenta para a criação de armazenamentos de símbolo. Ele está incluído no pacote de ferramentas de depuração para Windows.
ms.assetid: fe8a96e9-e780-4e96-98ef-c5128515ee6c
title: Usando SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a87b5c527717d78adb9202fd1eddd54d1f44c02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089209"
---
# <a name="using-symstore"></a><span data-ttu-id="7b316-104">Usando SymStore</span><span class="sxs-lookup"><span data-stu-id="7b316-104">Using SymStore</span></span>

<span data-ttu-id="7b316-105">SymStore (symstore.exe) é uma ferramenta para a criação de armazenamentos de símbolo.</span><span class="sxs-lookup"><span data-stu-id="7b316-105">SymStore (symstore.exe) is a tool for creating symbol stores.</span></span> <span data-ttu-id="7b316-106">Ele está incluído no pacote de [ferramentas de depuração para Windows](https://www.microsoft.com/?ref=go) .</span><span class="sxs-lookup"><span data-stu-id="7b316-106">It is included in the [Debugging Tools for Windows](https://www.microsoft.com/?ref=go) package.</span></span>

<span data-ttu-id="7b316-107">O SymStore armazena símbolos em um formato que permite ao depurador pesquisar os símbolos com base no carimbo de data/hora e no tamanho da imagem (para um arquivo. dbg ou executável), ou assinatura e idade (para um arquivo. pdb).</span><span class="sxs-lookup"><span data-stu-id="7b316-107">SymStore stores symbols in a format that enables the debugger to look up the symbols based on the time stamp and size of the image (for a .dbg or executable file), or signature and age (for a .pdb file).</span></span> <span data-ttu-id="7b316-108">A vantagem do armazenamento de símbolos sobre o formato de armazenamento de símbolo tradicional é que todos os símbolos podem ser armazenados ou referenciados no mesmo servidor e recuperados pelo depurador sem qualquer conhecimento prévio de qual produto contém o símbolo correspondente.</span><span class="sxs-lookup"><span data-stu-id="7b316-108">The advantage of the symbol store over the traditional symbol storage format is that all symbols can be stored or referenced on the same server and retrieved by the debugger without any prior knowledge of which product contains the corresponding symbol.</span></span>

<span data-ttu-id="7b316-109">Observe que várias versões de arquivos de símbolo. PDB (por exemplo, versões públicas e privadas) não podem ser armazenadas no mesmo servidor, pois cada uma delas contém a mesma assinatura e idade.</span><span class="sxs-lookup"><span data-stu-id="7b316-109">Note that multiple versions of .pdb symbol files (for example, public and private versions) cannot be stored on the same server, because they each contain the same signature and age.</span></span>

## <a name="symstore-transactions"></a><span data-ttu-id="7b316-110">Transações de SymStore</span><span class="sxs-lookup"><span data-stu-id="7b316-110">SymStore Transactions</span></span>

<span data-ttu-id="7b316-111">Cada chamada para SymStore é registrada como uma transação.</span><span class="sxs-lookup"><span data-stu-id="7b316-111">Every call to SymStore is recorded as a transaction.</span></span> <span data-ttu-id="7b316-112">Há dois tipos de transações: Adicionar e excluir.</span><span class="sxs-lookup"><span data-stu-id="7b316-112">There are two types of transactions: add and delete.</span></span>

<span data-ttu-id="7b316-113">Quando o armazenamento de símbolo é criado, um diretório, chamado "000admin", é criado sob a raiz do servidor.</span><span class="sxs-lookup"><span data-stu-id="7b316-113">When the symbol store is created, a directory, called "000admin", is created under the root of the server.</span></span> <span data-ttu-id="7b316-114">O diretório 000admin contém um arquivo para cada transação, bem como os arquivos de log Server.txt e History.txt.</span><span class="sxs-lookup"><span data-stu-id="7b316-114">The 000admin directory contains one file for each transaction, as well as the log files Server.txt and History.txt.</span></span> <span data-ttu-id="7b316-115">O arquivo de Server.txt contém uma lista de todas as transações que estão atualmente no servidor.</span><span class="sxs-lookup"><span data-stu-id="7b316-115">The Server.txt file contains a list of all transactions that are currently on the server.</span></span> <span data-ttu-id="7b316-116">O arquivo de History.txt contém um histórico cronológico de todas as transações.</span><span class="sxs-lookup"><span data-stu-id="7b316-116">The History.txt file contains a chronological history of all transactions.</span></span>

<span data-ttu-id="7b316-117">Cada vez que o SymStore armazena ou remove arquivos de símbolo, um novo número de transação é criado.</span><span class="sxs-lookup"><span data-stu-id="7b316-117">Each time SymStore stores or removes symbol files, a new transaction number is created.</span></span> <span data-ttu-id="7b316-118">Em seguida, um arquivo, cujo nome é esse número de transação, é criado em 000admin.</span><span class="sxs-lookup"><span data-stu-id="7b316-118">Then, a file, whose name is this transaction number, is created in 000admin.</span></span> <span data-ttu-id="7b316-119">Esse arquivo contém uma lista de todos os arquivos ou ponteiros que foram adicionados ao repositório de símbolos durante essa transação.</span><span class="sxs-lookup"><span data-stu-id="7b316-119">This file contains a list of all the files or pointers that have been added to the symbol store during this transaction.</span></span> <span data-ttu-id="7b316-120">Se uma transação for excluída, o SymStore lerá seu arquivo de transação para determinar quais arquivos e ponteiros devem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="7b316-120">If a transaction is deleted, SymStore will read through its transaction file to determine which files and pointers it should delete.</span></span>

<span data-ttu-id="7b316-121">As opções **Adicionar** e **del** especificam se uma transação Adicionar ou excluir deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="7b316-121">The **add** and **del** options specify whether an add or delete transaction is to be performed.</span></span> <span data-ttu-id="7b316-122">Incluir a opção **/p** com uma operação de adição especifica que um ponteiro deve ser adicionado; omitir a opção **/p** especifica que o arquivo de símbolo real deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="7b316-122">Including the **/p** option with an add operation specifies that a pointer is to be added; omitting the **/p** option specifies that the actual symbol file is to be added.</span></span>

<span data-ttu-id="7b316-123">Também é possível criar o armazenamento de símbolo em dois estágios separados.</span><span class="sxs-lookup"><span data-stu-id="7b316-123">It is also possible to create the symbol store in two separate stages.</span></span> <span data-ttu-id="7b316-124">No primeiro estágio, você usa SymStore com a opção **/x** para criar um arquivo de índice.</span><span class="sxs-lookup"><span data-stu-id="7b316-124">In the first stage, you use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="7b316-125">No segundo estágio, você usa SymStore com a opção **/y** para criar o armazenamento real de arquivos ou ponteiros a partir das informações no arquivo de índice.</span><span class="sxs-lookup"><span data-stu-id="7b316-125">In the second stage, you use SymStore with the **/y** option to create the actual store of files or pointers from the information in the index file.</span></span>

<span data-ttu-id="7b316-126">Isso pode ser uma técnica útil por vários motivos.</span><span class="sxs-lookup"><span data-stu-id="7b316-126">This can be a useful technique for a variety of reasons.</span></span> <span data-ttu-id="7b316-127">Por exemplo, isso permite que o armazenamento de símbolos seja recriado facilmente se o armazenamento estiver de alguma forma perdida, desde que o arquivo de índice ainda exista.</span><span class="sxs-lookup"><span data-stu-id="7b316-127">For instance, this allows the symbol store to be easily recreated if the store is somehow lost, as long as the index file still exists.</span></span> <span data-ttu-id="7b316-128">Ou talvez o computador que contém os arquivos de símbolo tenha uma conexão de rede lenta com o computador no qual o armazenamento de símbolo será criado.</span><span class="sxs-lookup"><span data-stu-id="7b316-128">Or perhaps the computer containing the symbol files has a slow network connection to the computer on which the symbol store will be created.</span></span> <span data-ttu-id="7b316-129">Nesse caso, você pode criar o arquivo de índice no mesmo computador que os arquivos de símbolo, transferir o arquivo de índice para o segundo computador e, em seguida, criar o armazenamento no segundo computador.</span><span class="sxs-lookup"><span data-stu-id="7b316-129">In this case, you can create the index file on the same machine as the symbol files, transfer the index file to the second machine, and then create the store on the second machine.</span></span>

<span data-ttu-id="7b316-130">Para obter uma lista completa de todos os parâmetros de SymStore, consulte [Opções de Command-Line de SymStore](symstore-command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="7b316-130">For a full listing of all SymStore parameters, see [SymStore Command-Line Options](symstore-command-line-options.md).</span></span>

> [!Note]  
> <span data-ttu-id="7b316-131">SymStore não oferece suporte a transações simultâneas de vários usuários.</span><span class="sxs-lookup"><span data-stu-id="7b316-131">SymStore does not support simultaneous transactions from multiple users.</span></span> <span data-ttu-id="7b316-132">É recomendável que um usuário seja designado como "administrador" do repositório de símbolos e seja responsável por todas as transações de **adição** e de **del** .</span><span class="sxs-lookup"><span data-stu-id="7b316-132">It is recommended that one user be designated "administrator" of the symbol store and be responsible for all **add** and **del** transactions.</span></span>

 

## <a name="transaction-examples"></a><span data-ttu-id="7b316-133">Exemplos de transação</span><span class="sxs-lookup"><span data-stu-id="7b316-133">Transaction Examples</span></span>

<span data-ttu-id="7b316-134">Aqui estão dois exemplos de SymStore que adicionam ponteiros de símbolo para a compilação 3790 do Windows Server 2003 a \\ \\ SampleDir \\ symsrv:</span><span class="sxs-lookup"><span data-stu-id="7b316-134">Here are two examples of SymStore adding symbol pointers for build 3790 of Windows Server 2003 to \\\\sampledir\\symsrv:</span></span>

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

<span data-ttu-id="7b316-135">No exemplo a seguir, SymStore adiciona os arquivos de símbolo reais para um projeto de aplicativo em \\ \\ compartimentos do largeapp do \\ AppServer \\ a \\ \\ TestDir \\ symsrv:</span><span class="sxs-lookup"><span data-stu-id="7b316-135">In the following example, SymStore adds the actual symbol files for an application project in \\\\largeapp\\appserver\\bins to \\\\testdir\\symsrv:</span></span>

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

<span data-ttu-id="7b316-136">Aqui está um exemplo de como um arquivo de índice é usado.</span><span class="sxs-lookup"><span data-stu-id="7b316-136">Here is an example of how an index file is used.</span></span> <span data-ttu-id="7b316-137">Primeiro, o SymStore cria um arquivo de índice baseado na coleção de arquivos de símbolo em \\ \\ compartimentos do largeapp do \\ AppServer \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="7b316-137">First, SymStore creates an index file based on the collection of symbol files in \\\\largeapp\\appserver\\bins\\.</span></span> <span data-ttu-id="7b316-138">Nesse caso, o arquivo de índice é colocado em um terceiro computador, \\ \\ hubserver \\ hubshare.</span><span class="sxs-lookup"><span data-stu-id="7b316-138">In this case, the index file is placed on a third computer, \\\\hubserver\\hubshare.</span></span> <span data-ttu-id="7b316-139">Você usa a opção **/g** para especificar que o prefixo do arquivo " \\ \\ largeapp \\ AppServer" pode ser alterado no futuro:</span><span class="sxs-lookup"><span data-stu-id="7b316-139">You use the **/g** option to specify that the file prefix "\\\\largeapp\\appserver" might change in the future:</span></span>

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

<span data-ttu-id="7b316-140">Agora suponha que você mova todos os arquivos de símbolo do computador \\ \\ largeapp \\ AppServer e coloque-os em \\ \\ myarchive \\ AppServer.</span><span class="sxs-lookup"><span data-stu-id="7b316-140">Now suppose you move all the symbol files off of the machine \\\\largeapp\\appserver and put them on \\\\myarchive\\appserver.</span></span> <span data-ttu-id="7b316-141">Em seguida, você pode criar o próprio armazenamento de símbolo no arquivo de índice \\ \\ hubserver \\ hubshare \\myindex.txt da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7b316-141">You can then create the symbol store itself from the index file \\\\hubserver\\hubshare\\myindex.txt as follows:</span></span>

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

<span data-ttu-id="7b316-142">Por fim, aqui está um exemplo de SymStore excluindo um arquivo adicionado por uma transação anterior.</span><span class="sxs-lookup"><span data-stu-id="7b316-142">Finally, here is an example of SymStore deleting a file added by a previous transaction.</span></span> <span data-ttu-id="7b316-143">Consulte a seção a seguir para obter uma explicação de como determinar a ID da transação (nesse caso, 0000000096).</span><span class="sxs-lookup"><span data-stu-id="7b316-143">See the following section for an explanation of how to determine the transaction ID (in this case, 0000000096).</span></span>

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a><span data-ttu-id="7b316-144">Arquivos compactados</span><span class="sxs-lookup"><span data-stu-id="7b316-144">Compressed Files</span></span>

<span data-ttu-id="7b316-145">SymStore pode ser usado com arquivos compactados de duas maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="7b316-145">SymStore can be used with compressed files in two different ways.</span></span>

1.  <span data-ttu-id="7b316-146">Use SymStore com a opção **/p** para armazenar ponteiros para os arquivos de símbolo.</span><span class="sxs-lookup"><span data-stu-id="7b316-146">Use SymStore with the **/p** option to store pointers to the symbol files.</span></span> <span data-ttu-id="7b316-147">Após a conclusão do SymStore, compacte os arquivos aos quais os ponteiros se referem.</span><span class="sxs-lookup"><span data-stu-id="7b316-147">After SymStore finishes, compress the files that the pointers refer to.</span></span>
2.  <span data-ttu-id="7b316-148">Use SymStore com a opção **/x** para criar um arquivo de índice.</span><span class="sxs-lookup"><span data-stu-id="7b316-148">Use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="7b316-149">Após a conclusão do SymStore, compacte os arquivos listados no arquivo de índice.</span><span class="sxs-lookup"><span data-stu-id="7b316-149">After SymStore finishes, compress the files listed in the index file.</span></span> <span data-ttu-id="7b316-150">Em seguida, use SymStore com a opção **/y** (e, se desejar, a opção **/p** ) para armazenar os arquivos ou ponteiros para os arquivos no repositório de símbolos.</span><span class="sxs-lookup"><span data-stu-id="7b316-150">Then use SymStore with the **/y** option (and, if you wish, the **/p** option) to store the files or pointers to the files in the symbol store.</span></span> <span data-ttu-id="7b316-151">(O SymStore não precisará descompactar os arquivos para executar esta operação.)</span><span class="sxs-lookup"><span data-stu-id="7b316-151">(SymStore will not need to uncompress the files to perform this operation.)</span></span>

<span data-ttu-id="7b316-152">O servidor de símbolos será responsável por descompactar os arquivos quando forem necessários.</span><span class="sxs-lookup"><span data-stu-id="7b316-152">Your symbol server will be responsible for uncompressing the files when they are needed.</span></span>

<span data-ttu-id="7b316-153">Se você estiver usando o SymSrv como seu servidor de símbolos, qualquer compactação deverá ser feita usando a ferramenta compress.exe que é distribuída com o SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7b316-153">If you are using SymSrv as your symbol server, any compression should be done using the compress.exe tool that is distributed with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7b316-154">Arquivos compactados devem ter um sublinhado como o último caractere em suas extensões de arquivo (por exemplo, Module1. PD \_ ou Module2. db \_ ).</span><span class="sxs-lookup"><span data-stu-id="7b316-154">Compressed files should have an underscore as the last character in their file extensions (for example, module1.pd\_ or module2.db\_).</span></span> <span data-ttu-id="7b316-155">Para obter detalhes, consulte [usando symsrv](using-symsrv.md).</span><span class="sxs-lookup"><span data-stu-id="7b316-155">For details, see [Using SymSrv](using-symsrv.md).</span></span>

## <a name="the-servertxt-and-historytxt-files"></a><span data-ttu-id="7b316-156">Os arquivos de server.txt e history.txt</span><span class="sxs-lookup"><span data-stu-id="7b316-156">The server.txt and history.txt Files</span></span>

<span data-ttu-id="7b316-157">Quando uma transação é adicionada, vários itens de informações são adicionados a server.txt e history.txt para a funcionalidade de pesquisa futura.</span><span class="sxs-lookup"><span data-stu-id="7b316-157">When a transaction is added, several items of information are added to server.txt and history.txt for future lookup capability.</span></span> <span data-ttu-id="7b316-158">Veja a seguir um exemplo de uma linha em server.txt e history.txt para uma transação de adição:</span><span class="sxs-lookup"><span data-stu-id="7b316-158">The following is an example of a line in server.txt and history.txt for an add transaction:</span></span>

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

<span data-ttu-id="7b316-159">Esta é uma linha separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="7b316-159">This is a comma-separated line.</span></span> <span data-ttu-id="7b316-160">Os campos são definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="7b316-160">The fields are defined as follows.</span></span>



| <span data-ttu-id="7b316-161">Campo</span><span class="sxs-lookup"><span data-stu-id="7b316-161">Field</span></span>      | <span data-ttu-id="7b316-162">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b316-162">Description</span></span>                                                                         |
|------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7b316-163">0000000096</span><span class="sxs-lookup"><span data-stu-id="7b316-163">0000000096</span></span> | <span data-ttu-id="7b316-164">Número da ID da transação, conforme criado por SymStore.</span><span class="sxs-lookup"><span data-stu-id="7b316-164">Transaction ID number, as created by SymStore.</span></span>                                      |
| <span data-ttu-id="7b316-165">add</span><span class="sxs-lookup"><span data-stu-id="7b316-165">add</span></span>        | <span data-ttu-id="7b316-166">Tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="7b316-166">Type of transaction.</span></span> <span data-ttu-id="7b316-167">Esse campo pode ser **Add** ou **del**.</span><span class="sxs-lookup"><span data-stu-id="7b316-167">This field can be either **add** or **del**.</span></span>                   |
| <span data-ttu-id="7b316-168">ptr</span><span class="sxs-lookup"><span data-stu-id="7b316-168">ptr</span></span>        | <span data-ttu-id="7b316-169">Se os arquivos ou ponteiros foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="7b316-169">Whether files or pointers were added.</span></span> <span data-ttu-id="7b316-170">Esse campo pode ser um **arquivo** ou um **PTR**.</span><span class="sxs-lookup"><span data-stu-id="7b316-170">This field can be either **file** or **ptr**.</span></span> |
| <span data-ttu-id="7b316-171">10/09/99</span><span class="sxs-lookup"><span data-stu-id="7b316-171">10/09/99</span></span>   | <span data-ttu-id="7b316-172">Data em que a transação ocorreu.</span><span class="sxs-lookup"><span data-stu-id="7b316-172">Date when transaction occurred.</span></span>                                                     |
| <span data-ttu-id="7b316-173">00:08:32</span><span class="sxs-lookup"><span data-stu-id="7b316-173">00:08:32</span></span>   | <span data-ttu-id="7b316-174">Hora em que a transação foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="7b316-174">Time when transaction started.</span></span>                                                      |
| <span data-ttu-id="7b316-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7b316-175">Windows XP</span></span> | <span data-ttu-id="7b316-176">Produto.</span><span class="sxs-lookup"><span data-stu-id="7b316-176">Product.</span></span>                                                                            |
| <span data-ttu-id="7b316-177">fre x86</span><span class="sxs-lookup"><span data-stu-id="7b316-177">x86 fre</span></span>    | <span data-ttu-id="7b316-178">Versão (opcional).</span><span class="sxs-lookup"><span data-stu-id="7b316-178">Version (optional).</span></span>                                                                 |
| <span data-ttu-id="7b316-179">Adicionado de</span><span class="sxs-lookup"><span data-stu-id="7b316-179">Added from</span></span> | <span data-ttu-id="7b316-180">Comentário (opcional)</span><span class="sxs-lookup"><span data-stu-id="7b316-180">Comment (optional)</span></span>                                                                  |
| <span data-ttu-id="7b316-181">Não usado</span><span class="sxs-lookup"><span data-stu-id="7b316-181">Unused</span></span>     | <span data-ttu-id="7b316-182">(Reservado para uso posterior.)</span><span class="sxs-lookup"><span data-stu-id="7b316-182">(Reserved for later use.)</span></span>                                                           |



 

<span data-ttu-id="7b316-183">Aqui estão algumas linhas de exemplo do arquivo de transação 0000000096.</span><span class="sxs-lookup"><span data-stu-id="7b316-183">Here are some sample lines from the transaction file 0000000096.</span></span> <span data-ttu-id="7b316-184">Cada linha registra o diretório e o local do arquivo ou ponteiro que foi adicionado ao diretório.</span><span class="sxs-lookup"><span data-stu-id="7b316-184">Each line records the directory and the location of the file or pointer that was added to the directory.</span></span>

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

<span data-ttu-id="7b316-185">Se você usar uma transação **del** para desfazer as transações de **adição** originais, essas linhas serão removidas do server.txt e a linha a seguir será adicionada ao history.txt:</span><span class="sxs-lookup"><span data-stu-id="7b316-185">If you use a **del** transaction to undo the original **add** transactions, these lines will be removed from server.txt, and the following line will be added to history.txt:</span></span>

``` syntax
0000000105,del,0000000096
```

<span data-ttu-id="7b316-186">Os campos para a transação de exclusão são definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="7b316-186">The fields for the delete transaction are defined as follows.</span></span>



| <span data-ttu-id="7b316-187">Campo</span><span class="sxs-lookup"><span data-stu-id="7b316-187">Field</span></span>      | <span data-ttu-id="7b316-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b316-188">Description</span></span>                                                       |
|------------|-------------------------------------------------------------------|
| <span data-ttu-id="7b316-189">0000000105</span><span class="sxs-lookup"><span data-stu-id="7b316-189">0000000105</span></span> | <span data-ttu-id="7b316-190">Número da ID da transação, conforme criado por SymStore.</span><span class="sxs-lookup"><span data-stu-id="7b316-190">Transaction ID number, as created by SymStore.</span></span>                    |
| <span data-ttu-id="7b316-191">del</span><span class="sxs-lookup"><span data-stu-id="7b316-191">del</span></span>        | <span data-ttu-id="7b316-192">Tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="7b316-192">Type of transaction.</span></span> <span data-ttu-id="7b316-193">Esse campo pode ser **Add** ou **del**.</span><span class="sxs-lookup"><span data-stu-id="7b316-193">This field can be either **add** or **del**.</span></span> |
| <span data-ttu-id="7b316-194">0000000096</span><span class="sxs-lookup"><span data-stu-id="7b316-194">0000000096</span></span> | <span data-ttu-id="7b316-195">Transação excluída.</span><span class="sxs-lookup"><span data-stu-id="7b316-195">Transaction that was deleted.</span></span>                                     |



 

## <a name="symbol-storage-format"></a><span data-ttu-id="7b316-196">Formato de armazenamento de símbolo</span><span class="sxs-lookup"><span data-stu-id="7b316-196">Symbol Storage Format</span></span>

<span data-ttu-id="7b316-197">O SymStore usa o próprio sistema de arquivos como um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7b316-197">SymStore uses the file system itself as a database.</span></span> <span data-ttu-id="7b316-198">Ele cria uma árvore grande de diretórios, com nomes de diretório baseados em coisas como carimbos de data/hora de arquivo de símbolo, assinaturas, idade e outros dados.</span><span class="sxs-lookup"><span data-stu-id="7b316-198">It creates a large tree of directories, with directory names based on such things as the symbol file time stamps, signatures, age, and other data.</span></span>

<span data-ttu-id="7b316-199">Por exemplo, depois que vários arquivos ACPI. dbg diferentes tiverem sido adicionados ao servidor, os diretórios poderão ter esta aparência:</span><span class="sxs-lookup"><span data-stu-id="7b316-199">For example, after several different acpi.dbg files have been added to the server, the directories could look like this:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\acpi.dbg
10/06/1999  05:46p      <DIR>          .
10/06/1999  05:46p      <DIR>          ..
10/04/1999  01:54p      <DIR>          37cdb03962040
10/04/1999  01:49p      <DIR>          37cdb04027740
10/04/1999  12:56p      <DIR>          37e3eb1c62060
10/04/1999  12:51p      <DIR>          37e3ebcc27760
10/04/1999  12:45p      <DIR>          37ed151662060
10/04/1999  12:39p      <DIR>          37ed15dd27760
10/04/1999  11:33a      <DIR>          37f03ce962020
10/04/1999  11:21a      <DIR>          37f03cf7277c0
10/06/1999  05:38p      <DIR>          37fa7f00277e0
10/06/1999  05:46p      <DIR>          37fa7f01620a0
```

<span data-ttu-id="7b316-200">Neste exemplo, o caminho de pesquisa para o arquivo de símbolo ACPI. dbg pode ser semelhante a este: \\ \\ mycompilations \\ symsrv \\ ACPI. dbg \\ 37cdb03962040.</span><span class="sxs-lookup"><span data-stu-id="7b316-200">In this example, the lookup path for the acpi.dbg symbol file might look something like this: \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040.</span></span>

<span data-ttu-id="7b316-201">Três arquivos podem existir dentro do diretório de pesquisa:</span><span class="sxs-lookup"><span data-stu-id="7b316-201">Three files may exist inside the lookup directory:</span></span>

1.  <span data-ttu-id="7b316-202">Se o arquivo foi armazenado, o ACPI. dbg existirá lá.</span><span class="sxs-lookup"><span data-stu-id="7b316-202">If the file was stored, then acpi.dbg will exist there.</span></span>
2.  <span data-ttu-id="7b316-203">Se um ponteiro foi armazenado, um arquivo chamado file. PTR existirá e conterá o caminho para o arquivo de símbolo real.</span><span class="sxs-lookup"><span data-stu-id="7b316-203">If a pointer was stored, then a file called file.ptr will exist and contain the path to the actual symbol file.</span></span>
3.  <span data-ttu-id="7b316-204">Um arquivo chamado refs. PTR, que contém uma lista de todos os locais atuais para ACPI. dbg com esse carimbo de data e hora e tamanho da imagem que são atualmente adicionados ao repositório de símbolos.</span><span class="sxs-lookup"><span data-stu-id="7b316-204">A file called refs.ptr, which contains a list of all the current locations for acpi.dbg with this timestamp and image size that are currently added to the symbol store.</span></span>

<span data-ttu-id="7b316-205">Exibindo a listagem de diretórios de \\ \\ mybuilds \\ symsrv \\ ACPI. dbg \\ 37cdb03962040 fornece o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7b316-205">Displaying the directory listing of \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040 gives the following:</span></span>

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

<span data-ttu-id="7b316-206">O arquivo file. PTR contém a cadeia de texto " \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ Sys \\ ACPI. dbg".</span><span class="sxs-lookup"><span data-stu-id="7b316-206">The file file.ptr contains the text string "\\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg".</span></span> <span data-ttu-id="7b316-207">Como não há nenhum arquivo chamado ACPI. dbg nesse diretório, o depurador tentará localizar o arquivo em \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ Sys \\ ACPI. dbg.</span><span class="sxs-lookup"><span data-stu-id="7b316-207">Since there is no file called acpi.dbg in this directory, the debugger will try to find the file at \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg.</span></span>

<span data-ttu-id="7b316-208">O conteúdo de refs. ptr é usado somente por SymStore, não pelo depurador.</span><span class="sxs-lookup"><span data-stu-id="7b316-208">The contents of refs.ptr are used only by SymStore, not the debugger.</span></span> <span data-ttu-id="7b316-209">Esse arquivo contém um registro de todas as transações realizadas neste diretório.</span><span class="sxs-lookup"><span data-stu-id="7b316-209">This file contains a record of all transactions that have taken place in this directory.</span></span> <span data-ttu-id="7b316-210">Uma linha de exemplo de refs. PTR pode ser:</span><span class="sxs-lookup"><span data-stu-id="7b316-210">A sample line from refs.ptr might be:</span></span>

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

<span data-ttu-id="7b316-211">Isso mostra que um ponteiro para \\ \\ mycompile \\ símbolos \\ x86 \\ 2128. chk \\ Symbols \\ Sys \\ ACPI. DBG foi adicionado com a transação "0000000026".</span><span class="sxs-lookup"><span data-stu-id="7b316-211">This shows that a pointer to \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg was added with transaction "0000000026".</span></span>

<span data-ttu-id="7b316-212">Alguns arquivos de símbolos permanecem constantes por meio de vários produtos ou compilações ou um produto específico.</span><span class="sxs-lookup"><span data-stu-id="7b316-212">Some symbol files stay constant through various products or builds or a particular product.</span></span> <span data-ttu-id="7b316-213">Um exemplo disso é o arquivo Msvcrt. pdb.</span><span class="sxs-lookup"><span data-stu-id="7b316-213">One example of this is the file msvcrt.pdb.</span></span> <span data-ttu-id="7b316-214">Fazer um diretório de \\ \\ mybuilds \\ symsrv \\ msvcrt. pdb mostra que apenas duas versões do msvcrt. pdb foram adicionadas ao servidor de símbolos:</span><span class="sxs-lookup"><span data-stu-id="7b316-214">Doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb shows that only two versions of msvcrt.pdb have been added to the symbols server:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

<span data-ttu-id="7b316-215">No entanto, fazer um diretório de \\ \\ mybuilds \\ symsrv \\ msvcrt. pdb \\ 37a8f40e2 mostra que refs. PTR tem vários ponteiros.</span><span class="sxs-lookup"><span data-stu-id="7b316-215">However, doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2 shows that refs.ptr has several pointers in it.</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

<span data-ttu-id="7b316-216">O conteúdo de \\ \\ mycompilations \\ symsrv \\ msvcrt. pdb \\ 37a8f40e2 \\ refs. ptr é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7b316-216">The contents of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2\\refs.ptr are the following:</span></span>

``` syntax
0000000001,ptr,\\mybuilds\symbols\x86\2137\symbols\dll\msvcrt.pdb
0000000002,ptr,\\mybuilds\symbols\x86\2137.chk\symbols\dll\msvcrt.pdb
0000000003,ptr,\\mybuilds\symbols\x86\2138\symbols\dll\msvcrt.pdb
0000000004,ptr,\\mybuilds\symbols\x86\2138.chk\symbols\dll\msvcrt.pdb
0000000005,ptr,\\mybuilds\symbols\x86\2139\symbols\dll\msvcrt.pdb
0000000006,ptr,\\mybuilds\symbols\x86\2139.chk\symbols\dll\msvcrt.pdb
0000000007,ptr,\\mybuilds\symbols\x86\2140\symbols\dll\msvcrt.pdb
0000000008,ptr,\\mybuilds\symbols\x86\2140.chk\symbols\dll\msvcrt.pdb
0000000009,ptr,\\mybuilds\symbols\x86\2136\symbols\dll\msvcrt.pdb
0000000010,ptr,\\mybuilds\symbols\x86\2136.chk\symbols\dll\msvcrt.pdb
0000000011,ptr,\\mybuilds\symbols\x86\2135\symbols\dll\msvcrt.pdb
0000000012,ptr,\\mybuilds\symbols\x86\2135.chk\symbols\dll\msvcrt.pdb
0000000013,ptr,\\mybuilds\symbols\x86\2134\symbols\dll\msvcrt.pdb
0000000014,ptr,\\mybuilds\symbols\x86\2134.chk\symbols\dll\msvcrt.pdb
0000000015,ptr,\\mybuilds\symbols\x86\2133\symbols\dll\msvcrt.pdb
0000000016,ptr,\\mybuilds\symbols\x86\2133.chk\symbols\dll\msvcrt.pdb
0000000017,ptr,\\mybuilds\symbols\x86\2132\symbols\dll\msvcrt.pdb
0000000018,ptr,\\mybuilds\symbols\x86\2132.chk\symbols\dll\msvcrt.pdb
0000000019,ptr,\\mybuilds\symbols\x86\2131\symbols\dll\msvcrt.pdb
0000000020,ptr,\\mybuilds\symbols\x86\2131.chk\symbols\dll\msvcrt.pdb
0000000021,ptr,\\mybuilds\symbols\x86\2130\symbols\dll\msvcrt.pdb
0000000022,ptr,\\mybuilds\symbols\x86\2130.chk\symbols\dll\msvcrt.pdb
0000000023,ptr,\\mybuilds\symbols\x86\2129\symbols\dll\msvcrt.pdb
0000000024,ptr,\\mybuilds\symbols\x86\2129.chk\symbols\dll\msvcrt.pdb
0000000025,ptr,\\mybuilds\symbols\x86\2128\symbols\dll\msvcrt.pdb
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\dll\msvcrt.pdb
0000000027,ptr,\\mybuilds\symbols\x86\2141\symbols\dll\msvcrt.pdb
0000000028,ptr,\\mybuilds\symbols\x86\2141.chk\symbols\dll\msvcrt.pdb
0000000029,ptr,\\mybuilds\symbols\x86\2142\symbols\dll\msvcrt.pdb
0000000030,ptr,\\mybuilds\symbols\x86\2142.chk\symbols\dll\msvcrt.pdb
```

<span data-ttu-id="7b316-217">Isso mostra que o mesmo msvcrt. pdb foi usado para várias compilações de símbolos armazenadas em \\ \\ mycompilações \\ symsrv.</span><span class="sxs-lookup"><span data-stu-id="7b316-217">This shows that the same msvcrt.pdb was used for multiple builds of symbols stored on \\\\mybuilds\\symsrv.</span></span>

<span data-ttu-id="7b316-218">Aqui está um exemplo de um diretório que contém uma mistura de adições de arquivo e ponteiro:</span><span class="sxs-lookup"><span data-stu-id="7b316-218">Here is an example of a directory that contains a mixture of file and pointer additions:</span></span>

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

<span data-ttu-id="7b316-219">Nesse caso, refs. PTR tem o seguinte conteúdo:</span><span class="sxs-lookup"><span data-stu-id="7b316-219">In this case, refs.ptr has the following contents:</span></span>

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="7b316-220">Assim, as transações 43, 44 e 45 adicionaram o mesmo arquivo ao servidor e transações 46 e 47 ponteiros adicionados.</span><span class="sxs-lookup"><span data-stu-id="7b316-220">Thus, transactions 43, 44, and 45 added the same file to the server, and transactions 46 and 47 added pointers.</span></span> <span data-ttu-id="7b316-221">Se as transações 43, 44 e 45 forem excluídas, o arquivo dbghelp. dbg será excluído do diretório.</span><span class="sxs-lookup"><span data-stu-id="7b316-221">If transactions 43, 44, and 45 are deleted, then the file dbghelp.dbg will be deleted from the directory.</span></span> <span data-ttu-id="7b316-222">O diretório terá o seguinte conteúdo:</span><span class="sxs-lookup"><span data-stu-id="7b316-222">The directory will then have the following contents:</span></span>

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

<span data-ttu-id="7b316-223">Now File. PTR contém " \\ \\ sampledir2 \\ bin \\ Symbols \\ Retail \\ dll \\ dbghelp. dbg" e refs. PTR contém</span><span class="sxs-lookup"><span data-stu-id="7b316-223">Now file.ptr contains "\\\\sampledir2\\bin\\symbols\\retail\\dll\\dbghelp.dbg", and refs.ptr contains</span></span>

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="7b316-224">Sempre que a entrada final em refs. PTR for um ponteiro, o arquivo. PTR existirá e conterá o caminho para o arquivo associado.</span><span class="sxs-lookup"><span data-stu-id="7b316-224">Whenever the final entry in refs.ptr is a pointer, the file file.ptr will exist and contain the path to the associated file.</span></span> <span data-ttu-id="7b316-225">Sempre que a entrada final em refs. PTR for um arquivo, nenhum arquivo. PTR existirá nesse diretório.</span><span class="sxs-lookup"><span data-stu-id="7b316-225">Whenever the final entry in refs.ptr is a file, no file.ptr will exist in this directory.</span></span> <span data-ttu-id="7b316-226">Portanto, qualquer operação de exclusão que remova a entrada final em refs. PTR pode resultar em File. PTR sendo criado, excluído ou alterado.</span><span class="sxs-lookup"><span data-stu-id="7b316-226">Therefore, any delete operation that removes the final entry in refs.ptr may result in file.ptr being created, deleted, or changed.</span></span>

 

 



