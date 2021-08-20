---
title: Sobre tabelas Atom
description: Esta seção discute tabelas atom.
ms.assetid: 12114a3e-99a4-480f-9d1a-57c1942b7382
keywords:
- Átomos
- tabelas atom
- nomes atom
- Dados Dinâmicos Exchange (DDE), átomos
- DDE (Dados Dinâmicos Exchange), átomos
- tabelas atom globais
- tabelas atom locais
- átomos inteiros
- átomos de cadeia de caracteres
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: abc745908c62d2c90165cfa1a8d5acb527a8c7ae8c2a75424d0021b40ce4126d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915556"
---
# <a name="about-atom-tables"></a>Sobre tabelas Atom

Uma *tabela atom é* uma tabela definida pelo sistema que armazena cadeias de caracteres e identificadores correspondentes. Um aplicativo coloca uma cadeia de caracteres em uma tabela atom e recebe um inteiro de 16 bits, chamado *atom*, que pode ser usado para acessar a cadeia de caracteres. Uma cadeia de caracteres que foi colocada em uma tabela atom é chamada de *nome atom*.

O sistema fornece várias tabelas atom. Cada tabela atom tem uma finalidade diferente. Por exemplo, Dados Dinâmicos Exchange (DDE) usam a tabela [atom global](#global-atom-table) para compartilhar cadeias de caracteres de nome de item e nome de tópico com outros aplicativos. Em vez de passar cadeias de caracteres reais, um aplicativo DDE passa átomos globais para seu aplicativo parceiro. O parceiro usa os átomos para obter as cadeias de caracteres da tabela atom.

Os aplicativos podem usar tabelas atom locais para armazenar suas próprias associações de nome de item.

O sistema usa tabelas atom que não são diretamente acessíveis a aplicativos. No entanto, o aplicativo usa esses átomos ao chamar uma variedade de funções. Por exemplo, os formatos de área de transferência registrados são armazenados em uma tabela atom interna usada pelo sistema. Um aplicativo adiciona átomos a essa tabela atom usando a [**função RegisterClipboardFormat.**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) Além disso, as classes registradas são armazenadas em uma tabela atom interna usada pelo sistema. Um aplicativo adiciona átomos a essa tabela atom usando [**a função RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) ou [**RegisterClassEx.**](/windows/desktop/api/winuser/nf-winuser-registerclassexa)

Os tópicos a seguir são discutidos nesta seção.

-   [Tabela Atom Global](#global-atom-table)
-   [Tabela Atom do Usuário](#user-atom-table)
-   [Tabelas Atom Locais](#local-atom-tables)
-   [Tipos atom](#atom-types)
    -   [Átomos de cadeia de caracteres](#string-atoms)
    -   [Átomos inteiros](#integer-atoms)
-   [Criação atom e contagem de uso](#atom-creation-and-usage-count)
-   [Consultas atom-table](#atom-table-queries)
-   [Formatos de cadeia de caracteres atom](#atom-string-formats)

## <a name="global-atom-table"></a>Tabela Atom Global

A tabela atom global está disponível para todos os aplicativos. Quando um aplicativo coloca uma cadeia de caracteres na tabela atom global, o sistema gera um atom exclusivo em todo o sistema. Qualquer aplicativo que tenha o atom pode obter a cadeia de caracteres que identifica consultando a tabela atom global.

Um aplicativo que define um formato de dados DDE privado para compartilhar dados com outros aplicativos deve colocar o nome do formato na tabela atom global. Essa técnica impede conflitos com os nomes de formatos definidos pelo sistema ou por outros aplicativos e torna os identificadores (átomos) para as mensagens ou formatos disponíveis para os outros aplicativos.

## <a name="user-atom-table"></a>Tabela Atom do Usuário

Além da tabela atom global, a tabela atom do usuário é outra tabela atom do sistema que também é compartilhada entre todos os processos. A tabela atom do usuário é usada para um pequeno número de cenários internos para win32k; por exemplo, nomes de módulo do Windows, cadeias de caracteres conhecidas em win32k, formatos OLE etc. Embora os aplicativos não interajam diretamente com a tabela atom do usuário, eles chamam várias APIs , como [RegisterClass,](/windows/win32/api/winuser/nf-winuser-registerclassexa) [RegisterWindowMessage](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)e [RegisterClipboardFormat,](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)que adicionam entradas à tabela atom do usuário. As entradas adicionadas `RegisterClass` por podem ser excluídas por `UnregisterClass` . No entanto, as entradas adicionadas por `RegisterWindowMessage` e `RegisterClipboardFormat` não são excluídas até que a sessão termine. Se a tabela atom do usuário não tiver mais espaço e a cadeia de caracteres que está sendo passada ainda não estiver na tabela, a chamada falhará. 

### <a name="atom-table-size"></a>Tamanho da tabela atom
 
Muitas APIs críticas, incluindo [CreateWindow,](/windows/win32/api/winuser/nf-winuser-createwindowa)dependem de átomos do usuário. Portanto, o esgotamento de espaço na tabela atom do usuário resultará em problemas sérios; por exemplo, todos os aplicativos podem falhar ao iniciar. Aqui estão algumas recomendações para garantir que seu aplicativo utilize tabelas atom com eficiência e preserve a confiabilidade e o desempenho do aplicativo e do sistema:  

1. Você deve limitar o uso do aplicativo da tabela atom do usuário. Armazenar cadeias de caracteres exclusivas usando APIs como , ou ocupa espaço na tabela atom do usuário, que é usada globalmente por outros aplicativos para registrar classes de janela usando `RegisterClass` `RegisterWindowMessage` `RegisterClipboardFormat` cadeias de caracteres. Se possível, você deverá usar [AddAtom](/windows/desktop/api/Winbase/nf-winbase-addatomw)DeleteAtom para armazenar cadeias de caracteres em uma tabela / [](/windows/desktop/api/Winbase/nf-winbase-deleteatom) atom local ou [GlobalAddAtom](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) / [GlobalDeleteAtom](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) se os átomos são necessários entre processos.

1. Se houver preocupação sobre o aplicativo que está causando problemas de tabela atom do usuário, você poderá investigar a causa raiz conectando o depurador de kernel e entrando no processo em chamadas para `UserAddAtomEx` ( `bae1 win32kbase!UserAddAtomEx /p <eprocess> "kc10;g"` ). Procure no `user32!` callstack para ver qual API está sendo chamada. A metodologia é semelhante à detecção de problemas de tabela atom global explicada em [Identificando vazamentos globais de tabela atom.](/archive/blogs/ntdebugging/identifying-global-atom-table-leaks) Outra maneira de despejar o conteúdo da tabela atom do usuário é chamando [GetClipboardFormatName pelo](/windows/win32/api/winuser/nf-winuser-getclipboardformatnamea) intervalo de átomos possíveis de 0xC000 a 0xFFFF. Se a contagem total de atoms aumentar constantemente enquanto o aplicativo estiver em execução ou não retornar à linha de base quando o aplicativo for fechado, haverá um problema.

## <a name="local-atom-tables"></a>Tabelas Atom Locais

Um aplicativo pode usar uma tabela atom local para gerenciar com eficiência um grande número de cadeias de caracteres usadas somente dentro do aplicativo. Essas cadeias de caracteres e os átomos associados estão disponíveis apenas para o aplicativo que criou a tabela.

Um aplicativo que exige a mesma cadeia de caracteres em várias estruturas pode reduzir o uso de memória usando uma tabela atom local. Em vez de copiar a cadeia de caracteres em cada estrutura, o aplicativo pode colocar a cadeia de caracteres na tabela atom e incluir o atom resultante nas estruturas. Dessa forma, uma cadeia de caracteres aparece apenas uma vez na memória, mas pode ser usada muitas vezes no aplicativo.

Os aplicativos também podem usar tabelas atom locais para economizar tempo ao pesquisar uma cadeia de caracteres específica. Para executar uma pesquisa, um aplicativo só precisa colocar a cadeia de caracteres de pesquisa na tabela atom e comparar o atom resultante com os átomos nas estruturas relevantes. A comparação de átomos normalmente é mais rápida do que comparar cadeias de caracteres.

As tabelas Atom são implementadas como tabelas de hash. Por padrão, uma tabela atom local usa 37 buckets para sua tabela de hash. No entanto, você pode alterar o número de buckets usados chamando a [**função InitAtomTable.**](/windows/desktop/api/Winbase/nf-winbase-initatomtable) No entanto, se o aplicativo chamar **InitAtomTable,** ele deverá fazer isso antes de chamar qualquer outra função de gerenciamento atom.

## <a name="atom-types"></a>Tipos atom

Os aplicativos podem criar dois tipos de átomos: átomos de cadeia de caracteres e átomos inteiros. Os valores de átomos inteiros e de cadeia de caracteres não se sobrepõem, portanto, ambos os tipos de átomos podem ser usados no mesmo bloco de código.

Várias funções aceitam cadeias de caracteres ou átomos como parâmetros. Ao passar um atom para essas funções, um aplicativo pode usar a macro [**MAKEINTATOM**](/windows/desktop/api/Winbase/nf-winbase-makeintatom) para converter o atom em um formulário que pode ser usado pela função.

As seções a seguir descrevem tipos atom.

-   [Átomos de cadeia de caracteres](#string-atoms)
-   [Átomos inteiros](#integer-atoms)

### <a name="string-atoms"></a>Átomos de cadeia de caracteres

Quando os aplicativos passam cadeias de caracteres terminadas em nulo para as funções [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma), [**AddAtom,**](/windows/desktop/api/Winbase/nf-winbase-addatomw) [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma)e [**FindAtom,**](/windows/desktop/api/Winbase/nf-winbase-findatoma) eles recebem átomos de cadeia de caracteres *(inteiros* de 16 bits) em retorno. Os átomos de cadeia de caracteres têm as seguintes propriedades:

-   Os valores de átomos de cadeia de caracteres estão no intervalo 0xC000 (MAXINTATOM) até 0xFFFF.
-   O caso não é significativo em pesquisas por um nome atom em uma tabela atom. Além disso, toda a cadeia de caracteres deve corresponder em uma operação de pesquisa; nenhuma correspondência de substring é executada.
-   A cadeia de caracteres associada a um atom de cadeia de caracteres não pode ter mais de 255 bytes de tamanho. Essa limitação se aplica a todas as funções atom.
-   Uma *contagem de* referência é associada a cada nome atom. A contagem é incrementada sempre que o nome atom é adicionado à tabela e decrementado sempre que o nome atom é excluído dela. Isso impede que diferentes usuários do mesmo atom de cadeia de caracteres destrói os nomes atom uns dos outros. Quando a contagem de referência para um nome atom é igual a zero, o sistema remove o atom e o nome atom da tabela.

### <a name="integer-atoms"></a>Átomos inteiros

Os átomos inteiros diferem dos átomos de cadeia de caracteres das seguintes maneiras:

-   Os valores de átomos inteiros estão no intervalo 0x0001 a 0xBFFF (**MAXINTATOM**– 1).
-   A representação de cadeia de caracteres de um atom inteiro é dddd , em que os valores representados por \#  *dddd são* dígitos decimais. Zeros à esquerda são ignorados.
-   Não há nenhuma contagem de referência ou sobrecarga de armazenamento associada a um atom inteiro.

## <a name="atom-creation-and-usage-count"></a>Criação de Atom e contagem de uso

Um aplicativo cria um Atom local chamando a função [**addatom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) ; Ele cria um Atom global chamando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) . Ambas as funções exigem um ponteiro para uma cadeia de caracteres. O sistema pesquisa a tabela de Atom apropriada para a cadeia de caracteres e retorna o átomo correspondente para o aplicativo. No caso de um átomo de cadeia de caracteres, se a cadeia de caracteres já residir na tabela Atom, o sistema incrementará a contagem de referência para a cadeia de caracteres durante esse processo.

Chamadas repetidas para adicionar o mesmo nome de Atom retornam o mesmo Atom. Se o nome do Atom não existir na tabela quando [**addatom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) for chamado, o nome do Atom será adicionado à tabela e um novo Atom será retornado. Se for uma cadeia de caracteres Atom, sua contagem de referência também será definida como um.

Um aplicativo deve chamar a função [**DeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-deleteatom) quando ele não precisar mais usar um Atom local; Ele deve chamar a função [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) quando ele não precisar mais de um átomo global. No caso de um átomo de cadeia de caracteres, qualquer uma dessas funções reduz a contagem de referência do átomo correspondente por um. Quando a contagem de referência chega a zero, o sistema exclui o nome do Atom da tabela.

O nome do Atom de uma cadeia de caracteres Atom permanece na tabela global Atom, desde que sua contagem de referência seja maior que zero, mesmo depois que o aplicativo que o colocou na tabela for encerrado. Uma tabela Atom local é destruída quando o aplicativo associado é encerrado, independentemente das contagens de referência dos átomos na tabela.

## <a name="atom-table-queries"></a>Consultas de Atom-Table

Um aplicativo pode determinar se uma cadeia de caracteres específica já está em uma tabela Atom usando a função [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) ou [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) . Essas funções pesquisam uma tabela Atom para a cadeia de caracteres especificada e, se a cadeia de caracteres estiver lá, retornará o átomo correspondente.

Um aplicativo pode usar a função [**Getatomname**](/windows/desktop/api/Winbase/nf-winbase-getatomnamea) ou [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) para recuperar uma cadeia de caracteres de nome Atom de uma tabela Atom, desde que o aplicativo tenha o átomo correspondente à cadeia de caracteres que está sendo procurada. Ambas as funções copiam a cadeia de caracteres Atom-Name do átomo especificado para um buffer e retornam o comprimento da cadeia de caracteres que foi copiada. **Getatomname** recupera uma cadeia de caracteres Atom-Name de uma tabela Atom local e **GlobalGetAtomName** recupera uma cadeia de caracteres de nome Atom da tabela global Atom.

## <a name="atom-string-formats"></a>Formatos de cadeia de caracteres Atom

As funções [**addatom**](/windows/desktop/api/Winbase/nf-winbase-addatomw), [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma), [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma)e [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) usam um ponteiro para uma cadeia de caracteres terminada em nulo. Um aplicativo pode especificar esse ponteiro de uma das maneiras a seguir.



|     Formato da cadeia de caracteres               |    Descrição                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------|
| \#*dia*           | Um inteiro especificado como uma cadeia de caracteres decimal. Usado para criar ou encontrar um Atom inteiro.                  |
| *nome Atom da cadeia de caracteres* | Um nome Atom de cadeia de caracteres. Usado para adicionar um nome Atom de cadeia de caracteres a uma tabela Atom e receber um Atom em retorno. |



 

 

 
