---
description: todos os sistemas de arquivos com suporte pelo Windows usam o conceito de arquivos e diretórios para acessar dados armazenados em um disco ou dispositivo.
ms.assetid: 121cd5b2-e6fd-4eb4-99b4-b652d27b53e8
title: Nomeando arquivos, caminhos e namespaces
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: f77b12fa133bb8b35260b49a90c24e202055c8564431f6a0d6d4c09527811ca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533446"
---
# <a name="naming-files-paths-and-namespaces"></a>Nomeando arquivos, caminhos e namespaces

todos os sistemas de arquivos com suporte pelo Windows usam o conceito de arquivos e diretórios para acessar dados armazenados em um disco ou dispositivo. Windows os desenvolvedores que trabalham com as APIs de Windows para e/s de arquivos e dispositivos devem entender as várias regras, convenções e limitações de nomes de arquivos e diretórios.

Os dados podem ser acessados de discos, dispositivos e compartilhamentos de rede usando APIs de e/s de arquivo. Os arquivos e diretórios, juntamente com namespaces, fazem parte do conceito de um caminho, que é uma representação de cadeia de caracteres de onde obter os dados independentemente de um disco ou um dispositivo ou uma conexão de rede para uma operação específica.

Alguns sistemas de arquivos, como NTFS, dão suporte a arquivos e diretórios vinculados, que também seguem as convenções e regras de nomenclatura de arquivo, assim como um arquivo ou diretório regular. Para obter informações adicionais, consulte [links físicos e junções](hard-links-and-junctions.md) e [pontos de nova análise e operações de arquivo](reparse-points-and-file-operations.md).

Para obter informações adicionais, consulte as seguintes subseções:

-   [Nomes de arquivos e diretórios](#file-and-directory-names)
    -   [Convenções de nomenclatura](#naming-conventions)
    -   [Nomes curtos versus longos](#short-vs-long-names)
-   [Caminhos](#fully-qualified-vs-relative-paths)
    -   [Caminhos vs. relativos totalmente qualificados](#fully-qualified-vs-relative-paths)
    -   [Limitação Máxima do Comprimento do Caminho](#maximum-path-length-limitation)
-   [Namespaces](#win32-file-namespaces)
    -   [Namespaces de arquivo Win32](#win32-file-namespaces)
    -   [Namespaces de dispositivo Win32](#win32-device-namespaces)
    -   [Namespaces do NT](#nt-namespaces)
-   [Tópicos relacionados](#related-topics)


para saber mais sobre como configurar Windows 10 para dar suporte a caminhos de arquivo longos, consulte [limitação de comprimento de caminho máximo](./maximum-file-path-limitation.md).


## <a name="file-and-directory-names"></a>Nomes de arquivos e diretórios

Todos os sistemas de arquivos seguem as mesmas convenções de nomenclatura gerais para um arquivo individual: um nome de arquivo base e uma extensão opcional, separados por um ponto. No entanto, cada sistema de arquivos, como NTFS, CDFS, exFAT, UDFS, FAT e FAT32, pode ter regras específicas e diferentes sobre a formação de componentes individuais no caminho para um diretório ou arquivo. Observe que um *diretório* é simplesmente um arquivo com um atributo especial que o designa como um diretório, mas, caso contrário, deve seguir todas as mesmas regras de nomenclatura que um arquivo regular. Como o termo *diretório* simplesmente se refere a um tipo especial de arquivo no que diz respeito ao sistema de arquivos, um material de referência usará o *arquivo* de termo geral para abranger os dois conceitos de diretórios e arquivos de dados como tal. Por isso, a menos que especificado de outra forma, qualquer nomenclatura ou regra de uso ou exemplos de um arquivo também devem ser aplicados a um diretório. O termo *caminho* refere-se a um ou mais diretórios, barras invertidas e, possivelmente, um nome de volume. Para obter mais informações, consulte a seção [caminhos](#fully-qualified-vs-relative-paths) .

As limitações de contagem de caracteres também podem ser diferentes e podem variar dependendo do formato do sistema de arquivos e do prefixo de nome de caminho usado. Isso é mais complicado pelo suporte a mecanismos de compatibilidade com versões anteriores. Por exemplo, o sistema de arquivos FAT mais antigo do MS-DOS dá suporte a um máximo de 8 caracteres para o nome do arquivo base e 3 caracteres para a extensão, com um total de 12 caracteres, incluindo o separador de pontos. Isso é conhecido normalmente como um *nome de arquivo 8,3*. os Windows sistemas de arquivos FAT e NTFS não estão limitados a 8,3 nomes de arquivo, pois têm *suporte a nome de arquivo longo*, mas ainda dão suporte à versão 8,3 de nomes de arquivo longos.

### <a name="naming-conventions"></a>Convenções de nomenclatura

As regras fundamentais a seguir permitem que os aplicativos criem e processem nomes válidos para arquivos e diretórios, independentemente do sistema de arquivos:

-   Use um período para separar o nome do arquivo base da extensão no nome de um diretório ou arquivo.
-   Use uma barra invertida ( \\ ) para separar os *componentes* de um *caminho*. A barra invertida divide o nome do arquivo do caminho para ele e um nome de diretório de outro nome de diretório em um caminho. Você não pode usar uma barra invertida no nome do arquivo ou diretório real porque ele é um caractere reservado que separa os nomes em componentes.
-   Use uma barra invertida conforme necessário como parte dos [nomes de volume](naming-a-volume.md), por exemplo, "c: \\ " em "c: \\ Path \\ File" ou " \\ \\ Server \\ share" em " \\ \\ Server \\ share \\ Path \\ File" para nomes UNC (Convenção de nomenclatura universal). Para obter mais informações sobre nomes UNC, consulte a seção [limite de comprimento máximo de caminho](#maximum-path-length-limitation) .
-   Não assuma a distinção entre maiúsculas e minúsculas. Por exemplo, considere os nomes OSCAR, Oscar e Oscar para serem os mesmos, mesmo que alguns sistemas de arquivos (como um sistema de arquivos compatível com POSIX) possam considerá-los como diferentes. Observe que o NTFS dá suporte à semântica POSIX para diferenciação de maiúsculas e minúsculas, mas esse não é o comportamento padrão. Para obter mais informações, consulte [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).
-   Os designadores de volume (letras da unidade) são não diferenciam maiúsculas de minúsculas. Por exemplo, "D: \\ " e "D: \\ " referem-se ao mesmo volume.
-   Use qualquer caractere na página de código atual para um nome, incluindo caracteres Unicode e caracteres no conjunto de caracteres estendidos (128 – 255), exceto para o seguinte:

    -   Os seguintes caracteres reservados:

        -   < (menor que)
        -   \> (maior que)
        -   : (dois-pontos)
        -   "(aspas duplas)
        -   / (barra)
        -   \\ barra invertida
        -   \| (barra vertical ou pipe)
        -   ? (ponto de interrogação)
        -   \* asterisco

    -   Valor inteiro zero, às vezes chamado de caractere ASCII *nul* .
    -   Caracteres cujas representações de inteiros estão no intervalo de 1 a 31, exceto para fluxos de dados alternativos em que esses caracteres são permitidos. para obter mais informações sobre fluxos de arquivos, consulte [arquivo Fluxos](file-streams.md).
    -   Qualquer outro caractere que o sistema de arquivos de destino não permita.

-   Use um ponto como um *componente* de diretório em um caminho para representar o diretório atual, por exemplo ". \\temp.txt ". Para obter mais informações, consulte [Paths](#fully-qualified-vs-relative-paths).
-   Use dois pontos consecutivos (..) como um *componente* de diretório em um caminho para representar o pai do diretório atual, por exemplo ".. \\temp.txt ". Para obter mais informações, consulte [Paths](#fully-qualified-vs-relative-paths).
-   Não use os seguintes nomes reservados para o nome de um arquivo:

    CON, PRN, AUX, NUL, COM1, COM2, COM3, COM4, COM5, COM6, COM7, COM8, COM9, LPT1, LPT2, LPT3, LPT4, LPT5, LPT6, LPT7, LPT8 e LPT9. Evite também esses nomes seguidos imediatamente por uma extensão; por exemplo, NUL.txt não é recomendável. Para obter mais informações, consulte [Namespaces](#win32-file-namespaces).

-   Não Finalize um nome de arquivo ou diretório com um espaço ou um ponto. embora o sistema de arquivos subjacente possa dar suporte a tais nomes, o shell de Windows e a interface do usuário não têm. No entanto, é aceitável especificar um ponto como o primeiro caractere de um nome. Por exemplo, ". Temp".

### <a name="short-vs-long-names"></a>Nomes curtos versus longos

Um nome de arquivo longo é considerado como qualquer nome de arquivo que exceda a Convenção de nomenclatura de estilo MS-DOS curto (também chamada de *8,3*). quando você cria um nome de arquivo longo, Windows também pode criar uma forma curta de 8,3 do nome, chamada *alias 8,3* ou nome curto, e armazená-lo no disco também. Esse alias de 8,3 pode ser desabilitado por motivos de desempenho em todo o sistema ou em um volume especificado, dependendo de um arquivo específico.

**Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** o alias de 8,3 não pode ser desabilitado para volumes especificados até Windows 7 e Windows Server 2008 R2.

Em muitos sistemas de arquivos, um nome de arquivo conterá um til (~) dentro de cada componente do nome que é muito longo para estar em conformidade com as regras de nomenclatura 8,3.

> [!Note]  
> Nem todos os sistemas de arquivos seguem a Convenção de substituição de til, e os sistemas podem ser configurados para desabilitar a geração de alias 8,3, mesmo que normalmente o ofereçam. Portanto, não faça a suposição de que o alias 8,3 já existe no disco.

 

Para solicitar nomes de arquivo 8,3, nomes de arquivo longos ou o caminho completo de um arquivo do sistema, considere as seguintes opções:

-   Para obter a forma 8,3 de um nome de arquivo longo, use a função [**GetShortPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getshortpathnamew) .
-   Para obter a versão de nome de arquivo longo de um nome curto, use a função [**GetLongPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getlongpathnamea) .
-   Para obter o caminho completo de um arquivo, use a função [**Getfullpathname**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) .

em sistemas de arquivos mais recentes, como NTFS, exFAT, UDFS e FAT32, o Windows armazena os nomes de arquivo longos em disco em Unicode, o que significa que o nome de arquivo longo original é sempre preservado. Isso é verdadeiro mesmo que um nome de arquivo longo contenha caracteres estendidos, independentemente da página de código que está ativa durante uma operação de leitura ou gravação de disco.

arquivos que usam nomes de arquivo longos podem ser copiados entre partições do sistema de arquivos NTFS e Windows partições do sistema de arquivos FAT sem perder nenhuma informação de nome de arquivo. Isso pode não ser verdadeiro para o FAT mais antigo do MS-DOS e alguns tipos de sistemas de arquivos CDFS (CD-ROM), dependendo do nome real do arquivo. Nesse caso, o nome de arquivo curto é substituído, se possível.

## <a name="paths"></a>Caminhos

O *caminho* para um arquivo especificado consiste em um ou mais *componentes*, separados por um caractere especial (uma barra invertida), com cada componente geralmente sendo um nome de diretório ou nome de arquivo, mas com algumas exceções notáveis discutidas abaixo. Geralmente, é fundamental para a interpretação do sistema de um caminho em que se parece o início, ou *prefixo*, do caminho. Esse prefixo determina o *namespace* que o caminho está usando e, além disso, os caracteres especiais são usados em qual posição dentro do caminho, incluindo o último caractere.

Se um componente de um caminho for um nome de arquivo, ele deverá ser o último componente.

Cada componente de um caminho também será restrito pelo comprimento máximo especificado para um sistema de arquivos específico. Em geral, essas regras se enquadram em duas categorias: *curta* e *longa*. Observe que os nomes de diretório são armazenados pelo sistema de arquivos como um tipo especial de arquivo, mas as regras de nomenização para arquivos também se aplicam a nomes de diretório. Para resumir, um caminho é simplesmente a representação de cadeia de caracteres da hierarquia entre todos os diretórios existentes para um determinado nome de arquivo ou diretório.

### <a name="fully-qualified-vs-relative-paths"></a>Caminhos totalmente qualificados versus relativos

Para Windows de API que manipulam arquivos, os nomes de arquivo geralmente podem ser relativos ao diretório atual, enquanto algumas APIs exigem um caminho totalmente qualificado. Um nome de arquivo será relativo ao diretório atual se ele não começar com um dos seguintes:

-   Um nome UNC de qualquer formato, que sempre começa com dois caracteres de faixa invertida (" \\ \\ "). Para obter mais informações, consulte a próxima seção.
-   Um designador de disco com uma faixa invertida, por exemplo " C: \\ " ou "d: \\ ".
-   Uma única faixa invertida, por exemplo, " \\ directory" ou \\ "file.txt". Isso também é conhecido como um *caminho absoluto.*

Se um nome de arquivo começar com apenas um designador de disco, mas não com a faixa invertida após os dois-pontos, ele será interpretado como um caminho relativo para o diretório atual na unidade com a letra especificada. Observe que o diretório atual pode ou não ser o diretório raiz, dependendo do que foi definido como durante a operação mais recente de "alterar diretório" nesse disco. Exemplos desse formato são os exemplos a seguir:

-   "C:tmp.txt" refere-se a um arquivo chamado "tmp.txt" no diretório atual na unidade C.
-   "C:tempdirtmp.txt" refere-se a um arquivo em um subdiretório para o \\ diretório atual na unidade C.

Um caminho também será relativo se ele contiver "pontos duplos"; ou seja, dois períodos juntos em um componente do caminho. Esse especificador especial é usado para denotar o diretório acima do diretório atual, também conhecido como "diretório pai". Exemplos desse formato são os exemplos a seguir:

-   "..\\tmp.txt" especifica um arquivo chamado tmp.txt localizado no pai do diretório atual.
-   "..\\..\\tmp.txt" especifica um arquivo que está dois diretórios acima do diretório atual.
-   "..\\ tempdirtmp.txt" especifica um arquivo chamado tmp.txt localizado em um diretório chamado tempdir que é um diretório \\ par para o diretório atual.

Caminhos relativos podem combinar os dois tipos de exemplo, por exemplo "C:.. \\tmp.txt". Isso é útil porque, embora o sistema mantenha o controle da unidade atual junto com o diretório atual dessa unidade, ele também mantém o controle dos diretórios atuais em cada uma das diferentes letras de unidade (se o sistema tiver mais de uma), independentemente de qual designador de unidade está definido como a unidade atual.

### <a name="maximum-path-length-limitation"></a>Limitação Máxima do Comprimento do Caminho


Nas edições do Windows antes Windows 10 versão 1607, o comprimento máximo de um caminho é **MAX \_ PATH,** que é definido como 260 caracteres. Em versões posteriores do Windows, alterar uma chave do Registro ou usar a Política de Grupo ferramenta é necessário para remover o limite. Consulte [Limitação máxima de comprimento do caminho](./maximum-file-path-limitation.md) para obter detalhes completos.


## <a name="namespaces"></a>Namespaces

Há duas categorias principais de convenções de namespace usadas nas APIs Windows, normalmente conhecidas como *namespaces NT* e *os namespaces win32*. O namespace NT foi projetado para ser o namespace de nível mais baixo no qual outros subsistemas e namespaces poderiam existir, incluindo o subsistema Win32 e, por extensão, os namespaces win32. POSIX é outro exemplo de um subsistema Windows criado sobre o namespace NT. As versões anteriores do Windows também definiam vários nomes predefinidos ou reservados para determinados dispositivos especiais, como portas de comunicação (serial e paralela) e o console de exibição padrão como parte do que agora é chamado de namespace do dispositivo NT e ainda têm suporte nas versões atuais do Windows para compatibilidade com versões anteriores.

### <a name="win32-file-namespaces"></a>Namespaces de arquivo Win32

Os prefixos e convenções do namespace Win32 são resumidos nesta seção e na seção a seguir, com descrições de como elas são usadas. Observe que esses exemplos destinam-se ao uso com as funções de API Windows e nem todos funcionam necessariamente com aplicativos de shell do Windows, como o Windows Explorer. Por esse motivo, há uma variedade maior de caminhos possíveis do que normalmente está disponível em aplicativos de shell do Windows e Windows aplicativos que aproveitam isso podem ser desenvolvidos usando essas convenções de namespace.

Para E/S de arquivo, o prefixo " ? " para uma cadeia de caracteres de caminho informa às APIs do Windows para desabilitar toda a análise de cadeia de caracteres e enviar a cadeia de caracteres que a segue diretamente para o sistema de \\ \\ \\ arquivos. Por exemplo, se o sistema de arquivos for compatível com caminhos grandes e nomes de arquivo, você poderá exceder os limites **\_ MAX PATH** que, de outra forma, são aplicados pelas APIs Windows. Para obter mais informações sobre a limitação de caminho máximo normal, consulte a seção anterior [Limitação máxima do comprimento do caminho.](#maximum-path-length-limitation)

Como ele desliga a expansão automática da cadeia de caracteres de caminho, o prefixo " ? " também permite o uso de \\ \\ ".." e "." nos nomes de caminho, o que pode ser útil se você estiver tentando executar operações em um arquivo com esses especificadores de caminho relativo reservados como parte do caminho totalmente \\ qualificado.

Muitas APIs de E/S de arquivo, mas não todas, suportam " ? "; você deve ver o tópico de referência de \\ \\ cada API para ter \\ certeza. 

Observe que as APIs Unicode devem ser usadas para garantir que o prefixo " ? " permita que você \\ \\ \\ exceda o **MAX \_ PATH** 

### <a name="win32-device-namespaces"></a>Namespaces de dispositivo Win32

O prefixo " . " acessará o namespace do dispositivo \\ \\ \\ Win32 em vez do namespace do arquivo Win32. É assim que o acesso a discos físicos e volumes é feito diretamente, sem passar pelo sistema de arquivos, se a API dá suporte a esse tipo de acesso. Você pode acessar muitos dispositivos diferentes de discos dessa maneira (usando as funções [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e [**DefineDosDevice,**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) por exemplo).

Por exemplo, se você quiser abrir a porta de comunicações seriais do sistema 1, poderá usar "COM1" na chamada para a [**função CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Isso funciona porque COM1-COM9 faz parte dos nomes reservados no namespace NT, embora o uso do prefixo " . " também funcione com esses nomes \\ \\ \\ de dispositivo. Por comparação, se você tiver uma placa de expansão serial de 100 portas instalada e quiser abrir o COM56, não poderá abri-lo usando "COM56" porque não há nenhum namespace NT predefinido para COM56. Você precisará abri-lo usando " \\ \\ . \\ COM56" porque " . " vai diretamente para o namespace do \\ \\ dispositivo sem tentar localizar um \\ alias predefinido.

Outro exemplo de como usar o namespace do dispositivo Win32 é usar a [**função CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com " \\ \\ . \\ PhysicalDisk *X*" (em *que X* é um valor inteiro válido) ou " \\ \\ . \\ CdRom *X*". Isso permite que você acesse esses dispositivos diretamente, ignorando o sistema de arquivos. Isso funciona porque esses nomes de dispositivo são criados pelo sistema à medida que esses dispositivos são enumerados e alguns drivers também criarão outros aliases no sistema. Por exemplo, o driver de dispositivo que implementa o nome "C:" tem seu próprio namespace que também é \\ o sistema de arquivos.

As APIs que passam pela [**função CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) geralmente funcionam com o prefixo " . " porque CreateFile é a função usada para abrir arquivos e \\ \\ \\ dispositivos, dependendo dos parâmetros usados. 

Se você estiver trabalhando com funções Windows API, deverá usar o prefixo " . " para acessar somente dispositivos \\ \\ e não \\ arquivos.

A maioria das APIs não dará suporte a " . "; somente as que foram projetadas para trabalhar com o namespace do dispositivo \\ \\ \\ o reconhecerão. Sempre verifique o tópico de referência de cada API para ter certeza.

### <a name="nt-namespaces"></a>NT Namespaces

Também há APIs que permitem o uso da convenção de namespace NT, mas o Windows Object Manager torna isso desnecessário na maioria dos casos. Para ilustrar, é útil procurar os namespaces Windows no navegador de objetos do sistema usando a ferramenta [WinObj](/sysinternals/downloads/winobj) Windows Sysinternals. Quando você executar essa ferramenta, o que verá é o namespace NT começando na raiz ou " \\ ". A subpasta chamada "Global??" é onde reside o namespace Win32. Os objetos de dispositivo nomeado residem no namespace NT no subdiretório "Dispositivo". Aqui você também pode encontrar Serial0 e Serial1, os objetos de dispositivo que representam as duas primeiras portas COM, se presentes em seu sistema. Um objeto de dispositivo que representa um volume seria algo como "HarddiskVolume1", embora o sufixo numérico possa variar. O nome "DR0" no subdiretório "Harddisk0" é um exemplo do objeto de dispositivo que representa um disco e assim por diante.

Para tornar esses objetos de dispositivo acessíveis por aplicativos Windows, os drivers de dispositivo criam um link simbólico (symlink) no namespace do Win32, "Global??", para seus respectivos objetos de dispositivo. Por exemplo, COM0 e COM1 no "Global??" O subdiretório são simplesmente symlinks para Serial0 e Serial1, "C:" é um symlink para HarddiskVolume1, "Physicaldrive0" é um symlink para DR0 e assim por diante. Sem um symlink, um dispositivo especificado "Xxx" não estará disponível para nenhum aplicativo Windows usando convenções de namespace win32, conforme descrito anteriormente. No entanto, um alça pode ser aberto para esse dispositivo usando todas as APIs que deem suporte ao caminho absoluto do namespace NT do formato " \\ Device \\ Xxx".

Com a adição do suporte para vários usuários por meio de Serviços de Terminal e máquinas virtuais, tornou-se necessário virtualizar ainda mais o dispositivo raiz em todo o sistema dentro do namespace Win32. Isso foi feito adicionando o symlink chamado "GLOBALROOT" ao namespace Win32, que você pode ver no "Global??" subdiretório da ferramenta de navegador WinObj discutido anteriormente e pode acessar por meio do caminho " \\ \\ ? \\ GLOBALROOT". Esse prefixo garante que o caminho a seguir se parece com o caminho raiz verdadeiro do gerenciador de objetos do sistema e não um caminho dependente de sessão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comparação de funcionalidades do sistema de arquivos](filesystem-functionality-comparison.md)
</dt> </dl>

 

 