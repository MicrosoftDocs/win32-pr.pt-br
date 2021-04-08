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
# <a name="using-symstore"></a>Usando SymStore

SymStore (symstore.exe) é uma ferramenta para a criação de armazenamentos de símbolo. Ele está incluído no pacote de [ferramentas de depuração para Windows](https://www.microsoft.com/?ref=go) .

O SymStore armazena símbolos em um formato que permite ao depurador pesquisar os símbolos com base no carimbo de data/hora e no tamanho da imagem (para um arquivo. dbg ou executável), ou assinatura e idade (para um arquivo. pdb). A vantagem do armazenamento de símbolos sobre o formato de armazenamento de símbolo tradicional é que todos os símbolos podem ser armazenados ou referenciados no mesmo servidor e recuperados pelo depurador sem qualquer conhecimento prévio de qual produto contém o símbolo correspondente.

Observe que várias versões de arquivos de símbolo. PDB (por exemplo, versões públicas e privadas) não podem ser armazenadas no mesmo servidor, pois cada uma delas contém a mesma assinatura e idade.

## <a name="symstore-transactions"></a>Transações de SymStore

Cada chamada para SymStore é registrada como uma transação. Há dois tipos de transações: Adicionar e excluir.

Quando o armazenamento de símbolo é criado, um diretório, chamado "000admin", é criado sob a raiz do servidor. O diretório 000admin contém um arquivo para cada transação, bem como os arquivos de log Server.txt e History.txt. O arquivo de Server.txt contém uma lista de todas as transações que estão atualmente no servidor. O arquivo de History.txt contém um histórico cronológico de todas as transações.

Cada vez que o SymStore armazena ou remove arquivos de símbolo, um novo número de transação é criado. Em seguida, um arquivo, cujo nome é esse número de transação, é criado em 000admin. Esse arquivo contém uma lista de todos os arquivos ou ponteiros que foram adicionados ao repositório de símbolos durante essa transação. Se uma transação for excluída, o SymStore lerá seu arquivo de transação para determinar quais arquivos e ponteiros devem ser excluídos.

As opções **Adicionar** e **del** especificam se uma transação Adicionar ou excluir deve ser executada. Incluir a opção **/p** com uma operação de adição especifica que um ponteiro deve ser adicionado; omitir a opção **/p** especifica que o arquivo de símbolo real deve ser adicionado.

Também é possível criar o armazenamento de símbolo em dois estágios separados. No primeiro estágio, você usa SymStore com a opção **/x** para criar um arquivo de índice. No segundo estágio, você usa SymStore com a opção **/y** para criar o armazenamento real de arquivos ou ponteiros a partir das informações no arquivo de índice.

Isso pode ser uma técnica útil por vários motivos. Por exemplo, isso permite que o armazenamento de símbolos seja recriado facilmente se o armazenamento estiver de alguma forma perdida, desde que o arquivo de índice ainda exista. Ou talvez o computador que contém os arquivos de símbolo tenha uma conexão de rede lenta com o computador no qual o armazenamento de símbolo será criado. Nesse caso, você pode criar o arquivo de índice no mesmo computador que os arquivos de símbolo, transferir o arquivo de índice para o segundo computador e, em seguida, criar o armazenamento no segundo computador.

Para obter uma lista completa de todos os parâmetros de SymStore, consulte [Opções de Command-Line de SymStore](symstore-command-line-options.md).

> [!Note]  
> SymStore não oferece suporte a transações simultâneas de vários usuários. É recomendável que um usuário seja designado como "administrador" do repositório de símbolos e seja responsável por todas as transações de **adição** e de **del** .

 

## <a name="transaction-examples"></a>Exemplos de transação

Aqui estão dois exemplos de SymStore que adicionam ponteiros de símbolo para a compilação 3790 do Windows Server 2003 a \\ \\ SampleDir \\ symsrv:

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

No exemplo a seguir, SymStore adiciona os arquivos de símbolo reais para um projeto de aplicativo em \\ \\ compartimentos do largeapp do \\ AppServer \\ a \\ \\ TestDir \\ symsrv:

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

Aqui está um exemplo de como um arquivo de índice é usado. Primeiro, o SymStore cria um arquivo de índice baseado na coleção de arquivos de símbolo em \\ \\ compartimentos do largeapp do \\ AppServer \\ \\ . Nesse caso, o arquivo de índice é colocado em um terceiro computador, \\ \\ hubserver \\ hubshare. Você usa a opção **/g** para especificar que o prefixo do arquivo " \\ \\ largeapp \\ AppServer" pode ser alterado no futuro:

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

Agora suponha que você mova todos os arquivos de símbolo do computador \\ \\ largeapp \\ AppServer e coloque-os em \\ \\ myarchive \\ AppServer. Em seguida, você pode criar o próprio armazenamento de símbolo no arquivo de índice \\ \\ hubserver \\ hubshare \\myindex.txt da seguinte maneira:

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

Por fim, aqui está um exemplo de SymStore excluindo um arquivo adicionado por uma transação anterior. Consulte a seção a seguir para obter uma explicação de como determinar a ID da transação (nesse caso, 0000000096).

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a>Arquivos compactados

SymStore pode ser usado com arquivos compactados de duas maneiras diferentes.

1.  Use SymStore com a opção **/p** para armazenar ponteiros para os arquivos de símbolo. Após a conclusão do SymStore, compacte os arquivos aos quais os ponteiros se referem.
2.  Use SymStore com a opção **/x** para criar um arquivo de índice. Após a conclusão do SymStore, compacte os arquivos listados no arquivo de índice. Em seguida, use SymStore com a opção **/y** (e, se desejar, a opção **/p** ) para armazenar os arquivos ou ponteiros para os arquivos no repositório de símbolos. (O SymStore não precisará descompactar os arquivos para executar esta operação.)

O servidor de símbolos será responsável por descompactar os arquivos quando forem necessários.

Se você estiver usando o SymSrv como seu servidor de símbolos, qualquer compactação deverá ser feita usando a ferramenta compress.exe que é distribuída com o SDK (Software Development Kit) do Microsoft Windows. Arquivos compactados devem ter um sublinhado como o último caractere em suas extensões de arquivo (por exemplo, Module1. PD \_ ou Module2. db \_ ). Para obter detalhes, consulte [usando symsrv](using-symsrv.md).

## <a name="the-servertxt-and-historytxt-files"></a>Os arquivos de server.txt e history.txt

Quando uma transação é adicionada, vários itens de informações são adicionados a server.txt e history.txt para a funcionalidade de pesquisa futura. Veja a seguir um exemplo de uma linha em server.txt e history.txt para uma transação de adição:

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

Esta é uma linha separada por vírgulas. Os campos são definidos da seguinte maneira.



| Campo      | Descrição                                                                         |
|------------|-------------------------------------------------------------------------------------|
| 0000000096 | Número da ID da transação, conforme criado por SymStore.                                      |
| add        | Tipo de transação. Esse campo pode ser **Add** ou **del**.                   |
| ptr        | Se os arquivos ou ponteiros foram adicionados. Esse campo pode ser um **arquivo** ou um **PTR**. |
| 10/09/99   | Data em que a transação ocorreu.                                                     |
| 00:08:32   | Hora em que a transação foi iniciada.                                                      |
| Windows XP | Produto.                                                                            |
| fre x86    | Versão (opcional).                                                                 |
| Adicionado de | Comentário (opcional)                                                                  |
| Não usado     | (Reservado para uso posterior.)                                                           |



 

Aqui estão algumas linhas de exemplo do arquivo de transação 0000000096. Cada linha registra o diretório e o local do arquivo ou ponteiro que foi adicionado ao diretório.

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

Se você usar uma transação **del** para desfazer as transações de **adição** originais, essas linhas serão removidas do server.txt e a linha a seguir será adicionada ao history.txt:

``` syntax
0000000105,del,0000000096
```

Os campos para a transação de exclusão são definidos da seguinte maneira.



| Campo      | Descrição                                                       |
|------------|-------------------------------------------------------------------|
| 0000000105 | Número da ID da transação, conforme criado por SymStore.                    |
| del        | Tipo de transação. Esse campo pode ser **Add** ou **del**. |
| 0000000096 | Transação excluída.                                     |



 

## <a name="symbol-storage-format"></a>Formato de armazenamento de símbolo

O SymStore usa o próprio sistema de arquivos como um banco de dados. Ele cria uma árvore grande de diretórios, com nomes de diretório baseados em coisas como carimbos de data/hora de arquivo de símbolo, assinaturas, idade e outros dados.

Por exemplo, depois que vários arquivos ACPI. dbg diferentes tiverem sido adicionados ao servidor, os diretórios poderão ter esta aparência:

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

Neste exemplo, o caminho de pesquisa para o arquivo de símbolo ACPI. dbg pode ser semelhante a este: \\ \\ mycompilations \\ symsrv \\ ACPI. dbg \\ 37cdb03962040.

Três arquivos podem existir dentro do diretório de pesquisa:

1.  Se o arquivo foi armazenado, o ACPI. dbg existirá lá.
2.  Se um ponteiro foi armazenado, um arquivo chamado file. PTR existirá e conterá o caminho para o arquivo de símbolo real.
3.  Um arquivo chamado refs. PTR, que contém uma lista de todos os locais atuais para ACPI. dbg com esse carimbo de data e hora e tamanho da imagem que são atualmente adicionados ao repositório de símbolos.

Exibindo a listagem de diretórios de \\ \\ mybuilds \\ symsrv \\ ACPI. dbg \\ 37cdb03962040 fornece o seguinte:

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

O arquivo file. PTR contém a cadeia de texto " \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ Sys \\ ACPI. dbg". Como não há nenhum arquivo chamado ACPI. dbg nesse diretório, o depurador tentará localizar o arquivo em \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ Sys \\ ACPI. dbg.

O conteúdo de refs. ptr é usado somente por SymStore, não pelo depurador. Esse arquivo contém um registro de todas as transações realizadas neste diretório. Uma linha de exemplo de refs. PTR pode ser:

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

Isso mostra que um ponteiro para \\ \\ mycompile \\ símbolos \\ x86 \\ 2128. chk \\ Symbols \\ Sys \\ ACPI. DBG foi adicionado com a transação "0000000026".

Alguns arquivos de símbolos permanecem constantes por meio de vários produtos ou compilações ou um produto específico. Um exemplo disso é o arquivo Msvcrt. pdb. Fazer um diretório de \\ \\ mybuilds \\ symsrv \\ msvcrt. pdb mostra que apenas duas versões do msvcrt. pdb foram adicionadas ao servidor de símbolos:

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

No entanto, fazer um diretório de \\ \\ mybuilds \\ symsrv \\ msvcrt. pdb \\ 37a8f40e2 mostra que refs. PTR tem vários ponteiros.

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

O conteúdo de \\ \\ mycompilations \\ symsrv \\ msvcrt. pdb \\ 37a8f40e2 \\ refs. ptr é o seguinte:

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

Isso mostra que o mesmo msvcrt. pdb foi usado para várias compilações de símbolos armazenadas em \\ \\ mycompilações \\ symsrv.

Aqui está um exemplo de um diretório que contém uma mistura de adições de arquivo e ponteiro:

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

Nesse caso, refs. PTR tem o seguinte conteúdo:

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

Assim, as transações 43, 44 e 45 adicionaram o mesmo arquivo ao servidor e transações 46 e 47 ponteiros adicionados. Se as transações 43, 44 e 45 forem excluídas, o arquivo dbghelp. dbg será excluído do diretório. O diretório terá o seguinte conteúdo:

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

Now File. PTR contém " \\ \\ sampledir2 \\ bin \\ Symbols \\ Retail \\ dll \\ dbghelp. dbg" e refs. PTR contém

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

Sempre que a entrada final em refs. PTR for um ponteiro, o arquivo. PTR existirá e conterá o caminho para o arquivo associado. Sempre que a entrada final em refs. PTR for um arquivo, nenhum arquivo. PTR existirá nesse diretório. Portanto, qualquer operação de exclusão que remova a entrada final em refs. PTR pode resultar em File. PTR sendo criado, excluído ou alterado.

 

 



