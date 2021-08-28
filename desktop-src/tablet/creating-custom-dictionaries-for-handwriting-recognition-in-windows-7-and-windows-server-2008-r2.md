---
description: Esta seção explica como criar um dicionário personalizado para o reconhecimento de manuscrito.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: criando dicionários personalizados para reconhecimento de manuscrito no Windows 7 e no Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c7b27fbb03897b406609590420bd8b69b7ceee
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631191"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a>criando dicionários personalizados para reconhecimento de manuscrito no Windows 7 e no Windows Server 2008 R2

Esta seção explica como criar um dicionário personalizado para o reconhecimento de manuscrito.

no sistema operacional Windows 7 e no sistema operacional Windows Server 2008 R2, a precisão do reconhecimento de manuscrito pode ser significativamente melhorada com o uso de dicionários personalizados. Esses dicionários complementam ou substituem os dicionários do sistema usados para manuscrito. O suporte ao reconhecimento de manuscrito é fornecido por meio do recurso Serviços de Reconhecimento de Manuscrito que precisa ser habilitado por meio de Gerenciador do Servidor.

> [!Note]  
> Os dicionários personalizados podem ser instalados para um idioma somente se o reconhecedor de manuscrito para esse idioma estiver instalado.

 

Há duas etapas básicas para configurar um dicionário personalizado para manuscrito:

-   Compilar uma lista de palavras. A compilação cria um arquivo de dicionário personalizado compilado (. hwrdict).
-   Instale o dicionário personalizado compilado.

## <a name="compiling-a-word-list"></a>Compilando uma lista de palavras

A lista de palavras a ser compilada deve estar no formato de texto sem formatação e deve ser salva usando uma codificação Unicode. Outras codificações não funcionarão. Cada linha do arquivo de texto é usada como uma única entrada no dicionário. São permitidas entradas de unidades de multipalavra contendo um ou mais espaços. Os espaços no início ou no final de uma linha são ignorados.

Um dicionário personalizado é compilado a partir de uma linha de comando. Para compilar um dicionário, abra uma janela de comando, navegue até a pasta que contém a lista de palavras e execute HwrComp.exe com as opções de linha de comando que você deseja usar.

O exemplo a seguir mostra a sintaxe de uso para as opções de linha de comando.

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a>Explicação das opções



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Parâmetro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-lang <localename></td>
<td>O nome de localidade especificado atribuído ao arquivo de dicionário personalizado compilado. O argumento <localename> tem o formato idioma-região. Um exemplo disso é en-US, que significa o idioma inglês na região de Estados Unidos. Para obter exemplos desse formulário, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings). os idiomas a seguir têm suporte para o Windows 7 e Windows Server 2008 R2 por esse recurso: en-US, en-GB, en-CA, en-AU, de-de, de-CH, fr-fr, es-es, es-MX, es-AR, ti, nl-nl, nl-it, pt-BR, pt-pt, da-DK, sv-ES, nb-no, nn-no, fi-fi, pl-pl, cs-CZ, ru-ru, ro-ro, sr-Latn-cs, sr-Cyrl-cs, CA-es e hr-hr.<br/></td>
</tr>
<tr class="even">
<td>-tipo <type></td>
<td>O argumento de opção <type> é uma concatenação de cadeia de caracteres única do uso do recurso como a lista de palavras principal (primária) ou como um suplemento para a lista de palavras principal (secundária) seguida pelo nome da lista de palavras real ao qual o recurso é aplicado (como Dictionary ou sobrenome). O valores possíveis são os seguintes:
<ul>
<li>PRIMÁRIO-CITYNAME-LISTA</li>
<li>PRIMÁRIO-PAÍSNAME-LISTA</li>
<li>COUNTRYSHORTNAME PRIMÁRIO-LISTA</li>
<li>DICIONÁRIO PRIMÁRIO</li>
<li>PRIMÁRIA-LISTA ESPECIFICADA</li>
<li>ESTADOOUPROVÍNCIA PRIMÁRIO-LISTA</li>
<li>PRIMÁRIO-RUA-DA-LISTA</li>
<li>PRIMARY-SOBRENOME-LISTA</li>
<li>SECUNDÁRIA-CITYNAME-LISTA</li>
<li>LISTA DE PAÍSNAME SECUNDÁRIA</li>
<li>COUNTRYSHORTNAME SECUNDÁRIO-LISTA</li>
<li>DICIONÁRIO SECUNDÁRIO</li>
<li>EMAILSMTP SECUNDÁRIO-LISTA</li>
<li>EMAILUSERNAME SECUNDÁRIO-LISTA</li>
<li>SECUNDÁRIA-LISTA ESPECIFICADA</li>
<li>ESTADOOUPROVÍNCIA SECUNDÁRIO-LISTA</li>
<li>LISTA DE ENDEREÇOS SECUNDÁRIOS</li>
<li>SECUNDÁRIA-SOBRENOME-LISTA</li>
<li>URL SECUNDÁRIA-LISTA</li>
</ul>
Se um valor de tipo começar com o prefixo primário, o dicionário compilado, depois de instalado, substituirá o dicionário do sistema para esse idioma. O valor principal-DICTIONARY representa o dicionário principal do sistema para um idioma.
<blockquote>
[!Note]<br />
Substituir um dicionário do sistema não faz nada para o conteúdo original do dicionário do sistema, pois a substituição estará em vigor somente até que o dicionário personalizado tenha sido removido.
</blockquote>
<br/> Se um valor de tipo começar com o prefixo secundário, o dicionário compilado irá complementar o dicionário do sistema sem substituí-lo.</td>
</tr>
<tr class="odd">
<td>-Comentário <comment></td>
<td>O comentário especificado é compilado no arquivo de dicionário. O comentário deve ser uma única cadeia de caracteres e não mais de 64 caracteres.</td>
</tr>
<tr class="even">
<td>-o <dictfile.hwrdict></td>
<td>A saída é gravada no nome de arquivo especificado por <dictfile.hwrdict> .<br/> Se essa opção estiver ausente, o nome do arquivo de saída será derivado do nome do arquivo de entrada original, com a extensão de arquivo de entrada substituída por. hwrdict.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a>Padrões

Se nenhum parâmetro for especificado, os valores de opção padrão serão

-lang <current input language> -tipo de dicionário secundário

### <a name="examples"></a>Exemplos

O seguinte compila o arquivo de entrada mylist1.txt, aplica os valores de opção padrão e cria o arquivo de saída mylist1. hwrdict.

``` syntax
hwrcomp mylist1.txt
```

Por outro lado, o seguinte compila mylist1.txt em myrsrc1. hwrdict, mas atribui "Inglês (EUA)" (en-US) como o idioma e o dicionário secundário como o tipo.

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a>Instalando um dicionário personalizado compilado

HwrComp.exe cria um arquivo. hwrdict, que está em um formato binário utilizável por um reconhecedor de manuscrito. esse arquivo pode ser instalado em qualquer computador que execute o Windows 7 ou Windows Server 2008 R2 que dê suporte ao reconhecimento de manuscrito. Um dicionário é instalado apenas para o usuário atual ou para todos os usuários em um computador.

Um arquivo de dicionário personalizado compilado pode ser instalado a partir da linha de comando usando a ferramenta HwrReg.exe. Essa ferramenta é útil se você deseja substituir alguns dos valores de configuração que são compilados no arquivo ou são os valores padrão. Há duas maneiras de executar HwrReg.exe: no modo de verificação/instalação e no modo de lista/remoção.

### <a name="running-hwrregexe-in-checkinstall-mode"></a>Executando HwrReg.exe no modo de verificação/instalação

Esse modo é para arquivos de dicionário personalizados que ainda não foram instalados. O seguinte mostra a sintaxe de uso para as opções de linha de comando.

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a>Explicação das opções



| Parâmetro                | Descrição                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -verificar                   | O arquivo de dicionário é verificado sem ser instalado. A opção verificar exibe o comentário do arquivo, além das informações de registro que seriam usadas para instalar o arquivo. Essa opção é útil para verificar as informações de registro antes da execução da instalação. <br/> Se essa opção estiver ausente, HwrReg.exe instalará o dicionário personalizado.<br/>  |
|  lang <localename> | O arquivo de dicionário é verificado sem ser instalado. A opção verificar exibe o comentário do arquivo, além das informações de registro que seriam usadas para instalar o arquivo. Essa opção é útil para verificar as informações de registro antes da execução da instalação. <br/> Se essa opção estiver ausente, HwrReg.exe instalará o dicionário personalizado. <br/> |
|  escopo {todos \| me}         | O dicionário personalizado é instalado para todos os usuários (escopo todos) ou apenas para o usuário atual (escopo me). A instalação com escopo todos requer que o comando seja executado em um prompt de comando com privilégios elevados; caso contrário, um código de erro será retornado. <br/> Se essa opção estiver ausente, a instalação será delimitada apenas ao usuário atual.<br/>                          |
|  noprompt                | HwrReg.exe não solicita confirmação. Isso pode ser útil ao executar hwrReg.exe de um script. <br/>                                                                                                                                                                                                                                                                 |



 

O exemplo a seguir instala o dicionário personalizado myrsrc1. hwrdict para a linguagem "dinamarquês (Dinamarca)" (da DK), com o escopo padrão apenas do usuário atual.

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a>Executando HwrReg.exe no modo de lista/remoção

Esse modo lista ou remove os dicionários personalizados instalados. O seguinte mostra a sintaxe de uso para as opções de linha de comando.

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a>Explicação das opções



| Parâmetro                | Descrição                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  lang <localename> | Os dicionários registrados somente para esse nome de localidade são listados ou removidos. O argumento <localename> tem a região de idioma do formulário. Para obter exemplos desse formulário, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings). <br/> Se essa opção estiver ausente, os dicionários para todos os idiomas serão listados ou removidos.<br/> |
|  escopo {todos \| me}         | O dicionário personalizado é instalado para todos os usuários (escopo todos) ou apenas para o usuário atual (escopo me). A instalação com escopo todos requer que o comando seja executado em um prompt de comando com privilégios elevados; caso contrário, um código de erro será retornado. <br/> Se essa opção estiver ausente, a instalação será delimitada apenas ao usuário atual.<br/>                      |
|  Escreva <type>       | Lista ou remove somente os dicionários que são registrados com o tipo especificado.<br/> Se essa opção estiver ausente, todos os tipos de dicionário serão listados ou removidos. Instalar ou remover um dicionário personalizado de outro tipo (como a lista de PAÍSname primário) pode afetar o reconhecimento de manuscrito em outros contextos. <br/>                                              |
|  list                    | Lista todos os dicionários instalados que correspondem às outras opções.<br/> Se essa opção estiver ausente, a opção remover deverá ser especificada.<br/>                                                                                                                                                                                                                          |
|  remove                  | Solicita a remoção de qualquer dicionário que corresponda às outras opções.<br/> Se essa opção estiver ausente, a lista de opções deverá ser especificada.<br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Exemplos

O seguinte lista os dicionários que têm o idioma "Inglês (EUA)" (en US) e o dicionário principal do tipo e que são instalados apenas para o usuário atual.

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

Da mesma forma, o seguinte remove os dicionários que correspondem aos mesmos critérios.

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a>Observações gerais sobre dicionários personalizados

-   Se você instalar dois dicionários personalizados que têm o mesmo tipo, idioma e escopo, a segunda instalação substituirá o primeiro.
-   Se você instalar dois dicionários personalizados com o mesmo tipo e idioma, mas com escopos diferentes (um para todos os usuários e outro para o usuário atual), o dicionário instalado para o usuário atual terá precedência e o dicionário instalado para todos os usuários será ignorado.

 

