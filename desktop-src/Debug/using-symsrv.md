---
description: Usando SymSrv
ms.assetid: d400f222-c50c-4c7b-8f8a-0c3ed3bba3b9
title: Usando SymSrv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bbaf68e80555629db8bc9a2a21394b95fe6fb85
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550031"
---
# <a name="using-symsrv"></a>Usando SymSrv

O SymSrv entrega arquivos de símbolo de armazenamentos de símbolo centralizados. Esses armazenamentos podem conter qualquer número de arquivos de símbolo, correspondentes a qualquer número de programas ou sistemas operacionais. As lojas também podem conter arquivos binários, que são particularmente úteis durante a depuração de arquivos de minidespejo.

As lojas podem conter o símbolo real e os arquivos binários ou simplesmente ponteiros para arquivos de símbolo. Se o repositório contiver ponteiros, o SymSrv recuperará os arquivos reais diretamente de suas origens.

SymSrv também pode separar um repositório de símbolos grande em um subconjunto menor apropriado para uma tarefa de depuração especializada.

Por fim, o SymSrv pode obter arquivos de símbolo de uma fonte HTTP ou HTTPS usando as informações de logon fornecidas pelo sistema operacional. O SymSrv dá suporte a sites HTTPS protegidos por cartões inteligentes, certificados e logons e senhas regulares.

## <a name="setting-the-symbol-path"></a>Configurando o caminho do símbolo

Conforme descrito em [caminhos de símbolo](symbol-paths.md), o caminho do símbolo ( \_ variável de ambiente do caminho do NT \_ Symbol \_ ) pode ser composto por vários elementos de caminho separados por ponto e vírgula. Se qualquer um ou mais desses elementos de caminho começar com o texto "SRV \* ", o elemento será um servidor de símbolos e usará symsrv para localizar arquivos de símbolo.

> [!Note]  
> Se o texto "SRV \* " não for especificado, mas o elemento de caminho real for um armazenamento de servidor de símbolos, o manipulador de símbolo atuará como se "SRV \* " fosse especificado. O manipulador de símbolos faz essa determinação pesquisando a existência de um arquivo chamado "pingme.txt" no diretório raiz do caminho especificado.

 

Assim como os caminhos de símbolo são compostos de elementos de caminho de símbolo separados por ponto e vírgula, os servidores de símbolos são compostos de elementos de repositório de símbolos separados por asteriscos. Pode haver até 10 repositórios de símbolo após o prefixo "SRV \* ". As lojas listadas à esquerda da lista são chamadas armazenamentos *downstream* e armazenamentos à direita são chamados de armazenamentos *upstream* .

<dl> \**SymbolStore* SRV  
srv \* *SymbolStore1* \* *SymbolStoreN*  
</dl>

Se apenas um elemento de armazenamento de símbolos estiver incluído no caminho, SymSrv tentará usar qualquer arquivo solicitado diretamente desse armazenamento.

Se houver dois armazenamentos de símbolos no caminho, o SymSrv procura o arquivo de símbolo no armazenamento de símbolos mais à esquerda. Se o arquivo estiver lá, ele será usado. Se ele não estiver lá, SymSrv olhará no armazenamento de símbolos imediatamente à direita. Se o arquivo estiver lá, ele será copiado para o armazenamento esquerdo e aberto de lá.

Se houver mais de dois armazenamentos, esse comportamento continuará à direita até que o arquivo seja encontrado ou não haja mais armazenamentos na lista.

O arquivo nunca é aberto em nenhum armazenamento, mas no armazenamento mais à esquerda. Se o arquivo for encontrado em qualquer outro lugar na cadeia, ele será copiado para todos os armazenamentos à esquerda dele. Esse processo de cópia é chamado de "em cascata" e fornece alguns benefícios que serão esclarecedos posteriormente neste documento.

## <a name="types-of-symbol-stores"></a>Tipos de armazenamentos de símbolos

A tabela a seguir exibe exemplos dos tipos de armazenamento de símbolos com suporte.

|  Tipo de armazenamento de símbolos       |  Description |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\\\compartilhamento \\ de servidor          | Um caminho UNC totalmente qualificado para um compartilhamento em um servidor remoto.                                                                                                                                                                                                                                                                                                 |
| c: \\ LocalCache             | Um caminho para um diretório no computador cliente.                                                                                                                                                                                                                                                                                                             |
| https://InternetSite        | A URL para um site que hospeda os símbolos. Deve ser o armazenamento mais à direita na lista e não deve ser o único armazenamento na lista.                                                                                                                                                                                                                          |
| https://SecureInternetSite | A URL para um site seguro que hospeda os símbolos. Isso pode dar suporte a senhas, credenciais de logon do Windows, certificados e cartões inteligentes. Deve ser o armazenamento mais à direita na lista e não deve ser o único repositório na lista.                                                                                                                              |
| <blank>              | Se não houver texto entre dois asteriscos, isso indicará o *armazenamento downstream padrão*. O local é definido chamando [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory). O valor padrão é um diretório chamado "Sym" logo abaixo do diretório de programa do aplicativo de chamada. Isso às vezes é chamado de *cache local padrão*. |



 

Como um armazenamento de símbolo baseado em HTTP não pode ser gravado, ele deve ser o armazenamento mais à direita na lista. Se um armazenamento de símbolo baseado em HTTP estiver localizado no meio ou à esquerda da lista da loja, não será possível copiar os arquivos encontrados nele e a cadeia seria interrompida. Além disso, como o manipulador de símbolo não pode abrir um arquivo de um site, um armazenamento baseado em HTTP não deve ser o mais à esquerda ou apenas armazenar na lista. Se SymSrv for apresentado com esse caminho de símbolo, ele tentará se recuperar copiando o arquivo para o armazenamento downstream padrão e o abrirá a partir daí, independentemente de o armazenamento downstream padrão ser indicado no caminho do símbolo ou não.

## <a name="examples"></a>Exemplos

Para usar o SymSrv com um repositório de símbolos em \\ \\ mybuilds \\ mysymbols, defina o seguinte caminho de símbolo:

**definir \_ caminho do símbolo do NT \_ \_ = SRV \ \* \\ \\ Builds \\ mysymbols**

Para definir o caminho do símbolo para que o depurador Copie os arquivos de símbolo de um repositório de símbolos em \\ \\ mycompila \\ mysymbols para o diretório local c: \\ localsymbols, use:

**definir \_ \_ caminho do símbolo NT \_ = SRV \* c: \\ localsymbols \* \\ \\ mycompila \\ mysymbols**

Para definir o caminho do símbolo para que o depurador Copie os arquivos de símbolo de um repositório de símbolos em \\ \\ mycompila \\ mysymbols para o armazenamento de downstream padrão (normalmente c: \\ Debuggers \\ Sym), use:

**definir \_ caminho do símbolo do NT \_ \_ = SRV \ \* \* \\ \\ Builds \\ mysymbols**

Para usar um armazenamento em cascata, de definir o seguinte caminho de símbolo:

**set \_ NT \_ SYMBOL PATH = \_ srv \* c: \\ localsymbols \* \\ \\ \\ NearbyServer store\*https://DistantServer**

Neste exemplo, SymSrv primeiro procura o arquivo em c: \\ localsymbols. Se for encontrado lá, ele retornará um caminho para o arquivo. Caso contrário, SymSrv procura o arquivo no \\ \\ armazenamento \\ NearbyServer. Se ele for encontrado lá, SymSrv copia o arquivo para c: localsymbols e retorna um caminho para o arquivo; se ele não for encontrado, SymSrv procura o arquivo em e, se ele for encontrado lá, SymSrv copia o arquivo para o armazenamento NearbyServer e, em seguida, para \\ https://DistantServer \\ \\ \\ c: \\ localsymbols.

Este último exemplo mostra como o design criterioso de um caminho de símbolo pode ser usado para otimizar o download de símbolos. Se você tiver um site de trabalho com um grupo de depurador e todos eles precisarem obter símbolos de um local distante, você poderá configurar um servidor comum com um armazenamento de símbolos próximo a todos os depurador. Em seguida, configure cada depurador com o caminho de símbolo acima. O primeiro depurador que requer uma determinada versão do foo.pdb o baixará do para o nearbyServer store e, em seguida, para seu próprio computador https://DistantServer \\ \\ \\ em c: \\ localsymbols. O próximo depurador que requer o mesmo arquivo poderá baixá-lo do armazenamento NearbyServer porque ele já foi baixado para esse local pelo \\ \\ \\ depurador anterior. Esse cache de vários níveis economiza tempo significativo e largura de banda de rede.

## <a name="microsoft-symbol-store"></a>Microsoft Symbol Store

A Microsoft fornece acesso a um servidor de símbolos da Internet que contém arquivos de símbolo para as várias versões do sistema operacional Windows. Não há garantia de que esse catálogo de símbolos seja concluído, mas é abrangente. Outros produtos da Microsoft também são representados.

O servidor de símbolos da Internet é populado com uma variedade de símbolos do Windows para sistemas operacionais Microsoft Windows, incluindo correções ativas, Service Packs, Pacotes de Rollup de Segurança e versões de varejo. Os símbolos também estão disponíveis no servidor para betas atuais e candidatos à versão para produtos windows, além de uma variedade de outros produtos da Microsoft, como o Microsoft Internet Explorer.

Se você tiver acesso à Internet durante a depuração, poderá configurar o depurador para baixar símbolos conforme necessário durante uma sessão de depuração, em vez de baixar arquivos de símbolo separadamente antes de uma sessão de depuração. Os símbolos são baixados para um local de diretório que você especifica e, em seguida, o depurador os carrega de lá.

A URL do armazenamento de símbolos da Microsoft é https://msdl.microsoft.com/download/symbols . O exemplo a seguir mostra como definir o caminho do símbolo do depurador (substitua o caminho do repositório downstream por *c: \\ DownstreamStore*):

``` syntax
srv*c:\DownstreamStore*https://msdl.microsoft.com/download/symbols
```

## <a name="compressed-files"></a>Arquivos compactados

O SymSrv é compatível com os armazenamentos de símbolos que contêm arquivos compactados, desde que essa compactação tenha sido pré-formada com a ferramenta compress.exe que foi distribuída com o Kit de Recursos do Windows Server 2003. Arquivos compactados devem ter um sublinhado como o último caractere em suas extensões de arquivo (por exemplo, module1.pd \_ ou module2.db \_ ). Para obter detalhes, [consulte Usando SymStore](using-symstore.md).

Durante a cascata, os arquivos não são descompactados, a menos que o armazenamento de destino seja o armazenamento mais à esquerda no caminho. Se houver apenas um armazenamento no caminho e contiver um arquivo compactado, o SymSrv copiará o arquivo para o armazenamento downstream padrão e o abrirá a partir daí, mesmo que o armazenamento downstream padrão não seja indicado no caminho do símbolo.

**DbgHelp 6.1 e anterior.:** Se os arquivos no armazenamento mestre são compactados, você deve usar um armazenamento downstream. O SymSrv descompacta todos os arquivos antes de copiá-los para o armazenamento downstream.

## <a name="deleting-the-cache"></a>Excluindo o cache

Se você estiver usando um armazenamento downstream como cache, poderá excluir esse diretório a qualquer momento para economizar espaço em disco.

É possível ter um grande armazenamento de símbolos que inclui arquivos de símbolo para muitos programas diferentes ou versões do Windows. Se você atualizar a versão do Windows usada em seu computador de destino, os arquivos de símbolo armazenados em cache corresponderão à versão anterior. Esses arquivos armazenados em cache não serão mais usados e, portanto, esse pode ser um bom momento para excluir o cache.

As ferramentas de depuração para Windows vêm com um utilitário chamado agestore.exe que removerá os arquivos de uma árvore de diretório de forma seletiva, deixando os arquivos usados mais recentemente. Essa ferramenta foi projetada para remover arquivos não utilizados de repositórios de servidores de símbolos. Ele permite que você controle várias opções, incluindo algoritmos de data de corte e tamanho de diretório.

## <a name="flat-cache-directory"></a>Diretório de cache simples

É possível declarar o armazenamento downstream padrão como um diretório simples, em vez de uma estrutura de árvore de símbolos padrão. Para fazer isso, chame a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) com **o \_ \_ diretório Flat do SYMOPT** (isso também define a opção de **\_ \_ \_ armazenamento padrão de SSRVOPT simples** em SymSrv). Certifique-se de chamar [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) antes de fazer isso; caso contrário, os arquivos de símbolo podem ser gravados no diretório do programa.

## <a name="pointer-files"></a>Arquivos de ponteiro

O SymStore pode criar e usar arquivos que apontam para um arquivo de destino em vez do próprio arquivo de destino. Se um repositório de símbolos contiver esse arquivo de ponteiro, o padrão será copiar o arquivo do local indicado no arquivo de ponteiro para a loja. Para configurar um repositório de modo que o arquivo de ponteiro seja copiado em vez do arquivo para o qual ele aponta, crie um arquivo chamado wantsptr.txt na raiz do repositório de destino. O conteúdo de wantsptr.txt não são importantes, apenas a presença do arquivo.

## <a name="excluding-files-from-symbols-list"></a>Excluindo arquivos da lista de símbolos

Para excluir arquivos de uma pesquisa de símbolos, você pode especificar seus nomes no symsrv.ini ou no registro. Para especificar os arquivos em symsrv.ini, crie uma seção chamada exclusões e liste os arquivos. Os nomes de arquivo podem conter curingas, conforme mostrado no exemplo a seguir:

``` syntax
[Exclusions]
dbghelp.pdb
symsrv.*
mso*
```

Symsrv.ini deve estar localizado no mesmo diretório em que symsrv.dll reside. Na maioria das instalações, o arquivo não existe e você precisará criar um novo.

Como alternativa, você pode armazenar os arquivos a serem excluídos no Registro. Crie a seguinte chave do Registro: Exclusões do servidor de símbolos da **Microsoft HKEY \_ LOCAL MACHINE \_ \\ Software \\ \\ \\**. Armazene cada nome de arquivo como um valor de cadeia de caracteres (REG \_ SZ) dentro dessa chave. O nome do valor da cadeia de caracteres especifica o nome do arquivo a ser excluído. Você pode usar o conteúdo do valor da cadeia de caracteres para armazenar um comentário que descreve por que o arquivo está sendo excluído.

## <a name="installation"></a>Instalação

O servidor de símbolos SymSrv (symsrv.dll) está incluído no pacote Ferramentas de Depuração para Windows. Ele deve ser instalado no mesmo diretório que a cópia do dbghelp.dll que você está carregando. Para obter mais detalhes, consulte [Chamando a biblioteca DbgHelp.](calling-the-dbghelp-library.md)

 

 



